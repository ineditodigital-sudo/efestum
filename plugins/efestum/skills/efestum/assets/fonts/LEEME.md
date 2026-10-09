# Efestum Display — archivos de fuente

Tres pesos: **Light, Regular, Bold**. 171 glifos, 136 mapeados en cmap: mayúsculas y
minúsculas latinas, cifras, puntuación y los acentos del español (Á É Í Ó Ú Ü Ñ Ç y
sus minúsculas). Kerning en GPOS.

| Formato | Para qué |
|---|---|
| `.woff2` | Web. Es el que debe cargar el sitio; pesa ~16–20 KB por peso. |
| `.woff` | Web, respaldo para herramientas viejas que no leen woff2. |
| `.ttf` | Escritorio: Windows, Office, Figma, Canva. |
| `.otf` | Escritorio: Adobe (InDesign, Illustrator, Photoshop) y prensa. |

## Sobre el OTF

Los `.otf` se generaron convirtiendo los `.ttf` publicados, no recompilando desde
`fuente-src/`: ese script apunta a una ruta de SVG que ya no existe, y convirtiendo
el archivo publicado el OTF queda con **exactamente** las mismas formas que el WOFF2
que ya sirve el sitio. Verificado contorno por contorno sobre los 171 glifos de los
tres pesos: desviación máxima **0,30 unidades sobre 1000** de em (0,03 %), ningún
ancho de avance distinto, cmap y kerning idénticos.

## Reglas de uso (SKILL §6)

- Efestum Display es **solo para titulares y rótulos cortos**. Todo lo demás, Rubik.
- **Nunca por debajo de 24 px** en digital. Los numerales van en Rubik.
- Máximo dos tamaños display por superficie. Tracking ≈ −3 % cuando aplique.
- **Nunca componer la palabra EFESTUM con esta fuente** dentro de un titular ni de un
  lockup: el logotipo es el archivo de `current_logo/`, no texto tipografiado.

## Licencia

Propiedad de Inédito Digital. Licencia de uso concedida a Maindsoft. La cadena de
licencia incrustada en los archivos dice literalmente *"para la marca Efestum
Systems"*; si se decide retirar "Systems" del nombre legal, hay que recompilar los
siete archivos de cada peso para que el metadato no contradiga a la marca.
`fsType = 0` (instalable sin restricción).
