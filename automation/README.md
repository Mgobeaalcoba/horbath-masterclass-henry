# Workflow n8n

El archivo [`workflow.template.json`](workflow.template.json) es un export sanitizado e importable del workflow. No contiene credenciales ni IDs privados.

## Flujo

```text
Gmail Trigger
  -> Normalizar Datos
  -> Analizar Solicitud con IA
  -> Structured Output Parser
  -> Validar Confianza y Datos
  -> Validación Pasó?
       No  -> Solicitar Información Faltante
           -> Registrar Solicitud Incompleta
       Sí  -> Registrar Solicitud Válida
           -> Asignar por Categoría
           -> Notificar por Slack
```

## Modelos configurados

- OpenAI GPT-5-mini como modelo principal.
- Gemini Flash Lite 3.1 como fallback.
- Qwen 3.6 para auto-fix del output estructurado.

Las conexiones a estos proveedores deben configurarse en la instancia de n8n donde se importe la plantilla.
