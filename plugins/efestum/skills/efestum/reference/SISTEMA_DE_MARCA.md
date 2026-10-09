# EFESTUM — MASTER SKILL

## 0. Cómo usar esta skill

Esta skill es la **fuente de verdad operativa** para cualquier agente que trabaje con EFESTUM.

Antes de producir algo:

1. Lee este archivo completo.
2. Aplica la jerarquía de precedencia de la sección 1.
3. Si la tarea es visual, usa los archivos de `assets/logos/` y no reconstruyas el logotipo.
4. Si la tarea usa dioses, consulta además `modules/EFESTUM_Skill_Posts_con_Dioses_v2.md`.
5. Si la tarea es un post sin dioses, consulta `modules/EFESTUM_Skill_Posts_Automaticos.md`.
6. Si el usuario entrega una nueva referencia o directiva, **la instrucción más reciente manda** y esta skill debe actualizarse.

---

# 1. Jerarquía de verdad y anti-regresión

Cuando dos reglas se contradigan, usar este orden:

1. **Última instrucción explícita del usuario**
2. **Assets actuales de `assets/logos/`**
3. Esta `SKILL.md`
4. Design System v1.0 guardado en `sources/`
5. Banco de copys v1.1 guardado en `sources/`
6. Módulos históricos y prompts previos
7. Exploraciones de `assets/archive/`

## Regla crítica

`assets/archive/` **no define la identidad vigente**. Contiene aprendizaje, pruebas y versiones antiguas.

No regresar automáticamente a:
- logotipos anteriores con símbolo enlazado/intertwined
- martillos literales
- yunques con `</>`
- logos con “SYSTEMS” integrado
- símbolos que se perciban agresivos, malvados o demasiado pesados
- fondos oscuros como sistema principal de redes
- dioses excesivamente sonrientes
- composiciones repetidas dios-derecha/texto-izquierda

---

# 2. Contexto de marca

## Empresa

EFESTUM es la evolución de **Maindsoft**, empresa de software e inteligencia artificial con sede en **Aguascalientes, México**.

Áreas de negocio trabajadas en el proyecto:
- software a la medida
- inteligencia artificial empresarial
- agentes de IA
- ERP / Atalaya
- CRM
- integración de sistemas y APIs
- OCR + IA
- RPA y automatización
- dashboards / BI / observabilidad
- PWA
- infraestructura
- ciberseguridad
- desarrollo web / plataformas

## Ambición

Crecimiento de Aguascalientes hacia México y mercados internacionales, con evolución gradual de servicios hacia productos.

## Origen conceptual

EFESTUM deriva conceptualmente de **Hefesto / Hephaestus**: forja, técnica, artesanía, construcción, precisión y creación de herramientas.

La marca **no vende mitología**. La mitología es una capa conceptual selectiva.

Mensaje público prioritario:

> **Ingeniería, software e inteligencia artificial.**

Idea central:

> **FORJAMOS SISTEMAS INTELIGENTES**

---

# 3. Personalidad

EFESTUM debe sentirse:
- preciso
- sobrio
- técnico
- premium
- contemporáneo
- seguro
- ambicioso sin grandilocuencia
- con confianza calmada
- más ingeniería que “startup de IA”

Nunca debe sentirse:
- gamer
- cyberpunk
- infantil
- fantasioso
- ornamentalmente griego
- motivacional
- “hype”
- genérico de tecnología

---

# 4. Principios de diseño

1. **Ingeniería, no ornamento.** Todo elemento debe ordenar, jerarquizar o explicar.
2. **Contraste extremo, acento único.** Blanco/negro sostienen; rojo significa algo.
3. **Una idea por superficie.** Una pieza = una idea principal.
4. **El vacío es material.** El espacio negativo comunica control.
5. **Consistencia por construcción.** Usar retícula y múltiplos, no decisiones arbitrarias.
6. **La imagen manda en redes.** El texto remata, no describe lo que ya se ve.

---

# 5. Identidad visual actual

## 5.1 Logotipo vigente

**Siempre que se pueda, usar el SVG**: es el original vectorial, escala sin pérdida
y no trae fondo. Los PNG son respaldo para herramientas que no leen vector.

```
assets/logos/svg/logo-horizontal-{negro,blanco,rojo}.svg   <- prioritario
assets/logos/svg/logo-cuadrado-{negro,blanco,rojo}.svg
assets/logos/svg/isotipo-{negro,blanco,rojo}.svg
assets/logos/png/…                                          mismos, en PNG
```

Las versiones **roja y cuadrada sí existen** y son oficiales. La roja se usa solo
cuando el logotipo es el único elemento de la pieza y no hay otro rojo en la
superficie: el tope de 5 % de §7 sigue aplicando. La cuadrada es para avatares y
formatos donde el horizontal no cabe, nunca por gusto compositivo.

Los PNG antiguos rasterizados a 2048 px (`NUEVO LOGO EFESTUM … (2).png`,
`ISOTIPO EFESTUM … .png`) no se incluyen en esta skill. **Para trabajo nuevo va el SVG**.

### Reglas
- Priorizar **logo horizontal**.
- No redibujarlo.
- No reinterpretarlo.
- No deformarlo.
- No comprimir ni estirar.
- No rotarlo.
- No agregar “SYSTEMS”.
- No agregar sombras, contornos o efectos arbitrarios.
- Si la fidelidad importa, **componer el asset oficial encima del mockup**; no pedir al modelo generativo que lo invente.
- En fondos claros: logo negro.
- En superficies negras: logo blanco.

### Isotipo

El isotipo actual se compone de cuatro formas enfrentadas que convergen alrededor de un vacío central con lectura de destello/punto de precisión.

Justificación recomendada:

> Cuatro fuerzas convergen en un punto de precisión. El símbolo representa integración, construcción e inteligencia aplicada: datos, procesos, tecnología y ejecución convirtiéndose en un solo sistema.

Otra lectura comercial:

> **De varias piezas, un solo sistema.**

El destello central se justifica como **resultado del espacio negativo**, no como brillo decorativo.

### Uso del isotipo solo

Permitido en:
- avatar
- favicon/app icon
- hardware/dispositivos
- sellos compactos
- algunos textiles o piezas icon-only cuando se solicite expresamente

En aplicaciones institucionales generales, priorizar símbolo + EFESTUM horizontal.

### Isotipo reducido (tamaños pequeños)

El isotipo oficial tiene una **costura vertical central de 2,30 % del ancho**. Es lo
primero que se cierra al reducir: a 16 px las dos mitades se funden en una mancha y
se pierde el vacío central, que es el concepto del símbolo. En bordado la aguja no
deja huecos de menos de ~1,2 mm, así que pasa lo mismo.

`assets/isotipo_reducido/` resuelve eso **sin redibujar nada**: los cuatro cuerpos
conservan su trazado original y solo se separan en el eje X, lo que lleva la costura
a 6,00 % simétrico. Curvas, radios y grosores quedan idénticos.

| Uso | Archivo | Mínimo |
|---|---|---|
| ≥ 44 px / ≥ 53 mm | `assets/logos/svg/isotipo-*.svg` | oficial |
| Favicon, app icon | `isotipo_reducido/favicon/` | 17 px de ancho |
| Bordado plano | `isotipo-reducido-1bit-2048.png` | 33 mm de ancho |
| Grabado láser | el mismo 1 bit | 9 mm de ancho |
| Grabado mecánico | el mismo 1 bit | 18 mm de ancho |

Por debajo de 33 mm en bordado no va este archivo: va el isotipo en una sola masa,
sin costura. Detalle y cálculo en `assets/isotipo_reducido/LEEME.md`.

---

# 6. Tipografía

## Títulos

**EFESTUM Display** / lenguaje tipográfico del wordmark.

Archivos en `assets/fonts/`: **Light, Regular y Bold** en `.otf`, `.ttf`, `.woff2` y
`.woff`. Web carga `.woff2`; escritorio y Adobe, `.otf`; Office y Figma, `.ttf`.
171 glifos con los acentos del español y kerning en GPOS. Muestra visual en
`assets/type_reference/`, notas en `assets/fonts/LEEME.md`.

- Light / Regular / Bold según jerarquía
- no bajar de 24 px en digital si se usa como display
- máximo dos tamaños display por superficie
- tracking display aprox. -3 % cuando aplique

## Texto

**Rubik** para:
- cuerpo
- subtítulos
- UI
- metadatos
- etiquetas
- microcopy

## Labels

- uppercase
- Rubik
- tracking +30 % en presentaciones e impresos; +0,14 a +0,22 em en web e interfaz
- discretos
- no competir con el titular

---

# 7. Paleta

```text
Ink        #0A0A0A
White      #FFFFFF
Paper      #F4F4F4
Accent     #E60004
Muted      #8A8A8A
Rule light #D8D8D8
Rule dark  #262626
Panel      #141414
```

## Rojo

`#E60004` es el rojo vigente y sustituye versiones previas como `#E40800`.

Regla:

> **El rojo es señal, no relleno.**

Objetivo: menos de ~5 % del área.

Usos:
- Filo de Forja
- una palabra clave
- un dato
- un pequeño indicador UI
- un punto/acento
- CTA principal cuando corresponda

No usar:
- fondos rojos grandes
- rojo por decoración
- múltiples tonos rojos

---

# 8. Mármol Digital

**Mármol Digital NO es mármol físico.**

Sistema canónico:
- base `white` o `paper`
- grid técnico extremadamente tenue
- campos de puntos
- líneas de ingeniería muy sutiles
- aire / espacio negativo
- monocromático
- rojo superpuesto, nunca integrado a la textura

Masters en `assets/marmol/`, nombrados por su proporción real:

```
marmol-1x1.png     1800x1800    marmol-16x9.png  3840x2160
marmol-4x5.png     2160x2700    marmol-21x9.png  3780x1620
marmol-9x16.png    2160x3840    marmol-A4-vertical.png    2480x3508  (300 ppp)
marmol-3x4.png     2160x2880    marmol-A4-horizontal.png  3508x2480  (300 ppp)
```

Se **generan** a cada proporción, no se estiran ni se recortan: §24 prohíbe deformar,
y al estirar cambian el paso de retícula y la densidad de puntos, que es lo que da la
escala del sistema. El paso va referido al lado corto, así que un A4 y un banner 21:9
tienen la misma densidad aparente.

Parámetros: fondo `#F5F5F5` (los PNG llevan este valor horneado; en CSS el Mármol usa Papel `#F4F4F4`, un nivel de diferencia imperceptible. Si un bloque de color sólido debe empatar exacto con un PNG, usar `#F5F5F5`), retícula 5,66 % del lado corto, puntos 1,52 %, retícula
mayor cada 4 celdas, densidad radial con el centro limpio, contraste total dentro de
~20 niveles. **El fondo nunca compite con el contenido**: si la retícula se nota a
primera vista, está mal.

**Los tres masters originales tienen los nombres cruzados.** `MARMOL RECTANGULAR.png`
es 1086x1448, o sea vertical 3:4; `MARMOL VERTICAL.png` es 1672x941, o sea horizontal
16:9. Siguen ahí para no romper referencias, pero para trabajo nuevo van los `marmol-*`.

Evitar:
- vetas de mármol real como textura gráfica de marca
- piedra envejecida
- grietas
- greca griega
- columnas decorativas
- capiteles
- laureles gráficos
- dorado
- retículas cyberpunk
- circuitos literales de adorno

## Uso reciente

Para redes y aplicaciones institucionales de presentación de marca, usar **fondos claros con Mármol Digital** como base predeterminada.

Fondos oscuros quedan reservados principalmente para:
- tela negra
- objetos negros mate
- ciertos mockups físicos
- exploraciones expresamente solicitadas

---

# 9. Filo de Forja

Línea horizontal roja: **firma visual oficial**.

Referencias de medida en 1920×1080:
- bajo título: 120×4
- sección: 1720×5
- separador: 1720×4
- acento centrado: 200×6

Debe sentirse como trazo de ingeniería.

No sustituir con:
- crosshairs
- targets
- cruces tech
- ornamentos mitológicos

---

# 10. Retícula y motion

Base de referencia 1920×1080:
- margen 100
- contenido desde y=150
- espaciado en múltiplos de 20

Motion:
- preciso y contenido
- sin rebote
- sin elasticidad
- sin rotaciones decorativas
- 200–800 ms en presentaciones y video; 160–460 ms en web (ver `DESIGN.md`)
- curva `cubic-bezier(.22,1,.36,1)`
- reveal de texto: subida leve + opacidad
- reveal de imagen: escala sutil + opacidad
- Filo: barrido horizontal

---

# 11. Sistema verbal

## Regla madre

**Una idea por oración.**

## Verbos preferidos

- forjar
- construir
- diseñar
- integrar
- automatizar
- escalar
- conectar
- ordenar
- medir
- operar
- decidir
- monitorear

## Evitar siempre

- líder
- innovador
- disruptivo
- de vanguardia
- de última generación
- revolucionar
- transformación digital
- sinergia
- ecosistema
- potenciar
- impulsar como verbo genérico de venta
- empoderar
- soluciones a la medida de tus necesidades
- estamos emocionados de
- ¿sabías que…?
- en un mundo cada vez más digital
- la tecnología del futuro, hoy

## Forma

- sin signos de exclamación
- no usar MAYÚSCULAS dentro de una frase para “gritar” énfasis; si el titular completo es display uppercase, debe ser una decisión tipográfica de pieza
- anglicismos solo cuando el equivalente español no funciona: software, ERP, dashboard sí; insight/engagement/deliverable no
- cliente como sujeto; EFESTUM como medio
- cifras verificables antes que adjetivos

---

# 12. Datos, clientes y legal

No inventar:
- clientes
- testimonios
- métricas
- porcentajes
- número de proyectos
- empleados
- fecha de fundación
- resultados
- tiempos de implementación que no estén validados

Los ejemplos como “cinco días a seis horas”, “ocho semanas”, etc. son **plantillas ilustrativas** y deben sustituirse por datos verificados antes de publicar.

No usar logotipos de clientes sin permiso escrito.

Nombres tentativos de producto como **Talos, Kourai, Brontes, Pyra** no están validados legalmente y no deben publicarse como productos reales.

EFESTUM / Efestum sigue sujeto a las validaciones legales/marcarias correspondientes; no afirmar registro si no se ha comprobado.

---

# 13. Banco de titulares

## Marca / construcción
- Forjamos sistemas inteligentes
- Forjamos soluciones
- Construimos lo que no existe
- Aquí se construye
- Del problema al sistema

## Datos / control
- Mareas de información, control total
- Tu operación, sin puntos ciegos
- Lo que no se mide, se paga
- Cuatro sistemas, una sola verdad
- Tu inventario miente. Te decimos dónde

## Velocidad
- Rapidez y eficacia
- Entregas cada dos semanas

## Escala
- Plataformas que aguantan cuando creces
- Forjamos tu imperio digital

## Mitológico selectivo
- Forjamos soluciones para dioses
- Criterio de artesano. Escala industrial
- Claridad total sobre tus datos
- Cero fugas. Nada sale de donde no debe
- Contra la ineficiencia, sin excepciones

---

# 14. Mitología: regla de uso

La mitología opera por **contraste irónico**:

> estética clásica de mármol + hardware/código contemporáneo

La marca no “cuenta cuentos”.

## Frecuencia

Máximo recomendado: **1 pieza mitológica por cada 4 publicaciones**.

## Solo panteón griego

No usar:
- guerreros genéricos
- filósofos aleatorios
- fantasía
- personajes sin correspondencia conceptual

## Dios → dominio

| Dios | Dominio | Titular / territorio |
|---|---|---|
| Zeus | mando, control, decisiones | Forjamos soluciones para dioses / control |
| Poseidón | big data, flujo, data lakes | Mareas de información, control total |
| Atenea | IA, estrategia, arquitectura | Forjamos tu imperio digital / estrategia |
| Hermes | APIs, conectividad, velocidad | Rapidez y eficacia |
| Hades | backend, infraestructura, seguridad | Cero fugas. Nada sale de donde no debe |
| Apolo | BI, dashboards, observabilidad | Claridad total sobre tus datos |
| Ares | automatización, eficiencia | Contra la ineficiencia, sin excepciones |
| Hefesto | construcción de software | Construimos lo que no existe |

---

# 15. Dirección de esculturas

## Material

- mármol blanco
- mate
- detalle de museo
- mineral, no piel humana
- realista como escultura

## Expresión

Debe ser:
- divina
- serena
- contenida
- segura
- contemplativa
- apenas satisfecha

No:
- gran sonrisa
- felicidad comercial
- alegría exagerada
- enojo
- gesto malvado
- ceño dramático
- pose superheroica

La expresión buscada es **dominio tranquilo**.

## Pose y composición

Variar activamente:
- dios izquierda / texto derecha
- dios derecha / texto izquierda
- dios central
- close-up
- sentado
- de pie
- busto
- cuerpo parcial
- cámara 3/4 izquierda
- cámara 3/4 derecha
- contrapicado leve
- dispositivo protagonista, dios secundario

No repetir siempre la misma dirección o layout.

---

# 16. Dispositivos

Cuando aparezca un dios, debe **usar activamente** un dispositivo:
- laptop
- tablet
- smartphone
- monitor
- workstation
- dashboard

El dispositivo debe ser:
- físicamente plausible
- con aluminio/vidrio/policarbonato/metal anodizado
- proporciones correctas
- biseles, cámara, bisagra y puertos realistas
- sin sci-fi imposible

Aplicar el **isotipo EFESTUM** en el hardware de forma discreta.

Si el prompt pide ver la parte trasera de la tablet, debe verse la parte trasera, no la pantalla.

---

# 17. Posts sin dioses

El sistema visual debe funcionar igual de bien sin mitología.

Usar:
- laptops
- monitores
- smartphones
- tablets
- dashboards
- arquitectura de software
- módulos
- flujos
- interfaces
- capas de sistemas
- workstation

Regla de correspondencia:

> Si el copy habla de módulos, mostrar módulos. Si habla de integración, mostrar sistemas conectados. Si habla de observabilidad, mostrar dashboard/alertas. La imagen debe tener una relación semántica real con el copy.

Rutas aprobadas:
- integración de sistemas
- automatización
- dashboard/observabilidad
- arquitectura modular

---

# 18. Composición social

Evitar series donde todas las piezas tienen:
- texto a la izquierda
- figura a la derecha
- mismo tamaño de logo
- misma altura de titular

Rotar layouts:

A. texto izquierda / visual derecha  
B. visual izquierda / texto derecha  
C. titular superior / visual inferior  
D. figura central / texto periférico  
E. split vertical sistema/escultura  
F. dispositivo protagonista / escultura secundaria  
G. close-up editorial  
H. escritorio / workstation  
I. arquitectura de capas  
J. dashboard grande con copy mínimo

---

# 19. Instagram

Rol: la imagen demuestra nivel; el copy remata.

- 2 posts feed/semana como referencia de cadencia
- carrusel quincenal
- reel mensual
- stories 2–3/semana
- primera línea debe funcionar sola
- caption 1–2 líneas cuando sea posible
- sin emojis en cuerpo; flecha `→` permitida
- máximo 3 hashtags
- fondo claro / Mármol Digital
- máximo una pieza mitológica de cada cuatro
- reels <=15 s, proceso/manos/pantallas/código, sin voz motivacional
- texto en pantalla <=6 palabras por frame

No:
- happy Friday
- frases motivacionales
- “5 tips” genéricos
- captions largos
- stock de oficina con sonrisas
- audio trend como base de identidad

---

# 20. Facebook

Rol: alcance local y reclutamiento en **Aguascalientes/Bajío**. No es un segundo LinkedIn.

Audiencia:
- candidatos técnicos locales
- proveedores/aliados
- familias/equipo
- empresas medianas locales

Reglas:
- más concreto que LinkedIn, no más informal
- mencionar ubicación
- párrafo ligeramente más largo permitido
- sin emojis en cuerpo; como máximo uno al final de una vacante si fuera necesario
- sin exclamaciones
- vacantes deben incluir salario o rango
- distinguirse del copy de LinkedIn

Tipos:
1. Vacantes
2. Empresa/equipo
3. Presencia local
4. Servicio en lenguaje llano

---

# 21. Sitio web

## Rol

El sitio **confirma lo que las redes prometieron**. Su trabajo es quitar dudas y provocar una reunión, no explicar la empresa exhaustivamente.

## Reglas

1. El encabezado afirma, no saluda.
2. Los botones son verbos.
3. Cada servicio se explica en una línea.
4. Sin carrusel de logos de clientes sin permiso.
5. Mármol Digital de fondo.
6. Rojo solo en dato importante y CTA principal.
7. Formularios de máximo 3 datos.

## Hero aprobado

### Forjamos sistemas inteligentes

Desarrollamos software e inteligencia artificial para empresas que necesitan que su operación deje de depender de hojas de cálculo.

`Agendar diagnóstico` · `Ver cómo trabajamos`

Alternativas:
- Construimos lo que tu operación necesita y no existe
- Tu empresa ya genera los datos. Falta que trabajen para ti
- Ingeniería de software para operaciones que no pueden detenerse

## Servicios

- **Software a la medida:** Construimos lo que tu operación necesita y no existe en el mercado.
- **Inteligencia artificial:** Agentes que leen, deciden y ejecutan dentro de tus procesos.
- **Integración:** Conectamos lo que ya tienes para que deje de vivir en islas.
- **Infraestructura:** Plataformas que aguantan cuando la empresa crece.

## Página interior de servicio — ejemplo Integración

### Integración
Conectamos lo que ya tienes para que deje de vivir en islas.

**Cuándo lo necesitas**  
Cuando el mismo dato se captura dos veces. Cuando el reporte sale de copiar y pegar. Cuando nadie sabe cuál de los dos sistemas dice la verdad.

**Qué entregamos**  
Un flujo de datos entre tus sistemas, documentado, monitoreado y con alguien que responde si se cae.

**Cuánto tarda**  
De seis a doce semanas según cuántos sistemas y qué tan ordenados estén.

`Agendar diagnóstico`

## Cómo trabajamos

1. **Diagnóstico.** Dos semanas dentro de tu operación. Salimos con el problema escrito y un alcance con precio.
2. **Construcción.** Entregas cada dos semanas. Ves avances, no reportes de avances.
3. **Operación.** Lo que construimos lo mantenemos. Sabes a quién llamar.

## Casos

No publicar logos sin permiso escrito.

Estructura:
- Cliente · Industria
- El problema
- Qué hicimos
- Qué no hicimos
- El resultado: cifra + unidad + antes
- Cuánto tardó

## Contacto

### Cuéntanos qué se está rompiendo.
Respondemos en 24 horas hábiles.

Campos: Nombre · Correo · Qué se está rompiendo  
Botón: `Enviar`

## Microcopy

- Principal: `Agendar diagnóstico`
- Secundario: `Ver cómo trabajamos`
- Enviado: `Recibido. Te escribimos en menos de 24 horas hábiles.`
- Error: `Falta el correo. Sin eso no podemos responder.`
- Obligatorio: `Este dato sí lo necesitamos.`
- Cargando: `Construyendo…`
- Vacío: `Todavía no hay nada aquí.`
- 404: `Esta página no existe. Lo que sí construimos está aquí.`
- 500: `Se cayó algo de nuestro lado. Ya lo estamos viendo.`
- Cookies: `Usamos cookies para que el sitio funcione. Nada más.`
- Suscripción: `Escribimos poco y solo cuando tenemos algo que decir.`
- Fin: `Aguascalientes, México.`

## Metadatos

- Inicio: `EFESTUM · Software e inteligencia artificial`
- Servicios: `Qué construimos · EFESTUM`
- Integración: `Integración de sistemas · EFESTUM`
- Casos: `Casos · EFESTUM`
- Contacto: `Contacto · EFESTUM`

**La marca es EFESTUM, a secas** (decisión del usuario, 5 oct 2026). No se escribe
"Efestum Systems" en ningún lado: ni en el lockup, ni en titulares, ni en metadatos,
ni en la firma de correo, ni en `name`/`alternateName` del schema. El veto del
DECISION_LOG no era solo gráfico.

Description: `Desarrollamos software e IA a la medida para empresas en México. Integración, automatización e infraestructura. Aguascalientes.`

---

# 22. Mockups institucionales

## Sistema actual preferido

Para presentaciones de marca e institucionales:
- fondos claros
- Mármol Digital tenue
- blanco/paper predominante
- rojo mínimo
- logo horizontal negro
- isotipo como acento secundario
- dioses opcionales, siempre con dispositivo

Aplicaciones:
- papelería
- tarjetas
- sobres
- carpetas
- informes
- credenciales
- banners
- rollups
- stands
- espectaculares
- mobiliario urbano
- publicidad digital
- web banners
- displays
- recepciones
- salas de juntas
- muros institucionales

## Textiles

- tela negra
- logo blanco
- sobrio
- sin adorno
- bordado/impresión limpia

---

# 23. Espacios físicos

## Lobby EFESTUM

Estética:
- alto nivel
- profesional
- blanco
- madera gris
- piso blanco
- mobiliario gris
- iluminación original o cálida contenida
- logo metálico EFESTUM

Correcciones históricas:
- cerrar puerta trasera cuando se solicite
- eliminar líneas/elementos técnicos no deseados del techo

## Fachada compartida INÉDITO + EFESTUM

- mantener logo INÉDITO
- sustituir Maindsoft por EFESTUM
- respetar exactamente el logo vigente
- tagline corregida según copy aprobado
- sin inventar “SYSTEMS” en el lockup si no está en el asset

## Sala de juntas compartida

- EFESTUM + INÉDITO DIGITAL
- ambos en acabado metálico/satinado monocromático
- sobrios
- separador vertical
- Inédito aprox. 2 % más pequeño cuando se solicite ese balance
- mantener fidelidad extrema de ambos logos
- TV recta
- versiones sala vacía/ordenada y con junta

## Muro compartido

- blanco mate
- Mármol Digital tenue
- logos metálicos satinados
- montaje con separador
- vista frontal para ficha técnica cuando se requiera

---

# 24. Reglas de fidelidad visual

Cuando el usuario da una foto existente:
- preservar perspectiva
- preservar iluminación salvo instrucción
- no cambiar arquitectura innecesariamente
- modificar solo lo solicitado
- para logos, compositar el original

Cuando el usuario pide adaptación de formato:
- no estirar
- no comprimir
- no deformar
- reacomodar proporcionalmente
- expandir fondo si hace falta
- no cortar información importante

---

# 25. Historia del naming y restricciones

El concepto EFESTUM gusta por su historia; la preocupación principal fue **memorabilidad**.

Exploraciones previas incluyeron:
- BRONTUM
- TEMPRUM
- EFERUM
- FERVUM
- TESSUM
- ERGIUM
- TRAMUM
- LIGIUM

Feedback y rechazos importantes:
- demasiadas terminaciones `-UM` reducen diferenciación
- nombres acabados en `FEST` evocan fiesta/festividad en México
- `Efesto` / `Hefesto` evidentes pero con problemas de ocupación/registro/dominio reportados en la investigación previa
- `Efra` suena informal y remite a Efraín
- `Hefra` suena igual que Efra
- `Eferum` es débil fonéticamente y menos memorable
- `Hefto` suena informal/alien/juguete
- `Efor` / `Hefor` carecen de fuerza
- `Festor` se acerca a “Néstor” y marca demasiado “fest”
- otras rutas se percibieron como medicamento, difíciles de escribir o demasiado alejadas del concepto

**No presentar estas conclusiones como verificación legal vigente.** Son historial creativo, no dictamen marcario.

---

# 26. Evolución del isotipo

Rutas exploradas:
- llama tecnológica / E
- herrero con martillo
- martillo geométrico
- yunque `</>`
- símbolos abstractos de forja
- destello central

Aprendizajes:
- martillo demasiado literal
- ciertas versiones parecían informales, juguete o agresivas
- algunas rutas con destello parecían “malvadas” o no comunicaban el concepto
- el isotipo debía caber perfectamente en cuadrado
- la solución actual gana por simetría, compactación y sistema

No volver a rutas antiguas salvo que el usuario lo pida como exploración.

---

# 27. Generación de imagen: prompt maestro

```text
Create a premium EFESTUM brand piece.

SOURCE OF TRUTH
Use the exact current EFESTUM assets provided. Do not redesign the logo.
Prefer the horizontal lockup. Do not append SYSTEMS.

STYLE
High-end B2B software engineering brand.
Light Digital Marble background: white/paper, extremely subtle technical grid,
faint dot fields, minimal engineering lines, generous negative space.
No real decorative marble veins, Greek-key ornaments, gold, cyberpunk or neon.

TYPOGRAPHY
Headlines: EFESTUM Display visual language.
Body/UI: Rubik.

COLOR
#0A0A0A, #FFFFFF, #F4F4F4, #8A8A8A, accent #E60004.
Red under 5% of the composition.

COMPOSITION
One idea per surface. Strong hierarchy. Vary composition from previous pieces.
Use the red Filo de Forja as the principal decorative accent.

IF A DEITY IS USED
Use only a Greek pantheon deity appropriate to the technical domain.
Museum-quality white marble sculpture, matte mineral surface.
Expression divine, serene, controlled, subtly satisfied; not smiling, angry or sinister.
The deity actively uses a realistic modern device.

DEVICES
Photoreal, plausible materials/proportions, with the exact EFESTUM isotipo subtly applied.

COPY
Assertive, concrete, short, engineering-led. No hype, no exclamation marks.
```

---

# 28. Negative prompt maestro

```text
no fake EFESTUM logo
no old EFESTUM logo
no SYSTEMS appended to logo
no logo distortion
no excessive red
no dark feed background unless explicitly requested
no real marble veins as brand graphic texture
no Greek key pattern
no decorative columns
no laurels
no gold
no cyberpunk
no neon
no humanoid robot
no glowing AI brain
no gamer aesthetic
no random circuit decoration
no target/crosshair ornaments
no broad smile
no cheerful commercial expression
no angry deity
no evil expression
no fantasy armor
no superhero pose
no human skin on sculpture
no impossible device
no warped laptop keyboard
no clutter
no invented metrics
no invented client logo
```

---

# 29. Procedimiento para cualquier agente

## Antes de producir

1. Identificar canal y objetivo.
2. Determinar si la pieza debe ser mitológica o de ingeniería pura.
3. Seleccionar copy existente o escribir uno bajo el sistema verbal.
4. Verificar si cualquier cifra es comprobable.
5. Elegir layout distinto a piezas recientes.
6. Elegir asset de logo correcto.
7. Usar Mármol Digital si la pieza es clara.
8. Reservar rojo para una sola función.

## Después de producir

Verificar:
- ¿Logo actual exacto?
- ¿Sin SYSTEMS?
- ¿Rojo <5%?
- ¿Título EFESTUM / cuerpo Rubik?
- ¿Mármol Digital canónico?
- ¿Filo de Forja como principal acento?
- ¿Una idea por superficie?
- ¿Si hay dios, corresponde al dominio y usa dispositivo?
- ¿Expresión serena/divina, no alegre?
- ¿Dispositivo realista con isotipo?
- ¿Composición distinta a la anterior?
- ¿Sin datos inventados?
- ¿Se puede quitar algo sin perder mensaje? Si sí, quitarlo.

---

# 30. Interacción con el solicitante

- Idioma por defecto: español.
- Ejecutar directamente cuando la solicitud es clara.
- No pedir confirmación innecesaria.
- Si se solicitan varios mockups, entregar imágenes separadas cuando sea posible, no una cuadrícula, salvo que se pida tablero/board.
- Si se solicita una edición, cambiar solo lo pedido.
- Si el usuario corrige un detalle visual, tratar la corrección como nueva norma para las siguientes piezas.
- Si se requiere fidelidad de logo, usar asset original.

---

# 31. Archivos y referencias

## Actuales
`assets/logos/svg/` — logotipo vectorial, las nueve variantes  
`assets/logos/png/` — las mismas en PNG  
`assets/isotipo_reducido/` — favicon, bordado y grabado  
`assets/fonts/` — Efestum Display en otf, ttf, woff2 y woff  
`assets/marmol/` — ocho masters por proporción  
`assets/type_reference/` — muestra tipográfica

## Ejemplos actuales
`assets/referencias/` — **auditado el 5 oct 2026**

## Referencias retiradas
`reference/REFERENCIAS_RETIRADAS.md` — piezas con "SYSTEMS", wordmark roto, copy en inglés o
símbolo anterior. No se usan como referencia. El motivo de cada una y la corrección
aplicada a los ocho posts están en `reference/REFERENCIAS_RETIRADAS.md`.

## Historia y pruebas
`assets/archive/`

## Documentos fuente
`sources/`

## Skills especializadas
`modules/`

---

# 32. Regla final

Cuando haya duda, EFESTUM debe sentirse como:

> **una firma de ingeniería que sabe exactamente lo que está construyendo**

No como una agencia genérica de tecnología, una marca de fantasía griega ni una startup futurista de clichés.
