# PROPUESTA DE MASTERCLASS

AI Automation aplicada a la gestión de solicitudes internas
Horbath Technologies × Henry
Documento de trabajo para validación con Agustina y posterior iteración del contenido

# 1\. Descripción breve para compartir con Agustina

Proponemos una masterclass cerrada para Horbath Technologies sobre AI Automation aplicada a tareas administrativas y operativas.
El caso central será transformar emails o formularios desordenados en solicitudes gestionadas de punta a punta.
La automatización identificará el tipo de pedido, extraerá sus datos relevantes y lo registrará automáticamente.
Luego asignará la solicitud al responsable correspondiente y notificará al equipo por email o Slack.
También generará una respuesta inicial para revisión humana, manteniendo control y trazabilidad.
El ejemplo es relevante para Horbath porque conecta equipos, proyectos, clientes y procesos internos.
La audiencia podrá reconocer tareas habituales de Administración, Operaciones, Finanzas, People, Compras o Soporte.
La demostración se construirá en n8n e integrará IA con Gmail, Google Sheets o Airtable y Slack.
La sesión será práctica, sin requerir conocimientos técnicos previos ni instalar herramientas.
El objetivo es que cada participante se lleve una oportunidad concreta de automatización para su propio trabajo.

# 2\. Ficha ejecutiva

Título sugerido: Cómo automatizar la gestión de solicitudes internas con IA: del email al seguimiento automático
Fecha y horario: martes 4 de agosto, de 13:00 a 14:00 hs. Argentina.
Modalidad: virtual, vía Zoom provisto por Horbath.
Expositor: instructor de Henry, en representación de la carrera AI Automation.
Audiencia: perfiles administrativos y de soporte de Horbath Technologies.
Duración: 60 minutos.
Formato: introducción conceptual breve, demo guiada, participación por chat y cierre.
Hipótesis a validar: los equipos administrativos de Horbath gestionan solicitudes que llegan por distintos canales y requieren clasificación, derivación, seguimiento y respuesta.

# 3\. Por qué este caso tiene sentido para Horbath

Horbath se presenta públicamente como una compañía tecnológica que combina desarrollo de software, analítica de datos, automatización de procesos, soporte y outsourcing TI. En ese contexto, una parte importante del trabajo administrativo consiste en coordinar personas, proyectos, clientes, pedidos y estados.
La propuesta no intenta automatizar el desarrollo de software ni convertir a los asistentes en programadores. Muestra cómo un proceso transversal y cotidiano puede ordenarse con IA y automatización, incluso cuando quienes lo gestionan no tienen un perfil técnico.
El caso debe presentarse como un escenario demostrativo, no como una afirmación sobre el proceso interno actual de Horbath. Antes de la sesión conviene validar con el equipo organizador qué canal y categorías resultan más representativos.

# 4\. Caso de uso detallado

## Nombre del caso

De email desordenado a solicitud gestionada.

## Situación inicial

Un colaborador, líder de proyecto o responsable de cliente envía una solicitud por email o formulario. El pedido puede involucrar accesos, People, Compras, Finanzas, soporte, documentación o coordinación de un proyecto. La información suele llegar en lenguaje natural, con distintos niveles de detalle y sin una clasificación uniforme.

## Resultado esperado

Cada pedido se convierte en un registro estructurado, con categoría, prioridad, responsable, fecha objetivo, estado y trazabilidad. El equipo recibe una notificación y el solicitante obtiene una respuesta inicial, siempre con revisión humana antes de ejecutar acciones sensibles.

## Ejemplo de solicitud

“Necesitamos gestionar el acceso de Juan Pérez al proyecto Cliente X y actualizar la información de facturación. Idealmente debería quedar resuelto antes del viernes.”

## Qué hace la automatización

1\. Recibe la solicitud desde Gmail o un formulario.
2\. Envía el texto a un modelo de IA para clasificarlo.
3\. Extrae persona, cliente, proyecto, categoría, prioridad y fecha límite.
4\. Valida si faltan datos y, si corresponde, marca el pedido para revisión.
5\. Crea un registro en Google Sheets o Airtable.
6\. Asigna el pedido a un responsable según reglas predefinidas.
7\. Notifica por email o Slack al responsable.
8\. Redacta una respuesta inicial para que un administrativo la revise.
9\. Actualiza el estado: recibido, en revisión, asignado, resuelto o requiere información.
10\. Conserva un historial simple de la solicitud y sus decisiones.

# 5\. Objetivos de la masterclass

## Objetivo general

Demostrar que los perfiles administrativos pueden diseñar automatizaciones útiles con IA, conectando herramientas existentes y manteniendo supervisión humana.

## Objetivos específicos

Entender qué es AI Automation y cómo se diferencia de usar un chatbot aislado.
Identificar tareas candidatas para automatizar por repetición, volumen, reglas o necesidad de seguimiento.
Visualizar la estructura de un flujo en n8n: entrada, procesamiento, decisión, acción y control.
Reconocer cómo la IA interpreta lenguaje natural y lo transforma en datos operables.
Comprender el valor de integrar email, planillas, bases de datos y canales de comunicación.
Discutir límites: datos sensibles, errores de clasificación, permisos y aprobación humana.
Conectar la experiencia con los contenidos y proyectos de la carrera AI Automation de Henry.

# 6\. Guion paso a paso de la sesión

## Bloque 1 — Apertura y contexto | 5 minutos

Presentar el objetivo: no se trata de reemplazar el criterio de las personas, sino de quitar trabajo repetitivo y ordenar la operación. Pregunta de entrada por chat: ¿por qué canal reciben hoy la mayoría de las solicitudes internas?
\[TRANSICIÓN → SLIDE 2\] Si las solicitudes llegan por múltiples canales, el problema no es únicamente responder: es clasificar, priorizar y hacer seguimiento.

## Bloque 2 — Qué significa automatizar con IA | 10 minutos

Explicar la diferencia entre una automatización tradicional, que sigue reglas fijas, y una automatización con IA, que puede interpretar textos, extraer datos, clasificar pedidos y redactar respuestas.
\[TRANSICIÓN → SLIDE 3\] La pregunta pasa de “¿podemos usar IA?” a “¿en qué punto del proceso aporta criterio y dónde debe seguir interviniendo una persona?”.

## Bloque 3 — Presentación del caso | 5 minutos

Mostrar el email de ejemplo y el resultado esperado. Aclarar que se trata de datos ficticios y que la demo no utiliza información confidencial de Horbath.
\[TRANSICIÓN → SLIDE 4\] Ahora que tenemos claro el problema y el resultado, vamos a recorrer el flujo que lo conecta.

## Bloque 4 — Demo en vivo del flujo n8n | 25 minutos

Construir o recorrer el flujo visualmente: Trigger → extracción → clasificación → estructuración → registro → asignación → notificación → borrador de respuesta → aprobación humana. En cada nodo explicar qué entra, qué sale y qué decisión se toma.
\[TRANSICIÓN → SLIDE 5\] El valor no está en un nodo aislado, sino en la cadena completa: cada paso deja al siguiente mejor preparado.

## Bloque 5 — Aplicación al trabajo de los asistentes | 10 minutos

Pedir a los participantes que piensen en una tarea repetitiva de su área. Guiar la conversación con cuatro preguntas: ¿qué dispara el proceso?, ¿qué información hay que extraer?, ¿quién debe actuar?, ¿cómo sabemos que quedó resuelto?
\[TRANSICIÓN → SLIDE 6\] La misma lógica puede reutilizarse en distintos procesos, cambiando las categorías, responsables y herramientas.

## Bloque 6 — Cierre y conexión con Henry | 5 minutos

Recapitular el método: detectar una tarea, diseñar el flujo, conectar herramientas, incorporar IA, validar y mejorar. Presentar AI Automation como una formación práctica para construir automatizaciones y agentes sin requerir programación previa.
\[TRANSICIÓN → SLIDE 7\] La masterclass muestra el punto de partida; la carrera acompaña el desarrollo de soluciones más completas y un portafolio propio.

# 7\. Diseño funcional del flujo en n8n

Flujo conceptual:
Gmail/Formulario → Normalización del pedido → IA: clasificación y extracción → Validación de campos → Google Sheets/Airtable → Router por categoría → Slack/Email al responsable → IA: borrador de respuesta → Aprobación humana → Actualización de estado → Registro de auditoría

## Nodos sugeridos

Trigger: Gmail Trigger o Webhook/Form Trigger.
Normalización: Set / Edit Fields.
IA: OpenAI Chat Model o nodo equivalente.
Salida estructurada: Structured Output Parser.
Reglas: IF / Switch para categoría, prioridad o información faltante.
Registro: Google Sheets o Airtable.
Comunicación: Gmail y Slack.
Control: aprobación humana antes de enviar o ejecutar acciones.
Seguimiento: actualización del estado y timestamp.
Documentación: nota sobre supuestos, errores y decisiones.

## Datos mínimos del registro

ID de solicitud | fecha de ingreso | solicitante | canal | categoría | cliente/proyecto | descripción | prioridad | responsable | fecha objetivo | estado | última actualización | enlace al pedido original | observaciones.

## Guardrails para la demo

No ejecutar cambios reales en accesos, facturación o datos de clientes.
Usar información ficticia y cuentas de prueba.
Mostrar aprobación humana para acciones sensibles.
Dejar claro que la IA puede equivocarse y que la salida debe validarse.
Evitar exponer información personal o confidencial en pantalla.

# 8\. Deck ejecutivo de soporte

Comunicación del deck: al finalizar, el equipo de Horbath debe entender que existe un caso concreto, transversal y accionable para aprender AI Automation; no debe quedarse con una definición abstracta de IA.
Mensaje central: una solicitud que hoy llega desordenada puede convertirse en un proceso trazable con IA, sin quitarle a la persona el control de la decisión.

## Slide 1 — Una solicitud no debería perderse en una bandeja de entrada

Objetivo: abrir con una situación reconocible para perfiles administrativos. Mostrar el título del caso y una frase breve: “La oportunidad no es responder más rápido; es ordenar el proceso completo.”
Nota del expositor: presentar el contexto y anticipar que se verá un flujo aplicado a la operación.
TRANSICIÓN A SLIDE 2: “Antes de mostrar la solución, veamos dónde se genera la fricción.”

## Slide 2 — El problema aparece cuando el pedido llega sin estructura

Mostrar cuatro fricciones: pedidos en distintos canales, datos incompletos, derivaciones manuales y poco seguimiento. No afirmar que son problemas confirmados de Horbath: presentarlos como hipótesis de trabajo a validar.
TRANSICIÓN A SLIDE 3: “Si el pedido está en lenguaje natural, la IA puede ayudar a convertirlo en información accionable.”

## Slide 3 — La IA convierte lenguaje natural en datos operables

Mostrar el email ficticio a la izquierda y los campos estructurados a la derecha: categoría, prioridad, responsable, proyecto, fecha objetivo y estado.
TRANSICIÓN A SLIDE 4: “Con los datos estructurados, ya podemos conectar cada paso del proceso.”

## Slide 4 — El flujo conecta entrada, decisión y seguimiento

Mostrar el lienzo de n8n con el flujo completo. Marcar visualmente el punto de decisión de IA y el punto de aprobación humana.
TRANSICIÓN A SLIDE 5: “Veamos qué sucede cuando el flujo corre de punta a punta.”

## Slide 5 — La demo: de un email a una solicitud asignada

Usar el deck como soporte mínimo y pasar a n8n. El slide debe mostrar el antes y después: email libre → registro → responsable notificado → borrador de respuesta.
TRANSICIÓN A SLIDE 6: “Este patrón no depende de un único tipo de solicitud.”

## Slide 6 — El patrón se adapta a varias áreas

Mostrar ejemplos de aplicación: People, Finanzas, Compras, Accesos, Soporte y Gestión de proyectos. Enfatizar que se cambian reglas y responsables, no la lógica base.
TRANSICIÓN A SLIDE 7: “La masterclass deja una forma concreta de detectar estas oportunidades.”

## Slide 7 — Cinco preguntas para encontrar una automatización

¿Qué dispara el proceso? ¿Qué datos hay que extraer? ¿Qué decisión se repite? ¿Quién debe actuar? ¿Cómo queda registrada la resolución?
TRANSICIÓN A SLIDE 8: “Ese método es justamente el punto de partida de AI Automation.”

## Slide 8 — AI Automation: aprender construyendo

Conectar la experiencia con Henry: automatizaciones, integraciones, APIs, webhooks, agentes y proyectos prácticos con herramientas no-code y low-code.
Cierre: “La pregunta no es si la IA puede hacer todo. Es qué parte del proceso podemos mejorar hoy, con criterio y control.”

# 9\. Lienzo de n8n para iterar

Este lienzo debe mantenerse como pieza viva antes y durante la preparación. La primera versión puede usar nombres genéricos; la segunda debe incorporar las categorías y canales que Horbath valide.

## Entrada

¿Email, formulario, Slack u otro canal? ¿Qué tipo de pedidos ingresan? ¿Qué información suele faltar?

## Interpretación con IA

¿Qué categorías debe reconocer? ¿Qué campos debe extraer? ¿Qué casos requieren pedir información adicional?

## Decisión

¿Qué reglas determinan prioridad y responsable? ¿Qué pedidos pueden avanzar automáticamente y cuáles requieren aprobación?

## Acción

¿Dónde se registra? ¿Quién recibe la notificación? ¿Qué respuesta se prepara? ¿Qué herramienta ya usa el equipo?

## Control y mejora

¿Cómo se valida la salida? ¿Qué errores deben registrarse? ¿Qué métrica mostraría que el flujo funciona mejor?

## Versión inicial para la demo

Gmail/Formulario → IA clasifica y extrae → Google Sheets registra → Switch asigna → Slack/Email notifica → IA redacta respuesta → aprobación humana → estado actualizado.

## Versión a validar con Horbath

Reemplazar categorías genéricas por las áreas reales; definir un ejemplo de solicitud representativo; confirmar herramienta de registro; confirmar canal de notificación; acordar qué parte se puede simular y qué parte debe quedar explícitamente fuera de alcance.

# 10\. Preguntas de validación para Agustina / Horbath

¿El público será exclusivamente administrativo o también participarán People, Operaciones, Finanzas o PMO?
¿Qué canal resulta más representativo para la demo: email, formulario o Slack?
¿Qué tipo de solicitud interna sería más reconocible para la audiencia?
¿Prefieren un caso de accesos, People, Finanzas, Compras, soporte o coordinación de proyectos?
¿Qué herramientas utilizan o pueden simular en el entorno de la sesión?
¿Podemos mostrar Gmail, Google Sheets/Airtable y Slack como herramientas ficticias?
¿Hay alguna restricción sobre grabación, uso de IA o exposición de información?
¿Quién moderará el Zoom y cómo se tomarán las preguntas?
¿Quieren un cierre comercial breve sobre la carrera o una invitación a conocerla posteriormente?
¿Qué definición de éxito usarán para evaluar la masterclass?

# 11\. Fuentes y supuestos

La propuesta se basa en el posicionamiento público de Horbath como empresa de desarrollo de software, analítica, automatización y servicios tecnológicos, y en la descripción vigente de AI Automation de Henry como formación en automatización de procesos, flujos, agentes, APIs, webhooks y herramientas no-code/low-code.
No se asumen procesos internos específicos de Horbath. El caso, las categorías y las herramientas deben validarse antes de convertir la demo en un ejemplo definitivo.
Fuente Henry: [https://www.soyhenry.com/carrera-ai-automation](https://www.soyhenry.com/carrera-ai-automation)
Fuente Horbath: [https://horbath.com/en/](https://horbath.com/en/)
Contenido de referencia: [https://www.youtube.com/watch?v=24xGV4vqSZk](https://www.youtube.com/watch?v=24xGV4vqSZk)
Última actualización del documento: 23 de julio de 2026\.

12\. Versión final basada en la automation implementada

Arquitectura real del workflow
Gmail Trigger (cada minuto) → Normalizar Datos → Analizar Solicitud con IA → Validar Confianza y Datos → Validación Pasó?

Capa de IA
El nodo “Analizar Solicitud con IA” es un agente LangChain con Structured Output Parser. Usa OpenAI GPT-5-mini como modelo principal, Gemini Flash Lite 3.1 como fallback y Qwen 3.6 conectado al parser para auto-fix. La salida se valida contra el JSON Schema de la propuesta.

Criterio real de validación
La solicitud se considera válida solo cuando confidence \>= 0.75, la categoría y prioridad son válidas, existe requester\_email y missing\_information está vacío. Si no se cumple, validation\_passed=false y validation\_reason identifica “Confianza baja”, “Información faltante” o “Datos inválidos”.

Rama de solicitudes incompletas
Marcar Requiere Información → Solicitar Información Faltante por Gmail → Registrar Solicitud Incompleta en la pestaña Solicitudes\_Incompletas. Esta es la rama que debe mostrarse primero en la demo porque hace visible el valor de la IA: detectar qué falta y pedirlo.

Rama de solicitudes válidas
Registrar Solicitud Válida en Solicitudes\_Completas → Asignar por Categoría → notificación Slack. El Switch contempla People, Finanzas, Compras, Accesos, Soporte, Proyectos, Administración y Revisión Manual. En la versión actual, las ramas notifican al canal masterclass-n8n; los responsables reales son configurables.

Alcance actual de la aprobación humana
El workflow calcula requires\_human\_approval y lo muestra en Sheets y Slack, pero todavía no incluye un nodo de aprobación que detenga la ejecución. En el deck debe presentarse como “señal de control para revisión humana”, no como una aprobación automatizada ya implementada.

Libreto actualizado para la demo
1\. En el deck: presentar el problema y el resultado esperado.
2\. TRANSICIÓN DECK → LIENZO: “Ya vimos qué problema resolvemos; ahora abrimos n8n para seguir una solicitud real dentro del workflow.”
3\. En el lienzo: mostrar Gmail Trigger, Normalizar Datos, Agente LangChain, modelos, parser, validación y las dos ramas.
4\. Mostrar primero la rama incompleta: email de información faltante y registro en Solicitudes\_Incompletas.
5\. Mostrar luego la rama válida: registro en Solicitudes\_Completas, Switch por categoría y Slack.
6\. TRANSICIÓN LIENZO → DECK: “El lienzo muestra cómo funciona; volvamos al deck para resumir qué patrón puede reutilizar cada área.”
7\. En el deck: cerrar con las categorías, las cinco preguntas para detectar oportunidades y la conexión con AI Automation de Henry.

Prompt actualizado para NotebookLM
Actuá como especialista en storytelling ejecutivo y presentaciones sobre IA. Usá la propuesta y el JSON de la automation final como fuentes. Creá una PPT editable para una masterclass de Henry dirigida a perfiles administrativos de Horbath Technologies. La estructura visual queda a tu criterio, pero la narrativa debe avanzar de problema → caso → workflow real → ramas incompleta/válida → Slack → aprendizajes.

Representá exactamente esta arquitectura: Gmail Trigger cada minuto → Normalizar Datos → agente LangChain con OpenAI GPT-5-mini, Gemini Flash Lite 3.1 como fallback, Structured Output Parser con Qwen 3.6 para auto-fix → Validar Confianza y Datos → IF Validación Pasó?. La rama falsa solicita información faltante por Gmail y registra en Solicitudes\_Incompletas. La rama verdadera registra en Solicitudes\_Completas, asigna por categoría con Switch y notifica Slack en ocho salidas: People, Finanzas, Compras, Accesos, Soporte, Proyectos, Administración y Revisión Manual.

No presentes la aprobación humana como un paso ya implementado: el workflow solo calcula requires\_human\_approval y lo muestra en Sheets/Slack. No inventes métricas ni procesos internos de Horbath. Marcá visiblemente estas transiciones: “TRANSICIÓN DECK → LIENZO: Ya vimos qué problema resolvemos; ahora abrimos n8n para seguir una solicitud real dentro del workflow.” y “TRANSICIÓN LIENZO → DECK: El lienzo muestra cómo funciona; volvamos al deck para resumir qué patrón puede reutilizar cada área.” Incluilas también en las notas del presentador.

Última actualización de esta sección: 24 de julio de 2026\.
