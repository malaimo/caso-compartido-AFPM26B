---
date: 2026-10-28
source: survey
survey_design: product/surveys/2026-10-21-1944-colaboracion-en-vivo-fuera-de-teams.md
results: product/surveys/2026-10-25-1800-respuestas-colaboracion-en-vivo-fuera-de-teams.csv
n: 210 completas (76 email, 134 panel)
---

# Análisis de encuesta: trabajo colaborativo fuera de Teams en reuniones de más de 5 participantes

## Denominador y límites

- **249 registros:** 210 completas, 34 descalificadas por filtro, 5 parciales (excluidas).
- **Por canal:** email 76 completas (85 entradas), panel 134 completas (164 entradas sobre cuota de 150). Tasa de respuesta del email: no calculable (alcance `unknown` en el diseño).
- **Metas de n:** salen (Q1 ≠ "En ninguna") = **182** (meta ≥150 ✓); no salen = **28** (meta ≥30 ✗ → **direccional**); ≥30 por canal ✓.
- **Sesgos:** el email es canal propio (sobrerrepresenta conformes con Teams); el panel tiene firmografía autodeclarada.
- **Velocidad:** 15 completas en <100 s (mediana ~230 s). Se conservan; excluirlas mueve las cifras clave ≤1 punto.
- **Recuerdo:** Q2–Q9 son sobre la última reunión de memoria; los minutos de Q6 son percibidos, no medidos.

**Corte por canal.** La fricción es casi idéntica entre canales (54% email vs 56% panel con ≥5 min o alguien afuera), lo que la hace robusta. Las diferencias están en:

| | Email | Panel |
|---|---|---|
| Salen en la mitad o más de las reuniones | 46% | 69% |
| La herramienta ya existía | 43% | 59% |
| Lo decidido quedó en chat o notas de Teams | 23% | 7% |
| Lo decidido quedó en un chat fuera de Teams | 18% | 26% |
| Acepta entrevista | 25% | 43% |

Las cinco diferencias van en la dirección del sesgo del canal propio: son rasgos de la muestra antes que del segmento. Para dimensionar el segmento, pesa más el panel.

## O1. Origen del artefacto

**Creíamos:** el tablero se crea para la reunión porque en Teams no se puede hacer ese trabajo.

**Datos (n=182):**
- Q4: ya existía y se siguió usando **51%**; ya existía y no se volvió a usar 3%; se creó y se siguió usando 24%; se creó y no se volvió a usar 15%; no sabe 7%.
- Q2 (opción múltiple): Google Docs/Sheets/Slides 32%, Jira 29%, Miro 20%, dashboards 16%, Confluence 14%, Notion 12%, FigJam 12%, Slido/Mentimeter 9%, Mural 9%, Lucidspark 4%, Otra 5% (Canva, ClickUp, Excel en SharePoint, Retrotool, Trello).
- Dos poblaciones distintas:

| | n | Ya existía | Creada para la reunión | ≥5 min o alguien afuera |
|---|---|---|---|---|
| Usó pizarra (Miro, Mural, FigJam, Lucidspark) | 61 (34%) | 13% | 82% | 75% |
| Solo otras herramientas | 121 (66%) | 74% | 18% | 45% |

- El caso exacto de la creencia (pizarra + creada para la reunión + fricción) es **38 de 210 Team Leads (18%)**.

**Decisión:** la creencia vale para el subconjunto de pizarras (un tercio de quienes salen). Para los otros dos tercios, el problema es de integración con sistemas donde el trabajo ya vive (documentos, Jira, dashboards), no de colaboración en vivo.

## O2. Costo de acceso

**Creíamos:** la mayoría pierde 5 minutos o más, o deja participantes afuera.

**Datos (n=182):**
- Q6: <1 min 19%, 1–2 min 27%, 3–4 min 20%, 5–9 min 21%, ≥10 min 6%, no sabe 7%. **≥5 min: 27%.**
- Q7: ninguno afuera 46%, 1 afuera 27%, 2–3 afuera 18%, 4 o más afuera 5%. **Al menos 1 afuera: 51%.**
- Alguna de las dos: **55%**. El componente fuerte es dejar 1–2 personas afuera, no los minutos.
- Externos (Q8):

| | n | ≥5 min | Alguien afuera | Cualquiera |
|---|---|---|---|---|
| Con externos | 39 | 62% | 64% | 77% |
| Sin externos | 137 | 18% | 46% | 48% |

- Sin externos, las pizarras tardan ≥5 min en el 43% de los casos (21/49); las otras herramientas, en el 5% (5/94).
- Q3: 54% pegó un enlace en el chat, 22% ya la tenía abierta, 15% compartió pantalla y cada uno la abrió, 8% la abrió como app en la reunión. En este último grupo, 13 de 15 dejaron gente afuera (n chico, direccional).
- La telemetría (enlaces en el chat) ve ~54% de los casos: subestima la salida.

**Decisión:** el umbral de 5 minutos no se sostiene en general. Se sostiene para pizarras y para reuniones con externos; esta última fricción es en parte de otro segmento (consultores y agencias).

## O3. Qué se hace afuera y dónde queda la decisión

**Datos:**
- Q5 (n=182): votar o priorizar 40%, editar un documento entre varios 35%, revisar datos o métricas 34%, anotar decisiones 33%, aportar ideas 29%, actualizar tareas 25%, agrupar ideas 22%, diagramar 13%, otro 5% (revisar incidentes, roadmap, presupuesto, planning poker).
  - En pizarras dominan aportar ideas, votar y agrupar.
  - En las otras herramientas dominan revisar datos, editar y actualizar tickets.
- Q9 (n=182): **no quedó registrado 24%**, chat fuera de Teams 23%, Jira 23%, otro 18%, la misma herramienta externa 15%, chat o notas de Teams 13%, acta 12%, correo 10%, no hubo decisiones 7%.
- **Q9 "Otro" = 18% (>15%): la lista está incompleta.** 23 de 32 menciones son resumen automático, Copilot, recap o transcripción, casi siempre con una queja: *"En el recap de Copilot, que resume todo pero no distingue lo decidido"*, *"En el recap pero le faltaba quien hacia que"*, *"En el resumen de IA, que nadie leyó"*. Hay que agregar la opción en la próxima ola.

**Q11, lo más difícil (95 respuestas, codificadas con temas múltiples):**

| Tema | Menciones | Verbatim |
|---|---|---|
| A. Lo decidido no queda registrado ni se cumple (dueño, fecha, el porqué) | 21 | *"Que quede registro del POR QUÉ decidimos algo. El qué queda en Jira, el por qué se pierde"* · *"Tuvimos un release que salio con el alcance viejo porque la decision quedo en un comentario"* |
| B. Sin continuidad entre reuniones: no se encuentra lo anterior | 15 | *"Cada reunion es una isla. Lo que se trabajo en la anterior esta en otro lado"* |
| D. Límites de la pizarra nativa (sin votación ni plantillas, lenta, escondida, se pierde) | 15 | *"Arme una retro en la whiteboard de Teams y a la semana siguiente no la pude encontrar para continuar. Volvimos a Miro"* · *"es lenta con más de 8 personas"* |
| G. Dinámica y participación | 14 | *"Hay 12 personas y opinan 3"* · *"el facilitador soy yo y a la vez tengo que opinar"* |
| I. Ajeno a esta oportunidad (audio, horarios, idioma, demasiadas reuniones, "no aplica") | 14 | *"Demasiadas reuniones, no hay tiempo para trabajar"* |
| C. Converger, priorizar, votar | 12 | *"Divergir es fácil, todos tiran ideas. Ordenarlas y elegir es lo que nos cuesta"* |
| E. Acceso (externos, permisos, SSO, celular, licencias de filiales) | 11 | *"Los permisos del Miro. Siempre hay alguien que no puede editar y pierde los primeros 10 minutos"* |
| K. Mirar todos lo mismo | 3 | *"Cada uno abre el dashboard con su filtro y estamos hablando de numeros distintos"* |
| H. El resumen de IA no distingue lo decidido | 3 | *"marca como decisión cosas que eran solo ideas"* |
| F. Compliance o normativa limitan las externas | 3 (+2 en Q12) | *"compliance no nos deja meter datos de clientes en Miro, asi que o lo hacemos en Teams o no se hace"* |

**Q12, quienes no salen (16 de 28, direccional):** hablan y alguien anota (6), comparten un Excel y escriben lo que les dictan (2), votan con la mano, reacciones o Forms (4), usan la pizarra o las notas de Teams (3, dos de ellas por compliance), deciden en otra reunión más chica o por mail (2).

**Decisión:** el dolor más mencionado está en el cierre, no en el acceso. Registrar lo decidido, que se cumpla y que conecte con la reunión siguiente suma 36 menciones (A + B); el acceso suma 11. Cualquier solución, incluida la IA, debería cubrir **votar/priorizar → registrar la decisión (qué, quién, cuándo, por qué) → retomarla en la próxima reunión**. Hoy los resúmenes de IA ocupan ese lugar y fallan en distinguir lo decidido de lo conversado.

## O4. Conocimiento y uso de lo nativo (n=210)

| Función | No sabía | Sabe, nunca usó | Usó y dejó | Algunas reuniones | Mayoría |
|---|---|---|---|---|---|
| Whiteboard | 8% | 27% | **43%** | 17% | 4% |
| Notas (Loop) | **31%** | 28% | 14% | 20% | 8% |
| Apps de terceros en la reunión | **40%** | 28% | 9% | 18% | 5% |
| IA en la reunión | 12% | **39%** | 13% | 22% | 14% |

**Decisión:** con Whiteboard el problema es "no me sirve": la conocen, la probaron y la dejaron, y Q11 da las razones (falta votar y agrupar, faltan plantillas, rendimiento, no se encuentra después). Con Loop y las apps de terceros el problema es "no sé que existe": hay un problema de descubrimiento barato de atacar. Con la IA el problema es la calidad del resultado, no el conocimiento.

## Insights priorizados

1. **El problema principal es el cierre, no el acceso.** El 24% no registró lo decidido; Q11 suma 36 menciones de cierre y continuidad contra 11 de acceso; y 23 respuestas espontáneas sobre el recap de IA dicen que no distingue lo decidido. *Acción:* replantear la oportunidad hacia "decidir y retomar" y testear antes un recap que separe decisiones con dueño y fecha. *Impacto: alto.*
2. **La creencia de la pizarra cubre solo al 18% de los Team Leads.** En ese grupo es fuerte: 82% creó el tablero para la reunión y 75% tuvo fricción. *Acción:* si se sigue con colaboración en vivo, acotarla a pizarras (votar, agrupar, plantillas, persistencia). *Impacto: alto.*
3. **Los externos multiplican la fricción** (77% vs 48%). *Acción:* separarlo como problema de acceso de invitados, del segmento agencias y consultores. *Impacto: medio.*
4. **Whiteboard se abandona (43%) por funciones y por persistencia.** "No la encuentro la semana siguiente" aparece una y otra vez. *Acción:* la persistencia (link fijo, unido a la serie de reuniones) es una corrección acotada. *Impacto: medio.*
5. **Loop (31%) y las apps de terceros (40%) son desconocidas.** *Acción:* experimento de descubrimiento dentro de la reunión. *Impacto: bajo a medio, costo bajo.*
6. **Compliance y la normativa europea dejan lo nativo como única opción** para algunos (5 menciones, España y datos de clientes). Es una señal débil, pero sería un nicho donde lo nativo no compite con Miro. *Impacto: por dimensionar.*

## Por qué abiertos (para entrevistas)

1. ¿Qué hace que alguien abandone Whiteboard: las funciones, la persistencia o el rendimiento? ¿Cuál pesa más?
2. ¿Por qué el recap de IA no logra separar lo decidido? ¿Qué haría falta para confiar en él sin corregirlo?
3. Quienes trabajan sobre herramientas que ya existían: ¿les falta algo dentro de la reunión, o les basta con compartir pantalla?
4. ¿Cuánto restringe compliance? ¿Es un segmento?
5. Los 28 que no salen: ¿cómo deciden y qué pierden? (n insuficiente).

## Grupo de reclutamiento

77 aceptaron una conversación; 64 pasan R1/R2 (no son de IT y conducen 2 o más reuniones por semana). **Ya entrevistados el 26/10 (10):** R-024 Valeria Castro, R-036 Diego Paredes, R-097 Javier Molina, R-113 Tomás Aguirre, R-143 Lucía Fernández, R-151 Sofía Martínez, R-153 Paula Benítez, R-170 Andrés Quintero, R-196 Ricardo Salinas, R-224 Martina Rojas.

Pendientes, primero los que contradicen la creencia († respondió en <100 s, revisar calidad):

**Herramienta que ya existía y entraron todos en <2 min:**
- R-057† Florencia Medina, México
- R-094 Alejandro Navarro, EE. UU.
- R-102 Nicolás Castillo, Colombia
- R-128 Ignacio Arce, Argentina
- R-131 Sara Molina, España
- R-144 Pilar Ruiz, Chile
- R-176 Emiliano Cabrera, Argentina
- R-180 Agustín Ledesma, Argentina
- R-229 Tatiana Rincón, Colombia
- R-234 Martín Espinoza, Chile
- R-235 Felipe Acosta, Colombia
- R-240 Constanza Lagos, EE. UU.
- R-247† Marcos Silva, México
- R-194 (sin contacto)

**No salen ("En ninguna"):**
- R-009 Jimena Paz, Colombia (compliance)
- R-046 Mateo Gómez, Argentina
- R-085 Isabella Vargas, Colombia
- R-088 Ana Lozano, Argentina
- R-120 Irene Blanco, Colombia
- R-135 Álvaro Cano, Brasil
- R-242 Rocío Figueroa, México
- R-110 (sin contacto)

**Solo herramienta que ya existía:** R-042, R-065, R-086, R-132, R-159, R-171, R-201, R-227, R-228, R-238, R-244.

**Solo acceso rápido:** R-013, R-074, R-089, R-090, R-093, R-173 (normativa europea), R-230.

**Confirman la creencia:** R-006, R-011, R-019, R-031, R-038, R-070, R-076, R-077, R-099, R-101, R-103, R-204, R-205, R-245.

Los contactos están en la columna R4 del CSV de resultados.
