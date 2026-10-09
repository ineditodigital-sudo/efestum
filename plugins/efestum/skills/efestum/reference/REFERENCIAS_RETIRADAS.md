# Referencias retiradas — auditoría

Estas piezas estaban en `reference_current/`, que es de donde un agente aprende qué
cara tiene EFESTUM. Cada una contradice una regla vigente, así que enseñaban lo
contrario de lo que debían. **No se borraron**: se apartaron, con el motivo escrito,
por si sirven de historial.

Auditadas las 35 piezas de `reference_current/` el 5 de octubre de 2026.
La presencia del isotipo vigente se verificó por correlación cruzada contra la
plantilla oficial, no a ojo.

---

## `simbolo/` — símbolo anterior o wordmark con otra tipografía (5)

El DECISION_LOG rechaza los "símbolos antiguos enlazados/intertwined como logo
actual". Estas piezas los traen: una forma de lazo con una X dentro de un rectángulo
redondeado, que no es el isotipo de cuatro cuerpos.

- `dioses_del_software_a_medida.png`
- `ficha_técnica_de_muro_branding_compartido.png` — además el logo de INÉDITO tampoco
  es el suyo
- `ficha_técnica_de_muro_corporativo_metálico.png` — aquí el problema es otro y es
  peor: "EFESTUM" está **compuesto con una sans genérica**, no con Efestum Display.
  SKILL §5.1 y la regla de logotipo lo prohíben expresamente
- `ficha_técnica_muro_corporativo_compartido.png` — mismo caso
- `sala_de_juntas_moderna_efestum_inédito.png`

## `systems/` — "SYSTEMS" bajo el lockup (3)

DECISION_LOG, rechazados: *"SYSTEMS añadido automáticamente"*. SKILL §5.1: *"No
agregar SYSTEMS"*. El prompt maestro y el negative prompt lo repiten.

- `forjamos_soluciones_tecnología_en_mármol.png`
- `mareas_de_información_control_total.png`
- `smartphone_minimalista_sobre_pedestal_de_mármol.png`

## `wordmark/` — wordmark roto (1)

- `papelería_ef_estum_de_mármol_y_tecnología.png` — dice **"FESTUM"**, sin la E
  inicial, en la libreta y en el folleto. El copy además está en inglés.

## `ingles/` — copy en inglés (6)

La marca opera en español de México. SKILL §30: *"Idioma por defecto: español"*.
Varias usan además palabras vetadas por §11 ("innovation", "transform").

- `branding_corporativo_efestum_en_mármol.png` — "Technology for a stronger tomorrow"
- `muro_corporativo_moderno_con_estatua_de_artemisa.png` — "OUR AREAS", "OUR VALUES"
- `papelería_efestum_tecnología_divina.png` — "BUILD DIVINE SOFTWARE", "BUILD BEYOND
  MORTAL LIMITS". Rompe también §14: la mitología es capa selectiva, no el discurso
- `plantillas_digitales_efestum_sobre_mármol.png` — "BUILDING DIGITAL POWER"
- `recepción_futurista_de_efestum.png` — "TECHNOLOGY FOR THE MODERN WORLD"
- `stand_efestum_inteligencia_forjada_en_mito.png` — "Intelligence Forged in Myth"

## `_originales_corregidos/` — los ocho posts, antes de arreglarlos (8)

Estos **sí se corrigieron** y la versión buena volvió a `reference_current/`. Aquí
queda el original por si hace falta comparar. Ver la sección siguiente.

---

# Corrección aplicada a los ocho posts

Los ocho `EFESTUM_Post_*` traían el símbolo anterior pero el **wordmark correcto**,
en Efestum Display. Se corrigieron siguiendo lo que manda SKILL §5.1: *"Si la
fidelidad importa, componer el asset oficial encima del mockup; no pedir al modelo
generativo que lo invente."*

Procedimiento, por pieza:

1. Localizar el lockup y medir la **altura de caja del wordmark**.
2. Escalar el SVG oficial (`assets/logos/svg/logo-horizontal-negro.svg` / `-blanco.svg`) para que su wordmark
   mida exactamente esa altura. Las proporciones internas del lockup oficial son
   símbolo 20,17 % del ancho, hueco 3,21 %, wordmark 76,62 %, y símbolo y wordmark
   comparten altura.
3. Borrar el lockup viejo copiando el parche de fondo **más limpio de la misma
   imagen** (buscado por integral de área, no la franja de abajo: ahí vive el rótulo
   rojo y lo arrastraba dentro).
4. Componer el lockup oficial con el borde izquierdo en el margen original.

Resultado: el tamaño óptico del texto no cambia y el margen izquierdo se respeta.
Verificado por correlación contra la plantilla del símbolo antiguo: **de 1,000 a
0,33** en las cuatro piezas de 1080 px. Ninguna conserva rastro del símbolo viejo.

| Pieza | Caja del wordmark | Lockup nuevo |
|---|---|---|
| Post_01_Forjamos_Sistemas_Inteligentes | 30 px | x 70–357, y 65–95 |
| Post_01_Operacion_Tablero | 18 px | x 35–207, y 58–76 |
| Post_02_Cuatro_Sistemas_Una_Verdad | 30 px | x 70–357, y 65–95 |
| Post_02_Sin_Puntos_Ciegos | 18 px | x 38–210, y 60–78 |
| Post_03_Sin_Puntos_Ciegos | 30 px | x 70–357, y 65–95 |
| Post_03_Soluciones_Medida | 18 px | x 35–207, y 61–79 |
| Post_04_Construimos_Lo_Que_No_Existe | 30 px | x 70–357, y 65–95 |
| Post_04_Detras_del_Trabajo | 18 px | x 38–210, y 62–80 (logo blanco, fondo plano) |

**El logo quedó bien, pero tres de estas piezas siguen sin cumplir otras reglas** y
conviene no usarlas como referencia sin revisarlas:

- `Post_01_Operacion_Tablero` — lleva un **crosshair rojo** decorativo, que el
  DECISION_LOG rechaza ("target/crosshair decorativo") y §9 también.
- `Post_02_Sin_Puntos_Ciegos` y `Post_03_Sin_Puntos_Ciegos` — traen cifras en pantalla
  (98,6 %, 1 280, 96 %) que §12 prohíbe si no están verificadas.
- `Post_04_Detras_del_Trabajo` — fondo oscuro con foto de archivo, no Mármol Digital.

---

# Pendientes de revisión humana (5)

La correlación contra la plantilla quedó en zona intermedia (0,50–0,61) porque son
fotos en perspectiva o capturas pequeñas, donde el método pierde precisión. Siguen en
`reference_current/`; conviene que alguien las mire de cerca antes de darlas por buenas.

| Pieza | Correlación |
|---|---|
| `web_and_spaces/lobby_corporativo_moderno_efestum.png` | 0,603 |
| `web_and_spaces/recepción_moderna_con_logo_efestum.png` | 0,578 |
| `web_and_spaces/página_de_inicio_tecnológica_de_efestum.png` | 0,466 |
| `web_and_spaces/página_de_servicios_tecnológicos_efestum.png` | 0,496 |
| `devices_only/integración_de_sistemas_efestum.png` | 0,528 |

Las dos páginas web además muestran cifras sin verificar (+98 %, −70 %, +2,5 M, 100 %,
99,98 %), que §12 prohíbe.
