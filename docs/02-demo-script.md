# Guion de demo

## Preparación

- Usar solamente cuentas de prueba y datos inventados.
- Tener abiertos n8n, un email de ejemplo, la planilla y el canal Slack de demo.
- Desactivar acciones reales sobre accesos, pagos, clientes o información personal.
- Preparar un ejemplo incompleto y uno válido.

## Secuencia

1. Presentar el email ficticio y el resultado esperado.
2. Decir: **“Ya vimos qué problema resolvemos; ahora abrimos n8n para seguir una solicitud real dentro del workflow.”**
3. Mostrar `Detectar Nuevos Emails` y `Normalizar Datos`.
4. Mostrar el agente LangChain, sus modelos y el `Structured Output Parser`.
5. Explicar que la validación exige confianza mínima de `0.75`, categoría y prioridad válidas, email del solicitante y ningún dato faltante.
6. Ejecutar primero la rama incompleta: pedir información adicional por Gmail y registrar en `Solicitudes_Incompletas`.
7. Ejecutar luego la rama válida: registrar en `Solicitudes_Completas`, derivar por categoría y notificar Slack.
8. Aclarar que `requires_human_approval` es una señal visible, pero no pausa todavía el workflow.
9. Decir: **“El lienzo muestra cómo funciona; volvamos al deck para resumir qué patrón puede reutilizar cada área.”**
10. Volver al deck y cerrar con las cinco preguntas.

## Mensajes que conviene repetir

- La IA interpreta y estructura; no inventa datos.
- La automatización no reemplaza el criterio en acciones sensibles.
- El patrón se adapta cambiando categorías, reglas, responsables y herramientas.
