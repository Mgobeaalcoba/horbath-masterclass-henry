# Checklist de validación

## Antes de la sesión

- [ ] El PPTX editable está en `deck/assets/`.
- [ ] La propuesta y el PDF de referencia están disponibles en `docs/sources/`.
- [ ] n8n usa cuentas de prueba.
- [ ] El trigger está configurado para el buzón de demo.
- [ ] La planilla tiene las pestañas `Solicitudes_Completas` y `Solicitudes_Incompletas`.
- [ ] Slack apunta al canal de prueba.
- [ ] No hay credenciales ni IDs privados en el repositorio.

## Prueba incompleta

- [ ] El email no tiene uno o más datos requeridos.
- [ ] La IA identifica `missing_information`.
- [ ] `validation_passed` es `false`.
- [ ] Se envía una solicitud de información faltante.
- [ ] Se escribe una fila en `Solicitudes_Incompletas`.

## Prueba válida

- [ ] La confianza es igual o mayor que `0.75`.
- [ ] Categoría y prioridad pertenecen a los enums.
- [ ] Existe `requester_email`.
- [ ] `missing_information` está vacío.
- [ ] Se escribe una fila en `Solicitudes_Completas`.
- [ ] El Switch deriva a la categoría esperada.
- [ ] Slack recibe la notificación.
- [ ] La señal `requires_human_approval` aparece correctamente.

## Presentación

- [ ] Se aclara que los procesos de Horbath son una hipótesis a validar.
- [ ] Se muestran primero la rama incompleta y después la válida.
- [ ] No se presenta la aprobación humana como implementada.
