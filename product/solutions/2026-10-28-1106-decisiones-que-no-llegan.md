---
opportunity: decisiones-que-no-llegan
status: chosen
chosen: recap-de-decisiones
tests:
---

# Soluciones para: las decisiones de las reuniones no llegan bien a quienes tienen que ejecutarlas

## Qué dice hoy la evidencia
- Valor (#2): sin anotaciones en el registro, apoyado por evidencia real. Los 10 entrevistados contaron un incidente con costo y 8 de 10 rehacen el cierre a mano (20 a 60 min) (`real`, `product/insights/2026-10-28-1022-entrevistas-colaboracion-en-vivo.md`). El 24% no registró lo decidido (`survey`, n=182, `product/insights/2026-10-28-0945-colaboracion-en-vivo-fuera-de-teams.md`). Sesgo: todos los entrevistados trabajan fuera de Teams. El umbral de "la mitad en 3 meses" sigue sin medirse.
- Viabilidad (#1): abierta. Sin conversaciones con compradores. Las señales que hay van en contra: el resumen con IA ya viene incluido y la escalera de precios lleva a Copilot y E7 (`secondary`, `product/research/2026-10-14-1133-colaboracion-en-vivo-reuniones.md`).
- Toda la evidencia es sobre el problema. Nadie reaccionó todavía a una solución.
- La exploración se hizo antes de la decisión de seguir o no que la agenda fija para el 2026-12-11. Lo que se testee convive con las preguntas abiertas de #1 y #2.

## Línea de base: lo que se hace hoy
El líder rehace el cierre a mano después de cada reunión (correo, Jira o el recap de IA reescrito), con un costo de 20 a 60 min, y "nadie más lo hace" (8 de 10, `real`). Igual falla: el responsable no queda claro, la decisión queda donde nadie la lee, el cierre llega tarde o se transcribe mal. Javier reescribe el recap (30 min), Paula lo corrige siempre (10 min o más) y Martina lo abandonó (`real`). Quien ejecuta busca la minuta o pregunta "¿qué se decidió?". En Teams sin herramientas externas, "hablan y alguien anota" (6 de 16, `survey`, direccional).

## Alternativas
### A1. Recap de decisiones confirmado por el líder (`recap-de-decisiones`)
Al terminar la reunión, la IA arma una lista que contiene solo decisiones y compromisos, cada uno con responsable, fecha y porqué, e incluye lo que se vio en pantalla o en el tablero. El líder la corrige y la confirma antes de enviarla. Ataca "se transcribe mal" y "no queda claro quién lo hace". Para Andrés Quintero y Lucía Ferreyra (primary). Reemplaza el recap reescrito y el cierre manual. Reúne las ideas candidatas 1 y 6 del brief.

### A2. Cierre en vivo con acuerdo explícito (`cierre-en-vivo`)
Durante la reunión se anotan las decisiones en un registro que todos ven. En los últimos minutos, cada participante confirma si está de acuerdo o deja su objeción. Ataca el responsable ambiguo y el desacuerdo que aparece después. Para Andrés y Lucía (primary). Reemplaza el cierre posterior. Reúne las ideas 2 y 5.

### A3. Publicar lo decidido donde vive el trabajo (`decision-donde-se-trabaja`)
Cada decisión, con su responsable, se publica como ítem en Jira o Planner, en el canal o en el documento del equipo, enlazada a la reunión. Ataca "la decisión queda donde nadie la lee". Para Ramiro Gutiérrez (secondary, quien ejecuta). Reemplaza la copia manual del líder a Jira o al correo. Idea 3.

### A4. Retomar las decisiones al abrir la siguiente reunión de la serie (`decisiones-de-la-serie`)
Al abrir la reunión siguiente se muestran las decisiones anteriores y su estado (hecho, pendiente, sin responsable). El registro sobrevive a reprogramaciones y a cambios de la serie. Ataca la continuidad y la detección tardía. Para Andrés y Lucía. Reemplaza el tablero de Miro por trimestre y la reconstrucción de memoria. Idea 4.

### A5. Ritual de cierre de 5 minutos con plantilla en Loop (`ritual-de-cierre`)
No es software nuevo y es lo más chico que podría funcionar. Una práctica más una plantilla en las notas de Loop, que ya vienen incluidas y sincronizan con Planner. Se reservan los últimos 5 min para leer cada decisión en voz alta: qué, quién, cuándo, por qué y si hubo acuerdo. Ataca el responsable ambiguo y el cierre tardío. Para Andrés y Lucía. Reemplaza el cierre manual posterior.

## Comparación
| Alternativa | Deseable | Factible | Viable | Creencia de mayor riesgo |
|---|---|---|---|---|
| A1 | mixed: pain evidenced, relief not tested. 6 de 10 ya usan el recap y le piden esto, el recap causó 2 incidentes (`real`, entrevistas) y hay 23 menciones espontáneas (`survey`, n=182) | to check with tech: leer pantalla y tablero bajo las restricciones de privacidad y rendimiento del brief | weak: el resumen con IA ya viene incluido y el recap está en Teams Premium (`secondary`, research) | Con un recap que lista solo decisiones y compromisos (responsable, fecha, porqué), el líder lo confirma con 5 min o menos de correcciones y sin ideas marcadas como decisiones en 8 de cada 10 reuniones. Cae si sigue reescribiéndolo (más de 10 min) en más de la mitad |
| A2 | mixed: pain evidenced, relief not tested. Cumple el criterio de acuerdo del equipo (`real`). En contra: notas en el 8% de las reuniones (`real`, datos internos, overview) y Paula y Ricardo no deciden en reuniones grandes (`real`) | to check with tech: tiempo real y rendimiento con 9 a 14 personas | unknown (`assumption`) | Alguien registra las decisiones durante la reunión y los participantes confirman su acuerdo en 7 de cada 10 reuniones, sin alargarla más de 5 min. Cae si se abandona antes de las 3 semanas |
| A3 | mixed: pain evidenced, relief not tested. 3 de 10 incidentes por "quedó donde nadie la lee" (`real`); "el qué queda en Jira, el porqué se pierde" (`survey`). Nadie entrevistó a quien ejecuta | to check with tech: integraciones con Jira, Slack y Confluence bajo restricciones de seguridad. Depende de un mecanismo de captura | unknown (`assumption`): la más cercana al argumento de #1, sin evidencia de compradores | Cuando la decisión llega como ítem en la herramienta de quien ejecuta, esa persona la ejecuta sin preguntar "¿qué se decidió?". Cae si en más de 3 de cada 10 decisiones igual pregunta o la ejecuta distinto |
| A4 | mixed: sustituto en uso, el frame de Miro revisado al empezar la sesión (`real`, n=2), pero de tableros, no de decisiones, y solo en series recurrentes | to check with tech: anclar artefactos a la serie, defecto conocido de Whiteboard y Loop (`real`) | unknown (`assumption`) | La mayoría de las decisiones que fallan nace en reuniones recurrentes y se detecta en la siguiente sesión antes de que el costo ocurra. Cae si la mayoría de los incidentes se volvió caro antes o vino de reuniones únicas |
| A5 | mixed: pain evidenced, relief not tested. Se parece al workaround que ya falla; problemas de descubrimiento de Loop (`real`) | strong: Loop y la sincronización con Planner incluidos en todos los planes (`secondary`, research) | weak: gratis, no da motivo para pasar a Max (`assumption`) | Los líderes sostienen el cierre de 5 min durante 4 semanas y los incidentes bajan frente al cierre posterior. Cae si menos de la mitad lo sostiene después de 2 semanas |

Riesgo común: ninguna alternativa tiene evidencia de viabilidad. La creencia #1 puede tumbar la oportunidad cualquiera sea la solución.

## Decisión
El usuario (PM) eligió A1 para testear el 2026-10-28. La IA había recomendado testear A1 y A3 en paralelo: entre las dos cubren las cuatro causas de falla, A3 mira a quien ejecuta y sostiene mejor el argumento de viabilidad, y sus creencias son independientes. El PM eligió A1 sola por foco: un solo test llega antes a CollabCon, y A3 puede sumarse después como destino del recap confirmado. La diferencia quedó registrada en `product/corrections.md`.

## A testear
- A1: "Con un recap que lista solo decisiones y compromisos (responsable, fecha, porqué), el líder lo confirma con 5 min o menos de correcciones y sin ideas marcadas como decisiones en 8 de cada 10 reuniones." Es la que la mata: si el líder igual tiene que reescribirlo, A1 es el recap actual con otro formato y no supera el workaround. Se diseña en /design-solution-tests.

## Propuesta de valor: recap-de-decisiones
- **Dolor que alivia:** el cierre manual de 20 a 60 min que rehace el líder (8 de 10, `real`) y el recap que mezcla ideas con decisiones y no dice quién se comprometió a qué. Ese recap causó 2 incidentes: una semana de dos devs (Paula) y una entrega dos semanas tarde en México (Javier) (`real`).
- **Ganancia:** el cierre queda hecho en minutos, antes de que nadie lo lea. Cada decisión tiene responsable, fecha, porqué e indica si hubo acuerdo explícito u objeción (criterio del equipo). Lo que fue solo una idea no aparece como decisión.
- **Qué reemplaza:** reescribir o corregir el recap (Javier 30 min, Paula 10 min o más) o abandonarlo (Martina). El cambio no pide un hábito nuevo: el recap ya está en el flujo de 6 de 10. Cambia que el líder confirma en lugar de reescribir.
- **Lo que deliberadamente no hace:** no publica en Jira, Slack ni Confluence (A3, estacionada). No pide que nadie registre ni vote durante la reunión (A2). No da continuidad entre sesiones de la serie (A4). No resume la conversación: lo que no es decisión ni compromiso queda afuera. No aborda la participación ni el desacuerdo como problema, solo registra si hubo acuerdo.

## Creencias
- [opportunity: decisiones-que-no-llegan] [viability] #1 del registro (referenciada).
- [opportunity: decisiones-que-no-llegan] [value] #2 del registro (referenciada).
- [feature: recap-de-decisiones] [value] #10 del registro. Con un recap que lista solo decisiones y compromisos (responsable, fecha, porqué, y si hubo acuerdo), los líderes que conducen reuniones de más de 5 personas lo confirman con 5 min o menos de correcciones y sin ideas marcadas como decisiones en al menos 8 de cada 10 reuniones, frente a los 20 a 60 min del cierre manual. Cae si en más de la mitad de las reuniones el líder lo reescribe (más de 10 min) o vuelve al cierre manual.
- [feature: recap-de-decisiones] [feasibility] #11 del registro. El recap puede distinguir decisiones de ideas y sumar lo compartido en pantalla o en el tablero dentro de las restricciones de privacidad, seguridad corporativa y rendimiento del brief. Cae si tech no puede leer el contenido compartido sin sacar datos del tenant o sin afectar el rendimiento de la reunión. — to check with tech
- [feature: recap-de-decisiones] [viability] #12 del registro. Los compradores de IT del segmento distinguen un recap de decisiones confirmado del recap incluido en Teams Premium y lo cuentan como parte de una razón para pasar a Max. Cae si menos de 3 de cada 10 lo distinguen del resumen que ya consideran incluido.

## Descartadas o estacionadas
- A2 (`cierre-en-vivo`): parked. Depende de registrar durante la reunión, y la evidencia de notas nativas (8% de las reuniones) va en contra. Vuelve si el test de A1 muestra que el acuerdo explícito no se puede capturar después de la reunión.
- A3 (`decision-donde-se-trabaja`): parked, por decisión de foco del PM. Vuelve como destino del recap confirmado si A1 pasa su test, o antes si las entrevistas a quienes ejecutan (agenda, 2026-12-02) muestran que el lugar pesa más que el contenido.
- A4 (`decisiones-de-la-serie`): parked. Solo cubre series recurrentes. Vuelve si al releer los 10 incidentes resulta que la mayoría se habría detectado en la siguiente sesión.
- A5 (`ritual-de-cierre`): parked como control. No mueve el upgrade. Puede servir de comparación en /design-solution-tests: si un ritual gratis logra lo mismo, Max no tiene qué vender.

## Resultado
