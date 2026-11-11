---
opportunity: none (declared)
slug: pizarra-con-profundidad
origen: propuesta del sponsor
status: por probar
---

# Idea: pizarra con profundidad

Usar la cámara para seguir la cabeza de cada persona y mover el fondo de la pizarra según su posición, para dar sensación de profundidad y sostener la atención de quienes la miran.

## La idea, aclarada

- **Problema (supuesto):** en las reuniones con pizarra, los participantes que no conducen se van a otra ventana mientras la pizarra está en pantalla. No hay ningún dato de esto en `product/`.
- **Para quién:** Ramiro Gutiérrez (`product/personas/ramiro-gutierrez.md`), participante que no conduce, es el objetivo. Lucía Ferreyra (`product/personas/lucia-ferreyra.md`), que conduce plannings con tablero, es la beneficiaria.
- **Valor:** para Lucía, que los participantes mantengan la reunión en primer plano más tiempo durante el tramo de pizarra, sostenido en la tercera sesión y no solo en la primera. Para Ramiro no hay valor propio; la promesa es que no le cueste nada: sin configurar nada, sin obligarlo a prender la cámara, sin marearlo ni enlentecer la reunión.
- **Qué reemplaza:** Lucía hoy sostiene la atención nombrando a la gente o pidiendo que opinen, sin costo.
- **Versión mínima:** un prototipo web fuera de Teams, con una pizarra de ejemplo.
  - Usa la cámara del navegador para seguir la cabeza y mueve solo el fondo (grilla y sombras); las notas quedan fijas.
  - El seguimiento corre en el dispositivo; la imagen no sale ni se guarda.
  - Se activa solo si la persona acepta y ya tiene la cámara encendida. Con la cámara apagada, la pizarra se ve como siempre.
  - Se prueba con un equipo como el de Lucía en tres sesiones seguidas de su reunión habitual con tablero, alternando tramos con y sin efecto.
  - Mide el foco desde la propia página (cuándo pierde el primer plano), porque fuera de Teams no hay telemetría del producto.
- **Fuera de alcance:** móvil con giroscopio, integración con Whiteboard real, ajuste de intensidad por usuario.

## Decisiones tomadas

1. **Sin oportunidad madre.** La más cercana, `colaboracion-en-vivo-reuniones`, está descartada y no se reabre. La otra, `decisiones-que-no-llegan`, es sobre el cierre de la reunión.
2. **"Engagement" significa atención**, no participación ni adopción. Las causas medidas del abandono de Whiteboard (faltan votar, agrupar y plantillas; lentitud; no se encuentra después — `product/insights/2026-10-28-0945-colaboracion-en-vivo-fuera-de-teams.md`) quedan fuera de lo que esta idea toca.
3. **Ramiro es el objetivo y Lucía la beneficiaria.** Ninguno es del sector tecnología del segmento.
4. **El valor se mide en la tercera sesión**, para descontar la novedad.
5. **Solo se mueve el fondo**, para no dificultar apuntar a las notas ni romper la referencia compartida entre participantes.
6. **Prototipo fuera de Teams**, para contestar la pregunta de atención sin pasar antes por la revisión de privacidad y rendimiento.
7. **Los umbrales se acuerdan con el sponsor antes de correr** y no se cambian después de ver los datos.

## Supuestos abiertos

Referencias al registro de `product/overview.md`, en orden de qué tan rápido matan la idea.

1. **#16** [value] El problema existe: los participantes se van a otra ventana durante los tramos de pizarra. Cae si en los tramos sin efecto la reunión ya está en primer plano más del 85% del tiempo.
2. **#17** [usability] Los participantes aceptan el seguimiento con la cámara encendida. Cae si menos de la mitad lo activa en la primera sesión.
3. **#18** [value] La atención mejora y se sostiene. Cae si en la tercera sesión los tramos con efecto no superan a los tramos sin efecto en al menos 10 puntos porcentuales.
4. **#19** [usability] El efecto no molesta. Cae si 2 o más participantes lo apagan, o si alguno reporta que le costó más leer o seguir la pizarra.
5. **#20** [viability] IT permite análisis de cara en reuniones si corre en el dispositivo. Se contesta con una conversación, en paralelo al prototipo.
6. **#21** [feasibility] El seguimiento corre dentro de Teams sin afectar el rendimiento. Para consultar con tech; el prototipo no lo contesta.
7. **#22** [viability] El efecto suma como razón para pasar a Max. No es criterio de corte del prototipo.

Relacionada, ya registrada: **#7** [product] [value] (para quienes participan, el problema es la cantidad y duración de las reuniones, no las funciones). Si es cierta, juega en contra de esta idea.

Los umbrales de #16 a #19 son propuestas sin dato previo que los respalde.
