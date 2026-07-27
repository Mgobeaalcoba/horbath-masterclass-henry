# Configuración y uso

## Requisitos

- Una instancia de n8n.
- Credencial OAuth de Gmail.
- Credencial del proveedor de modelos de IA.
- Credencial OAuth de Google Sheets.
- Credencial de Slack.

## Pasos

1. Importar `automation/workflow.template.json` en n8n.
2. Abrir los nodos de Gmail, modelos, Google Sheets y Slack y seleccionar credenciales propias.
3. Configurar el Gmail Trigger para el buzón de prueba.
4. Crear una planilla con las pestañas `Solicitudes_Completas` y `Solicitudes_Incompletas`.
5. Reemplazar el documento y las hojas de Google Sheets por los recursos propios.
6. Configurar el canal de Slack de prueba y las salidas del Switch.
7. Ejecutar primero una solicitud incompleta y después una solicitud completa.

## Categorías

`People`, `Finanzas`, `Compras`, `Accesos`, `Soporte`, `Proyectos`, `Administración` y `Otro`.

## Estados

La plantilla utiliza estados como `received`, `requires_information` y `assigned`. Se pueden adaptar al sistema de seguimiento de cada equipo.
