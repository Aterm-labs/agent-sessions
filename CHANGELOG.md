# Changelog

Todas las novedades destacables de la extensión **Agent Sessions**.

## [1.3.0]

### Nuevo

- **Gráfico de memoria (Pro)** — nueva vista que mapea la jerarquía de memoria
  del proveedor (global del usuario, del proyecto, local y el directorio de
  memoria por-proyecto) con sus `@imports` y enlaces `[[…]]`:
  - **Árbol jerárquico** por capas (formas/colores por capa) + **vista de
    secciones** con índice plegable que filtra.
  - **Vista previa estructurada** de cada `.md` (Secciones / Texto crudo) con
    *callouts* (`Why:`/`How:`/`IMPORTANT:`), tarjetas por sección y frontmatter
    aparte; al pasar el ratón, **descripción de la función real** de cada fichero.
  - **Crear / añadir / nota / borrar**: el **agente redacta** el contenido y la
    extensión lo **guarda** (con tu confirmación); nunca se edita en silencio ni
    se saltan las comprobaciones de Claude.
  - Botón **«Gráfico de memoria»** en cada proyecto + **auto-refresco** al
    cambiar los ficheros.
- **Estado del servicio como badge** junto al nombre del proveedor; al pulsarlo
  abre su **página de estado** (Claude, Codex, Gemini, OpenCode).
- **Comandos del proyecto**:
  - Los **scripts del repo** (npm / Make / justfile / Cargo) pasan a ser **Pro**
    y se **agrupan por lenguaje/intérprete** (Rust · cargo, Python, Node · npm,
    Make, just…). Los **slash-commands del agente** (`.claude/commands`) siguen
    siendo gratis.
  - **Inferencia de argumentos** y **ayuda persistente**: parámetros de `just`
    en línea y **parseo real de `--help`** para CLIs seguros (cargo, python, uv,
    pytest, go, deno…), con selector de flags reales.
  - **Recorre subcarpetas** (meta-repos / monorepos) y funciona sobre **cualquier
    carpeta** (opción «Examinar…»), sin abrirla en el workspace.

### Cambios

- **Quota de uso (5h / 7d) self-contained**: se obtiene del fichero nativo de
  Claude (`rate-limits-cache.json`) o, si falta, del **endpoint oficial de uso de
  Anthropic** con un cache propio (~5 min). **Ya no depende del plugin de terceros
  `claude-hud`.**
- Las **sesiones efímeras de generación de memoria** se **ocultan** por defecto;
  un botón en la barra de filtros las muestra en exclusiva.

## [1.2.5] y anteriores

Ver el historial de releases en GitHub.
