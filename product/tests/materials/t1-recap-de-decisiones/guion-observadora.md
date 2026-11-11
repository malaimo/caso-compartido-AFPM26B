# T1 · Guion de la observadora

Test concierge: la observadora hace a mano lo que haría el recap. El líder ve solo dos cosas: un documento con el recap y un mensaje. Todo lo demás pasa sin que lo vea. Los mensajes exactos están en `mensajes.md`, la plantilla en `plantilla-recap.md` y lo que se registra en `planilla-captura.md`.

**Regla general:** la observadora no opina sobre el recap, no explica qué cosas son decisiones, no insiste en que lo envíe y no le recuerda nada al líder entre la entrega y las preguntas del día siguiente. Si el líder pregunta algo, responde solo lo que sea operativo ("sí, puedes editarlo ahí mismo").

## Antes (del 2026-11-04 al 2026-11-09)
| Paso | Quién | Qué ve el líder | Detrás de escena | Plazo |
|---|---|---|---|---|
| 0. Reclutamiento | observadora | El mensaje de reclutamiento y consentimiento (M1) | Se registra cada respuesta en la planilla (participantes) | hasta el 2026-11-09 |
| 1. Elegir reuniones | líder | — | El líder elige 2 reuniones propias de más de 5 personas, del 2026-11-09 al 2026-11-20, en las que espera que se decida algo, y manda la invitación | hasta el 2026-11-09 |
| 2. Preparar | observadora | El recordatorio del día anterior (M2) | Prepara el documento editable con historial de versiones (Google Docs, Word Online o Loop, según la herramienta del líder) con la plantilla vacía. Lo comparte con permiso de edición solo para el líder. Le pide que active la transcripción si su herramienta lo permite (para T3) | 1 día antes |

## Durante la reunión
| Paso | Qué ve el líder | Detrás de escena |
|---|---|---|
| 3. Entrar | Una persona más en la lista, con cámara y micrófono apagados | Entra a la hora. No habla ni escribe en el chat. |
| 4. Seguir y anotar | — | Sigue la voz, la pantalla compartida, el tablero y el chat. Anota cada candidato con la hora y la fuente, y aplica la regla de la plantilla en el momento: si no hubo cierre explícito, queda afuera. |
| 5. Capturar para T3 | — | Toma una captura de cada pantalla o tablero en el que se cerró algo, guarda el chat y, al final, guarda la transcripción si existe. Se archiva en la carpeta de la reunión (ver planilla). |

Si no hubo ninguna decisión ni ningún compromiso según la regla, la reunión **no cuenta**: no se entrega recap, se anota en la planilla como "sin decisiones" y el líder elige otra reunión dentro del período.

## Después
| Paso | Qué ve el líder | Detrás de escena | Plazo |
|---|---|---|---|
| 6. Armar el recap | — | Pasa los ítems a la plantilla. Antes de entregar, guarda una copia de la versión entregada (versión 0), que sirve de referencia para la planilla y como clave de partida para T3. | dentro de los 30 min posteriores al cierre |
| 7. Entregar | El enlace al documento y el mensaje de entrega (M3), con el texto exacto | Anota la hora de entrega. Si pasaron más de 30 min, lo anota como desvío. | al terminar el paso 6 |
| 8. Esperar | — | No hace nada. No mira el documento hasta el día siguiente. | hasta el día siguiente |
| 9. Preguntar | Las preguntas del día siguiente (M4) | Las manda por el mismo canal de la entrevista. | el día siguiente hábil, a media mañana |
| 10. Leer el historial | — | Abre el historial de versiones y llena la planilla de la reunión: los minutos de corrección, los ítems marcados ❌, las decisiones agregadas y los campos corregidos. Guarda la versión final. | el mismo día que el paso 9 |
| 11. Clasificar | — | Con la planilla completa, clasifica la reunión como `confirmada`, `fallida` o `ninguna` según la regla de la planilla. | cuando llegan las respuestas de M4 |

Si no hay respuesta a M4 en 2 días hábiles, se manda un único recordatorio. Si sigue sin respuesta, las preguntas quedan como "sin respuesta" y la reunión se clasifica con lo que se pudo ver.

## Cierre del test (2026-11-20)
- Se cuentan las reuniones válidas, las confirmadas y las fallidas en la tabla resumen de la planilla.
- Si quedan menos de 8 reuniones válidas y queda tiempo en el período, se le pide una reunión de reemplazo a un líder que ya participó o a un suplente. Si no, el resultado es `inconclusive`.
- Se pasan las planillas y la carpeta de cada reunión a `/analyze-solution-tests`, y las carpetas a tech para T3.
