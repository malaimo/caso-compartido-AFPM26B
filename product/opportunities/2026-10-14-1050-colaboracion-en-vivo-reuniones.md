---
status: framed
segment: Team Leads y mandos medios de cuentas Business Premium (≥100 licencias, sector tecnología, ≥3 países, facturación >USD 100M) que conducen reuniones de más de 5 personas para producir algo en conjunto
personas: lucia-ferreyra, ramiro-gutierrez, hector-salinas, sofia-arrieta (negativa); pendiente Team Lead de tecnología (primary)
---

# Oportunidad: el trabajo colaborativo se va de las reuniones de Teams

En las cuentas Premium de tecnología con equipos distribuidos, cuando una reunión de más de 5 personas tiene que producir algo en conjunto, el trabajo se va de Teams a Miro, Mural o FigJam (38% de esas reuniones). El traspaso cuesta minutos y deja participantes afuera, y cuando se intenta quedarse en Teams se abandona enseguida. Es el momento de mirarlo porque el upgrade a Max del segmento está en 3,1%, IT no encuentra un problema de reuniones que justifique el plan y CollabCon es en 5 meses.

## Segmento y personas

- **Lucía Ferreyra** (primary) — lo sufre. Abre Miro en su planning y pierde ~10 min en "¿me ven el tablero?"; abandonó Whiteboard. Aproximación: trabaja en logística, fuera del sector del segmento.
- **Ramiro Gutiérrez** (secondary) — lo sufre en parte. Como participante, queda afuera mientras pide acceso al enlace externo.
- **Héctor Salinas** (tertiary) — no lo sufre. Responde a la creencia de viabilidad: decide el upgrade, ve el shadow IT (Miro y Notion pagados por fuera) y no encuentra con qué justificar Max.
- **Sofía Arrieta** (negative) — sufre otro problema: facilitación profesional de workshops de 2 a 4 horas. Marca el límite del alcance.
- **Falta:** Team Lead o mando medio de una empresa de tecnología con equipos en 3 o más países (primary), que se va a generar como una variante de Lucía en el sector → `/generate-personas`.

## Señales

| # | Señal | Procedencia | Fuente |
|---|---|---|---|
| 1 | En el 38% de las reuniones del segmento con más de 5 participantes se comparte un enlace a Miro, Mural o FigJam; mientras dura, cae la actividad en Teams | real | Telemetría del producto (confirmado 2026-10-14) |
| 2 | Whiteboard se abre en el 6% de las reuniones del segmento; la mitad se cierra antes de 2 min | real | Telemetría del producto |
| 3 | El 22% de los comentarios negativos post-reunión menciona la colaboración en vivo ("terminamos en otra herramienta", "la pizarra es difícil de encontrar y nadie la usa") | survey (n sin informar) | Encuestas post-reunión del segmento |
| 4 | 4.700 solicitudes de "colaboración durante reuniones" en 12 meses (3.ª categoría); describen soluciones pedidas, no el problema | real | Portal de feedback |
| 5 | Producto completo: 29% de reuniones de más de 5 personas con enlace externo; 19% de quejas sobre colaboración en la reunión; Whiteboard en 5% | real | Telemetría / `product/overview.md` |
| 6 | En renovaciones de cuentas grandes, "colaboración" aparece en las conversaciones sobre Max; sin conteo | unverified | Ventas (info complementaria) |
| 7 | Experiencias de Lucía, Ramiro y Héctor descritas arriba | synthetic | `product/personas/` |

Las señales 1 a 3 muestran el comportamiento. Ninguna explica por qué el trabajo se va, y la conexión con Max depende solo de la señal 6.

## Resultado de negocio

- **Principal:** tasa de upgrade de Premium a Max en el segmento (hoy 3,1%). Estimación con promedios: ~170 licencias por cuenta, así que +1 punto equivale a ~USD 2M por año, y recuperar USD 5M en el primer año requiere unos +2,5 puntos.
- **Resguardo:** retención en la renovación. No empeorar el motivo "pagamos por funciones que no usamos".

## Restricciones

- Presupuesto máximo: USD 5M.
- Presentación en CollabCon, ~mediados de marzo de 2027.
- Límites para cualquier solución: facilidad de uso, accesibilidad, compatibilidad con Microsoft 365, privacidad y seguridad corporativas, tiempo real, impacto mínimo en el rendimiento de la reunión.
- Fuera del alcance: sesiones de facilitación profesional (persona negativa).

## Creencias

Las creencias viven en `product/overview.md`, el registro único. Este brief solo las referencia.

- [opportunity: colaboracion-en-vivo-reuniones] [viability] — #2 del registro. Versión para el segmento de la creencia de producto sobre por qué las cuentas grandes no suben a Max.
- [opportunity: colaboracion-en-vivo-reuniones] [value] — #1 del registro. Versión para el segmento de la creencia de producto sobre por qué la colaboración se va a herramientas externas.
- Creencias de producto relacionadas: Teams se usa porque viene incluido; la colaboración se va porque Whiteboard y las notas no sirven; IT no ve un problema que justifique Max; el problema real es la cantidad de reuniones, no las funciones.

## Agenda de investigación

| Creencia          | Instrumento (del más barato al más caro)                                                                                                                                                                                                                     | Decisión que habilita                                                                                                                                       | Fecha          |
| ----------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------- |
| value             | **Datos internos:** de las reuniones con enlace externo, en cuántas el tablero existía antes de la reunión y se reusa después (¿herramienta del equipo o improvisada?); n de las encuestas; tiempo desde que se pega el enlace hasta que vuelve la actividad | Si la mayoría de los tableros ya existían, el problema es de acceso o integración y no de capacidad dentro de la reunión: hay que reformular la oportunidad | 2026-10-28     |
| viability         | **Datos internos:** conteo de menciones de "colaboración" por parte de Ventas en renovaciones; cruce de las cuentas que hicieron upgrade a Max con su uso de herramientas externas                                                                           | Decidir si la señal 6 se sostiene o la viabilidad parte de cero                                                                                             | 2026-10-28     |
| value + viability | **Investigación de mercado** (`/research-market`): cómo resuelven esto Zoom, Google Meet y Slack; integraciones de Miro y FigJam; si el mercado paga por colaboración dentro de la reunión                                                                   | Saber si "dentro de la reunión" es algo que se paga o una función que se da por incluida                                                                    | 2026-11-04     |
| value             | **Encuesta** (`/design-survey`) a Team Leads del segmento: frecuencia, costo del traspaso y por qué se usa la herramienta externa; con opt-in para entrevistas                                                                                               | Medir qué tan grande es el problema y reclutar entrevistados                                                                                                | 2026-11-18     |
| value             | **Entrevistas** (`/design-interview`) a Team Leads del segmento, elegidos entre los que respondieron la encuesta, priorizando a quienes contradicen la creencia                                                                                              | Entender qué hacen hoy y por qué                                                                                                                            | 2026-12-02     |
| viability         | **10 conversaciones con compradores de IT** (perfil Héctor)                                                                                                                                                                                                  | Ver si se alcanza el umbral de 3 de cada 10 compradores                                                                                                     | 2026-12-02     |
| —                 | **Decisión de seguir o no con la oportunidad**                                                                                                                                                                                                               | Pasar a `/explore-solutions` o descartar                                                                                                                    | **2026-12-04** |

## Ideas candidatas (sin evaluar)

- Herramientas colaborativas integradas en la reunión (el enunciado original)
- Edición de un documento entre varios durante la llamada (portal de feedback)
- Votación o priorización en vivo (portal de feedback)
- "No salir de Teams para una sesión de trabajo", por ejemplo con Miro, Mural o FigJam dentro de la reunión (portal de feedback)
- Que Whiteboard sea más fácil de encontrar y adoptar (encuestas)

## Oportunidades vecinas (fuera de este brief)

- **Acuerdos que se pierden después de la reunión:** Lucía dedica 20–30 minutos a reconstruirlos y en las encuestas aparece "pierdo tiempo pasando lo que decidimos a un documento".
- **Participantes pasivos en reuniones grandes:** se cruza con la creencia de producto de que el problema real es la cantidad de reuniones.
