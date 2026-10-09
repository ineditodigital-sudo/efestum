# Isotipo reducido — favicon, bordado y grabado

## Por qué existe

El isotipo oficial tiene una **costura vertical central de 2,33 % del ancho** de la
marca, donde se tocan los pares superior e inferior. Esa ranura es lo primero que se
cierra al reducir: a 16 px las dos mitades se funden en una mancha y desaparece el
vacío central, que es justo el concepto del símbolo ("cuatro fuerzas convergen en un
punto de precisión"). El mismo problema aparece en bordado, donde la aguja no puede
dejar un hueco de menos de ~1,2 mm, y en grabado mecánico.

## Qué se cambió

**Nada de la geometría.** No se redibujó la marca (SKILL §5.1 lo prohíbe). Los cuatro
cuerpos conservan su `d` original y reciben un `transform="translate(±54,80 0)"`:
las curvas, los radios y los grosores de trazo son idénticos al original. Lo único
que cambia es la separación entre la mitad izquierda y la derecha.

| | Oficial | Reducido |
|---|---|---|
| Costura central | 2,30 % del ancho | **6,00 %** |
| Trazo más fino | 4,80 % del ancho | 4,60 % |
| Relación | 1,924 : 1 | 2,000 : 1 |

La costura es simétrica arriba y abajo (6,00 % en ambas). El trazo pierde 0,2 puntos
porque la marca se ensancha un 3,9 %, no porque se haya adelgazado.

## Cuándo usar cuál

- **Oficial** (`current_logo/svg/isotipo-negro.svg`): de 44 px y de 53 mm para arriba.
- **Reducido** (este folder): por debajo de eso. Favicon, app icon, bordado, grabado,
  sellos, troqueles, cualquier aplicación pequeña o de una sola tinta.

## Tamaño mínimo medido

Calculado sobre la geometría real: el hueco de 6,00 % y el trazo de 4,60 % del ancho
de la marca contra el límite físico de cada técnica.

| Técnica | Límite del proceso | Mínimo con el oficial | **Mínimo con el reducido** |
|---|---|---|---|
| Pantalla | hueco ≥ 1 px | 44 px de ancho | **17 px de ancho** |
| Bordado plano | hueco ≥ 1,2 mm · trazo ≥ 1,5 mm | 53 mm | **33 mm** |
| Grabado láser | hueco ≥ 0,3 mm · trazo ≥ 0,4 mm | 13 mm | **9 mm** |
| Grabado mecánico / rotativo | hueco ≥ 0,8 mm | 35 mm | **18 mm** |

En bordado el que manda es el **trazo** (1,5 mm), no el hueco: por debajo de 33 mm de
ancho el satén se deshilacha aunque la costura todavía respire. Si hace falta bordar
más chico que 33 mm, va el isotipo en **una sola masa** sin costura, no este archivo.

## Archivos

```
isotipo-reducido-{negro,blanco,rojo}.svg           lienzo cuadrado, margen óptico 6 %
isotipo-reducido-{negro,blanco,rojo}-ajustado.svg  caja ceñida al dibujo, sin margen
isotipo-reducido-1bit-2048.png                     1 bit puro, para bordado y grabado
favicon/favicon.ico                                16, 32, 48 y 64 px en un archivo
favicon/favicon-{16..512}.png                      tinta, fondo transparente
favicon/favicon-{16..512}-blanco.png               blanco, fondo transparente
favicon/apple-touch-icon-180.png                   fondo blanco sólido (iOS ignora el alfa)
favicon/maskable-512.png                           margen 20 % para la zona segura de Android
favicon/maskable-512-oscuro.png                    la misma, en negativo
```

Las piezas `-ajustado` son para **componer dentro de otra pieza** (hardware de un
dispositivo, sello, marca de agua): no traen margen, así el encuadre lo decide quien
las coloca. Las de lienzo cuadrado ya traen el margen óptico y no se les añade más.

## Color

Un solo color plano, siempre. Tinta `#0A0A0A`, blanco `#FFFFFF`, o rojo `#E60004`
cuando el isotipo **es** el único elemento de la pieza. Nunca degradado, contorno
ni sombra, y nunca el rojo como fondo del disco.
