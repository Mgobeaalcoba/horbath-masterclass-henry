# Automation n8n

Esta carpeta documenta el workflow usado en la demo. El export original no se incluye porque contiene referencias a credenciales, cuentas y recursos externos. Para reconstruirlo, usar la arquitectura y el contrato descritos en `docs/03-automation-architecture.md` y `docs/04-data-contract.md`.

## Flujo real

```text
Gmail Trigger (cada minuto)
  -> Normalizar Datos
  -> Analizar Solicitud con IA
       - OpenAI GPT-5-mini
       - Gemini Flash Lite 3.1 como fallback
       - Structured Output Parser
       - Qwen 3.6 para auto-fix del parser
  -> Validar Confianza y Datos
  -> Validación Pasó?
       false -> Marcar Requiere Información
             -> Solicitar Información Faltante por Gmail
             -> Registrar Solicitud Incompleta
       true  -> Registrar Solicitud Válida
             -> Asignar por Categoría
             -> Notificar por Slack
```

## Categorías del Switch

People, Finanzas, Compras, Accesos, Soporte, Proyectos, Administración y Revisión Manual.

En la demo, las salidas notifican al canal de prueba `masterclass-n8n`; los responsables reales son configurables y no se asumen como procesos internos de Horbath.

## Importante sobre la aprobación humana

El workflow actual calcula `requires_human_approval` y lo muestra en Sheets y Slack. No contiene todavía un nodo que pause la ejecución hasta recibir una aprobación. La presentación debe describirlo como una señal de control para revisión humana, no como una aprobación automatizada ya implementada.

## Reconfiguración mínima

1. Crear credenciales de prueba para Gmail, el proveedor de modelos, Google Sheets y Slack.
2. Reemplazar los nombres de hojas y canales por recursos de demo.
3. Mantener las expresiones y categorías de este repositorio como referencia.
4. Probar primero con los ejemplos de `docs/examples/`.
5. Verificar que ningún dato sensible real aparezca en el email, la planilla, Slack o las capturas.
