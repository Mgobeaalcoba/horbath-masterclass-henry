# Intelligent Request Automation

Automation de n8n para convertir solicitudes internas recibidas por email en registros estructurados, solicitudes de información faltante y notificaciones por categoría.

## Qué resuelve

Las solicitudes internas suelen llegar en lenguaje natural, con datos incompletos y sin un circuito uniforme de seguimiento. Esta automation:

1. Detecta emails nuevos.
2. Extrae y clasifica la solicitud con IA.
3. Valida confianza, campos obligatorios y datos faltantes.
4. Solicita información adicional cuando el pedido está incompleto.
5. Registra solicitudes completas e incompletas en Google Sheets.
6. Deriva solicitudes completas por categoría y notifica en Slack.

## Obtener la automation

Descargar [`automation/workflow.template.json`](automation/workflow.template.json) e importarlo en n8n. Luego seguir [`docs/configuration.md`](docs/configuration.md) para conectar las credenciales y recursos propios.

## Documentación

- [Problema y solución](docs/problem-and-solution.md)
- [Configuración y uso](docs/configuration.md)
- [Contrato de datos](docs/data-contract.md)
- [Seguridad y límites](docs/safety.md)
- [Presentación](presentation/Intelligent%20Request%20Automation%20-%20Masterclass%20Horbath%20by%20Henry.pdf)

## Alcance

El workflow es una plantilla educativa para una demo. Usa cuentas, hojas y canales configurables. No ejecuta cambios reales sobre accesos, pagos, facturación, clientes ni datos personales.
