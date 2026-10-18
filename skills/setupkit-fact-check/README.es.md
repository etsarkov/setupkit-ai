# SetupKit Fact Check

Autor: **[Eugene Tsarkov](https://www.linkedin.com/in/etsarkov/)** · [SetupKit](https://github.com/etsarkov/setupkit-ai) · Licencia: **MIT**

[English](README.md) · Español · [Português (Brasil)](README.pt.md) · [日本語](README.ja.md) · [Deutsch](README.de.md) · [Français](README.fr.md) · [Русский](README.ru.md) · [简体中文](README.zh.md)

Revisa las afirmaciones y sus pruebas antes de publicar.

## Cuándo usarlo

Usa Fact Check cuando un texto público esté listo para la revisión factual o cuando quieras verificar una afirmación expresamente. Distingue hechos, experiencia personal, opiniones e hipótesis, comprueba las pruebas disponibles y devuelve un registro breve de afirmaciones.

La decisión es PASS, PASS WITH EDITS o BLOCK. Las afirmaciones esenciales sin respaldo o los requisitos importantes de los recursos multimedia que sigan sin resolverse llevan a BLOCK.

## Instalación

Lee primero las instrucciones del skill. Para una primera prueba, usa un proyecto de prueba nuevo y vacío. Antes de ejecutar el comando, comprueba si ya existen carpetas del skill en los destinos y las ubicaciones compartidas del proyecto; decide cualquier actualización por separado. Consulta la [guía común de instalación](../../INSTALL.es.md).

```bash
npx skills add etsarkov/setupkit-ai --skill setupkit-fact-check
```

Elige el asistente de destino y el ámbito del proyecto. Revisa las opciones preseleccionadas, los destinos y el resumen final antes de confirmar. Algunos asistentes comparten .agents/skills; otros asistentes del proyecto pueden descubrir los archivos guardados allí.

npx descarga y ejecuta el instalador. La guía común de instalación detalla las versiones y modalidades probadas y los límites de compatibilidad.

## Ejemplos

Fragmentos y datos ficticios, no afirmaciones sobre empresas reales, resultados medidos ni derechos sobre imágenes.

### Conservar el sentido de una cita

**Material que se revisa:**

```text
Usa setupkit-fact-check. Fragmento ficticio de la fuente: «Estamos considerando un lanzamiento en junio». Borrador: «La empresa ha lanzado el producto».
```

**Resultado ilustrativo:** Detecta que un posible lanzamiento futuro se convirtió en un hecho consumado. Sustituye la afirmación por una atribución fiel, como «La empresa dice que está considerando un lanzamiento en junio». Comprueba cualquier cita final con la fuente aportada.

### Comprobar porcentajes

**Material que se revisa:**

```text
Usa setupkit-fact-check. Datos ficticios aportados: antes, 10 conversiones de 100 visitas; después, 12 de 100. Borrador: «La conversión aumentó 20 puntos porcentuales».
```

**Resultado ilustrativo:** Corrige a «La conversión pasó del 10% al 12%: 2 puntos porcentuales o un aumento relativo del 20%». PASS WITH EDITS para este ejemplo aritmético tras comprobar la corrección; las cifras no acreditan una medición real, significación estadística ni causalidad.

### Comprobar la procedencia de una foto

**Material que se revisa:**

```text
Usa setupkit-fact-check. Un post incluye una foto encontrada en internet. Se desconocen su autor, la fuente original y el permiso para este uso.
```

**Resultado ilustrativo:** Registra la procedencia y el permiso que faltan. BLOCK mientras sigan sin resolverse los requisitos importantes aplicables al recurso multimedia. Pide la fuente y el permiso, o sustituye la imagen por otra cuyo uso previsto esté respaldado.

## Límites

La revisión depende de las fuentes y herramientas disponibles para tu asistente. Los datos que pueden cambiar necesitan una comprobación actual. PASS evalúa el texto y las pruebas revisados; no autoriza la publicación ni sustituye el asesoramiento profesional cuando sea necesario.

Los skills siguen sujetos a los permisos y las reglas de aprobación de tu asistente. No conceden acceso a cuentas ni autorizan gastos, envíos, instalaciones o publicaciones.

Comparte con el asistente elegido solo material que tengas derecho a compartir. Revisa sus condiciones de tratamiento de datos antes de aportar información confidencial o personal.

[SKILL.md](SKILL.md) · [SetupKit Skills](../README.es.md)

## Licencia y procedencia

[MIT](../LICENSE). Copyright (c) 2026 Eugene Tsarkov. Desarrollados con la asistencia de OpenAI Codex.

Consulta la [procedencia](../PROVENANCE.md) para conocer la historia del desarrollo y los trabajos relacionados conocidos. La atribución cubre estas implementaciones mantenidas; no reivindica la invención de los métodos generales de preguntas o verificación de hechos.

El nombre del autor, el enlace a SetupKit, el identificador MIT y el texto completo de la licencia también permanecen en cada SKILL.md, de modo que acompañan a una copia independiente.

El inglés es la fuente de referencia. Las traducciones de README describen los mismos skills; cada skill tiene un único SKILL.md en inglés.
