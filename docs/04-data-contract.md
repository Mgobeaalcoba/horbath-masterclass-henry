# Contrato de datos

## Entrada normalizada

| Campo | Tipo | Descripción |
|---|---|---|
| `request_id` | string | Identificador del email |
| `received_at` | string | Fecha de recepción |
| `requester_name` | string | Nombre visible del remitente |
| `requester_email` | string | Email del remitente |
| `subject` | string | Asunto |
| `body` | string | Cuerpo del pedido |
| `source` | string | Origen, inicialmente `gmail` |
| `status` | string | Estado inicial, `received` |
| `original_message_link` | string | Enlace al email original |

## Salida de IA

```json
{
  "category": "People | Finanzas | Compras | Accesos | Soporte | Proyectos | Administración | Otro",
  "priority": "Baja | Media | Alta | Crítica",
  "requester_name": "string | null",
  "requester_email": "string | null",
  "client_or_project": "string | null",
  "target_person": "string | null",
  "summary": "string",
  "requested_action": "string",
  "due_date": "YYYY-MM-DD | null",
  "missing_information": ["string"],
  "suggested_owner": "string | null",
  "draft_reply": "string",
  "requires_human_approval": true,
  "confidence": 0.0
}
```

## Campos de control

- `validation_passed`: booleano.
- `validation_reason`: `OK`, `Confianza baja`, `Información faltante` o `Datos inválidos`.
- `last_updated_at`: timestamp de la última modificación.

## Registro recomendado

El registro completo debe conservar ID, fechas, solicitante, canal, categoría, prioridad, proyecto/cliente, descripción, responsable, estado, respuesta preparada, motivo de validación y enlace al origen.
