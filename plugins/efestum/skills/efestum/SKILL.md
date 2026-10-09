---
name: efestum
description: Sistema de marca EFESTUM completo (antes Maindsoft) — logotipo oficial, tipografía Efestum Display + Rubik, paleta, Mármol Digital, Filo de Forja, voz y copy, dioses griegos, reglas de redes, sitio web y tokens CSS listos. Usar siempre que se cree, diseñe, escriba o revise cualquier cosa para EFESTUM: sitios, apps, landing pages, presentaciones, posts, mockups, documentos, correos, prompts de imagen o código de interfaz. También con "/efestum aplicar" para instalar la marca en el proyecto actual y "/efestum revisar" para auditar una pieza.
argument-hint: "[aplicar | revisar <ruta> | <qué vas a crear>]"
---

# EFESTUM — skill de marca

> Cuando haya duda, EFESTUM debe sentirse como **una firma de ingeniería que sabe
> exactamente lo que está construyendo**.

Esta skill trae todo: reglas, copy, logotipos, tipografía, fondos, referencias y
tokens. Se distribuye desde https://github.com/ineditodigital-sudo/efestum y al
instalar el plugin se descarga completa en:

`${CLAUDE_SKILL_DIR}`

Todas las rutas de abajo son relativas a esa carpeta. Léelas y cópialas desde ahí.
Si algún archivo no estuviera en disco, descárgalo del repositorio (rama `main`):
`https://raw.githubusercontent.com/ineditodigital-sudo/efestum/main/plugins/efestum/skills/efestum/<ruta>`
(codifica los espacios y acentos de la ruta).

Petición del usuario: **$ARGUMENTS**

---

## 1. Qué hacer según el argumento

| Argumento | Acción |
|---|---|
| *(vacío)* | Carga las reglas de §3, lee el proyecto actual y pregunta en una línea qué se va a crear si no es evidente. A partir de ahí, todo lo que se produzca en la sesión sigue la marca. |
| `aplicar` / `instalar` | Ejecuta **§4 Instalar la marca en el proyecto**. |
| `revisar <ruta>` | Ejecuta **§6 Auditoría** sobre esa ruta (archivo, carpeta, URL o imagen). |
| cualquier otra cosa | Es la tarea. Lee lo que indica §2 para ese tipo de tarea y prodúcela con la marca. Si es un proyecto de código y no tiene la marca instalada, haz §4 primero. |

Ejecuta directamente cuando la petición es clara. No pidas confirmación innecesaria.
Idioma por defecto: español de México.

## 2. Qué leer según la tarea

Lee **siempre** §3 (está aquí). Después, solo lo que la tarea necesite:

| Tarea | Leer |
|---|---|
| Cualquier pieza importante o duda de criterio | `reference/SISTEMA_DE_MARCA.md` (fuente de verdad completa, 32 secciones) y `reference/DECISION_LOG.md` (vigente vs. rechazado) |
| Sitio web, landing, app, UI, dashboard | `reference/DESIGN.md`, `reference/WEBSITE.md`, `assets/web/efestum.css` |
| Copy, textos, microcopy, correos | `reference/sources/EFESTUM_BANCO_COPYS_v1.1.md`, `reference/modules/EFESTUM_Sistema_Verbal_Arquetipos_Manual.md` |
| Posts para redes | `reference/CHANNELS.md` + `reference/modules/EFESTUM_Skill_Posts_Automaticos.md` (sin dioses) o `reference/modules/EFESTUM_Skill_Posts_con_Dioses_v2.md` (con dioses) |
| Esculturas / dioses | `reference/modules/EFESTUM_Skill_Esculturas_Dioses.md` y §14–16 de `SISTEMA_DE_MARCA.md` |
| Prompts de generación de imagen | §27–28 de `SISTEMA_DE_MARCA.md` y `reference/prompts/*.txt` |
| Presentaciones, documentos, impresos | `reference/sources/EFESTUM_DESIGN_SYSTEM_v1.md` (retícula 1920×1080) |
| Mármol Digital (por qué y cómo) | `assets/marmol/LEEME.md`, `reference/modules/justificacion_marmol_digital_efestum.md` |
| Favicon, bordado, grabado, tamaños mínimos | `assets/isotipo_reducido/LEEME.md` |
| Contexto de negocio, audiencia, posicionamiento | `reference/PRODUCT.md` |
| Qué NO imitar | `reference/REFERENCIAS_RETIRADAS.md` |
| Datos estructurados del sistema | `reference/brand.json` |

Para ver cómo se ve la marca aplicada, mira las imágenes de `assets/referencias/`
(guía de **composición y estilo**, nunca fuente del logotipo).

**Jerarquía de verdad** si dos reglas chocan: última instrucción del usuario →
archivos de `assets/logos/` (el SVG manda sobre el PNG) → `SISTEMA_DE_MARCA.md` →
`sources/` → `modules/` y `prompts/`.

## 3. Reglas que nunca se rompen

### Marca y logotipo
- La marca es **EFESTUM, a secas**. Nunca "Efestum Systems", ni en logo, títulos,
  metadatos, schema, firma ni copy. Durante la transición (hasta marzo 2028) se
  permite "EFESTUM (antes Maindsoft)" en subtítulos, bios, pie y firma.
- **El logotipo no se dibuja, se coloca.** Siempre desde `assets/logos/svg/`.
  Nunca escribir "EFESTUM" con una fuente para simular el logo. No redibujar,
  deformar, rotar, recolorear, añadir sombras ni efectos.
- Horizontal prioritario: `logo-horizontal-negro.svg` en fondo claro,
  `logo-horizontal-blanco.svg` en fondo oscuro. Cuadrado solo para avatares o donde
  el horizontal no cabe. Rojo solo si el logo es el único elemento y no hay otro rojo.
- Isotipo solo (`isotipo-*.svg`) en avatar, favicon, hardware y sellos; mínimo 44 px.
  Por debajo, `assets/isotipo_reducido/` (favicon ya generado en `favicon/`).
- En mockups o imágenes generadas, **componer el SVG oficial encima**; nunca pedir a
  un modelo generativo que dibuje el logotipo.

### Color
```
Ink     #0A0A0A   texto, logo en claro (nunca #000 puro)
White   #FFFFFF   superficies, tarjetas
Paper   #F4F4F4   fondo de página
Mist    #EAEAEA   rellenos neutros, pills, cabeceras de tabla
Muted   #8A8A8A   metadatos (no para cuerpo sobre paper; ahí #6B6B6B)
Rule    #D8D8D8   hairlines en claro      Panel  #141414  superficie oscura ocasional
Accent  #E60004   único acento            Accent-ink #C40004  rojo para texto pequeño
```
- **El rojo es señal, no relleno**: menos del 5 % del área. Un solo elemento rojo
  dominante por zona: Filo de Forja, una palabra, un dato o el CTA principal.
- Sin gradientes, sin otros rojos, sin colores nuevos. Verde/ámbar solo para estados.

### Tipografía
- **Efestum Display** (`assets/fonts/`): solo titulares grandes y rótulos cortos, en
  caja alta, **nunca por debajo de 24 px**, tracking −0,02 a −0,03 em, máximo dos
  tamaños display por superficie.
- **Rubik** (Google Fonts) para todo lo demás: cuerpo, subtítulos, UI, labels, cifras.
- Labels: Rubik 500, caja alta, tracking +0,14 a +0,22 em. Cuerpo ≥ 16 px, interlineado
  1,45–1,55, medida ≤ 65–75 caracteres.

### Sistema visual
- **Mármol Digital** es el fondo de marca: paper + campo de puntos y retícula técnica
  apenas visibles (clase `.marmol` en `efestum.css`, o el PNG de `assets/marmol/` de
  la **misma proporción**, nunca estirado). Si la retícula se nota a primera vista,
  está mal. No es mármol real: nada de vetas, grecas, columnas, laureles ni dorado.
- **Filo de Forja**: línea roja horizontal, firma visual. 120×4 bajo título, ancho
  completo ×4–5 como separador, 200×6 centrada.
- Fondos claros por defecto. Oscuros solo en textiles, objetos negros o si se piden.
- Radios: 12 px botones/inputs, 16 px tarjetas, 999 px pills. Hairlines de 1 px, sin
  sombras en tarjetas, sin cards anidadas, sin glassmorphism en contenido.
- Iconos estilo Lucide, 24 px, trazo 2, `currentColor`. Nunca emoji.
- Motion preciso: 160–460 ms, `cubic-bezier(.22,1,.36,1)`, solo transform y opacity,
  sin rebote ni elasticidad, respetar `prefers-reduced-motion`.
- Una idea por superficie. El vacío es material. Variar la composición entre piezas.
- Prohibido: cyberpunk, neón, gradientes morados, robots humanoides, cerebros que
  brillan, circuitos decorativos, crosshairs, estética gamer, eyebrows decorativos,
  numeración "01/02/03" de adorno, serif itálica en titulares, fondos crema.

### Voz
- Español de México, sentence case. **Una idea por oración.** Afirmativo, concreto, corto.
- Sin signos de exclamación, sin preguntas retóricas, sin emojis.
- Verbos: forjar, construir, diseñar, integrar, automatizar, escalar, conectar,
  ordenar, medir, operar, decidir, monitorear.
- Nunca: líder, innovador, disruptivo, vanguardia, última generación, revolucionar,
  transformación digital, sinergia, ecosistema, potenciar, impulsar, empoderar,
  "soluciones a la medida de tus necesidades", "estamos emocionados de",
  "¿sabías que…?", "en un mundo cada vez más digital".
- El cliente es el sujeto; EFESTUM es el medio. Botones = verbos
  (`Agendar diagnóstico`, `Ver cómo trabajamos`).
- **Cero datos inventados**: ni clientes, métricas, testimonios, porcentajes ni
  fechas. Si hace falta una cifra, deja un marcador visible `[CIFRA POR VERIFICAR]`.
  No usar logos de clientes. No publicar Talos, Kourai, Brontes ni Pyra como productos.

### Dioses (opcional, con moderación)
Máximo 1 pieza mitológica de cada 4. Solo panteón griego, escultura de mármol blanco
mate, expresión serena y contenida (ni sonrisa ni enojo), **siempre usando un
dispositivo real** con el isotipo. Dios según dominio: Zeus control · Poseidón datos ·
Atenea IA/estrategia · Hermes APIs/velocidad · Hades infraestructura/seguridad ·
Apolo BI/dashboards · Ares automatización · Hefesto construcción de software.

## 4. Instalar la marca en el proyecto (`/efestum aplicar`)

Objetivo: que el proyecto quede con los activos locales y con instrucciones
persistentes, para que cualquier sesión futura siga la marca aunque no se invoque
la skill.

1. **Detecta el tipo de proyecto** (Vite/React, Next, Astro, HTML estático, Tailwind,
   Python, documento, etc.) y su carpeta de estáticos (`public/`, `static/`,
   `assets/`…). Si no hay ninguna, usa `brand/` en la raíz.
2. **Copia** desde la skill a `<estáticos>/brand/` (no sobrescribas sin mirar):
   - `assets/logos/svg/*` → `brand/logos/`
   - `assets/fonts/*.woff2` → `brand/fonts/` (si es web; `.ttf`/`.otf` si es escritorio/impresión)
   - `assets/isotipo_reducido/favicon/*` → `brand/favicon/` y enlázalo en el `<head>`
   - `assets/web/efestum.css` → `brand/efestum.css` (ajusta las `url()` de `@font-face`
     si la ruta pública no es `/brand/fonts/`)
   - `assets/marmol/marmol-16x9.png` y `marmol-9x16.png` solo si se usarán como imagen
     (en web normalmente basta la clase `.marmol`).
3. **Conecta** la hoja: impórtala en el CSS global / layout raíz y carga Rubik
   (`https://fonts.googleapis.com/css2?family=Rubik:wght@300;400;500;600;700;900&display=swap`
   o `@fontsource-variable/rubik` si el proyecto usa npm).
   - **Tailwind v4**: añade en el CSS de entrada un bloque `@theme` con
     `--color-ink`, `--color-paper`, `--color-accent`, etc. y
     `--font-display`/`--font-sans` apuntando a las mismas familias.
   - **Tailwind v3**: extiende `theme.colors`, `fontFamily` y `borderRadius` con los
     valores de §3.
4. **Escribe la memoria del proyecto**: crea o añade al `CLAUDE.md` de la raíz una
   sección `## Marca EFESTUM` con: invocar `/efestum` ante cualquier trabajo visual o
   de copy; las rutas locales de `brand/`; y un resumen de §3 (logo como archivo,
   sin "Systems", rojo < 5 %, Display ≥ 24 px solo titulares, Rubik para lo demás,
   Mármol Digital, Filo de Forja, voz sin exclamaciones, cero cifras inventadas).
   Si ya existe, actualízala en lugar de duplicarla.
5. **Verifica** cargando la página o compilando si es posible, y reporta qué se copió
   y dónde.

## 5. Patrones listos para web

`assets/web/efestum.css` trae tokens y clases: `.marmol`, `.filo`, `.filo--sec`,
`.filo--center`, `.t-hero`, `.t-display`, `.t-h2`, `.t-h3`, `.t-lead`, `.t-body`,
`.t-label`, `.btn--primary`, `.btn--ghost`, `.btn--accent`, `.btn--link`, `.pill`,
`.pill--red`, `.card`, `.rows`, `.container`, `.section`, `.on-dark`, `.rv`.
`assets/web/efestum.tokens.original.css` es la hoja de producción del sitio, como
referencia de implementación.

Estructura de titular aprobada: Efestum Display en caja alta + Filo de Forja de
120×4 debajo + lead en Rubik 300. Un solo botón primario (fondo ink) por vista.
Prefiere filas con hairline (`.rows`) a cuadrículas de tarjetas idénticas
icono+título+texto. Microcopy oficial en `reference/WEBSITE.md`.

## 6. Auditoría (`/efestum revisar`)

Revisa la pieza contra esta lista y reporta cada punto como cumple / no cumple con
la corrección concreta (y aplícala si es código y el usuario lo pidió):

- ¿Logo oficial exacto desde SVG, sin deformar, color correcto para el fondo?
- ¿Sin "Systems" en ningún texto ni metadato?
- ¿Rojo < 5 % del área y con una sola función?
- ¿Display solo en titulares ≥ 24 px; todo lo demás en Rubik?
- ¿Solo colores de la paleta, sin gradientes, sin #000 puro?
- ¿Mármol Digital canónico y apenas visible; Filo de Forja como acento principal?
- ¿Una idea por superficie; composición distinta a la anterior?
- ¿Copy sin exclamaciones, sin palabras prohibidas, una idea por oración?
- ¿Cero cifras, clientes o testimonios inventados?
- Si hay dios: ¿griego, corresponde al dominio, sereno, usando dispositivo real?
- ¿Se puede quitar algo sin perder el mensaje? Si sí, quitarlo.

## 7. Antes de entregar cualquier cosa

Pasa mentalmente la lista de §6. Si el usuario corrige un detalle visual, trátalo
como norma nueva para el resto de la sesión. Si se piden varias piezas, entrégalas
por separado salvo que se pida un tablero.
