# DESIGN.md — EFESTUM visual system

Fuente de verdad: `reference/SISTEMA_DE_MARCA.md` de esta skill. Este archivo resume lo que Impeccable necesita para no inventar un sistema.

## Colors
| Token | Hex | Uso |
|---|---|---|
| ink | #0A0A0A | texto principal, logo en fondo claro, barras |
| ink-700 | #333333 | cuerpo de texto |
| ink-500 | #6B6B6B | texto secundario |
| muted | #8A8A8A | metadatos, etiquetas |
| white | #FFFFFF | superficies, tarjetas |
| paper | #F4F4F4 | fondo de página |
| mist | #EAEAEA | rellenos neutros, cabeceras de tabla, pills |
| accent | #E60004 | único acento: Filo de Forja, una palabra, un dato, CTA principal |
| accent-soft | #FDECEC | fondo de pill roja |
| rule | #D8D8D8 | hairlines en claro |
| rule-dark | #262626 | hairlines en oscuro |
| panel | #141414 | superficie oscura ocasional |

Semánticos solo en contexto de estado: success #1C9D5B (fondo #E6F5EC), warning #D98A09 (fondo #FBF1DF). Danger reutiliza el acento.

Reglas: rojo por debajo del 5 % del área; un solo elemento rojo dominante por zona; nunca #000 puro; sin gradientes; sin múltiples rojos.

## Typography
- **Rubik** (Google Fonts, 300/400/500/600/700/900): todo lo que no es titular grande: subtítulos, cuerpo, UI, labels, cifras. Jerarquía por peso: 700 para títulos de sección, 400 cuerpo, 500 labels.
- **Efestum Display** (`assets/fonts/*.woff2`, 300/400/700): titulares grandes (hero, display, portadas, títulos de diapositiva), afirmaciones y rótulos cortos. Caja alta por diseño. Nunca por debajo de 24 px, nunca en cuerpo, subtítulos, tablas ni UI. Nunca para escribir la palabra EFESTUM: el logotipo es un archivo.
- Escala (base 1920×1080): display 104, h2 58, h3 26, cuerpo 22, pequeño 19, label 15, mínimo funcional 13.
- **Escala del sitio web (`efestum-web`, revisada 7 sep 2026 para bajar el ruido visual).** Valores mínimo → máximo del `clamp`:
  hero 42 → 76 · display 34 → 56 · display largo 30 → 46 · display extralargo 26 → 38 · h2 24 → 32 · h3 19 → 22 · lead 17 → 20 · cuerpo **16 → 17** · label 13.
  El cuerpo **nunca baja de 16 px**: al reducir el máximo es fácil arrastrar el mínimo y dejar la lectura corta en móvil.
  Todos los escalones de Efestum Display quedan por encima del piso de 24 px, incluido el extralargo.
- Ratio entre pasos ≥ 1.25. Interlineado cuerpo 1.45–1.5. Medida de lectura ≤ 65–75 caracteres.
- Labels en caja alta, solo para etiquetas cortas. Tracking: **web e interfaz +0.14 a +0.22 em** (a 13 px, +30 % se desarma); **presentaciones e impresos +30 %** (Design System v1). Cuerpo sin tracking.
- Display tracking −0.02 a −0.03 em en web; −3 % a −5 % en presentaciones según el tamaño (Design System v1).

## Shape and elevation
- Radios: 12 px inputs y botones, 16 px tarjetas, 999 px pills. Nada por encima de 16 px en tarjetas.
- Bordes hairline 1 px (`rule`). Sin sombras en tarjetas. Si una superficie necesita elevación (modal), usar una sola sombra suave, sin borde.
- Sin cards anidadas. Sin borde grueso de acento en un lado de la tarjeta.

## Layout
- Retícula base 1920×1080: margen 100, contenido desde y=150, espaciado en múltiplos de 20.
- **Contenedor del sitio web:** `--container:1680px`, `--gutter:clamp(20px, 4.2vw, 80px)`, `--section:clamp(56px, 6.4vw, 112px)`. Antes eran 1360 y hasta 100 px de gutter, y en una pantalla de 1875 el **37 % del ancho quedaba sin usar**; ahora es 19 %. Medir la medida de lectura con la métrica real de la fuente (`canvas.measureText`), no estimando 0.5em por carácter: esa estimación da falsos positivos de ~25 %.
- **Relleno vertical:** `--section` estaba en `clamp(64px, 9vw, 140px)`, o sea 280 px por sección. En 41 secciones eso era más alto que el contenido mismo (hasta 67 % de la altura). Bajó a 112 px máximo: quedan 19 secciones con aire alto, y son las de contenido genuinamente corto, donde el aire sí corresponde.
- **Medir el centrado con `document.documentElement.clientWidth`, nunca con `innerWidth`:** `innerWidth` incluye la barra de desplazamiento y reporta una asimetría falsa de ~10 px en todos los contenedores.
- Espacio negativo generoso. Agrupar por cercanía; separar secciones con más aire que dentro de ellas.
- Mármol Digital (fondo de marca): base paper, campo de puntos rgba(10,10,10,.07) cada 20 px, retícula rgba(10,10,10,.03) cada 100 px. Es sistema de marca, no decoración; mantenerlo apenas visible.
- Filo de Forja: línea roja 120×4 bajo título, 1720×5 como separador de sección.
- Variar composiciones entre piezas consecutivas. Evitar cuadrículas de tarjetas idénticas icono+título+texto.

## Components
- Botón primario: fondo ink, texto white, radio 12, press = translateY(1px), sin scale-shrink. Un primario por vista. Rojo solo cuando el CTA es el dato más importante de la superficie.
- Pill: mist/ink; variantes red (accent-soft/accent), ok, warn, solid (ink/white). Solo para estado, fechas y responsables.
- Tabla: cabecera en caja alta 13 px sobre mist, filas hairline, primera columna en 700.
- Lista de trabajo: icono de línea 22 px + texto + pill de responsable, separadas por hairline.
- Iconos: estilo Lucide, 24 px, trazo 2, puntas redondas, `currentColor`, en línea con el título. Nunca dentro de un cuadro de color encima del título. Nunca emoji.
- Logo: usar SVG oficiales de `assets/logos/svg/` (PNG en `assets/logos/png/` solo si la herramienta no lee vector). Negro en claro, blanco en oscuro. Horizontal prioritario; isotipo solo en avatar, favicon y hardware.

## Motion
- Curva única: `cubic-bezier(.22,1,.36,1)`.
- **Web:** entradas 300–460 ms, subida 10–14 px + opacidad, escalonado 45–60 ms. Hover 160 ms.
- **Presentaciones y video:** valores del Design System v1 (300–700 ms). En ningún medio menos de 160 ms ni más de 800 ms.
- Hover: Sin rebote, sin elasticidad, sin rotaciones, sin marquesinas, sin puntos pulsantes.
- Solo transform y opacity. Respetar `prefers-reduced-motion` (dejar solo opacidad).
- Hover gateado con `@media (hover:hover) and (pointer:fine)`.

## Do / Don't
- Do: una idea por superficie; la imagen manda y el texto remata; cifras con unidad y comparación.
- Don't: eyebrows decorativos sobre titulares, números diminutos "01/02/03" como adorno, titulares italic serif, fondos crema, gradientes de texto, glassmorphism, carrusel de logos sin permiso, "SYSTEMS" añadido al logo.
- **Alcance de la prohibición de glassmorphism:** aplica a superficies de contenido (tarjetas, paneles, modales), que van opacas y con hairline. **No** aplica a la barra fija: la cabecera usa `backdrop-filter:blur(8px)` sobre `rgba(244,244,244,.92)` para que el texto no se pegue al contenido al desplazar. Es legibilidad, no material esmerilado.
