# SetupKit Skills

Autor: **[Eugene Tsarkov](https://www.linkedin.com/in/etsarkov/)** · [SetupKit](https://github.com/etsarkov/setupkit-ai) · Lizenz: **MIT**

[English](README.md) · [Español](README.es.md) · [Português (Brasil)](README.pt.md) · [日本語](README.ja.md) · Deutsch · [Français](README.fr.md) · [Русский](README.ru.md) · [简体中文](README.zh.md)

Kläre die Aufgabe vor der Arbeit. Prüfe die Belege vor der Veröffentlichung.

## Wähle einen Skill

| Deine Situation | Skill | Dein Ergebnis |
|---|---|---|
| Eine Anfrage enthält Lücken, die die Aufgabe verändern könnten | [Clarify](setupkit-clarify/README.de.md) | Gezielte Fragen und ein klarerer Umfang |
| Ein öffentlicher Text oder eine Aussage braucht eine Faktenprüfung | [Fact Check](setupkit-fact-check/README.de.md) | Eine Aussagenübersicht, Beleglücken und eine Prüfentscheidung |

Jede Skill-Seite enthält die ausgewählten Beispielszenarien und einen Link zur vollständigen SKILL.md.

## Installation

Lies zuerst die Anweisungen des Skills. Nutze für den ersten Versuch ein neues, leeres Testprojekt. Prüfe vor dem Ausführen des Befehls, ob die Skill-Ordner an den Zielorten und den gemeinsam genutzten Projektpfaden schon existieren; entscheide über jede Aktualisierung gesondert. Siehe die [gemeinsame Installationsanleitung](../INSTALL.de.md).

```bash
npx skills add etsarkov/setupkit-ai \
  --skill setupkit-clarify \
  --skill setupkit-fact-check
```

Wähle den Zielassistenten und die Installation für dieses Projekt. Prüfe vorausgewählte Optionen, Zielpfade und die abschließende Übersicht, bevor du bestätigst. Manche Assistenten teilen sich .agents/skills; andere Assistenten im Projekt können dort abgelegte Dateien ebenfalls entdecken.

npx lädt das Installationsprogramm herunter und führt es aus. Die gemeinsame Installationsanleitung nennt die geprüften Versionen und Verfahren sowie die Grenzen der Kompatibilität.

## Skills verwenden

Verwende setupkit-clarify oder setupkit-fact-check, nachdem dein Assistent den Skill geladen hat. Erkennung, Aufruf, Quellenzugriff und Werkzeugberechtigungen hängen vom Host ab; ein unterstütztes Installationsziel belegt kein identisches Verhalten in verschiedenen Assistenten.

Fact Check kann auf einen redaktionellen Schritt wie einen Humanizer folgen. Dieses Paket setzt keinen Humanizer voraus, enthält keinen und installiert keinen.

Für die Skills gelten weiterhin die Berechtigungen und Freigaberegeln deines Assistenten. Sie gewähren keinen Kontozugriff und erlauben keine Ausgaben, Sendungen, Installationen oder Veröffentlichungen.

Verwende nur Material, das du mit dem gewählten Assistenten teilen darfst. Prüfe dessen Regeln zur Datenverarbeitung, bevor du vertrauliche oder personenbezogene Informationen übermittelst.

## Lizenz und Herkunft

[MIT](LICENSE). Copyright (c) 2026 Eugene Tsarkov. Mit Unterstützung von OpenAI Codex entwickelt.

Die [Herkunft](PROVENANCE.md) dokumentiert die Entwicklung und bekannte verwandte Arbeiten. Die Autorenangabe bezieht sich auf diese gepflegten Implementierungen; sie beansprucht nicht die Erfindung allgemeiner Frage- oder Faktenprüfungsmethoden.

Autorenname, SetupKit-Link, MIT-Kennung und vollständiger Lizenztext bleiben auch in jeder SKILL.md erhalten und begleiten daher eine einzeln kopierte Datei.

Englisch ist die maßgebliche Quelle. Die README-Übersetzungen beschreiben dieselben Skills; jeder Skill hat eine einzige englische SKILL.md.
