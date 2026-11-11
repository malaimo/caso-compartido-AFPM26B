# Correcciones

## 2026-10-21

- Primera `/review-evidence`. Sin correcciones a lo propuesto por la IA esta semana.

## 2026-10-28

- **Artefacto:** `product/solutions/2026-10-28-1106-decisiones-que-no-llegan.md`
  **Propuesta de la IA:** testear A1 (`recap-de-decisiones`) y A3 (`decision-donde-se-trabaja`) en paralelo: entre las dos cubren las cuatro causas de falla, A3 mira a quien ejecuta y sostiene mejor el argumento de viabilidad (#1), y sus creencias son independientes.
  **Decisión del PM:** testear solo A1.
  **Motivo:** foco. Un solo test llega antes a CollabCon, y A3 puede sumarse después como destino del recap confirmado.

## 2026-11-20

- **Artefacto:** `product/tests/2026-11-04-0832-decisiones-que-no-llegan.md` (T1) y creencia #10 en `product/overview.md`
  **Propuesta de la IA:** aplicar el umbral escrito antes del test (8 confirmadas de 10). Con 6 confirmadas, T1 salía `failed` y la regla daba `change` para A1: rediseñar el campo responsable y volver a testear con el mismo protocolo.
  **Decisión del PM:** bajar el umbral a 6 de 10 después de ver los resultados. T1 queda `passed` y A1 en `continue`.
  **Motivo:** "con 6 confirmadas estamos Ok".
