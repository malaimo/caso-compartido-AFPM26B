---
date: 2026-10-28
source: real
guide: product/interview-guides/2026-10-21-2030-colaboracion-en-vivo-fuera-de-teams.md
sources:
  - product/interviews/2026-10-26-0900-javier-molina.md (real)
  - product/interviews/2026-10-26-0930-martina-rojas.md (real)
  - product/interviews/2026-10-26-1000-diego-paredes.md (real)
  - product/interviews/2026-10-26-1000-tomas-aguirre.md (real)
  - product/interviews/2026-10-26-1100-andres-quintero.md (real)
  - product/interviews/2026-10-26-1200-sofia-martinez.md (real)
  - product/interviews/2026-10-26-1400-paula-benitez.md (real)
  - product/interviews/2026-10-26-1500-valeria-castro.md (real)
  - product/interviews/2026-10-26-1600-lucia-fernandez.md (real)
  - product/interviews/2026-10-26-1700-ricardo-salinas.md (real)
n: 10 entrevistas (6 panel, 4 email), 10 empresas SaaS de 650 a 2.000 empleados, 8 países
---

# Insights de entrevistas: colaboración en vivo en reuniones de más de 5 personas

**Límites.** Los 10 salieron del grupo de la encuesta que aceptó una conversación, así que todos ya trabajan fuera de Teams en alguna reunión (salvo Lucía, que no puede por compliance). Nadie del grupo "no salen" fue entrevistado. Son líderes que conducen, no participantes. Tomás admitió haber exagerado en la encuesta ("puse que salgo de Teams en todas las reuniones. No es así"): las cifras de frecuencia de la encuesta pueden estar infladas.

## 1. El cierre de la reunión lo hace a mano el líder, y cuando falla cuesta semanas de trabajo (10 de 10)

En las 10 entrevistas, lo decidido se pierde, se malinterpreta o queda sin dueño entre la reunión y la ejecución. 8 de 10 líderes rehacen el cierre a mano después de cada reunión (20 a 60 minutos: correo, Jira, recap reescrito), "nadie más lo hace". Los 10 contaron un incidente concreto con costo: una release movida (Javier), 2 semanas de trabajo deshecho (Sofía), una semana de un diseñador (Valeria), una semana de dos devs (Paula), 3 días de campaña pagada de más (Diego), un cliente 4 días sin atención (Andrés), una incidencia de un banco una semana sin tocar (Lucía), 2 días y un fin de semana de guardia (Ricardo). Las causas se repiten: **no queda claro quién lo hace** (Andrés, Lucía, Ricardo), **la decisión queda donde nadie la lee** (Sofía, en un comentario resuelto; Martina, el porqué en Slack; Javier, en un hilo de Slack que México no leyó), **el cierre llega tarde** (Diego) o **se transcribe mal** (Valeria). *Implicación:* el problema con más impacto no es colaborar durante la reunión, sino cerrarla: decisión + responsable + fecha + porqué, confirmados antes de terminar y publicados donde vive el trabajo (Jira, canal, documento). Coincide con el insight 1 de la encuesta (36 menciones de cierre contra 11 de acceso).

> Evidencia: "Yo pensé que el arquitecto iba a hacer el ADR y él pensó que yo lo iba a mandar por correo." — Ricardo Salinas
> Evidencia: "En mi correo quedó, pero el líder de Ecuador entendió que lo pasaba yo, y yo entendí que lo pasaba él. Nadie lo pasó. [...] El cliente esperó cuatro días." — Andrés Quintero
> Evidencia: "Lo que sí me serviría es algo que cierre la reunión con lo decidido y el por qué, y que eso quede en el ticket. Eso no lo tengo." — Martina Rojas

## 2. El recap de IA ya ocupa ese lugar, pero falla en tres cosas concretas (6 de 10)

Seis lo usan o lo probaron, y los seis describen el mismo hueco: **no separa lo decidido de lo conversado** (Javier, Martina), **marca ideas como decisiones** (Paula), **no dice quién se comprometió a qué** (Lucía) y **no ve lo que pasó fuera de la voz**: los votos en el tablero (Valeria), el filtro o gráfico que se miraba (Diego), lo resuelto en Slack (Martina). Dos de los incidentes del insight 1 los causó el recap: México leyó "se habló de la API de geocercas" y entregó dos semanas tarde; Porto Alegre empezó una integración por una "decisión" que era una idea. Resultado: Javier reescribe el recap (30 min), Paula lo corrige siempre (10 min o más), Martina lo abandonó. *Implicación:* un recap que liste solo decisiones y compromisos con responsable y fecha, que el líder confirme antes de enviarlo y que incorpore el contenido compartido en pantalla o en el tablero de la reunión. Es la vía más corta hacia el insight 1, porque ya está en el hábito de los usuarios.

> Evidencia: "Alguien dice 'podríamos pasar el release al 20' y en el resumen aparece 'se decidió pasar el release al 20'. [...] Perdimos más o menos una semana de dos desarrolladores." — Paula Benítez
> Evidencia: "El recap resume todo al mismo nivel. Dos páginas. No distingues qué se decidió de qué se comentó." — Javier Molina

## 3. Lo nativo se pierde cuando cambia la serie de reuniones, y por eso los equipos eligen Miro (5 de 10)

Las pizarras y notas de Teams quedan atadas al chat de una instancia de reunión. Si la serie se recrea, se reprograma o la siguiente sesión es una invitación nueva, desaparecen: Tomás perdió los acuerdos de una retro y hubo que discutirlos de nuevo; Lucía no encontró la pizarra con el cliente esperando y la incidencia quedó sin dueño; Sofía la reconstruyó desde una captura; Ricardo "supongo que sigue en algún lado"; a Paula le pasa con las notas de Loop al reprogramar. Al revés, la continuidad es la razón explícita por la que Javier y Tomás usan Miro: un tablero por trimestre, con un frame por sesión, que se revisa al empezar la siguiente. De los 6 que probaron Whiteboard, todos la dejaron o la sufren. Además de la persistencia, faltan votación (Javier, Tomás, Lucía; Valeria pregunta si existe), plantillas (Javier, Tomás), agrupar (Lucía, Ricardo) y rendimiento con 9 a 14 personas (Javier, Tomás, Sofía, Ricardo). *Implicación:* antes de sumar funciones, anclar los artefactos nativos al equipo o a la serie (link fijo que sobrevive a reprogramaciones) y mostrar la sesión anterior al abrir la siguiente. Es la condición mínima para competir con Miro en retros y plannings recurrentes.

> Evidencia: "A las dos semanas, para la retro siguiente, fui a buscarla y no estaba. [...] se había recreado la serie de la reunión. [...] Perdí los acuerdos, así de simple." — Tomás Aguirre
> Evidencia: "Esa continuidad es la razón por la que estamos en Miro. Si tuviera que empezar de cero cada vez, perdería el hilo." — Tomás Aguirre

## 4. Cuando el trabajo ya vive en Jira, Excel, Power BI o Figma, el problema no es el acceso sino señalar: todo pasa por el líder (7 de 10)

Martina, Diego, Andrés y Sofía trabajan sobre la herramienta donde ya vive el trabajo, entran rápido con SSO y no quieren otra ("Si hacemos el planning en otro lado después hay que pasarlo a Jira igual"). Lo que cuesta es la referencia compartida. Nadie puede señalar sobre la pantalla compartida: "la fila 43, no, la de abajo" (Andrés), "el pico de abril, no, el otro" (Diego), "la del label rojo" (Tomás en Jira), "el botón de arriba, no, el otro" (Valeria en Figma). Además, cada uno mira una versión distinta (Diego: filtros distintos, 10 a 15 minutos hablando de números diferentes). Como solo el líder toca, el resto le dicta: Martina, Andrés, Tomás, Lucía y Javier lo describen. El error más caro vino de ahí: Andrés cerró el ticket de la fila de al lado y al cliente le llegó el cierre. *Implicación:* para los dos tercios de la encuesta que usan herramientas que ya existían, la oportunidad no es traer el trabajo a Teams, sino un puntero o marcado de los participantes sobre la pantalla compartida y una forma de que todos vean la misma vista. Es acotado, no compite con Jira y reduce errores de quien conduce.

> Evidencia: "Ellos ven mi pantalla. No pueden marcar nada, no pueden señalar. Si pudieran apuntar con algo, me dirían 'esta' y listo." — Andrés Quintero
> Evidencia: "Uno decía 'las ventas bajaron ocho por ciento' y otro 'no, a mí me sale que subieron'. Y estábamos hablando de números distintos sin darnos cuenta." — Diego Paredes

## 5. Los que no hablan no votan ni objetan, y la decisión termina en "decidí yo" (8 de 10)

En 8 de 10 hay participantes que casi no intervienen: los nuevos, otra zona horaria u otro idioma, quien no pudo entrar al tablero o quien no tiene permisos. En 6 la decisión trabada la cerró el líder solo ("al final decidí yo": Javier, Martina, Tomás, Andrés, Sofía, Lucía), y en 3 las objeciones aparecieron después, por privado o en un café (Martina, Valeria, Sofía). Valeria se enteró una semana después de una objeción clave de soporte. Votar con la mano o con reacciones no es confiable (Andrés: "a veces se me pasa uno"; Lucía: "no te fías del todo del número"; Ricardo cuenta 9 a 7), y en FigJam hubo doble voto y 10 minutos discutiendo si valía (Valeria). Contrapeso: Paula y Ricardo sostienen que en reuniones de 14 o 16 personas no se debe decidir ("es dar la sensación de que todos participaron"), y deciden en grupos de 3 o 4. *Implicación:* una votación o priorización nativa y breve (con límite de votos, contada sola y con la opción de dejar una objeción por escrito) sirve más para que aparezca el desacuerdo antes de cerrar que para "decidir entre todos". Se conecta con el insight 1: el resultado debería ir al registro de la decisión.

> Evidencia: "Después, como a la semana, me la encuentro en un café de la oficina y me dice que no estaba de acuerdo con sacar la reprogramación de citas por WhatsApp. [...] Una objeción importante, y yo ni me enteré en la reunión." — Valeria Castro
> Evidencia: "No hay forma de que cada uno marque su prioridad sin que se transforme en conversación. Hablamos veinte minutos. Al final decidí yo." — Martina Rojas

## Señales secundarias

- **Acceso:** pesa solo con pizarras y licencias externas (4 de 10: Javier más de 10 min por instancias de Miro por filial; Tomás 5 a 7 min con invitados que no pueden editar; Valeria 6 a 8 min con cuentas personales de Google; Sofía, comercial sin permiso en Confluence). Con SSO sobre herramientas corporativas es "cero fricción" (Martina, Diego). Javier: el costo mayor es saltar entre ventanas durante dos horas, no el acceso inicial.
- **Compliance:** Lucía (pagos, España) no puede usar herramientas externas con datos de clientes, y aprobar una toma meses. Lo nativo es su única opción. Coincide con la señal débil de la encuesta.
- **Descubrimiento:** Andrés no sabía que existen las notas de Loop, Ricardo no sabía que se pueden usar apps dentro de la reunión, Valeria no sabía que existe Whiteboard y Lucía tardó tres intentos en encontrarla.
- **Cantidad de reuniones:** Ricardo (27 h por semana) cree que el problema son las reuniones; Andrés dice que su reunión de 1 h 30 debería durar 40 min, pero "es por todo esto que hablamos" (la fricción dentro de la reunión).

## Recurrencia

| Insight | Javier | Martina | Diego | Tomás | Andrés | Sofía | Paula | Valeria | Lucía | Ricardo |
|---|---|---|---|---|---|---|---|---|---|---|
| 1. Cierre manual o fallido | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ |
| 2. Recap de IA insuficiente | ✓ | ✓ | ✓ | | | | ✓ | ✓ | ✓ | |
| 3. Persistencia de lo nativo | | | | ✓ | | ✓ | ✓ | | ✓ | ✓ |
| 4. Señalar o dictar al líder | ✓ | ✓ | ✓ | ✓ | ✓ | | | ✓ | ✓ | |
| 5. Silenciosos y "decidí yo" | ✓ | ✓ | | ✓ | ✓ | ✓ | | ✓ | ✓ | ✓ |
