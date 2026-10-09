# EFESTUM — marca para Claude Code

Un comando, `/efestum`, le da a Claude todo el sistema de marca EFESTUM: reglas,
voz, logotipos, tipografía, Mármol Digital, referencias y tokens CSS. Lo que crees
con Claude sale con la estética y los lineamientos de EFESTUM.

## Instalar (una vez por computadora)

Dentro de Claude Code (terminal, app de escritorio o IDE):

```
/plugin marketplace add ineditodigital-sudo/efestum
/plugin install efestum@efestum
```

O desde la terminal:

```bash
claude plugin marketplace add ineditodigital-sudo/efestum
claude plugin install efestum@efestum
```

Claude Code descarga este repositorio con todos los archivos. La skill queda
disponible en todos tus proyectos.

## Actualizar

Cuando la marca cambie en este repositorio:

```
/plugin marketplace update efestum
```

Para que se actualice sola: `/plugin` → **Marketplaces** → *efestum* → **Enable auto-update**.

## Usar

| Comando | Qué hace |
|---|---|
| `/efestum` | Carga la marca para todo lo que hagas en la sesión. |
| `/efestum aplicar` | Instala la marca en el proyecto actual: copia logos, fuentes, favicon y `efestum.css`, conecta los estilos y deja las reglas en el `CLAUDE.md` del proyecto. |
| `/efestum revisar <ruta>` | Audita una pieza, archivo o carpeta contra la lista de marca. |
| `/efestum <tarea>` | Hace la tarea con la marca: `/efestum landing para el servicio de IA`, `/efestum post de Instagram sobre integración`. |

Si otro comando ya se llama `/efestum`, usa `/efestum:efestum`. Claude también
activa la skill solo cuando una tarea menciona EFESTUM.

## Qué hay en el repositorio

```
.claude-plugin/marketplace.json        catálogo del marketplace
plugins/efestum/
  .claude-plugin/plugin.json           manifiesto del plugin
  skills/efestum/
    SKILL.md                           reglas esenciales y enrutamiento por tarea
    reference/                         sistema de marca completo v3.1.0, decision log,
                                       design system, banco de copys, sistema verbal,
                                       canales, sitio web, módulos de dioses, prompts
    assets/logos/                      logotipo oficial SVG y PNG
    assets/isotipo_reducido/           favicon, bordado y grabado
    assets/fonts/                      Efestum Display (woff2, woff, ttf, otf)
    assets/marmol/                     fondos Mármol Digital por proporción
    assets/referencias/                piezas aprobadas como guía de composición
    assets/web/efestum.css             tokens y componentes para web
```

## Mantener

Para cambiar la marca, edita los archivos dentro de `plugins/efestum/skills/efestum/`
y haz push a `main`. Quien tenga el plugin lo recibe con `/plugin marketplace update efestum`.
