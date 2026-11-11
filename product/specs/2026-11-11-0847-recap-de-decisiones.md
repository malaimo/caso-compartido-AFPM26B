# Recap de decisiones confirmado por el líder

Estado: borrador. Oportunidad: [decisiones-que-no-llegan](../opportunities/2026-10-28-1041-decisiones-que-no-llegan.md) · Alternativa A1 de [soluciones](../solutions/2026-10-28-1106-decisiones-que-no-llegan.md)

## Problema
Lo que se decide en reuniones de más de 5 personas se pierde, llega distinto o queda sin responsable. El líder lo compensa rehaciendo el cierre a mano después de cada reunión (20 a 60 min; 8 de 10 entrevistados), y aun así falla: los 10 contaron un incidente con costo. El recap de IA ya está en el hábito de 6 de 10, pero mezcla ideas con decisiones, no dice quién se comprometió a qué y no ve lo que pasó en pantalla o en el tablero. Ese recap causó 2 de los incidentes.

> Evidencia: "Alguien dice 'podríamos pasar el release al 20' y en el resumen aparece 'se decidió pasar el release al 20'. [...] Perdimos más o menos una semana de dos desarrolladores." — Paula Benítez, `product/insights/2026-10-28-1022-entrevistas-colaboracion-en-vivo.md`
> Evidencia: "El recap resume todo al mismo nivel. Dos páginas. No distingues qué se decidió de qué se comentó." — Javier Molina, ídem
> Evidencia: "Yo pensé que el arquitecto iba a hacer el ADR y él pensó que yo lo iba a mandar por correo." — Ricardo Salinas, ídem

## Para quién
- **Andrés Quintero** (primary, persona del recorrido): lidera un equipo distribuido en cuatro países y escribe él mismo el resumen de cada reunión, 30 a 40 min. Es la persona sintética, no el entrevistado real del mismo nombre.
- **Lucía Ferreyra** (primary): reconstruye los acuerdos de memoria, 20 a 30 min; "si no lo hace, los compromisos se pierden".
- Segmento: Team Leads y mandos medios de cuentas Business Premium de tecnología (≥100 licencias, ≥3 países) que conducen reuniones de más de 5 personas donde se decide algo que ejecutan otros.

## Recorrido del usuario
Desde el punto de vista de Andrés. Los pasos 1, 2 y 6 son lo que las entrevistas y T1 mostraron; los pasos 3 a 5 son la funcionalidad en el punto de dolor.

1. **Disparador** — Termina una planning de 9 personas en Teams. Se decidieron varias cosas: algunas en voz, otras sobre el tablero o la pantalla de Jira que compartió. Hoy le toca escribir el cierre: 30 a 40 min, y nadie más lo hace (insight 1).
2. Antes abría el recap de IA y lo reescribía o lo abandonaba, porque "resume todo al mismo nivel" (insight 2).
3. Dentro de los 30 min posteriores le llega un aviso por correo, porque es el organizador de la reunión. Hace clic y se abre Teams con el recap de decisiones en primer plano. Solo él lo ve. Llega en el idioma de la conversación, que el modelo detecta sin que Andrés lo configure, indicado en el encabezado. Contiene dos listas, decisiones y compromisos, cada ítem con responsable, fecha, porqué, acuerdo y fuente. El acuerdo dice si el equipo dio una señal a favor, si alguien objetó o si no hubo señal. Lo que fue una idea no aparece.
4. Lo revisa. Donde la reunión nombró un área o a nadie, dice "sin responsable": pone a la persona (en T1 fue la corrección más frecuente, 13 de 23). Si un ítem no era una decisión, lo marca. Si falta una decisión que se cerró fuera de lo compartido, la agrega.
5. Lo confirma, desde la notebook o desde el celular. Recién ahí el recap queda como cierre de la reunión. Si no lo confirma, recibe un recordatorio a las 3 h (o a las 8:00 del día siguiente, si cae después de las 18:00) y otro a las 24 h de terminada la reunión; el recap queda como borrador.
6. **Resultado** — Lo pega donde su equipo lee (en T1: Slack, canal de Teams, Confluence, correo) y no hace su cierre de siempre. El cierre le llevó minutos (mediana de 3,5 en T1) en lugar de 30 a 40. Aquí llega el valor.

## Historias de usuario críticas

### 1. Recibir solo decisiones y compromisos
Como Andrés Quintero, quiero recibir al terminar la reunión una lista que contenga solo lo que se decidió y lo que alguien se comprometió a hacer, para no tener que separar yo lo decidido de lo conversado.

Criterios de aceptación:
- [ ] El recap está disponible para el líder dentro de los 30 min posteriores al fin de la reunión.
- [ ] Cada ítem tiene los seis campos: decisión o compromiso, responsable, fecha, porqué, acuerdo (explícito / objeción / no se vio) y fuente.
- [ ] El recap no contiene resumen de la conversación, temas tratados ni preguntas abiertas.
- [ ] Un dato que no se dijo en la reunión aparece como "sin responsable", "sin fecha" o "no se dijo"; nunca completado por inferencia.
- [ ] El campo acuerdo toma uno de tres valores:
  - `explícito`: hubo un sí, un voto o una reacción a favor, y nadie objetó.
  - `objeción`: alguien objetó; el ítem dice quién y qué en una línea. La decisión se cerró igual, y por eso está en el recap.
  - `no se vio`: no hubo señal a favor ni en contra. El silencio va acá, nunca como `explícito`.
- [ ] El acuerdo registra lo que se vio o se dijo en la reunión. No afirma que el equipo esté de acuerdo: una objeción que llega después por otro canal no figura, y el líder puede cambiar el valor (historia 3).
- [ ] El idioma del recap lo decide el modelo que lo genera, a partir del idioma de la conversación de la reunión. Nadie lo configura antes ni lo elige al recibirlo, y no depende del idioma de la interfaz de Teams ni del perfil del líder.
- [ ] El recap indica en el encabezado el idioma que el modelo eligió.
- [ ] Caso límite: si en la conversación se habló más de un idioma, el modelo elige el que más se usó.
- [ ] El porqué y la objeción conservan las palabras de la reunión; si se dijeron en otro idioma, se traducen al del recap.
- [ ] Caso límite: una propuesta o una votación que nadie dio por cerrada (por ejemplo, stickers en el tablero sin que alguien diga el resultado) no aparece como decisión.
- [ ] Caso límite: si no se cerró ninguna decisión, el recap lo dice y no lista ítems.

Trazabilidad: insight 2 (entrevistas); regla de `product/tests/materials/t1-recap-de-decisiones/plantilla-recap.md` (de ahí salen los tres valores del acuerdo); R05 y R08 de T1. El idioma no tiene evidencia real: viene de la crítica sintética `product/insights/2026-11-11-0911-critique-recap-de-decisiones.md` (Andrés), y T1 no lo observó.

### 2. Incluir lo que se cerró en pantalla, en el tablero o en el chat
Como Andrés Quintero, quiero que el recap incluya lo que se decidió sobre la pantalla compartida, el tablero o el chat de la reunión, para que no falte la mitad de lo decidido.

Criterios de aceptación:
- [ ] Una decisión cerrada sobre contenido compartido en la reunión aparece en el recap aunque nadie la haya repetido en voz.
- [ ] Cada ítem indica su fuente: voz, pantalla, tablero o chat.
- [ ] Caso límite: lo que no se compartió en la reunión (un frame del tablero que nadie mostró, un mensaje en otra herramienta) no aparece; el líder puede agregarlo (historia 3).

Trazabilidad: insight 2 ("no ve lo que pasó fuera de la voz"); T1: 27 de 54 ítems mantenidos tenían como fuente la pantalla o el tablero.

### 3. Corregir y confirmar antes de que nadie lo lea
Como Lucía Ferreyra, quiero corregir el recap y confirmarlo antes de que llegue a mi equipo, para que nadie ejecute algo que no se decidió.

Criterios de aceptación:
- [ ] Hasta que el líder confirma, ningún otro participante puede ver el recap. "El líder" es quien tiene la confirmación: el organizador, o la persona a quien se la cedió (historia 5).
- [ ] El líder puede editar cualquier campo de cualquier ítem.
- [ ] El líder puede cambiar el idioma del recap antes de confirmar; la versión confirmada sale en un solo idioma.
- [ ] Los ítems "sin responsable" o "sin fecha" se distinguen a simple vista, y el líder puede asignar una persona de la reunión.
- [ ] El líder puede marcar un ítem como "no era decisión"; ese ítem no aparece en la versión confirmada.
- [ ] El líder puede agregar una decisión o un compromiso que el recap no traía.
- [ ] Desde el celular, el líder puede abrir el recap, asignar responsable a los ítems "sin responsable" y confirmar. La edición del resto de los campos, marcar "no era decisión" y agregar ítems se hacen desde el escritorio.
- [ ] Caso límite: si el líder no confirma, nada se envía ni se publica de forma automática. El recap queda como borrador y no vence.

Trazabilidad: insight 2 (Javier reescribe, Paula corrige siempre); T1: 23 campos corregidos, 13 del responsable; 1 ítem marcado, 2 decisiones agregadas.

### 4. Enviarlo como cierre donde el equipo lee
Como Andrés Quintero, quiero llevar el recap confirmado al lugar donde mi equipo lee, para que reemplace el cierre que hoy escribo a mano.

Criterios de aceptación:
- [ ] Después de confirmar, el líder puede copiar el recap con formato y pegarlo en un chat, un canal, un documento o un correo sin perder la tabla.
- [ ] La versión confirmada muestra quién la confirmó y cuándo.
- [ ] El producto no publica por sí mismo en Jira, Slack ni Confluence.
- [ ] Caso límite: en una reunión con participantes externos, el recap confirmado no se comparte con ellos de forma automática; el líder decide a quién llega.

Trazabilidad: T1: 9 de 10 lo enviaron como cierre (Slack 5, canal de Teams 3, correo 1); R10 (sesión con cliente). Restricción de la oportunidad: lo decidido convive con Jira, Slack y Confluence.

### 5. Enterarse de que el recap está listo y llegar a él en un clic
Como Lucía Ferreyra, quiero que me avisen cuando el recap está listo y abrirlo sin buscarlo, para confirmarlo el mismo día aunque esté entre reuniones.

Criterios de aceptación:
- [ ] Cuando el recap está disponible, el líder recibe un aviso por correo. Solo el líder lo recibe.
- [ ] El aviso tiene un enlace que abre Teams con el recap en primer plano, sin pasos intermedios: el líder no tiene que buscar la reunión ni el chat.
- [ ] El enlace funciona igual desde el celular: abre la aplicación de Teams con el recap en primer plano.
- [ ] El líder es, por defecto, el organizador de la reunión.
- [ ] El organizador puede ceder la confirmación a otro participante de la reunión. Desde ese momento, esa persona recibe el aviso y los recordatorios, y es la única que ve, corrige y confirma el recap.
- [ ] El líder recibe como máximo tres correos por reunión, todos con el mismo enlace:
  - el aviso, apenas el recap está listo;
  - un primer recordatorio a las 3 h del aviso; si esa hora cae después de las 18:00 del líder, sale a las 8:00 del día siguiente;
  - un segundo recordatorio a las 24 h de terminada la reunión.
- [ ] Los recordatorios saltan el fin de semana: el que caería en sábado o domingo sale el lunes. El primero, a las 8:00; el segundo, a la misma hora en que habría salido. El aviso inicial no se posterga.
- [ ] Los recordatorios salen solo si el líder todavía no confirmó. No hay más recordatorios después del segundo.
- [ ] Los recordatorios se cortan cuando el líder confirma.
- [ ] Caso límite: si no se cerró ninguna decisión (historia 1), el aviso lo dice y no hay recordatorios.
- [ ] Caso límite: si el líder nunca confirma, el recap queda como borrador, sin vencer, y nadie más lo ve.

Trazabilidad: supuesto #14. Sin evidencia real: en T1 una persona entregó el recap con un enlace y un mensaje, en reuniones propias de cada líder, y no se registró el dispositivo. El canal del aviso, el organizador como líder por defecto, la confirmación desde el celular y los dos recordatorios son decisiones del PM (2026-11-11) a partir de la crítica sintética `product/insights/2026-11-11-0911-critique-recap-de-decisiones.md`.

## Hipótesis
Creemos que los Team Leads del segmento que conducen reuniones de más de 5 personas van a confirmar y enviar el recap de decisiones como cierre de la reunión, con 5 min o menos de correcciones y sin hacer además su cierre manual, en al menos 6 de cada 10 reuniones, porque les entrega ya separado lo que hoy separan a mano: qué se decidió, quién lo hace, cuándo y por qué.

Nos equivocamos si en más de la mitad de las reuniones el líder reescribe el recap (más de 10 min de corrección), no lo envía o hace igual su cierre manual.

Una reunión cuenta como confirmada con las cuatro condiciones de T1: lo envía como cierre, lo corrige en 5 min o menos, no marca ningún ítem como "no era decisión" y no hace además su cierre manual.

## Alternativas consideradas
Exploradas en: `product/solutions/2026-10-28-1106-decisiones-que-no-llegan.md`
- A2 `cierre-en-vivo` — parked: depende de registrar durante la reunión, y las notas nativas se usan en el 8% de las reuniones.
- A3 `decision-donde-se-trabaja` — parked: decisión de foco del PM; puede volver como destino del recap confirmado.
- A4 `decisiones-de-la-serie` — parked: solo cubre series recurrentes.
- A5 `ritual-de-cierre` — parked como control: es gratis y no da motivo para pasar a Max.

## Testeado antes de la spec
Testeado en: `product/tests/2026-11-04-0832-decisiones-que-no-llegan.md`
- T1 recap armado a mano en reuniones reales — passed (real, n=10 reuniones, 5 líderes) · creencia #10. El umbral se bajó de 8 a 6 después de ver los datos; con el umbral original era failed (`product/corrections.md`, 2026-11-20). El resultado vale para un recap armado por una persona: la repetición de T1 con el recap generado no se corrió.
- T2 ¿IT distingue el recap de decisiones del de Premium? — not run · creencia #12: not tested (declared)
- T3 precisión del recap generado — not run · creencia #11: not tested (declared)
- El archivo de tests dice que A1 no está lista para spec hasta correr T2, T3 y la repetición de T1. Esta spec se escribe antes, por decisión del PM (declarado).
- Casos de T1 donde el recap no reemplazó el cierre, sin rediseño: reunión con acta formal obligatoria (R06) y reunión con participantes externos (R10).

## Supuestos
Viven en `product/overview.md`, el registro único.
- [opportunity: decisiones-que-no-llegan] [viability] #1 — sin evidencia de compradores.
- [opportunity: decisiones-que-no-llegan] [value] #2 — el umbral de "la mitad en 3 meses" sigue sin medirse.
- [feature: recap-de-decisiones] [value] #10 — confirmada para el recap armado a mano, con el umbral bajado; sin verificar para el recap generado.
- [feature: recap-de-decisiones] [feasibility] #11 — sin verificar (T3 not run).
- [feature: recap-de-decisiones] [viability] #12 — sin verificar (T2 not run).
- [feature: recap-de-decisiones] [value] #13 — Quienes ejecutan leen el recap confirmado donde el líder lo pega y ejecutan lo decidido sin preguntar "¿qué se decidió?". Cae si en más de 3 de cada 10 decisiones igual preguntan o la ejecutan distinto.
- [feature: recap-de-decisiones] [usability] #14 — Sin que una persona se lo entregue con un mensaje, el líder encuentra y abre el recap el mismo día de la reunión. Cae si menos de 6 de cada 10 recaps se abren ese día.
- [feature: recap-de-decisiones] [value] #15 — Las reuniones con acta formal obligatoria o con participantes externos, donde el recap no reemplazó el cierre, son 2 de cada 10 o menos en el segmento. Cae si superan 3 de cada 10.
