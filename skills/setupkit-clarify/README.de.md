# SetupKit Clarify

Autor: **[Eugene Tsarkov](https://www.linkedin.com/in/etsarkov/)** · [SetupKit](https://github.com/etsarkov/setupkit-ai) · Lizenz: **MIT**

[English](README.md) · [Español](README.es.md) · [Português (Brasil)](README.pt.md) · [日本語](README.ja.md) · Deutsch · [Français](README.fr.md) · [Русский](README.ru.md) · [简体中文](README.zh.md)

Mache aus einer unklaren Anfrage einen brauchbaren Arbeitsauftrag.

## Wann du den Skill nutzt

Nutze Clarify, wenn eine offene Frage Umfang, Kosten, Risiken oder Erfolgskriterien verändern könnte. Der Skill nutzt den vorhandenen Kontext, fragt nur nach wesentlichen Lücken und hört auf, sobald genügend Informationen zum Fortfahren vorliegen.

Das Ergebnis hält den geklärten Umfang, akzeptierte Annahmen, zurückgestellte Fragen und den nächsten Schritt fest.

## Installation

Lies zuerst die Anweisungen des Skills. Nutze für den ersten Versuch ein neues, leeres Testprojekt. Prüfe vor dem Ausführen des Befehls, ob die Skill-Ordner an den Zielorten und den gemeinsam genutzten Projektpfaden schon existieren; entscheide über jede Aktualisierung gesondert. Siehe die [gemeinsame Installationsanleitung](../../INSTALL.de.md).

```bash
npx skills add etsarkov/setupkit-ai --skill setupkit-clarify
```

Wähle den Zielassistenten und die Installation für dieses Projekt. Prüfe vorausgewählte Optionen, Zielpfade und die abschließende Übersicht, bevor du bestätigst. Manche Assistenten teilen sich .agents/skills; andere Assistenten im Projekt können dort abgelegte Dateien ebenfalls entdecken.

npx lädt das Installationsprogramm herunter und führt es aus. Die gemeinsame Installationsanleitung nennt die geprüften Versionen und Verfahren sowie die Grenzen der Kompatibilität.

## Beispiele

Veranschaulichungen, keine protokollierten Durchläufe. Die Fragen gelten nur, wenn die Antworten im Kontext fehlen.

### Einen Wochenbericht automatisieren

**Beispielanfrage:**

```text
Nutze setupkit-clarify: Unser Wochenbericht kostet mich zu viel Zeit. Hilf mir zu entscheiden, was wir automatisieren sollten.
```

**Mögliche Fragen:**

- Woher stammen die Daten für den Bericht?
- Wer nutzt den Bericht und welche Entscheidung soll er unterstützen?
- Welche Schritte können automatisch laufen und welche brauchen deine Prüfung?

**Beispielhaftes Ergebnis:** Ein abgegrenzter Ablauf mit Eingaben, nützlichem Ergebnis, automatisierten Schritten und menschlichen Prüfpunkten. Dieser Arbeitsauftrag erlaubt weder die Umsetzung noch das Versenden des Berichts.

### Einen Beitrag zur Produkteinführung vorbereiten

**Beispielanfrage:**

```text
Nutze setupkit-clarify: Ich möchte unsere Produkteinführung ankündigen. Hilf mir, den Beitrag zu klären, bevor wir ihn schreiben.
```

**Mögliche Fragen:**

- Wer soll den Beitrag lesen und was sollen diese Personen verstehen?
- Was ist die eine zentrale Aussage, die du vermitteln möchtest?
- Welche Ergebnisse oder Produktaussagen können wir belegen und welche Reaktion wünschst du dir?

**Beispielhaftes Ergebnis:** Ein Inhaltsbriefing mit Leserschaft, Autorenposition, belegten Aussagen und gewünschter Reaktion.

## Grenzen

Die Beispielfragen dienen der Veranschaulichung. Clarify erzwingt keinen festen Fragebogen und fragt nicht erneut nach bereits vorliegenden Antworten. Eine einfache, ausreichend klare Anfrage kann ohne weitere Fragen bearbeitet werden.

Für die Skills gelten weiterhin die Berechtigungen und Freigaberegeln deines Assistenten. Sie gewähren keinen Kontozugriff und erlauben keine Ausgaben, Sendungen, Installationen oder Veröffentlichungen.

Verwende nur Material, das du mit dem gewählten Assistenten teilen darfst. Prüfe dessen Regeln zur Datenverarbeitung, bevor du vertrauliche oder personenbezogene Informationen übermittelst.

[SKILL.md](SKILL.md) · [SetupKit Skills](../README.de.md)

## Lizenz und Herkunft

[MIT](../LICENSE). Copyright (c) 2026 Eugene Tsarkov. Mit Unterstützung von OpenAI Codex entwickelt.

Die [Herkunft](../PROVENANCE.md) dokumentiert die Entwicklung und bekannte verwandte Arbeiten. Die Autorenangabe bezieht sich auf diese gepflegten Implementierungen; sie beansprucht nicht die Erfindung allgemeiner Frage- oder Faktenprüfungsmethoden.

Autorenname, SetupKit-Link, MIT-Kennung und vollständiger Lizenztext bleiben auch in jeder SKILL.md erhalten und begleiten daher eine einzeln kopierte Datei.

Englisch ist die maßgebliche Quelle. Die README-Übersetzungen beschreiben dieselben Skills; jeder Skill hat eine einzige englische SKILL.md.
