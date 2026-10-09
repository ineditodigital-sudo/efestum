# Mármol Digital — masters

**Mármol Digital no es mármol físico** (SKILL §8). Es un campo técnico monocromático:
fondo papel, retícula de ingeniería muy tenue, campo de puntos modulado y mucho aire.
Nada de vetas, grietas, greca griega, columnas, laureles ni dorado.

## Masters nuevos (generados, no estirados)

| Archivo | Píxeles | Para qué |
|---|---|---|
| `marmol-1x1.png` | 1800 × 1800 | Feed cuadrado, avatar, tarjeta |
| `marmol-4x5.png` | 2160 × 2700 | Retrato de feed (Instagram, LinkedIn) |
| `marmol-9x16.png` | 2160 × 3840 | Stories, reels, pantalla de móvil |
| `marmol-3x4.png` | 2160 × 2880 | Retrato clásico |
| `marmol-16x9.png` | 3840 × 2160 | Presentación, video, hero de web |
| `marmol-21x9.png` | 3780 × 1620 | Banner ancho, espectacular, muro |
| `marmol-A4-vertical.png` | 2480 × 3508 | A4 210 × 297 mm a 300 ppp |
| `marmol-A4-horizontal.png` | 3508 × 2480 | A4 297 × 210 mm a 300 ppp |

Se **generan** a cada proporción en vez de recortar o estirar un master: §24 prohíbe
deformar, y al estirar cambian el paso de la retícula y la densidad de puntos, que es
precisamente lo que da la escala del sistema. El paso va referido al **lado corto**,
así que un A4 y un banner 21:9 tienen la misma densidad aparente.

## Parámetros del sistema

Medidos sobre `MARMOL CUADRADO.png`, el master original:

```
fondo                #F5F5F5
paso de retícula     5,66 % del lado corto   (71 px sobre 1254)
paso de puntos       1,52 % del lado corto   (19 px sobre 1254)
retícula mayor       cada 4 celdas
densidad             radial: centro limpio, esquinas densas
contraste            p1 = 227, p50 = 243, p99 = 247  (todo en ~20 niveles)
```

El contraste es lo que no se puede tocar: **el fondo nunca debe competir con el
contenido**. Si la retícula se nota a primera vista, está mal.

## Masters originales: los nombres están cruzados

Los tres archivos originales siguen aquí porque SKILL §8 los cita por nombre, pero
**dos de los tres nombres no corresponden a su orientación**:

| Archivo | Dice | Es en realidad |
|---|---|---|
| `MARMOL CUADRADO.png` | cuadrado | 1254 × 1254 — correcto |
| `MARMOL RECTANGULAR.png` | rectangular | 1086 × 1448 — **vertical 3:4** |
| `MARMOL VERTICAL.png` | vertical | 1672 × 941 — **horizontal 16:9** |

Para trabajo nuevo, usar los `marmol-*` de arriba, que se llaman por su proporción
real. Los originales se conservan solo para no romper referencias existentes.

## Uso

- El rojo va **superpuesto**, nunca integrado a la textura.
- Sobre fondo oscuro no se usa este campo: ahí va `--panel`.
- Fondo claro es el sistema predeterminado para redes e institucional. El oscuro
  queda para tela negra, objetos mate y mockups físicos.
