# Problema y solución

## Problema

Una solicitud interna puede llegar por email sin formato uniforme, mezclando contexto, personas, proyectos, fechas y acciones. Eso dificulta clasificarla, detectar qué información falta, derivarla al equipo correcto y mantener trazabilidad.

## Solución

La automation convierte el lenguaje natural en datos operables. Un modelo de IA clasifica la solicitud, extrae campos definidos por schema y señala la información faltante. A partir de esa salida, n8n aplica reglas determinísticas para decidir si el pedido puede registrarse como completo o si debe volver al solicitante para ser completado.

Las solicitudes completas se registran en Google Sheets, se derivan por categoría y se notifican en Slack. Las incompletas reciben un email con los datos necesarios para continuar y quedan registradas por separado.

## Validación

Una solicitud pasa la validación cuando tiene confianza mínima de `0.75`, categoría y prioridad válidas, email del solicitante y `missing_information` vacío. La confianza no reemplaza la revisión humana para acciones sensibles.
