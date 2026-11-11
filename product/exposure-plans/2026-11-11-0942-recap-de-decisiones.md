# Plan de exposición: recap de decisiones confirmado por el líder

Spec: [recap-de-decisiones](../specs/2026-11-11-0847-recap-de-decisiones.md) · Mecanismo: rollout progresivo (decisión del PM, 2026-11-11)

## Hipótesis
Creemos que los Team Leads del segmento que conducen reuniones de más de 5 personas van a confirmar y enviar el recap de decisiones como cierre de la reunión, con 5 min o menos de correcciones y sin hacer además su cierre manual, en al menos 6 de cada 10 reuniones, porque les entrega ya separado lo que hoy separan a mano: qué se decidió, quién lo hace, cuándo y por qué.

Nos equivocamos si en más de la mitad de las reuniones el líder reescribe el recap (más de 10 min de corrección), no lo envía o hace igual su cierre manual.

## Secuencia de creencias
1. El líder reconoce en el recap generado lo que se decidió en su reunión, sin ideas presentadas como decisiones.
2. El líder lo corrige en minutos, lo confirma y lo envía en lugar de su cierre manual.
3. El líder que no confirma en el momento lo hace igual cuando se le recuerda, desde el celular o cediendo la confirmación.

Si la 1 falla, la 2 mide cuánto tarda el líder en arreglar un recap en el que no confía. Si la 2 falla, la 3 solo empuja a confirmar algo que no reemplaza el cierre.

## Nivel 1 — El recap llega solo y trae solo decisiones
- **Qué se revela:**
  - El aviso por correo al organizador, con el enlace que abre Teams en el recap.
  - El recap generado con los seis campos, el idioma detectado y lo cerrado en voz, pantalla, tablero y chat (historias 1 y 2).
  - Una sola acción: marcar un ítem como "no era decisión".
  - Todavía oculto: editar campos, agregar ítems, confirmar, copiar con formato, recordatorios, celular y ceder la confirmación.
- **Creencia:** el líder reconoce en el recap generado lo que se decidió en su reunión y no encuentra ideas presentadas como decisiones.
- **Audiencia:** friends and family: un grupo pequeño de líderes identificados que aceptaron ayudar a validar y refinar este nivel, en sus reuniones de más de 5 personas donde se cierra al menos una decisión. Este nivel no cierra el ciclo de valor (no se puede confirmar ni enviar), y por eso no sale al resto.
- **Duración:** 2 semanas.
- **Validación:**
  - **Avanzar si:** en 8 o más de cada 10 recaps abiertos el líder no marca ningún ítem como "no era decisión", y en las conversaciones con el grupo no aparece más de 1 decisión faltante por reunión.
  - **Detener si:** en más de la mitad de los recaps abiertos el líder marca al menos un ítem.
  - **En el medio:** se refina el recap con el grupo y se vuelve a leer antes de abrir el nivel 2.
  - **Condición de lectura:** al menos 20 recaps con decisiones en las 2 semanas, y al menos 6 de cada 10 abiertos el mismo día de la reunión (supuesto #14). Con menos de 20, el resultado es no concluyente. Si la apertura no llega, lo primero que se rediseña es el aviso.

## Nivel 2 — Corregir, confirmar y enviar como cierre
- **Qué se revela:**
  - Para todo el mundo, por primera vez, lo del nivel 1: el aviso y el recap generado.
  - Editar cualquier campo, asignar responsable, agregar ítems y cambiar el idioma, desde el escritorio (historia 3).
  - Confirmar, con quién confirmó y cuándo.
  - Copiar con formato para pegar donde el equipo lee, sin envío automático a externos (historia 4).
  - Todavía oculto: recordatorios, confirmación desde el celular y ceder la confirmación.
- **Creencia:** el líder confirma el recap con 5 min o menos de correcciones y lo envía en lugar de su cierre manual.
- **Audiencia:** todos los organizadores de reuniones de más de 5 personas en las que se cerró al menos una decisión. La lectura se hace sobre Team Leads y mandos medios del segmento (cuentas Business Premium de tecnología, ≥100 licencias, ≥3 países).
- **Duración:** 3 semanas, para tener varias reuniones por líder.
- **Validación:**
  - **Avanzar si:** 6 o más de cada 10 reuniones cumplen las cuatro condiciones de la spec: enviado como cierre, 5 min o menos de corrección, ningún ítem marcado y sin cierre manual.
  - **Detener si:** en más de la mitad de las reuniones el líder corrige más de 10 min, no lo copia después de confirmar o hace igual su cierre manual.
  - **En el medio:** se revisa qué campo concentra las correcciones (en T1 fue el responsable, 13 de 23) y se rediseña ese punto.

## Nivel 3 — Confirmar entre reuniones
- **Qué se revela:**
  - Los dos recordatorios, con las reglas de horario y fin de semana.
  - Asignar responsable y confirmar desde el celular.
  - Ceder la confirmación a otro participante (resto de la historia 5).
- **Creencia:** el líder que no confirma en el momento confirma cuando se le recuerda, sin sentir los correos como ruido.
- **Audiencia:** la misma del nivel 2, leída sobre los líderes con recaps sin confirmar a las 3 h del aviso.
- **Duración:** 2 semanas.
- **Validación:**
  - **Avanzar si:** al menos 3 de cada 10 recaps sin confirmar al primer recordatorio se confirman dentro de las 24 h siguientes a un recordatorio.
  - **Detener si:** menos de 1 de cada 10 se confirma después de un recordatorio, o si baja la apertura del aviso inicial respecto del nivel 2.
  - Estos umbrales no tienen evidencia previa: son una propuesta para que el PM los ajuste.

## Mecanismo de exposición
Rollout progresivo, por decisión del PM (reemplaza la preferencia inicial por incremental): el nivel 1 se enciende solo para friends and family; a las 2 semanas, si pasa, los niveles 1 y 2 se revelan juntos a todo el mundo; el nivel 3 se suma después para todos.

- **Qué exige:** poder encender el nivel 1 para usuarios identificados y no para el resto. Eso es exposición por grupo, no desarrollo incremental puro; cómo se implementa lo decide ingeniería.
- **Qué gana:** el recap generado, cuya precisión no se testeó (T3 no se corrió), no llega a todos hasta que un grupo conocido lo haya visto en sus reuniones reales, y se puede refinar con ellos.
- **Qué cuesta:** friends and family es un grupo dispuesto a ayudar. Su lectura sirve para refinar y para descartar, pero un resultado favorable está sesgado; la primera lectura sin ese sesgo es la del nivel 2.

## Validaciones en paralelo
- **Precisión y restricciones del recap generado (#11):** el nivel 1 da una lectura de precisión en uso real, pero no reemplaza la parte de T3 que confirma que el procesamiento queda dentro del tenant y no afecta el rendimiento de la reunión. Esa confirmación de tech tiene que estar antes de abrir el nivel 2 a todos.
- **Compradores de IT (#12 y #1):** T2 sigue agendado para el 2026-12-02. Ningún nivel dice si esto es razón para pasar a Max.
- **Quienes ejecutan (#13):** desde el nivel 2, conversaciones con miembros de los equipos para saber si ejecutan lo decidido sin preguntar.
- **Reuniones con acta formal o con externos (#15):** desde el nivel 2, registrar qué proporción son. Cae si superan 3 de cada 10.
- **Privacidad y legal:** revisar el procesamiento de lo compartido en pantalla y tablero dentro del tenant, y el caso de participantes externos.

## Preguntas abiertas para el equipo de producto
- ¿Quiénes y cuántos son friends and family, y cuántos son del segmento? Con pocos líderes, llegar a 20 recaps con decisiones en 2 semanas pide unas 2 reuniones por semana de al menos 5 líderes.
- "No hace su cierre manual" no se ve en el producto. ¿Se lee con una pregunta al confirmar o con una muestra de líderes contactados al día siguiente, como en T1?
- El 6 de cada 10 del nivel 2 es el umbral bajado después de T1, que era 8 con un recap armado a mano. ¿Se mantiene para el recap generado?
- La detección de idioma y la confirmación desde el celular no tienen evidencia real. ¿Se registran idioma y dispositivo desde el nivel 1?
