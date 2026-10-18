# Instalar los skills de SetupKit

[English](INSTALL.md) · Español · [Português (Brasil)](INSTALL.pt.md) · [日本語](INSTALL.ja.md) · [Deutsch](INSTALL.de.md) · [Français](INSTALL.fr.md) · [Русский](INSTALL.ru.md) · [简体中文](INSTALL.zh.md)

Elige [Clarify](skills/setupkit-clarify/README.es.md) para convertir una petición poco clara en un encargo definido, o [Fact Check](skills/setupkit-fact-check/README.es.md) para revisar afirmaciones y pruebas. Lee el SKILL.md elegido antes de instalarlo.

Esta guía cubre la instalación en un proyecto. Para la primera prueba, usa un proyecto de prueba nuevo y vacío. Estas instrucciones no conectan cuentas ni requieren una clave o una API de modelos de pago. Siguen aplicándose los costes y permisos de tu asistente.

## Antes de instalar

1. Elige uno o ambos skills y el asistente que usarás.
2. Comprueba las carpetas de destino del asistente y las compartidas `.agents/skills/setupkit-clarify` y `.agents/skills/setupkit-fact-check`. Si ya existe alguna, detente y decide esa actualización por separado. Los avisos de sobrescritura pueden no cubrir todos los destinos compartidos.
3. Elige el ámbito del proyecto. Varios asistentes usan `.agents/skills`; otros asistentes del mismo proyecto podrían descubrir esos archivos.

## Skills CLI

La [documentación original de Skills CLI](https://github.com/vercel-labs/skills/blob/13e4063a1cf913f5606d57d42ab83a86f5001e04/README.md) incluye Codex, Claude Code, Cursor, Gemini CLI, OpenCode, Windsurf y GitHub Copilot. El manifiesto del repositorio inspeccionado requiere Node.js 22.20.0 o posterior. Usa el entorno requerido por la versión que elijas.

Abre una terminal en el proyecto de destino. `npx` descarga y ejecuta el instalador; revisa el paquete original antes de ejecutarlo.

Ambos skills:

```bash
npx skills add etsarkov/setupkit-ai \
  --skill setupkit-clarify \
  --skill setupkit-fact-check
```

Solo Clarify:

```bash
npx skills add etsarkov/setupkit-ai --skill setupkit-clarify
```

Solo Fact Check:

```bash
npx skills add etsarkov/setupkit-ai --skill setupkit-fact-check
```

Elige el asistente y el ámbito del proyecto. Revisa todas las opciones preseleccionadas, las rutas y el resumen final antes de confirmar. Cancela si se sustituiría un skill existente sin haber acordado esa actualización por separado. Estos ejemplos mantienen la confirmación activada.

Para indicar un destino, añade su identificador, por ejemplo `--agent cursor`, `--agent gemini-cli` o `--agent opencode`. La [tabla original de destinos](https://github.com/vercel-labs/skills/blob/13e4063a1cf913f5606d57d42ab83a86f5001e04/README.md#supported-agents) enumera otros identificadores y directorios.

Destinos representativos del código inspeccionado:

| Destino del instalador | Directorio del proyecto |
|---|---|
| Codex, Cursor, Gemini CLI, OpenCode, GitHub Copilot | `.agents/skills/` |
| Claude Code | `.claude/skills/` |
| Windsurf | `.windsurf/skills/` |

Esta tabla describe el enrutamiento del instalador; no demuestra que SetupKit se haya probado en cada asistente. Los comandos anteriores no fijan una versión: una versión posterior puede diferir del código inspeccionado.

## Alternativa para Codex

Si skill-installer está disponible en tu entorno Codex, abre el proyecto de destino y envía:

```text
$skill-installer Instala SetupKit Clarify y SetupKit Fact Check desde:
https://github.com/etsarkov/setupkit-ai/tree/main/skills/setupkit-clarify
https://github.com/etsarkov/setupkit-ai/tree/main/skills/setupkit-fact-check
Instálalos solo para este proyecto. Conserva los skills existentes. Si la instalación en el proyecto no está disponible, explica la limitación sin modificar archivos.
```

Para un solo skill, incluye únicamente su nombre y URL. La petición expresa el ámbito deseado; confirma el destino real antes de permitir cambios. Si solo se ofrece una instalación para todo el usuario, detente y elige un método para el proyecto. Consulta la [guía oficial de Codex](https://learn.chatgpt.com/docs/build-skills).

## Instalación manual y Claude Code

Descarga el archivo del repositorio desde GitHub y extráelo fuera de las carpetas donde el asistente descubre skills. Lee los SKILL.md seleccionados. Copia solo sus carpetas desde `skills/` al directorio del proyecto documentado por tu asistente, conservando los nombres y el contenido. Comprueba tanto el destino como las ubicaciones compartidas; no reemplaces una carpeta sin decidir esa actualización por separado.

Codex, ámbito del proyecto:

```text
.agents/skills/setupkit-clarify/SKILL.md
.agents/skills/setupkit-fact-check/SKILL.md
```

Claude Code, ámbito del proyecto:

```text
.claude/skills/setupkit-clarify/SKILL.md
.claude/skills/setupkit-fact-check/SKILL.md
```

Para instalar un solo skill basta su carpeta. Conserva las traducciones de README que copies y todos los avisos de autoría y licencia de SKILL.md. En Claude Code, una vez descubierto el skill, comienza el mensaje con `/setupkit-clarify` o `/setupkit-fact-check`. Consulta la [documentación oficial de Claude Code](https://code.claude.com/docs/en/skills).

En otros asistentes, comprueba la ruta oficial de descubrimiento y el método de invocación. Mantén una copia de las instrucciones de cada skill; adaptar una ruta no exige traducir ni reescribir SKILL.md.

## Comprueba el resultado

1. Confirma que los identificadores elegidos aparecen en la lista o vista de descubrimiento del asistente con ámbito del proyecto. Inicia una tarea nueva o reinicia el asistente si lo requiere.
2. Prueba uno de los ejemplos de [Clarify](skills/setupkit-clarify/README.es.md) o [Fact Check](skills/setupkit-fact-check/README.es.md). Comprueba que se haya cargado el skill correcto.
3. Compara el resultado con el propósito del ejemplo. Clarify debe preguntar solo por información relevante que falte. Fact Check debe mostrar las carencias de pruebas y una decisión adecuada, incluido BLOCK cuando corresponda.

## Compatibilidad y permisos

La estructura de archivos y los patrones de comandos se contrastaron con documentación y código original capturados. El alcance de las pruebas con versiones concretas se describe abajo; estas pruebas no aportan evidencia de invocación nativa en los demás asistentes enumerados. Un destino del instalador no demuestra igualdad de activación, herramientas, acceso a fuentes, permisos o calidad de revisión.

Fact Check necesita acceso a fuentes actuales para afirmaciones sensibles al tiempo. Si faltan pruebas relevantes, la afirmación queda sin resolver. El paquete no incluye ni instala un humanizer; Fact Check puede funcionar sin uno.

El asistente controla la carga, ejecución y permisos. Un skill o una decisión PASS no autoriza publicar, enviar, gastar, instalar ni conectar cuentas. Comparte únicamente materiales que tengas derecho a compartir con ese asistente y revisa sus condiciones de tratamiento de datos.

## Modalidad de prueba verificada

El 18 de octubre de 2026 se verificó la instalación por copia en proyectos macOS nuevos mediante npm/npx 11.6.2 y Skills CLI 1.7.2. Ambos skills se invocaron explícitamente en Codex 0.163.0-alpha.10.2 (gpt-6.1-sol) y OpenCode 2.0.22 (gpt-5.6-sol), usando una suscripción existente de ChatGPT. Las pruebas sintéticas cubrieron encargos incompletos/completos y afirmaciones sin respaldo/correctas.

El entorno de prueba tenía desactivados los scripts de ciclo de vida de npm.

Comando probado para copiar en Codex sin interacción:

```bash
npx --yes skills@1.7.2 add etsarkov/setupkit-ai --skill setupkit-clarify --skill setupkit-fact-check --agent codex --copy --yes --json
```

Para el destino OpenCode probado, sustituye `codex` por `opencode`. Usa esta modalidad sin confirmaciones solo después de revisar por tu cuenta los skills, el ámbito del proyecto y todas las carpetas de destino. Los ejemplos anteriores mantienen la confirmación.

Estas pruebas no verifican las opciones interactivas predeterminadas, el modo de enlaces simbólicos predeterminado, la instalación global, la activación automática, la comprobación de fuentes web en vivo ni otras versiones de asistentes. No garantizan la calidad del resultado para cualquier tarea.

## Autor y licencia

Autor y responsable de mantenimiento: [Eugene Tsarkov](https://www.linkedin.com/in/etsarkov/). Parte de [SetupKit](https://github.com/etsarkov/setupkit-ai), desarrollado con ayuda de OpenAI Codex. Estos dos skills usan la [licencia MIT](skills/LICENSE); consulta su [procedencia](skills/PROVENANCE.md). La guía principal de SetupKit tiene su propia licencia, descrita en el [README del repositorio](README.md#author-and-reuse).

El inglés es la fuente de referencia. Esta traducción mantiene las mismas instrucciones, identificadores y límites.
