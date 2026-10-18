# SetupKit Skills

Autor: **[Eugene Tsarkov](https://www.linkedin.com/in/etsarkov/)** · [SetupKit](https://github.com/etsarkov/setupkit-ai) · Licencia: **MIT**

[English](README.md) · Español · [Português (Brasil)](README.pt.md) · [日本語](README.ja.md) · [Deutsch](README.de.md) · [Français](README.fr.md) · [Русский](README.ru.md) · [简体中文](README.zh.md)

Aclara la tarea antes de trabajar. Revisa las pruebas antes de publicar.

## Elige un skill

| Tu situación | Skill | Qué obtienes |
|---|---|---|
| Una petición tiene lagunas que podrían cambiar la tarea | [Clarify](setupkit-clarify/README.es.md) | Preguntas concretas y un alcance más claro |
| Un texto público o una afirmación necesita revisión factual | [Fact Check](setupkit-fact-check/README.es.md) | Un registro de afirmaciones, lagunas de evidencia y una decisión de revisión |

La página de cada skill incluye los escenarios de ejemplo seleccionados y un enlace a su SKILL.md completo.

## Instalación

Lee primero las instrucciones del skill. Para una primera prueba, usa un proyecto de prueba nuevo y vacío. Antes de ejecutar el comando, comprueba si ya existen carpetas del skill en los destinos y las ubicaciones compartidas del proyecto; decide cualquier actualización por separado. Consulta la [guía común de instalación](../INSTALL.es.md).

```bash
npx skills add etsarkov/setupkit-ai \
  --skill setupkit-clarify \
  --skill setupkit-fact-check
```

Elige el asistente de destino y el ámbito del proyecto. Revisa las opciones preseleccionadas, los destinos y el resumen final antes de confirmar. Algunos asistentes comparten .agents/skills; otros asistentes del proyecto pueden descubrir los archivos guardados allí.

npx descarga y ejecuta el instalador. La guía común de instalación detalla las versiones y modalidades probadas y los límites de compatibilidad.

## Uso de los skills

Cuando tu asistente haya cargado el skill, usa el identificador setupkit-clarify o setupkit-fact-check. El descubrimiento, la invocación, el acceso a fuentes y los permisos de las herramientas dependen del entorno; que un instalador admita un destino no demuestra que todos los asistentes se comporten igual.

Fact Check puede seguir a una revisión editorial, como un humanizer. Un humanizer no es obligatorio; este paquete no lo incluye ni lo instala.

Los skills siguen sujetos a los permisos y las reglas de aprobación de tu asistente. No conceden acceso a cuentas ni autorizan gastos, envíos, instalaciones o publicaciones.

Comparte con el asistente elegido solo material que tengas derecho a compartir. Revisa sus condiciones de tratamiento de datos antes de aportar información confidencial o personal.

## Licencia y procedencia

[MIT](LICENSE). Copyright (c) 2026 Eugene Tsarkov. Desarrollados con la asistencia de OpenAI Codex.

Consulta la [procedencia](PROVENANCE.md) para conocer la historia del desarrollo y los trabajos relacionados conocidos. La atribución cubre estas implementaciones mantenidas; no reivindica la invención de los métodos generales de preguntas o verificación de hechos.

El nombre del autor, el enlace a SetupKit, el identificador MIT y el texto completo de la licencia también permanecen en cada SKILL.md, de modo que acompañan a una copia independiente.

El inglés es la fuente de referencia. Las traducciones de README describen los mismos skills; cada skill tiene un único SKILL.md en inglés.
