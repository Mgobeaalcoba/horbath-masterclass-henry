# Seguridad y privacidad

## Reglas para la demo

- No usar información real de Horbath, clientes, colaboradores, accesos, pagos ni facturación.
- No mostrar tokens, IDs de credenciales, enlaces privados o direcciones personales.
- Usar cuentas dummy y un canal Slack de prueba.
- No ejecutar cambios reales; la demo es de clasificación, registro y notificación simulada.
- Mantener revisión humana para accesos, facturación, pagos, datos personales y clientes.
- Explicar que una confianza alta no garantiza que la interpretación sea correcta.

## Datos y permisos

Aplicar el principio de mínimo privilegio a Gmail, Sheets, Slack y proveedores de modelos. Separar las credenciales de demo de cualquier cuenta de producción y rotarlas si se compartieron en un export.

## Qué no debe versionarse

Exports crudos de n8n, archivos `.env`, tokens, cookies, IDs de credenciales, IDs de documentos privados, enlaces a buzones y muestras con datos personales.
