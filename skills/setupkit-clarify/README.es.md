# SetupKit Clarify

Autor: **[Eugene Tsarkov](https://www.linkedin.com/in/etsarkov/)** · [SetupKit](https://github.com/etsarkov/setupkit-ai) · Licencia: **MIT**

[English](README.md) · Español · [Português (Brasil)](README.pt.md) · [日本語](README.ja.md) · [Deutsch](README.de.md) · [Français](README.fr.md) · [Русский](README.ru.md) · [简体中文](README.zh.md)

Convierte una petición poco clara en un encargo bien definido.

## Cuándo usarlo

Usa Clarify cuando una pregunta sin resolver pueda cambiar el alcance, el coste, el riesgo o la definición de éxito. Aprovecha el contexto disponible, pregunta solo por las lagunas relevantes y se detiene cuando hay información suficiente para continuar.

El resultado recoge el alcance acordado, los supuestos aceptados, las preguntas aplazadas y el siguiente paso.

## Instalación

Lee primero las instrucciones del skill. Para una primera prueba, usa un proyecto de prueba nuevo y vacío. Antes de ejecutar el comando, comprueba si ya existen carpetas del skill en los destinos y las ubicaciones compartidas del proyecto; decide cualquier actualización por separado. Consulta la [guía común de instalación](../../INSTALL.es.md).

```bash
npx skills add etsarkov/setupkit-ai --skill setupkit-clarify
```

Elige el asistente de destino y el ámbito del proyecto. Revisa las opciones preseleccionadas, los destinos y el resumen final antes de confirmar. Algunos asistentes comparten .agents/skills; otros asistentes del proyecto pueden descubrir los archivos guardados allí.

npx descarga y ejecuta el instalador. La guía común de instalación detalla las versiones y modalidades probadas y los límites de compatibilidad.

## Ejemplos

Ilustraciones, no ejecuciones registradas. Las preguntas solo se aplican cuando las respuestas faltan en el contexto.

### Automatizar un informe semanal

**Petición de ejemplo:**

```text
Usa setupkit-clarify: dedico demasiado tiempo a nuestro informe semanal. Ayúdame a decidir qué automatizar.
```

**Posibles preguntas:**

- ¿De dónde proceden los datos del informe?
- ¿Quién usa el informe y qué decisión debería ayudarle a tomar?
- ¿Qué pasos pueden ejecutarse automáticamente y cuáles necesitan tu revisión?

**Resultado ilustrativo:** Un flujo acotado: entradas, resultado útil, pasos automáticos y puntos de revisión humana. Este encargo no autoriza la implementación ni el envío del informe.

### Definir un post de lanzamiento

**Petición de ejemplo:**

```text
Usa setupkit-clarify: quiero anunciar el lanzamiento de nuestro producto. Ayúdame a definir el post antes de escribirlo.
```

**Posibles preguntas:**

- ¿Quién debería leerlo y qué debería entender?
- ¿Cuál es la idea principal que quieres transmitir?
- ¿Qué resultados o afirmaciones del producto podemos respaldar y qué respuesta esperas?

**Resultado ilustrativo:** Un encargo editorial con el lector, la idea del autor, las afirmaciones respaldadas y la respuesta deseada.

## Límites

Las preguntas de ejemplo son ilustrativas. Clarify no impone un cuestionario fijo ni vuelve a pedir respuestas ya disponibles. Una petición sencilla y bien definida puede avanzar sin más preguntas.

Los skills siguen sujetos a los permisos y las reglas de aprobación de tu asistente. No conceden acceso a cuentas ni autorizan gastos, envíos, instalaciones o publicaciones.

Comparte con el asistente elegido solo material que tengas derecho a compartir. Revisa sus condiciones de tratamiento de datos antes de aportar información confidencial o personal.

[SKILL.md](SKILL.md) · [SetupKit Skills](../README.es.md)

## Licencia y procedencia

[MIT](../LICENSE). Copyright (c) 2026 Eugene Tsarkov. Desarrollados con la asistencia de OpenAI Codex.

Consulta la [procedencia](../PROVENANCE.md) para conocer la historia del desarrollo y los trabajos relacionados conocidos. La atribución cubre estas implementaciones mantenidas; no reivindica la invención de los métodos generales de preguntas o verificación de hechos.

El nombre del autor, el enlace a SetupKit, el identificador MIT y el texto completo de la licencia también permanecen en cada SKILL.md, de modo que acompañan a una copia independiente.

El inglés es la fuente de referencia. Las traducciones de README describen los mismos skills; cada skill tiene un único SKILL.md en inglés.
