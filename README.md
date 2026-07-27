# Masterclass AI Automation - Horbath Technologies

Repositorio de trabajo para la masterclass de Henry sobre automatización inteligente de solicitudes internas.

## Idea central

Una solicitud que llega desordenada por email puede convertirse en un proceso trazable: la IA interpreta el pedido, extrae datos, valida si está completo, lo registra, lo deriva por categoría y notifica al equipo. La automatización ayuda a ordenar el trabajo sin quitarle a la persona el control sobre decisiones sensibles.

## Estado

- Contenido base: propuesta y deck de referencia disponibles.
- Workflow n8n: implementado en un entorno de demo; documentado sin credenciales ni identificadores privados.
- PPTX editable: pendiente de carga por el autor.
- Aprobación humana: pendiente de implementar como pausa real del workflow; hoy se calcula como señal de control.

## Estructura

```text
.
├── README.md
├── automation/
│   └── README.md
├── deck/
│   ├── README.md
│   └── assets/              # PPTX, capturas y recursos visuales
├── docs/
│   ├── 00-overview.md
│   ├── 01-session-plan.md
│   ├── 02-demo-script.md
│   ├── 03-automation-architecture.md
│   ├── 04-data-contract.md
│   ├── 05-safety-and-privacy.md
│   ├── 06-validation-checklist.md
│   ├── 07-deck-notes.md
│   ├── examples/
│   └── sources/
└── .gitignore
```

## Recorrido recomendado

1. Leer [la visión general](docs/00-overview.md).
2. Preparar la sesión con [el plan](docs/01-session-plan.md) y [el guion de demo](docs/02-demo-script.md).
3. Revisar [la arquitectura real del workflow](docs/03-automation-architecture.md) y [el contrato de datos](docs/04-data-contract.md).
4. Usar [los ejemplos](docs/examples/) para probar solicitudes completas e incompletas.
5. Subir el PPTX a `deck/assets/` y completar [las notas del deck](docs/07-deck-notes.md).

## Fuentes

- [Propuesta original](docs/sources/Propuesta%20Masterclass%20AI%20Automation%20-%20Horbath%20Technologies.md)
- [PDF del deck de referencia](docs/sources/Intelligent%20Request%20Automation%20-%20Masterclass%20Horbath%20by%20Henry.pptx.pdf)
- [Documentación de la automation](automation/README.md)

## Regla de seguridad

No versionar exports crudos de n8n, tokens, cookies, IDs de credenciales, enlaces privados de Gmail/Sheets ni datos reales de participantes. Usar variables, cuentas dummy y ejemplos ficticios.
