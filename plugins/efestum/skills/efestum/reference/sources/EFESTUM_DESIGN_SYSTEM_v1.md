# EFESTUM — Design System

**v1.0 · Agosto de 2026 · Inédito Digital para Maindsoft**

Especificación de aplicación. Para el *porqué* de la marca, ver `EFESTUM_CONTEXTO_MARCA.md`.

---

## 1. Principios

1. **Ingeniería, no ornamento.** Todo elemento decorativo debe poder justificarse como estructura. Si no ordena, no va.
2. **Contraste extremo, acento único.** Blanco y negro sostienen el sistema. El rojo aparece poco y siempre significa algo: es señal, no relleno.
3. **Una idea por superficie.** Una diapositiva, una pieza, un mensaje.
4. **El vacío es material.** El aire alrededor del contenido comunica control.
5. **Consistencia por construcción.** Las medidas se derivan de la retícula, no se eligen pieza a pieza.

---

## 2. Color

### Tokens

| **TokenHEXRGBRol** |           |               |                                               |
| ------------------ | --------- | ------------- | --------------------------------------------- |
| `--efe-ink`        | `#0A0A0A` | 10, 10, 10    | Fondo oscuro · texto sobre claro              |
| `--efe-white`      | `#FFFFFF` | 255, 255, 255 | Texto sobre oscuro · logotipo en negativo     |
| `--efe-paper`      | `#F4F4F4` | 244, 244, 244 | Fondo claro (base de Mármol Digital)          |
| `--efe-accent`     | `#E60004` | 230, 0, 4     | **Acento único.** Énfasis, numerales, filo    |
| `--efe-muted`      | `#8A8A8A` | 138, 138, 138 | Pies, metadatos, etiquetas, cuerpo secundario |
| `--efe-rule-light` | `#D8D8D8` | 216, 216, 216 | Divisiones sobre claro                        |
| `--efe-rule-dark`  | `#262626` | 38, 38, 38    | Divisiones sobre oscuro · pista de progreso   |
| `--efe-panel`      | `#141414` | 20, 20, 20    | Tarjetas y celdas sobre fondo oscuro          |

> **`#E60004`**** es el rojo oficial.** Sustituye a `#E40800`, usado en versiones anteriores. Cualquier pieza heredada con el rojo antiguo debe migrarse.

### Reglas

- **El rojo no se usa para superficies grandes.** Máximo orientativo: 5 % del área de una pieza. Las excepciones son deliberadas y contadas — un numeral de portadilla, una barra de progreso completa.
- **Nunca rojo sobre rojo, ni rojo sobre gris medio.** Solo sobre `ink`, `white` o `paper`.
- **No se introducen colores nuevos.** No hay secundarios, ni de estado, ni de categoría. Si un gráfico necesita diferenciar series, se usa la escala de grises entre `ink` y `paper`.

### Contraste

| **CombinaciónRatioUso** |          |                                                     |
| ----------------------- | -------- | --------------------------------------------------- |
| `white` sobre `ink`     | 19.0 : 1 | Cualquier tamaño                                    |
| `ink` sobre `paper`     | 17.3 : 1 | Cualquier tamaño                                    |
| `accent` sobre `ink`    | 4.9 : 1  | ✅ texto ≥ 18 px · ⚠️ evitar en cuerpo pequeño       |
| `accent` sobre `white`  | 4.3 : 1  | ⚠️ solo ≥ 24 px o en negrita                        |
| `muted` sobre `ink`     | 6.4 : 1  | Texto secundario ≥ 14 px                            |
| `muted` sobre `paper`   | 2.7 : 1  | ❌ **No apto para texto.** Solo reglas y separadores |

---

## 3. Tipografía

Dos familias, dos funciones. No se mezclan roles.

### Efestum Display — títulos

Tipografía propietaria, trazada sobre el eje del propio logotipo. Tres pesos: Light · Regular · Bold. Caja alta. Versalitas reales (`smcp` / `c2sc`).

**Se usa para:** títulos grandes, afirmaciones, manifiestos, numerales de portadilla, rótulos de gran formato. Todo aquello que se lee de un vistazo.

**No se usa para:** cuerpo de texto, subtítulos, tablas, pies, interfaz. Nunca por debajo de 24 px.

> Para reproducir el logotipo exacto, usar **Regular**. En Light y Bold las seis letras del logotipo están trazadas sobre el mismo eje pero con otro grosor.

### Rubik — todo lo demás

Subtítulos, cuerpo, tablas, etiquetas, pies, interfaz y documentación. Pesos en uso: Light · Regular · Medium · SemiBold · Bold · Black.

### Escala (base 1920 × 1080)

| **RolFamiliaTamañoTrackingInterlínea** |                 |        |           |       |
| -------------------------------------- | --------------- | ------ | --------- | ----- |
| Manifiesto                             | Efestum Display | 200    | −4 %      | 88 %  |
| Numeral de portadilla                  | Efestum Display | 280    | −5 %      | 90 %  |
| Display                                | Efestum Display | 96–140 | −3 %      | 92 %  |
| Afirmación                             | Efestum Display | 88     | −3 %      | 95 %  |
| Título de diapositiva                  | Efestum Display | 64     | −3 %      | 100 % |
| Subtítulo                              | Rubik Bold      | 44     | −2 %      | 125 % |
| Destacado                              | Rubik Medium    | 34     | −2 %      | 120 % |
| Cuerpo                                 | Rubik Regular   | 24–30  | 0         | 150 % |
| Cuerpo menor                           | Rubik Regular   | 18–20  | 0         | 150 % |
| Etiqueta / eyebrow                     | Rubik Medium    | 12     | **+30 %** | 140 % |
| Rail                                   | Rubik Medium    | 11     | **+30 %** | 140 % |

**Reglas**

- Los títulos van en **caja alta o capital inicial**, nunca en versalitas falsas.
- Las etiquetas van **siempre en mayúsculas** con tracking +30 %. Es la firma tipográfica del sistema.
- Tracking negativo **solo** en Efestum Display y en Rubik Black/Bold a partir de 34 px. En cuerpo, tracking 0.
- Una línea de cuerpo no pasa de **90 caracteres**.
- Nunca más de **dos tamaños de display** en la misma superficie.

---

## 4. Retícula y espaciado

### Lienzo 1920 × 1080

| **GuíaValor**       |                  |
| ------------------- | ---------------- |
| Margen lateral      | 100              |
| Rail superior       | y = 52, alto 18  |
| Inicio de contenido | y = 150          |
| Ancho útil          | 1720             |
| Barra de progreso   | y = 1076, alto 4 |

### Escala de espaciado

Múltiplos de 20. `20 · 40 · 60 · 80 · 100 · 140 · 180 · 220`

- Separación entre bloques de contenido: **80–100**
- Separación entre elementos de un mismo bloque: **20–40**
- Canal entre columnas: **40**
- Eyebrow → título: **32**
- Título → cuerpo: **60**

### Columnas de referencia

| **RejillaAncho de columnaCanal** |     |    |
| -------------------------------- | --- | -- |
| 2 columnas                       | 840 | 40 |
| 3 columnas                       | 546 | 41 |
| 4 columnas                       | 400 | 40 |

---

## 5. Superficie — Mármol Digital

Textura propietaria: **fondo blanco + retícula técnica + campos de puntos**. No imita mármol real: sin vetas, sin grietas, sin relieve.

| **RecursoSignificado** |                                         |
| ---------------------- | --------------------------------------- |
| Blanco                 | Materialidad clásica, claridad, espacio |
| Retícula               | Estructura, arquitectura, precisión     |
| Puntos                 | Datos, procesamiento, señal             |
| Vacío                  | Control, sofisticación, jerarquía       |

**Reglas**

- Es un sistema **exclusivamente claro**. Nunca sobre fondo oscuro.
- Es el fondo **por defecto de toda pieza clara**. Las oscuras usan `ink` plano.
- La textura acompaña: nunca compite con el titular ni con el logotipo.
- Se conserva **monocromática**. El rojo entra por encima, no dentro de ella.

**Masters disponibles:** 1:1, 3:4, 16:9. **Pendientes:** 4:5, 9:16, 21:9, A4.

> ⚠️ Los nombres de archivo están cruzados: `MARMOL VERTICAL.png` es 16:9 **horizontal** y `MARMOL RECTANGULAR.png` es 3:4 **vertical**. Verificar por dimensiones, no por nombre.

---

## 6. Logotipo

### Versiones

| **VersiónUso**         |                                          |
| ---------------------- | ---------------------------------------- |
| Horizontal · colores   | Preferente sobre blanco                  |
| Horizontal · blanco    | Sobre `ink` y sobre fotografía oscura    |
| Horizontal · negro     | Sobre `paper` y Mármol Digital           |
| Horizontal · rojo      | Uso restringido, piezas de un solo tinte |
| Cuadrado (4 variantes) | Avatar, perfiles, aplicaciones compactas |

### Reglas

- **Área de respeto:** la altura del símbolo por cada lado.
- **Tamaño mínimo:** 120 px de ancho en digital · 25 mm impreso.
- El símbolo **no se separa del logotipo en indumentaria**.
- **Prohibido:** deformar, rotar, cambiar el color de una sola parte, añadir sombra o contorno, encerrarlo en una forma que no sea la versión cuadrada oficial, colocarlo sobre fondo de contraste insuficiente o sobre la zona ocupada de una fotografía.

**Pendiente:** versión reducida del símbolo, con menos circuitos, para favicon, bordado y grabado.

---

## 7. Elementos del sistema

### Filo de forja

Línea horizontal roja. **Es la firma visual del sistema.**

| **ContextoMedida**                |          |
| --------------------------------- | -------- |
| Bajo el título                    | 120 × 4  |
| Portadilla de sección             | 1720 × 5 |
| Separador tipográfico             | 1720 × 4 |
| Acento centrado (portada, cierre) | 200 × 6  |

Metáfora de ingeniería. **Nunca ornamento mitológico.**

### Rail superior

Presente en toda diapositiva salvo la portada.

- Izquierda: logotipo blanco, 120 × 18, en `x = 100, y = 52`
- Derecha: `SECCIÓN · NN / TT` — Rubik Medium 11, tracking +30 %, `muted`, alineado a la derecha, terminando en `x = 1820`

### Barra de progreso

Al borde inferior, `y = 1076`, alto 4. Pista en `rule-dark`, avance en `accent`, ancho = `1920 × posición / total`.

### Portadilla de sección

Fondo `ink`. Numeral gigante en `accent` (280 px) junto al nombre de sección en blanco (110 px), alineados por la base. Filo de 1720 × 5 debajo, y una línea descriptiva en `muted`.

### Chips

Contenedor de dato breve: alto 88, radio 8, fondo `white` o `panel`, borde 1 px en `rule`, cuadro rojo de 10 × 10 a la izquierda, texto Rubik Medium 19.

### Barras de nivel

Cinco segmentos de 42 × 8, canal 8. Llenos en `accent`, vacíos en `rule`.

---

## 8. Imagen

### Esculturas

Solo **deidades del panteón griego**. La escultura aporta legado; el dispositivo digital introduce el presente; Mármol Digital es el plano que los une.

Tratamiento: pieza de museo trasladada a un entorno contemporáneo. **Nunca disfraz, parodia ni fantasía.**

### Mockups

Registro único: **negro mate, logotipo en blanco, sin adorno.** Luz suave, fondo neutro, sombra contenida. Un objeto por encuadre salvo en las láminas de sistema.

### Fotografía sobre texto

Si hay texto sobre imagen, se usa **degradado**, nunca un velo de borde duro:

- Inferior: de `ink` α 0 a α 0.96, cubriendo el 60 % inferior
- Superior: de `ink` α 0.85 a α 0, cubriendo los 220 px superiores

### Qué evitar

Robots humanoides · cerebros neón · gradientes arcoíris · estética gamer · circuitos literales decorativos · columnas, capiteles, laureles y grecas · dorados · piedra envejecida · retículas cyberpunk.

---

## 9. Movimiento

Especificación de referencia. El tono es **preciso y contenido**: nada rebota, nada gira.

| **ElementoMovimientoDuraciónCurva** |                                             |        |                             |
| ----------------------------------- | ------------------------------------------- | ------ | --------------------------- |
| Transición entre diapositivas       | Disolvencia                                 | 300 ms | `ease-out`                  |
| Transición a portadilla             | Desplazamiento vertical                     | 450 ms | `cubic-bezier(.22,1,.36,1)` |
| Reveal de texto                     | Subida 24 px + opacidad 0→1                 | 400 ms | `cubic-bezier(.22,1,.36,1)` |
| Escalonado entre líneas             | —                                           | 60 ms  | —                           |
| Reveal de logotipo                  | Escala 0.96→1 + opacidad                    | 600 ms | `cubic-bezier(.22,1,.36,1)` |
| Reveal de imagen                    | Escala 1.04→1 + opacidad                    | 700 ms | `ease-out`                  |
| Filo de forja                       | Barrido de ancho 0→100 % desde la izquierda | 500 ms | `ease-out`                  |
| Numeral de portadilla               | Opacidad + subida 40 px                     | 500 ms | `cubic-bezier(.22,1,.36,1)` |
| Barra de progreso                   | Ancho, continuo entre diapositivas          | 300 ms | `linear`                    |

**Reglas**

- Nada dura menos de 200 ms ni más de 800 ms.
- Sin rebote, sin elástico, sin rotación.
- El escalonado va de arriba abajo y de izquierda a derecha, nunca aleatorio.
- Una sola entrada por elemento. No se anima lo que ya está en pantalla.

---

## 10. Tokens en código

```
:root {
```

`  --efe-ink:        #0A0A0A;`

`  --efe-white:      #FFFFFF;`

`  --efe-paper:      #F4F4F4;`

`  --efe-accent:     #E60004;`

`  --efe-muted:      #8A8A8A;`

`  --efe-rule-light: #D8D8D8;`

`  --efe-rule-dark:  #262626;`

`  --efe-panel:      #141414;`

`  --efe-font-display: "Efestum Display", "Rubik", sans-serif;`

`  --efe-font-text:    "Rubik", system-ui, sans-serif;`

`  --efe-space-1:  20px;`

`  --efe-space-2:  40px;`

`  --efe-space-3:  60px;`

`  --efe-space-4:  80px;`

`  --efe-space-5: 100px;`

`  --efe-space-6: 140px;`

`  --efe-track-label: 0.30em;`

`  --efe-track-display: -0.03em;`

`  --efe-ease: cubic-bezier(.22, 1, .36, 1);`

`}`

```
{
```

`  "color": {`

`    "ink": "#0A0A0A", "white": "#FFFFFF", "paper": "#F4F4F4",`

`    "accent": "#E60004", "muted": "#8A8A8A",`

`    "ruleLight": "#D8D8D8", "ruleDark": "#262626", "panel": "#141414"`

`  },`

`  "font": { "display": "Efestum Display", "text": "Rubik" },`

`  "space": [20, 40, 60, 80, 100, 140, 180, 220],`

`  "canvas": { "w": 1920, "h": 1080, "margin": 100, "contentTop": 150 },`

`  "motion": { "ease": "cubic-bezier(.22,1,.36,1)", "fast": 300, "base": 450, "slow": 700 }`

`}`

---

## 11. Lista de comprobación

Antes de dar por buena una pieza:

- sin completar¿El rojo ocupa menos del 5 % y significa algo?
- sin completar¿Los títulos van en Efestum Display y el cuerpo en Rubik?
- sin completar¿Las etiquetas están en mayúsculas con tracking +30 %?
- sin completar¿Los márgenes respetan la retícula y los espacios son múltiplos de 20?
- sin completar¿El fondo claro usa Mármol Digital, y el oscuro `ink` plano?
- sin completar¿Hay filo de forja, y es el único elemento decorativo?
- sin completar¿El logotipo tiene su área de respeto y contraste suficiente?
- sin completar¿Si hay escultura, es del panteón griego y se trata como pieza de museo?
- sin completar¿Se puede quitar algo sin perder el mensaje? Quítalo.