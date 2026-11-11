---
date: 2026-11-11
source: synthetic
type: persona-critique
document: product/specs/2026-11-11-0847-recap-de-decisiones.md
panel:
  - product/personas/andres-quintero.md (primary)
  - product/personas/lucia-ferreyra.md (primary)
---

# Crítica de personas: Recap de decisiones confirmado por el líder

**Panel:** 2 primary, 0 secondary, 0 tertiary, 0 negative.

**Límite del panel.** Son personas sintéticas: lo que sigue son hipótesis sobre cómo leería la spec cada una, no evidencia. Y el panel es solo de `primary`, pedido así por el PM: da una lectura complaciente sobre compra, permisos y alcance. La spec tiene las tres implicaciones (el paso a Max, la visibilidad del recap, las reuniones con externos) y nadie de este panel puede opinar sobre ellas. Héctor Salinas (tertiary, IT) y Sofía Arrieta (negative, invitada externa) existen en `product/personas/` y no fueron consultados.

---

### Andrés Quintero — Engineering Team Lead, equipo distribuido en 4 países · primary

**Overall rating:** 3,5/5

**Strengths:**
- Que no aparezcan las ideas. Mi problema con el recap de hoy es exactamente ese: dos páginas donde un "podríamos" pesa lo mismo que un "queda así". Si esto de verdad trae solo lo cerrado, ya me ahorra la mitad del trabajo.
- Que lea la pantalla y el tablero. En mi planning la mitad de lo que se decide pasa sobre Jira compartido o sobre el FigJam, sin que nadie lo diga en voz. Un recap que solo escucha no me sirve.
- "Sin responsable" en lugar de inventar uno. Prefiero un hueco visible a un nombre equivocado; el nombre equivocado es el que me costó cuatro días con un cliente.
- Que nadie lo vea hasta que yo confirme. Con un equipo en tres idiomas, un recap malo que se filtra a Varsovia antes de que yo lo lea me genera más trabajo que no tener recap.
- El campo de acuerdo con "objeción" y "no se vio". Es lo más interesante de toda la spec para mí, aunque dudo de que funcione (ver abajo).

**Concerns:**
- El paso 6 es copiar y pegar. Yo documento en Confluence y aviso en Slack: son dos pegados a mano por reunión, y la spec dice expresamente que el producto no publica en ninguno de los dos. Entiendo el porqué, pero para mí "agrega un paso manual" es el motivo por el que abandono herramientas.
- No dice en qué idioma llega. Mis reuniones son en inglés con gente que piensa en español, portugués y polaco, y hoy a veces traduzco el resumen. Si el recap sale en un idioma que tengo que reescribir, los 3,5 minutos no son míos.
- El "acuerdo" se apoya en lo que se dijo o se vio. En mi equipo los que no están de acuerdo se callan y me escriben después por privado. Un "no se vio" al lado de cada ítem no me dice nada, y un "explícito" porque nadie habló es peor: le da apariencia de consenso a un silencio.
- Dice "el líder", pero no dice quién es el líder. En mi planning soy yo. En las reuniones de dependencias de 10 a 15 personas que convoca otro, donde también se decide lo que ejecuta mi equipo, ¿quién recibe el recap? ¿El organizador? ¿Yo no lo veo hasta que esa persona confirme, si es que confirma?
- Todo lo probado fue un recap armado por una persona. La spec lo dice ella misma: no se corrió la prueba con el recap generado, ni la de precisión. Yo no creo en una función de Teams hasta verla con mi equipo real, y acá ni el equipo que la construye la vio funcionar todavía.
- "Dentro de los 30 minutos" está bien para mí, pero mi ventana compartida termina a las 11 y en Varsovia son las 18. Si confirmo a las 11:40, Polonia lo lee al día siguiente. No es culpa de la spec, pero el valor para los que ejecutan llega un día tarde y el supuesto #13 no lo contempla.
- No sé si esto me toca pagarlo o pedirlo. Leo "no da motivo para pasar a Max" en las alternativas y entiendo que esto vive en un plan que yo no decido. Si depende de que IT lo compre, mi opinión vale poco.

**Suggestions:**
- Que el recap confirmado tenga un enlace estable, no solo un copiar con formato: pego el enlace en Slack y en el ADR, y si corrijo algo después se corrige en un solo lugar.
- Definir el idioma del recap (el de la reunión, el mío, o elegible) y decirlo en los criterios de aceptación.
- Dejar que el líder cambie el campo "acuerdo" después de la reunión, o que pueda abrir una ventana corta para que el equipo objete por escrito antes de confirmar. La objeción real en mi equipo llega por escrito y tarde.
- Decir quién es "el líder" cuando el que conduce no es el que convocó, y qué pasa si esa persona nunca confirma.
- No me lo muestren hasta haber corrido la prueba con el recap generado. Con el hecho a mano ya sé que funciona: es lo que yo hago hoy.

Si esto hace lo que dice, me devuelve dos horas por semana y lo usaría. Pero hoy la spec me pide que le crea a una prueba donde el recap lo escribió una persona, y eso es justamente lo que estoy tratando de dejar de hacer yo.

---

### Lucía Ferreyra — Team Lead de Operaciones, logística · primary

**Overall rating:** 4/5

**Strengths:**
- La historia 3 está escrita con mi nombre y es la que más me importa: corregir antes de que mi equipo lo lea. Si alguien ejecuta algo que no se decidió, la que queda mal ante mi gerente soy yo.
- Responsable y fecha en cada ítem. Es lo que busco en cada reunión y lo que hoy reconstruyo de memoria durante 20 o 30 minutos. Que venga armado, aunque tenga huecos, es lo que me ahorra tiempo de verdad.
- Que los "sin responsable" se vean a simple vista. Me sirve incluso como espejo: si salgo de un planning con cuatro ítems sin dueño, la reunión estuvo mal cerrada y lo veo en el momento.
- Si no confirmo, no se manda nada. Me da tranquilidad; no quiero una herramienta que hable por mí.
- Pegarlo en un correo sin perder la tabla. Yo mando el cierre por mail, así que eso me resuelve el último paso tal como trabajo hoy.

**Concerns:**
- No sé si esto es para mí. El segmento dice cuentas "de tecnología" y yo trabajo en logística. Me nombran como persona, pero después el segmento me deja afuera. ¿Lo voy a tener o no?
- En mis reuniones lo que se comparte es un Excel de incidencias y dashboards de entregas, no Jira ni un tablero de diseño. No sé si "lo que se decidió en pantalla" entiende una fila de un Excel que alguien señaló con el cursor. Los ejemplos de la spec son todos de equipos de software.
- Mi tablero es Miro abierto en otra pestaña, con el enlace pegado en el chat. Si entiendo bien, eso no cuenta como "compartido en la reunión" y no aparece. Entonces me falta una parte y tengo que agregarla de memoria, que es lo que hago hoy.
- Seis campos por ítem me parecen muchos para revisar. Decisión, responsable y fecha los entiendo. "Acuerdo: explícito / objeción / no se vio" tuve que leerlo dos veces, y no sé qué hago con un "no se vio": ¿lo dejo, lo cambio, le pregunto a alguien?
- No dice dónde lo encuentro. "Recibe el recap", pero ¿me llega un aviso, está en el chat de la reunión, en una pestaña? Ya hoy pierdo archivos entre el chat, el canal y el OneDrive. Si tengo que ir a buscarlo, un día con seis reuniones no lo abro.
- A veces salgo de una reunión y entro a la siguiente desde el celular. No dice si puedo revisar y confirmar desde el teléfono. Si solo se puede desde la notebook, lo confirmo a las seis de la tarde y ya nadie lo lee ese día.
- Después de mandarlo, el seguimiento sigue siendo mío: paso las tareas a Jira o a Notion a mano. El recap me resuelve el cierre, no el seguimiento. Está bien que lo digan, pero mi trabajo posterior a la reunión no baja a 3 minutos.

**Suggestions:**
- Aclarar si el segmento incluye equipos de operaciones fuera de empresas de tecnología, o sacarme de "Para quién".
- Mostrar por defecto decisión, responsable y fecha, y dejar el porqué, el acuerdo y la fuente como detalle que abro si lo necesito.
- Decir en la spec dónde aparece el recap y cómo me entero de que está listo.
- Que se pueda confirmar desde el celular aunque sea sin editar: un "está bien, mandalo" entre reunión y reunión.
- Que yo pueda decirle de antemano dónde está el tablero de la reunión cuando no lo comparto por Teams.

Esto me ahorra tiempo desde la primera semana si lo encuentro fácil y trae bien los nombres; con eso me alcanza para usarlo. Lo que no quiero es descubrir en la tercera reunión que la mitad de lo decidido quedó en el Miro y el recap no lo vio.

---

## Síntesis del panel

Escrita como investigador, fuera de personaje.

### Acuerdos (señal más fuerte)

- **La confirmación previa del líder es el núcleo del valor.** Ambos la ponen por delante del ahorro de tiempo: el miedo es que el equipo ejecute algo que no se decidió. La historia 3 sostiene a las otras tres.
- **"Sin responsable" visible en lugar de inferido** es bien recibido por los dos, y coincide con la corrección más frecuente de T1 (13 de 23).
- **El último tramo queda manual y la spec no lo cuenta.** Andrés pega dos veces (Slack y Confluence); Lucía pasa después las tareas a Jira o Notion. La mediana de 3,5 minutos mide la corrección, no el trabajo posterior a la reunión que le queda al líder.
- **El campo "acuerdo" no se entiende o no se cree.** Lucía no sabe qué hacer con "no se vio"; Andrés cree que confunde silencio con consenso. Es el campo más débil de los seis.
- **La entrega no está especificada.** Ninguno sabe dónde aparece el recap ni cómo se entera. Es el supuesto #14, sin historia ni criterio que lo cubra.

### Conflictos (tensiones de diseño)

- **Riqueza contra carga de revisión.** Andrés quiere más (enlace estable, idioma, objeciones posteriores); Lucía quiere menos (tres campos visibles, confirmar desde el celular). Los seis campos obligatorios le sirven a la alta alfabetización técnica y le pesan a la media.
- **Qué cuenta como "compartido".** Para Andrés el tablero suele estar en pantalla; para Lucía está en otra pestaña con el enlace en el chat. El caso límite de la historia 2 deja fuera el modo de trabajo de una de las dos personas `primary`.
- **Un recap rápido contra un acuerdo real.** Confirmar en minutos (lo que mide la hipótesis) va contra abrir una ventana para objeciones escritas (lo que pide Andrés para su equipo multilingüe).

### Cambios de mayor impacto

1. **Especificar la entrega y la confirmación en el recorrido:** dónde aparece el recap, cómo se avisa, si se confirma desde el celular y quién es "el líder" cuando conduce alguien distinto del organizador. Hoy el paso 3 dice "recibe" y de eso dependen el supuesto #14 y la hipótesis entera.
2. **Resolver el alcance del segmento y de "lo compartido".** La spec nombra a Lucía como `primary` y la excluye con "cuentas de tecnología"; sus reuniones comparten Excel y dashboards, y su tablero vive en otra pestaña. O el segmento se amplía y la historia 2 cubre esos casos, o Lucía sale de "Para quién".
3. **Simplificar o repensar el campo "acuerdo"** (y decidir el idioma del recap): las dos personas lo cuestionan por motivos distintos, y es el campo con menos respaldo en la evidencia citada.

### Lo que este panel no puede decir

- Nada sobre compra o gobierno: si IT distingue esto del recap de Premium (T2, sin correr) ni si lo permitiría. Corresponde a Héctor Salinas (tertiary).
- Nada sobre el caso de externos (R10) desde el lado del invitado. Corresponde a Sofía Arrieta (negative).
- Nada sobre quien ejecuta lo decidido (supuesto #13). Ramiro Gutiérrez (secondary) es el único participante no líder del set.
- La desconfianza de Andrés hacia el recap generado repite lo que la spec ya declara (T3 y la repetición de T1 sin correr); no es evidencia nueva.
