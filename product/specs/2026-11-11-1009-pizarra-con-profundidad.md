# Pizarra con profundidad

Estado: borrador. Oportunidad: none (declared) · Idea: [pizarra-con-profundidad](../ideas/2026-11-11-1005-pizarra-con-profundidad.md) · Origen: propuesta del sponsor

## Problema
Creemos que, en las reuniones con pizarra, los participantes que no conducen se van a otra ventana mientras la pizarra está en pantalla, y que una pizarra que responde al movimiento de la cabeza los haría seguirla más. Este problema es un supuesto (#16): ni la encuesta ni las 10 entrevistas mencionan la atención durante la pizarra. Lo que sí está medido es otra cosa: Whiteboard se abandona porque le faltan funciones, es lenta y no se encuentra después, y esta spec no toca ninguna de esas causas.

> Evidencia: no hay evidencia real del problema de atención.
> Indicio (persona sintética): "Yo entro, escucho, y si me necesitan me nombran. Lo mío se hace después de la reunión, no durante." — Ramiro Gutiérrez, `product/personas/ramiro-gutierrez.md`
> Contexto real: el 43% de quienes conocen Whiteboard la probó y la dejó; "es lenta con más de 8 personas" — `product/insights/2026-10-28-0945-colaboracion-en-vivo-fuera-de-teams.md`

## Para quién
- **Ramiro Gutiérrez** (secondary, persona del recorrido): participa en reuniones que convocan otros y habla 2 minutos. Es quien vive el efecto. No obtiene un valor propio; la promesa hacia él es que no le cueste nada.
- **Lucía Ferreyra** (primary, beneficiaria): conduce un planning semanal de 10 personas con tablero. Es quien notaría si el equipo la sigue más.
- Ninguno es del sector tecnología del segmento (banco y logística).

## Alcance de esta versión
Un prototipo web fuera de Teams, con una pizarra de ejemplo, probado con un equipo como el de Lucía en tres sesiones seguidas de su reunión habitual, alternando tramos con y sin efecto. Quedan fuera el móvil con giroscopio, la integración con Whiteboard real y el ajuste de intensidad por usuario.

## Recorrido del usuario
Desde el punto de vista de Ramiro. Los pasos 1 y 2 salen de su ficha; los pasos 3 a 6 son la funcionalidad y no tienen evidencia.

1. **Disparador** — Lucía abre la pizarra en el planning y pega el enlace. Ramiro está en su PC de escritorio, con la cámara apagada, como entra siempre.
2. Hoy, cuando aparece un enlace a un tablero, "no sabe si tiene que abrirlo" y la reunión avanza sin él. Mientras otros trabajan en la pizarra, él tiene el Excel del cierre abierto en otra ventana.
3. Abre la pizarra y ve un solo aviso: puede activar el efecto de profundidad, que usa su cámara, o seguir sin él. El aviso dice que la imagen no sale de su equipo.
4. Si acepta y prende la cámara, el fondo de la pizarra se desplaza levemente cuando mueve la cabeza. Las notas quedan en su lugar. Si no acepta, ve la pizarra como siempre y nadie se entera.
5. Si le molesta, lo apaga con un clic y no se le vuelve a ofrecer en esa sesión.
6. **Resultado** — Ramiro mantiene la pizarra en primer plano más tiempo mientras Lucía conduce. El valor llega acá, y es para Lucía: cuando dice "miren esta nota", más gente la está mirando.

## Historias de usuario críticas

### 1. Decidir si uso el efecto, en un paso
Como Ramiro Gutiérrez, quiero que me pregunten una sola vez si quiero el efecto y poder decir que no, para no tener que configurar nada ni prender la cámara si no quiero.

Criterios de aceptación:
- [ ] Al abrir la pizarra aparece un único aviso con dos opciones: activar el efecto o seguir sin él.
- [ ] El efecto está apagado hasta que la persona lo acepta.
- [ ] La pizarra no enciende la cámara por su cuenta: si la cámara está apagada, el aviso lo dice y la persona decide.
- [ ] Quien no acepta ve y usa la pizarra completa, sin funciones de menos.
- [ ] Los demás participantes no ven quién aceptó y quién no.
- [ ] Caso límite: si el equipo no tiene cámara o el navegador niega el permiso, el aviso no vuelve a aparecer y la pizarra funciona sin efecto.

Trazabilidad: supuesto #17. Ficha de Ramiro: entra "con cámara apagada" y "no explora menús ni configura nada que no le hayan mostrado" (persona sintética).

### 2. Que mi cara no salga de mi equipo
Como Ramiro Gutiérrez, quiero que el seguimiento de mi cabeza ocurra solo en mi equipo, para que nadie vea ni guarde mi imagen por usar la pizarra.

Criterios de aceptación:
- [ ] Con el efecto activo, la página no envía imagen ni video a ningún servidor (verificable en el tráfico de red).
- [ ] No se guarda imagen, video ni posición de la cabeza, ni en el equipo ni fuera de él.
- [ ] Lo único que la página registra es si el efecto está activo y cuándo la página pierde o recupera el primer plano.
- [ ] Mientras el efecto usa la cámara, hay un indicador visible en la pizarra.
- [ ] Caso límite: al apagar el efecto o cerrar la pizarra, el uso de la cámara por parte de la página se corta en el momento.

Trazabilidad: supuesto #20. Límite del brief del caso: privacidad y seguridad corporativas.

### 3. Ver profundidad sin que las notas se muevan
Como Lucía Ferreyra, quiero que el efecto mueva solo el fondo, para que cuando señalo una nota todos la vean en el mismo lugar y puedan arrastrarla sin errarle.

Criterios de aceptación:
- [ ] Al mover la cabeza, se desplazan la grilla y las sombras; las notas y el texto no cambian de posición en pantalla.
- [ ] El área donde se hace clic o se arrastra una nota coincide con donde se la ve, con y sin efecto.
- [ ] La posición de cada nota es la misma para todos los participantes, tengan o no el efecto activo.
- [ ] Con la cabeza quieta, el fondo queda quieto.
- [ ] Caso límite: si la cámara deja de detectar la cara, el fondo vuelve al centro de forma gradual y se queda ahí.
- [ ] Caso límite: si hay más de una cara frente a la cámara, sigue a una sola y no salta entre ellas.

Trazabilidad: decisión 5 del brief; supuesto #24. Sin evidencia de uso.

### 4. Apagarlo si me molesta
Como Ramiro Gutiérrez, quiero apagar el efecto con un clic, para que no me maree ni me enlentezca la reunión.

Criterios de aceptación:
- [ ] Hay un control siempre visible en la pizarra para apagar y volver a prender el efecto.
- [ ] Al apagarlo, el fondo queda fijo de inmediato y no se vuelve a ofrecer en esa sesión.
- [ ] Si el sistema operativo tiene activada la opción de reducir movimiento, el efecto no se ofrece.
- [ ] Al apagarlo, la página pregunta el motivo con una sola pregunta opcional (mareo, distracción, lentitud, otro).
- [ ] Caso límite: si el seguimiento hace que la pizarra responda con retraso visible, el efecto se apaga solo y avisa.

Trazabilidad: supuesto #19. Ficha de Ramiro: "la conexión de su casa se corta" (persona sintética). Queja real de lentitud con más de 8 personas en Whiteboard (`product/insights/2026-10-28-0945-colaboracion-en-vivo-fuera-de-teams.md`).

## Hipótesis
Creemos que los participantes que no conducen van a mantener la reunión en primer plano más tiempo durante los tramos de pizarra con efecto que durante los tramos sin efecto, y que la diferencia se va a sostener en la tercera sesión del mismo equipo, porque una pizarra que responde a su movimiento retiene la mirada más que una plana.

Nos equivocamos si pasa cualquiera de estas cuatro cosas:
- en la tercera sesión, los tramos con efecto no superan a los tramos sin efecto en al menos 10 puntos porcentuales de tiempo en primer plano;
- menos de la mitad de los participantes activa el efecto en la primera sesión;
- 2 o más participantes del equipo lo apagan, o alguno reporta que le costó más leer o seguir la pizarra;
- en los tramos sin efecto la reunión ya está en primer plano más del 85% del tiempo, porque entonces no había problema.

Estos umbrales se acuerdan con el sponsor antes de correr el prototipo y no se cambian después de ver los datos.

## Supuestos
Viven en `product/overview.md`, el registro único.
- [feature: pizarra-con-profundidad] [value] #16 — el problema de atención existe. Sin evidencia.
- [feature: pizarra-con-profundidad] [usability] #17 — los participantes aceptan el seguimiento con la cámara encendida. La ficha de Ramiro juega en contra: entra con la cámara apagada.
- [feature: pizarra-con-profundidad] [value] #18 — la atención mejora y se sostiene en la tercera sesión.
- [feature: pizarra-con-profundidad] [usability] #19 — el efecto no molesta.
- [feature: pizarra-con-profundidad] [viability] #20 — IT permite análisis de cara si corre en el dispositivo.
- [feature: pizarra-con-profundidad] [feasibility] #21 — corre dentro de Teams sin afectar el rendimiento. El prototipo no lo contesta.
- [feature: pizarra-con-profundidad] [viability] #22 — suma como razón para pasar a Max.
- [feature: pizarra-con-profundidad] [value] #23 — tener la reunión en primer plano refleja que la persona la está mirando. Toda la medición descansa en esto.
- [feature: pizarra-con-profundidad] [usability] #24 — mover solo el fondo alcanza para que se perciba profundidad.
- [product] [value] #7 — para quienes participan, el problema es la cantidad y duración de las reuniones. Si es cierta, juega en contra.
