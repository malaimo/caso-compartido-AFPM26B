---
opportunity: decisiones-que-no-llegan
solutions: product/solutions/2026-10-28-1106-decisiones-que-no-llegan.md
status: analyzed
---

# Tests de solución para: las decisiones de las reuniones no llegan bien a quienes tienen que ejecutarlas

## Por qué testear
A1 (`recap-de-decisiones`) es la única alternativa en test. Toda la evidencia es sobre el problema: 8 de 10 líderes rehacen el cierre a mano y el recap de IA actual les falla a 6 de 10 (`real`). Nadie vio ni usó todavía un recap que liste solo decisiones y compromisos. Siguen abiertas tres creencias: que reemplace el cierre manual (#10), que IT lo distinga del recap incluido en Premium (#12) y que la IA pueda armarlo (#11). Se testean en ese orden, porque T1 es el que puede descartar A1 más rápido y produce el material de T2 y la clave de respuestas de T3. A5 (`ritual-de-cierre`) no entra como control en esta ronda.

## T1. recap-de-decisiones: recap armado a mano en reuniones reales
- **Test status:** analyzed
- **Belief under test:** "[feature: recap-de-decisiones] [value] Con un recap que lista solo decisiones y compromisos (responsable, fecha, porqué, y si hubo acuerdo), los líderes que conducen reuniones de más de 5 personas lo confirman con 5 min o menos de correcciones y sin ideas marcadas como decisiones en al menos 6 de cada 10 reuniones, frente a los 20 a 60 min del cierre manual. Cae si en más de la mitad de las reuniones el líder lo reescribe (más de 10 min) o vuelve al cierre manual." (#10)
- **Risk:** [value]
- **Test type:** concierge
- **What we do:**
  1. Cada líder elige 2 reuniones propias de las 2 semanas siguientes, de más de 5 personas, donde se espera decidir algo. El líder avisa a los participantes que va a haber una observadora.
  2. Una persona del equipo entra en silencio, con cámara y micrófono apagados. Sigue lo que se habla, la pantalla, el tablero y el chat, y arma el recap con la plantilla.
  3. Dentro de los 30 min posteriores al cierre, le deja al líder el recap en un documento editable con historial de versiones, con un solo pedido: "Corrígelo si hace falta y, si te sirve, envíalo a tu equipo como cierre de la reunión. Si prefieres hacer tu cierre de siempre, hazlo."
  4. El líder corrige el recap, marca los ítems que no eran decisiones y lo envía, o no lo envía.
  5. Al día siguiente se le hacen dos preguntas por mensaje: si además hizo su cierre de siempre y, si no envió el recap, por qué.
- **With whom:** 5 de los entrevistados reales que rehacen el cierre a mano y conducen reuniones de más de 5 personas en las que se decide algo. Quedan afuera Paula y Ricardo, que no deciden en reuniones grandes. Tienen prioridad quienes usan o usaron el recap de IA. Son 2 reuniones por líder, 10 en total. El reclutamiento se hace por el mismo contacto de la entrevista. El consentimiento incluye usar el recap, la transcripción y las capturas de pantalla en T2 (anonimizados) y en T3. Sesgo conocido: todos trabajan fuera de Teams.
- **Material needed:** (a) Una plantilla del recap. Por cada ítem lleva: decisión o compromiso, responsable, fecha, porqué, acuerdo (explícito / objeción / no se vio) y fuente (voz / pantalla / tablero / chat). Incluye una regla escrita de qué cuenta como decisión (alguien la cerró explícitamente) y qué queda afuera. Queda deliberadamente afuera: el resumen de la conversación, los temas tratados, la publicación en Jira, Slack o Confluence y la continuidad con reuniones anteriores. (b) Un guion para la observadora, con el mensaje de reclutamiento y consentimiento, el mensaje de entrega y las preguntas del día siguiente. (c) Una planilla de captura por reunión con: hora de entrega; minutos de corrección (según el historial de versiones, del primer al último cambio antes del envío); ítems eliminados como "no era decisión"; decisiones que agregó el líder; campos corregidos, por tipo; si se envió y a dónde; si hubo además un cierre manual; y la fuente de cada ítem que se mantuvo.
- **Material:** [product/tests/materials/t1-recap-de-decisiones/](materials/t1-recap-de-decisiones/): `plantilla-recap.md`, `guion-observadora.md`, `mensajes.md`, `planilla-captura.md`
- **Duration:** 1 semana de reclutamiento y 2 semanas de reuniones, del 2026-11-09 al 2026-11-20.
- **Signal and threshold:** Una reunión cuenta como **confirmada** si cumple las cuatro condiciones: el líder envía el recap como cierre, lo corrige en 5 min o menos, no marca ningún ítem como "no era decisión" y no hace además su cierre manual. Una reunión cuenta como **fallida** si el líder reescribe el recap (más de 10 min de corrección), no lo envía o hace igual su cierre manual. Pasa si hay 6 o más reuniones confirmadas de 10. Las reuniones en las que no se decidió nada no cuentan y se reemplazan. Si quedan menos de 8 reuniones válidas, el resultado es `inconclusive`. Umbral original: 8 de 10. El PM lo bajó a 6 el 2026-11-20, después de ver los resultados (ver `product/corrections.md`).
- **Decision rule:**
  - continue si hay 6 o más reuniones confirmadas de 10.
  - discard si hay más de 5 reuniones fallidas de 10.
  - change en cualquier otro caso. Se revisa en la planilla qué se corrigió. Si las correcciones se concentran en un campo (por ejemplo, responsable o acuerdo), se rediseña ese punto y la nueva versión se testea con este mismo protocolo.
- **Expected provenance:** real
- **Next step if it passes:** T2 y T3. Este resultado vale para un recap armado por una persona. Si T3 pasa, se repite este protocolo con el recap que genera el prompt antes de pasar a la spec.

## T2. recap-de-decisiones: ¿IT distingue el recap de decisiones del recap de Premium?
- **Test status:** designed
- **Belief under test:** "[feature: recap-de-decisiones] [viability] Los compradores de IT del segmento distinguen un recap de decisiones confirmado del recap incluido en Teams Premium y lo cuentan como parte de una razón para pasar a Max. Cae si menos de 3 de cada 10 lo distinguen del resumen que ya consideran incluido." (#12)
- **Risk:** [viability]
- **Test type:** buyer-conversation
- **What we do:** Es un bloque de unos 10 min al final de las 10 conversaciones con compradores de IT que la agenda fija para el 2026-12-02 por la creencia #1. Va después de las preguntas de #1 para no contaminarlas. Se corre solo si T1 no termina en `discard`; si termina así, las conversaciones de #1 siguen sin este bloque.
  1. Se muestran dos cierres de la misma reunión de T1, anonimizados y sin rótulo: el recap de Teams Premium de esa reunión y el recap confirmado por el líder. Si la reunión no tiene recap de Premium, se genera uno con Premium a partir de la grabación. El orden de los dos cierres se alterna entre conversaciones.
  2. Se hace una pregunta abierta: "¿Qué diferencia ves entre los dos?". Se anota si el comprador nombra la diferencia sin que se la señalen: que lista solo decisiones, con responsable, y que lo confirmó el líder.
  3. Recién después se explica qué es cada cierre y se pregunta si eso entraría en el caso para pasar a Max, y con qué condición.
  4. Se pide un compromiso concreto: llevarlo a la conversación de renovación, presentar a quien aprueba el presupuesto o sumar su cuenta a una prueba.
- **With whom:** 10 compradores de IT con el perfil de Héctor (deciden el plan de Microsoft 365 y negocian la renovación) de cuentas Business Premium del segmento. Se reclutan por el mismo canal que las conversaciones de #1.
- **Material needed:** (a) El par de cierres de una reunión de T1, anonimizados (nombres, clientes, cifras), de una página cada uno y sin marca que indique cuál es el nuevo. (b) Un guion del bloque con las preguntas en orden y sin ningún argumento de venta antes de la pregunta abierta. (c) Una planilla de captura por comprador con: si distinguió los cierres sin ayuda y con qué palabras; si lo cuenta como razón para Max; las condiciones que nombró; y si asumió un compromiso concreto y cuál. Queda deliberadamente afuera: el precio, las demos y cualquier funcionalidad que no esté en T1 (Jira, continuidad).
- **Material:** (lo agrega /build-solution-test)
- **Duration:** dentro de las conversaciones del 2026-12-02, unos 10 min al final de cada una.
- **Signal and threshold:** Se cuentan dos cosas por comprador. Primero, si **distingue sin ayuda** el recap de decisiones del recap de Premium. Segundo, si **lo cuenta como razón** para Max, y para eso tiene que decir que entraría en el caso de Max y aceptar un compromiso concreto. Una respuesta verbal sin compromiso no alcanza. El umbral es 3 de 10, el mismo de la #12.
- **Decision rule:**
  - continue si 3 o más de 10 lo distinguen sin ayuda y lo cuentan como razón.
  - change si 3 o más lo distinguen pero menos de 3 lo cuentan como razón. Se registran las condiciones que nombran (por ejemplo, que publique en Jira, lo que reabre A3) y esa versión se testea aparte.
  - discard si menos de 3 de 10 lo distinguen del recap de Premium.
- **Expected provenance:** real
- **Next step if it passes:** una conversación con quien aprueba el presupuesto (CFO o sponsor) en las cuentas que se comprometieron, con el precio de Max sobre la mesa.

## T3. recap-de-decisiones: precisión del recap generado contra la clave de T1
- **Test status:** designed
- **Belief under test:** "[feature: recap-de-decisiones] [feasibility] El recap puede distinguir decisiones de ideas y sumar lo compartido en pantalla o en el tablero dentro de las restricciones de privacidad, seguridad corporativa y rendimiento del brief. Cae si tech no puede leer el contenido compartido sin sacar datos del tenant o sin afectar el rendimiento de la reunión." (#11)
- **Risk:** [feasibility]
- **Test type:** technical-test
- **What we do:**
  1. Tech arma un prompt o pipeline que produce el recap con la misma plantilla de T1. Usa como entrada la transcripción, el chat y las capturas de lo que se compartió en pantalla o en el tablero en cada reunión de T1.
  2. El resultado se compara con la clave de respuestas: el recap confirmado por el líder en T1, con las decisiones que agregó y los ítems que eliminó.
  3. En paralelo, tech verifica si el procesamiento puede correr dentro del tenant, sin sacar datos, y sin cargar el cliente de la reunión (por ejemplo, procesando después del cierre).
- **With whom:** el owner es tech. Los datos son las 10 reuniones de T1, con el consentimiento de los líderes.
- **Material needed:** (a) El set de entrada: transcripciones, chat y capturas de pantalla o tablero de las 10 reuniones. (b) La clave de respuestas: los recaps confirmados de T1, con la fuente de cada ítem. (c) Una planilla de captura por reunión y por ítem con: si la decisión de la clave está presente; los ítems del prompt que no están en la clave; si el responsable y la fecha son correctos; y la fuente del ítem. Queda deliberadamente afuera: la interfaz, la integración en Teams y el envío.
- **Material:** (lo agrega /build-solution-test)
- **Duration:** 1 semana después de T1, del 2026-11-23 al 2026-11-27.
- **Signal and threshold:** Hay tres condiciones de paso:
  - **Decisiones:** en 8 o más de 10 reuniones, ninguna idea aparece marcada como decisión y falta como máximo 1 decisión de la clave por reunión. Además, el responsable es correcto en el 90% o más de las decisiones.
  - **Contenido compartido:** recupera el 80% o más de las decisiones que en la clave tienen como fuente la pantalla o el tablero.
  - **Restricciones:** tech confirma por escrito que el procesamiento queda dentro del tenant y no afecta el rendimiento de la reunión.
- **Decision rule:**
  - continue si cumple las tres condiciones.
  - change si cumple las de decisiones y restricciones, pero falla con pantalla o tablero. En ese caso pasa a una versión de A1 sin contenido compartido. El resultado de T1 aplica a esa versión solo si en T1 los ítems con fuente pantalla o tablero fueron menos del 20% de los confirmados; si no, se repite T1 con la versión reducida.
  - discard si marca ideas como decisiones en más de la mitad de las reuniones (el mismo hueco que tiene el recap de hoy) o si tech no puede procesar dentro del tenant.
- **Expected provenance:** real
- **Next step if it passes:** repetir el protocolo de T1 con el recap que genera el prompt (5 líderes, 10 reuniones). Si pasa, A1 queda lista para la spec.

## Results

### T1. recap-de-decisiones: recap armado a mano en reuniones reales
- **Observado:** 10 reuniones válidas entre el 2026-11-09 y el 2026-11-20 (R05 no contó porque no se decidió nada y se reemplazó por R11). 6 confirmadas, 2 fallidas (R06, R10) y 2 ni confirmadas ni fallidas (R02, R08). 9 de 10 enviaron el recap como cierre y 8 de 10 no hicieron además su cierre manual. La corrección tuvo una mediana de 3,5 min y fue de 5 min o menos en 7 de 10. Hubo 1 ítem marcado "no era decisión" en 1 reunión (R08) y 2 decisiones agregadas por los líderes (R02, R07).
- **Qué se corrigió:** 23 campos. 13 son del responsable, en 7 de 10 reuniones. Sin R10, las 9 correcciones son el mismo caso: en la reunión se nombró un área o a nadie y el líder puso la persona después ("Eso lo decido yo después, siempre", Javier). Siguen fecha (5), texto (3), porqué (1) y acuerdo (1).
- **Las dos fallidas:** en R06 (comité de riesgos) el líder envió el recap con 1 min de corrección, pero hizo igual el acta formal que exige cumplimiento, copiando del recap, en 10 min en vez de una hora. En R10 (sesión con un cliente) había 3 personas del banco y el recap exponía responsables y prioridades internas; la líder lo reescribió 14 min, no lo envió y escribió dos mensajes aparte.
- **Las dos intermedias:** R02 tuvo 9 min de corrección, casi todo nombres y fechas que no se dijeron en la reunión. R08 tuvo 6 min y 1 ítem tachado: la observadora tomó una votación con stickers como decisión, cuando nadie la había cerrado.
- **Contenido compartido:** 27 de los 54 ítems mantenidos (50%) tienen como fuente la pantalla o el tablero. Las 2 decisiones agregadas estaban fuera de lo que vio la observadora (un mensaje de chat y un frame de FigJam no compartido).
- **Destino del envío:** Slack en 5 (una con página de Confluence), canal de Teams en 3 y correo en 1.
- **Con quién:** 5 líderes entrevistados del segmento, 2 reuniones cada uno, como pedía el diseño. Sesgo conocido: todos trabajan fuera de Teams.
- **Desvíos:** R08 se entregó a los 38 min (el límite era 30). R07 no tuvo transcripción. En R06 las preguntas del día siguiente se respondieron después del recordatorio.
- **Procedencia:** real
- **Resultado:** `passed` (6 confirmadas de 10, con el umbral en 6; con el umbral original de 8 era `failed`)
- **Decisión:** `continue`. No queda lista para spec: sigue a T2 y T3 y, si T3 pasa, se repite este protocolo con el recap que genera el prompt.

### T2. recap-de-decisiones: ¿IT distingue el recap de decisiones del recap de Premium?
- **Resultado:** `not run`. Está agendado para el 2026-12-02. Su condición se cumple, porque T1 no terminó en `discard`.

### T3. recap-de-decisiones: precisión del recap generado contra la clave de T1
- **Resultado:** `not run`. Está agendado del 2026-11-23 al 2026-11-27. Para revisar en el diseño antes de correrlo: R07 no tiene transcripción; la versión final de R10 se adaptó para el cliente y no sirve como clave tal cual; y con 50% de ítems de pantalla o tablero, una versión de A1 sin contenido compartido obligaría a repetir T1.

## Decision
- **A1 (`recap-de-decisiones`): `continue`.** Con el umbral en 6, T1 pasa: 6 de 10 reuniones confirmadas, 9 de 10 recaps enviados como cierre y 8 de 10 sin cierre manual. A1 sigue tal como se testeó. Quedan como hallazgos para el próximo paso, sin rediseño: 13 de 23 correcciones fueron del responsable (la reunión nombró un área o a nadie y el líder asignó después), y una votación con stickers se tomó como decisión sin que nadie la cerrara (R08).
- **Queda como memoria, sin rediseño todavía:** las reuniones con participantes externos (R10) y las que exigen un acta formal (R06) son los dos casos donde A1 no reemplazó el cierre. Es un caso de cada uno. No se excluyen del segmento después de ver los datos; el próximo test los registra como condición en la planilla.
- **T2 y T3 siguen como están agendados.**
