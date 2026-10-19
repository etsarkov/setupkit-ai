# SetupKit

[English](README.md) · Español · [Português (Brasil)](README.pt.md) · [日本語](README.ja.md) · [Deutsch](README.de.md) · [Français](README.fr.md) · [Русский](README.ru.md) · [简体中文](README.zh.md)

Ayuda a tu IA a entender cómo trabajas. Una guía gratuita te ayuda a definir reglas de trabajo y avanzar en una tarea real en tu propio chat de IA.

## Cómo empezar

1. Copia el [prompt de inicio](START_PROMPT.txt).
2. Pégalo en tu chat de IA y envíalo. Pide que la conversación sea en español.
3. Responde a las preguntas pertinentes y elige una tarea para trabajar juntos.

Puedes empezar en tu chat actual. Dile a tu asistente qué herramienta usas y cómo la utilizas. Si una tarea requiere acceso adicional, comprueba primero qué puede hacer tu chat. Puedes continuar manualmente, dejar ese paso para más adelante o elegir otro modo de trabajo. Instalar una aplicación no garantiza por sí solo las herramientas que necesitas.

## Edición actual

[La guía completa](STARTER.md) corresponde a la edición `0.17.1`, actualizada el `2026-10-19`. Tu asistente debe hacer preguntas pertinentes, explicar por qué importan y reutilizar las respuestas que ya hayas dado.

Si no puede leer la fuente, sigue los [pasos para proporcionar el texto completo](docs/getting-started.md#if-the-guide-cannot-be-read). El contenido que falte debe pedirse, no inventarse. La página [Compatibilidad y límites](docs/compatibility.md) explica qué se ha verificado y qué no. Estos documentos de referencia y la guía original están en inglés.

## Organización y contexto opcionales

Si te resulta útil, también puedes organizar tu espacio de trabajo actual y preparar un pequeño conjunto de archivos revisados sobre ti, tus objetivos y tu trabajo. Empieza con materiales que ya tengas, como un currículum o notas de los proyectos que elijas. Tú decides qué cambios hacer; puedes saltarte preguntas o dejarlas para más adelante.

Cuando retomes el trabajo, aporta tu progreso guardado o el resumen para continuar, para que tu asistente pueda reutilizar las respuestas confirmadas y revisar los pasos pendientes o nuevos que sean relevantes. Los archivos solo se guardan con tu aprobación y con el acceso que realmente tenga tu asistente; crearlos no garantiza memoria ni sincronización automáticas.

## Skills

- [Clarify](skills/setupkit-clarify/README.es.md): plantea preguntas concretas para aclarar una tarea antes de empezar.
- [Fact Check](skills/setupkit-fact-check/README.es.md): revisa las afirmaciones, las pruebas que las respaldan y los requisitos de los recursos multimedia antes de publicar.

Para instalar ambos, lee primero la [guía común de instalación](INSTALL.es.md) y comprueba las carpetas de skills existentes. Para una primera prueba, usa un proyecto de prueba nuevo y vacío.

```bash
npx skills add etsarkov/setupkit-ai \
  --skill setupkit-clarify \
  --skill setupkit-fact-check
```

Elige el asistente y el ámbito del proyecto; revisa los destinos antes de confirmar. npx ejecuta el instalador. Consulta [la presentación de los skills](skills/README.es.md) para ver los límites de compatibilidad y las instrucciones de instalación individual.

## Tu trabajo se queda contigo

No necesitas una cuenta de SetupKit. SetupKit no recibe las respuestas que das a tu asistente. Se aplican los costes, permisos y reglas de tratamiento de datos de tu asistente. Pedir un borrador no autoriza a enviar, publicar, instalar, conectar una cuenta ni modificar archivos.

## Autor y reutilización

Creado por [Eugene Tsarkov](https://www.linkedin.com/in/etsarkov/). Un proyecto independiente y gratuito. El texto de la guía está bajo licencia [CC BY 4.0](LICENSE.md), que permite compartirlo y adaptarlo, incluso comercialmente, según sus condiciones. Reconoce la autoría, enlaza la guía original y la licencia e indica los cambios que exija la licencia. Los siete textos de apoyo indicados en LICENSE.md tienen las mismas condiciones CC BY 4.0. La configuración del repositorio queda fuera de esta autorización. No se concede implícitamente ninguna licencia para código, logotipos o materiales de terceros.

## Comentarios e idioma

Consulta las [indicaciones para contribuir](CONTRIBUTING.md) y [cómo informar de problemas de seguridad](SECURITY.md). No publiques chats privados, archivos ni secretos en una incidencia de GitHub. El inglés es la fuente de referencia; la conversación guiada puede desarrollarse en el idioma que elijas. Las versiones del sitio web solo se presentarán como disponibles cuando se haya revisado el recorrido completo en cada idioma.
