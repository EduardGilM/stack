# Instalación y uso para agentes

Esta guía está dirigida al agente que recibe la distribución de Trace Style. Si el encargo consiste en diseñar una interfaz, carga la skill y continúa con ese trabajo. Si consiste en instalarla, sigue la ruta correspondiente al host y al alcance solicitado.

## Identifica el contenido

La raíz de la distribución contiene `README.md`, `docs/` y `.agents/skills/trace-style/`. La carpeta que debes instalar es **`.agents/skills/trace-style/`**: dentro están `SKILL.md`, sus referencias y los metadatos opcionales de interfaz.

Si recibes un ZIP, extrae la carpeta raíz `trace-style/`, incluidos los archivos ocultos. No copies toda la distribución dentro del directorio de skills del host ni añadas un nivel extra `trace-style/trace-style/`.

Las instrucciones no requieren MCP, servicios, paquetes de frontend, fuentes ni herramientas de un proveedor concreto. `agents/openai.yaml` aporta metadatos opcionales; el contenido de diseño está en Markdown.

## Instala con el gestor de skills

Desde el proyecto de destino, instala la skill desde GitHub:

```sh
npx skills add EduardGilM/stack --skill trace-style
```

El [gestor `skills`](https://github.com/vercel-labs/skills#source-formats) admite rutas locales. Ejecuta desde la raíz del proyecto que debe recibir la skill, usando como fuente la raíz de esta distribución:

```sh
npx skills add /ruta/a/trace-style --skill trace-style
```

Selecciona el agente receptor. Para una instalación acotada y sin preguntas interactivas, cuando ese destino ya esté autorizado, indícalo de forma explícita:

```sh
npx skills add /ruta/a/trace-style --skill trace-style --agent codex --copy --yes
```

Puedes sustituir `codex` por `claude-code`, `cursor` u otro identificador admitido por el gestor. `--copy` conserva una copia independiente; `--global` selecciona el ámbito de usuario. Las [opciones oficiales](https://github.com/vercel-labs/skills#options) describen selección, alcance y métodos de instalación.

Para descubrir la skill sin instalarla:

```sh
npx skills add /ruta/a/trace-style --skill trace-style --list
```

No uses una instalación para todos los agentes si solo se ha solicitado uno. Si se indica una raíz personalizada, utiliza esa ubicación mediante copia manual.

## Instalación manual

1. Identifica el host y el alcance solicitado. Usa la raíz de skills anunciada por el entorno; si no anuncia una, consulta la tabla. El ámbito de proyecto es adecuado cuando solo se necesita para ese trabajo.
2. Copia **el contenido de `.agents/skills/trace-style/`** a `<raíz-de-skills>/trace-style/`, conservando todas las rutas relativas.
3. Si existe una copia, compara los archivos y aplica la actualización solicitada conservando las personalizaciones ajenas al cambio. Evita duplicados del mismo nombre en varios ámbitos.
4. Comprueba los archivos y, si es posible, la carga en el agente. Informa del destino y del alcance comprobado.

Las rutas de proyecto parten de su raíz y `~` representa la carpeta personal del usuario.

| Host | Proyecto | Usuario | Invocación |
| --- | --- | --- | --- |
| [Codex CLI / extensión IDE](https://learn.chatgpt.com/docs/build-skills) | `.agents/skills/trace-style/` | `~/.agents/skills/trace-style/` | `$trace-style` o selección con `/skills` |
| [Claude Code](https://code.claude.com/docs/en/skills) | `.claude/skills/trace-style/` | `~/.claude/skills/trace-style/` | `/trace-style` seguido del encargo |
| [Cursor](https://cursor.com/docs/skills) | `.cursor/skills/trace-style/` o `.agents/skills/trace-style/` | `~/.cursor/skills/trace-style/` o `~/.agents/skills/trace-style/` | Escribe `/` y selecciona la skill |

Las rutas y la sincronización pueden variar según el host. En una sesión remota o en la nube, los archivos tienen que estar en el sistema que ese agente puede leer; una copia local no prueba disponibilidad remota. Consulta la documentación del host si no aparecen.

### Ejemplo POSIX

Ejecuta desde el proyecto de destino. El origen apunta a la carpeta interna de la skill, no a la raíz de la distribución.

```sh
trace_source="/ruta/a/trace-style/.agents/skills/trace-style"
trace_target=".agents/skills/trace-style"
test -f "$trace_source/SKILL.md" || exit 1
test ! -e "$trace_target" || exit 1
mkdir -p "$(dirname "$trace_target")"
cp -R "$trace_source" "$trace_target"
```

El ejemplo se detiene si el destino ya existe. Para actualizarlo, compara los archivos antes de aplicar los cambios.

### Ejemplo PowerShell

```powershell
$traceSource = "C:\ruta\a\trace-style\.agents\skills\trace-style"
$traceTarget = Join-Path (Get-Location).Path ".agents\skills\trace-style"
if (-not (Test-Path -LiteralPath (Join-Path $traceSource "SKILL.md"))) {
    throw "El origen no contiene SKILL.md"
}
if (Test-Path -LiteralPath $traceTarget) {
    throw "El destino ya existe; compara su contenido antes de actualizar"
}
New-Item -ItemType Directory -Force -Path (Split-Path $traceTarget) | Out-Null
Copy-Item -LiteralPath $traceSource -Destination $traceTarget -Recurse
```

## Comprueba la instalación

- Lee el `SKILL.md` instalado: su frontmatter debe contener `name: trace-style`, una descripción y la versión de las instrucciones.
- Confirma que los enlaces a `references/` se resuelven desde esa carpeta y que los archivos son legibles.
- Si el host ofrece un catálogo, comprueba que aparece `trace-style`. Si solo puedes comprobar archivos, comunica «copiada; carga automática sin verificar».
- Carga las instrucciones y continúa con el encargo original. Si la actualización no aparece, recarga la sesión según el mecanismo del host.

## Carga manual en otros agentes

Con acceso a archivos, proporciona la ruta real a este punto de entrada:

> Lee íntegramente `.agents/skills/trace-style/SKILL.md` y aplica sus instrucciones a este encargo. Resuelve las referencias desde esa carpeta y consulta solo las que necesites. Diseña e implementa la pantalla de ajustes conservando la marca y el stack del proyecto.

Si la skill se ha instalado en otra ubicación, sustituye la ruta. Sin acceso a archivos, adjunta el contenido de `SKILL.md` y las referencias que se necesiten, identificando cada documento. Un ZIP solo sirve si el agente puede extraerlo o leer sus archivos; escribir el nombre de una skill no carga sus instrucciones por sí solo.

## Actualiza, comparte o retira

Para una fuente local, vuelve a ejecutar la instalación desde la distribución actualizada o aplica sus cambios a la copia manual. Conserva el nombre `trace-style` y comprueba la versión y las referencias. Las copias manuales no se actualizan cuando cambia la carpeta de origen.

Comparte la distribución completa para incluir esta guía, o solo la carpeta interna si el receptor conoce su instalación. Al crear un ZIP o un repositorio, incluye `.agents/` aunque sea una carpeta oculta.

Si se instaló con el gestor, usa su [comando de retirada](https://github.com/vercel-labs/skills#skills-remove), seleccionando la skill, el agente y el ámbito correspondientes. Para una copia manual, retira únicamente `trace-style/` del destino elegido.
