# Contrato de datos

La IA devuelve un objeto estructurado con estos campos:

| Campo | Tipo | Descripción |
|---|---|---|
| `category` | enum | Área de la solicitud |
| `priority` | enum | `Baja`, `Media`, `Alta` o `Crítica` |
| `requester_name` | string/null | Nombre del solicitante |
| `requester_email` | string/null | Email del solicitante |
| `client_or_project` | string/null | Cliente o proyecto mencionado |
| `target_person` | string/null | Persona afectada |
| `summary` | string | Resumen del pedido |
| `requested_action` | string | Acción solicitada |
| `due_date` | string/null | Fecha explícita en formato `YYYY-MM-DD` |
| `missing_information` | array | Datos que faltan para procesar el pedido |
| `suggested_owner` | string/null | Responsable sugerido si está disponible |
| `draft_reply` | string | Respuesta inicial sugerida |
| `requires_human_approval` | boolean | Señal para revisión humana |
| `confidence` | number | Confianza entre `0` y `1` |

Además, el workflow conserva el ID, fecha, asunto, cuerpo, origen y enlace del email original.
