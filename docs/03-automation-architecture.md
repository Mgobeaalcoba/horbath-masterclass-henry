# Arquitectura de la automation

## Diagrama lógico

```mermaid
flowchart LR
    A["Gmail Trigger<br/>cada minuto"] --> B["Normalizar Datos"]
    B --> C["Agente LangChain<br/>clasificación y extracción"]
    C --> D["Structured Output Parser<br/>auto-fix con Qwen"]
    D --> E["Validar Confianza y Datos"]
    E --> F{"¿Validación pasó?"}
    F -- "No" --> G["Marcar requiere información"]
    G --> H["Solicitar información faltante<br/>por Gmail"]
    H --> I["Registrar Solicitud Incompleta"]
    F -- "Sí" --> J["Registrar Solicitud Válida"]
    J --> K["Switch por categoría"]
    K --> L["Notificar por Slack"]
```

## Capa de IA

- Modelo principal: OpenAI GPT-5-mini.
- Fallback: Gemini Flash Lite 3.1.
- Salida: JSON validado por schema.
- Auto-fix: Qwen 3.6 conectado al parser.
- Instrucción: extraer únicamente información presente, indicar faltantes y no ejecutar acciones sensibles.

## Criterio de validación

Una solicitud es válida cuando:

```text
confidence >= 0.75
category válida
priority válida
requester_email presente
missing_information está vacío
```

Si falla, se registra la razón como `Confianza baja`, `Información faltante` o `Datos inválidos`.

## Ramas

### Incompleta

Marca el pedido, envía un email profesional solicitando los datos faltantes y lo registra en `Solicitudes_Incompletas`.

### Válida

Registra el pedido en `Solicitudes_Completas`, lo deriva por categoría y notifica al canal Slack de prueba. Las ocho salidas son People, Finanzas, Compras, Accesos, Soporte, Proyectos, Administración y Revisión Manual.

## Limitación actual

La variable `requires_human_approval` se calcula y se expone en Sheets/Slack, pero todavía no existe una pausa real ni un callback de aprobación. Para convertirlo en control operativo habría que agregar un mecanismo de aprobación, persistir el estado y reanudar solo después de una decisión autorizada.
