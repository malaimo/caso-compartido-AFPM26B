---
status: framed
segment: Team Leads y mandos medios de cuentas Business Premium (≥100 licencias, sector tecnología, ≥3 países, facturación >USD 100M) que conducen reuniones de más de 5 personas donde se decide algo que después ejecutan otros, se use o no una herramienta externa
personas: andres-quintero, lucia-ferreyra, ramiro-gutierrez, hector-salinas, sofia-arrieta (negativa)
---

# Oportunidad: las decisiones de las reuniones no llegan bien a quienes tienen que ejecutarlas

En las cuentas Premium de tecnología con equipos distribuidos, lo que se decide en reuniones de más de 5 personas se pierde, llega distinto o queda sin responsable, y quien ejecuta rehace trabajo, lo hace tarde o no lo hace. El líder lo compensa con un cierre manual de 20 a 60 minutos por reunión, que igual falla. Es el momento de mirarlo porque la encuesta y las entrevistas muestran que el dolor está en el cierre y no en el acceso (lo que llevó a descartar `colaboracion-en-vivo-reuniones`), porque el recap de IA ya ocupa ese lugar en el hábito y falla, y porque CollabCon es a mediados de marzo de 2027.

## Segmento y personas

- **Andrés Quintero** (primary) — lo sufre. Escribe resúmenes de 30 a 40 min en Confluence; el contexto de cada decisión queda partido entre Slack, Teams y Confluence. (No confundir con el entrevistado real Andrés Quintero, de Tándem Software.)
- **Lucía Ferreyra** (primary) — lo sufre. Reconstruye acuerdos de memoria durante 20 a 30 min: "si no lo hace, los compromisos se pierden". Aproximación: trabaja en logística, fuera del sector del segmento.
- **Ramiro Gutiérrez** (secondary) — lo sufre del lado de quien ejecuta. Busca la minuta en el mail o pregunta "¿qué se decidió?". Cubre el rol de quien ejecuta.
- **Héctor Salinas** (tertiary) — no lo sufre. Responde a la creencia de viabilidad: hoy "no puede nombrar un problema de reuniones concreto" que justifique Max.
- **Sofía Arrieta** (negative) — no lo sufre. Marca el límite: la facilitación profesional de workshops queda afuera.
- **Falta:** ninguna. Ramiro cubre a quien ejecuta (decisión del equipo, 2026-10-28).

## Señales

| # | Señal | Procedencia | Fuente |
|---|---|---|---|
| 1 | Los 10 entrevistados contaron un incidente concreto de una decisión mal ejecutada, con costo: 2 semanas de trabajo deshecho, una release movida, una semana de 2 devs, una semana de un diseñador, 3 días de campaña de más, un cliente 4 días sin atención, una incidencia de un banco una semana sin tocar, 2 días y un fin de semana de guardia | real | `product/insights/2026-10-28-1022-entrevistas-colaboracion-en-vivo.md` |
| 2 | 8 de 10 líderes rehacen el cierre a mano después de cada reunión (20 a 60 min); "nadie más lo hace" | real | ídem |
| 3 | Causas que se repiten: no queda claro quién lo hace (3), la decisión queda donde nadie la lee (3), el cierre llega tarde (1), se transcribe mal (1) | real | ídem |
| 4 | El recap de IA falla en 6 de 10: no separa lo decidido de lo conversado, marca ideas como decisiones, no dice quién se comprometió a qué y no ve el tablero ni lo que estaba en pantalla. Causó 2 de los incidentes | real | ídem |
| 5 | Continuidad: Martina reabrió una decisión porque nadie recordaba el porqué (20 min); Tomás y Lucía perdieron el artefacto y, con él, quién tenía qué | real | ídem |
| 6 | El 24% no registró lo decidido en su última reunión | survey (n=182) | `product/insights/2026-10-28-0945-colaboracion-en-vivo-fuera-de-teams.md` |
| 7 | En "lo más difícil" hubo 21 menciones de "lo decidido no queda ni se cumple" y 15 de "sin continuidad entre reuniones", contra 11 de acceso | survey (n=95 respuestas abiertas) | ídem |
| 8 | 23 de 32 respuestas en "Otro" sobre dónde quedó lo decidido mencionan el recap de IA, casi siempre con una queja ("no distingue lo decidido", "le faltaba quién hacía qué") | survey (n=182) | ídem |
| 9 | Quienes no salen de Teams: "hablan y alguien anota" (6 de 16); el problema existe sin herramientas externas | survey (n=16, direccional) | ídem |
| 10 | La IA que resume y toma notas está saturada: todos los grandes la incluyen sin costo | secondary | `product/research/2026-10-14-1133-colaboracion-en-vivo-reuniones.md` |
| 11 | La escalera de precios de Microsoft lleva a Copilot y E7, no a Max; el recap con IA está en Teams Premium | secondary | ídem |
| 12 | Experiencias de Andrés, Lucía, Ramiro y Héctor descritas arriba | synthetic | `product/personas/` |

Las señales 1 a 9 sostienen que el problema existe y tiene costo, aunque la muestra de entrevistas está sesgada (todos salen de Teams) y la encuesta no midió incidentes. Las señales 10 y 11 van contra la viabilidad.

## Resultado de negocio

- **Principal:** tasa de upgrade de Premium a Max en el segmento (hoy 3,1%). Con ~170 licencias por cuenta, +1 punto equivale a ~USD 2M por año; recuperar USD 5M en el primer año requiere unos +2,5 puntos.
- **Resguardo:** retención en la renovación. No empeorar el motivo "pagamos por funciones que no usamos".

## Restricciones

- Presupuesto máximo: USD 5M.
- Presentación en CollabCon, ~mediados de marzo de 2027.
- Límites para cualquier solución: facilidad de uso, accesibilidad, compatibilidad con Microsoft 365, privacidad y seguridad corporativas, tiempo real, impacto mínimo en el rendimiento de la reunión.
- Lo decidido hoy vive también fuera de Teams (Jira, Slack, Confluence, comentarios de documentos): cualquier solución convive con esos sistemas (Martina, Sofía, Javier).
- En algunas cuentas el registro auditable es el correo ("si está en el correo, existe", Lucía, pagos).
- **Criterio del equipo para cualquier solución:** al registrar una decisión tiene que quedar explícito si hubo acuerdo, para que el desacuerdo aparezca antes de cerrar y no después (Valeria, Martina, Sofía). La participación como problema queda fuera de esta oportunidad.
- Fuera del alcance: sesiones de facilitación profesional (persona negativa).

## Creencias

Las creencias viven en `product/overview.md`, el registro único. Este brief solo las referencia.

- [opportunity: decisiones-que-no-llegan] [viability] — #1 del registro. Los compradores de IT pagarían Max si redujera de forma medible el retrabajo por decisiones mal ejecutadas, no por un resumen de IA.
- [opportunity: decisiones-que-no-llegan] [value] — #2 del registro. La mayoría de los Team Leads tuvo en 3 meses al menos una decisión mal ejecutada con retrabajo de al menos 1 día-persona o impacto en un cliente, y la mitiga con un cierre manual de 15 min o más.
- Creencias de producto relacionadas: IT no ve un problema de reuniones que justifique Max (#5); el problema real es la cantidad de reuniones, no las funciones (#7).

## Agenda de investigación

| Creencia  | Instrumento (del más barato al más caro)                                                                                                                                                                                                | Decisión que habilita                                                                  | Fecha          |
| --------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------- |
| value     | **Datos internos:** adopción del recap de IA y de las notas en el segmento; cuántas veces se edita o reenvía el recap; reuniones con tareas asignadas (Loop o Planner)                                                                  | Medir el *workaround* actual y la línea de base                                        | 2026-11-04     |
| viability | **Datos internos:** menciones de Ventas sobre "decisiones", "seguimiento" o "acuerdos" en renovaciones; uso del recap en cuentas Max contra Premium                                                                                     | Saber si hay alguna señal comercial o si la viabilidad parte de cero                   | 2026-11-04     |
| viability | **Investigación de mercado** (`/research-market`): herramientas que cobran por registrar decisiones y hacerles seguimiento más allá del resumen (Fellow, Read.ai, Fathom, Zoom AI Companion, Gemini en Meet); precios y posicionamiento | Saber si el mercado paga por "decisión que llega" o lo da por incluido como el resumen | 2026-11-11     |
| value     | **Encuesta, segunda ola** (`/design-survey`) al segmento: incidentes de decisiones mal ejecutadas en 3 meses, costo y tiempo del cierre manual; agregar la opción "recap de IA" a dónde quedó lo decidido                               | Probar el umbral de "la mitad" y dimensionar el costo                                  | 2026-11-25     |
| value     | **Entrevistas** (`/design-interview`) a quienes ejecutan sin haber estado en la reunión, y al grupo que no sale de Teams                                                                                                                | Entender cómo llega hoy una decisión a quien la ejecuta                                | 2026-12-02     |
| viability | **10 conversaciones con compradores de IT** (perfil Héctor), con el argumento de retrabajo frente a Copilot                                                                                                                             | Ver si se alcanza el umbral de 3 de cada 10                                            | 2026-12-02     |
| —         | **Decisión de seguir o no con la oportunidad**                                                                                                                                                                                          | Pasar a `/explore-solutions` o descartar                                               | **2026-12-11** |

## Ideas candidatas (sin evaluar)

Evaluadas en [product/solutions/2026-10-28-1106-decisiones-que-no-llegan.md](../solutions/2026-10-28-1106-decisiones-que-no-llegan.md).

- Recap que separe decisiones de conversación, con responsable, fecha y porqué, y que el líder confirme antes de enviarlo (entrevistas y encuesta) — `chosen` (A1, `recap-de-decisiones`)
- Registro de decisiones en vivo durante la reunión, visible para todos — `parked` (A2, `cierre-en-vivo`)
- Publicar lo decidido donde vive el trabajo: Jira, Planner, canal, documento (Martina) — `parked` (A3, `decision-donde-se-trabaja`)
- Mostrar las decisiones de la reunión anterior al abrir la siguiente de la serie — `parked` (A4, `decisiones-de-la-serie`)
- Confirmación explícita de acuerdo por participante al cerrar — `parked` (A2, `cierre-en-vivo`)
- Que la IA vea lo que se compartió en pantalla o en el tablero, no solo lo hablado — `chosen` (A1, `recap-de-decisiones`)

## Oportunidades vecinas (fuera de este brief)

- **Participación y desacuerdo:** los callados que objetan después (8 de 10 entrevistas, 14 menciones en la encuesta). Entra aquí solo como criterio.
- **Señalar sobre herramientas que ya existen:** todo se le dicta al líder (7 de 10 entrevistas); la encuesta no lo midió.
- **Colaboración en pizarras:** `colaboracion-en-vivo-reuniones`, descartada; se puede reabrir acotada al 18% que usa pizarras.
- **Invitados externos** y **compliance**: otros segmentos o nichos.
