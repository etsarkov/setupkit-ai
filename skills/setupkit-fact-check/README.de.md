# SetupKit Fact Check

Autor: **[Eugene Tsarkov](https://www.linkedin.com/in/etsarkov/)** · [SetupKit](https://github.com/etsarkov/setupkit-ai) · Lizenz: **MIT**

[English](README.md) · [Español](README.es.md) · [Português (Brasil)](README.pt.md) · [日本語](README.ja.md) · Deutsch · [Français](README.fr.md) · [Русский](README.ru.md) · [简体中文](README.zh.md)

Prüfe Aussagen und Belege vor der Veröffentlichung.

## Wann du den Skill nutzt

Nutze Fact Check, wenn ein öffentlicher Text zur Faktenprüfung bereit ist oder du ausdrücklich eine Aussage überprüfen möchtest. Der Skill unterscheidet Fakten, persönliche Erfahrungen, Meinungen und Hypothesen, prüft verfügbare Belege und liefert eine kompakte Übersicht der Aussagen.

Die Entscheidung lautet PASS, PASS WITH EDITS oder BLOCK. Nicht belegte tragende Aussagen oder ungeklärte wesentliche Anforderungen an Medien führen zu BLOCK.

## Installation

Lies zuerst die Anweisungen des Skills. Nutze für den ersten Versuch ein neues, leeres Testprojekt. Prüfe vor dem Ausführen des Befehls, ob die Skill-Ordner an den Zielorten und den gemeinsam genutzten Projektpfaden schon existieren; entscheide über jede Aktualisierung gesondert. Siehe die [gemeinsame Installationsanleitung](../../INSTALL.de.md).

```bash
npx skills add etsarkov/setupkit-ai --skill setupkit-fact-check
```

Wähle den Zielassistenten und die Installation für dieses Projekt. Prüfe vorausgewählte Optionen, Zielpfade und die abschließende Übersicht, bevor du bestätigst. Manche Assistenten teilen sich .agents/skills; andere Assistenten im Projekt können dort abgelegte Dateien ebenfalls entdecken.

npx lädt das Installationsprogramm herunter und führt es aus. Die gemeinsame Installationsanleitung nennt die geprüften Versionen und Verfahren sowie die Grenzen der Kompatibilität.

## Beispiele

Fiktive Quellenauszüge und Daten, keine Aussagen über reale Unternehmen, gemessene Ergebnisse oder Bildrechte.

### Die Bedeutung eines Zitats bewahren

**Zu prüfendes Material:**

```text
Nutze setupkit-fact-check. Fiktiver Quellenauszug: „Wir erwägen einen Start im Juni.“ Entwurf: „Das Unternehmen hat das Produkt eingeführt.“
```

**Beispielhaftes Ergebnis:** Erkennt, dass aus einem möglichen künftigen Start ein abgeschlossenes Ereignis wurde. Ersetzt die Aussage durch eine quellentreue Zuordnung wie „Das Unternehmen erklärt, dass es einen Start im Juni erwägt.“ Prüft jedes endgültige Zitat anhand der bereitgestellten Quelle.

### Prozentangaben prüfen

**Zu prüfendes Material:**

```text
Nutze setupkit-fact-check. Fiktive bereitgestellte Daten: vorher 10 Conversions bei 100 Besuchen, danach 12 bei 100. Entwurf: „Die Conversion-Rate stieg um 20 Prozentpunkte.“
```

**Beispielhaftes Ergebnis:** Korrigiert zu „Die Conversion-Rate stieg von 10% auf 12%: um 2 Prozentpunkte oder relativ um 20%.“ PASS WITH EDITS für dieses Rechenbeispiel nach Prüfung der Korrektur; die Zahlen belegen weder eine reale Messung noch statistische Signifikanz oder Kausalität.

### Die Herkunft eines Fotos prüfen

**Zu prüfendes Material:**

```text
Nutze setupkit-fact-check. Ein Beitrag enthält ein im Internet gefundenes Foto. Urheber, Originalquelle und Erlaubnis für diese Nutzung sind unbekannt.
```

**Beispielhaftes Ergebnis:** Erfasst die fehlende Herkunft und Nutzungserlaubnis. BLOCK, solange wesentliche anwendbare Medienanforderungen ungeklärt bleiben. Fordert Quelle und Erlaubnis an oder ersetzt das Bild durch Material, dessen vorgesehene Nutzung belegt ist.

## Grenzen

Die Prüfung hängt von den Quellen und Werkzeugen ab, auf die dein Assistent zugreifen kann. Zeitabhängige Fakten müssen aktuell überprüft werden. PASS bewertet den geprüften Wortlaut und die Belege; es erlaubt keine Veröffentlichung und ersetzt bei Bedarf keine professionelle Beratung.

Für die Skills gelten weiterhin die Berechtigungen und Freigaberegeln deines Assistenten. Sie gewähren keinen Kontozugriff und erlauben keine Ausgaben, Sendungen, Installationen oder Veröffentlichungen.

Verwende nur Material, das du mit dem gewählten Assistenten teilen darfst. Prüfe dessen Regeln zur Datenverarbeitung, bevor du vertrauliche oder personenbezogene Informationen übermittelst.

[SKILL.md](SKILL.md) · [SetupKit Skills](../README.de.md)

## Lizenz und Herkunft

[MIT](../LICENSE). Copyright (c) 2026 Eugene Tsarkov. Mit Unterstützung von OpenAI Codex entwickelt.

Die [Herkunft](../PROVENANCE.md) dokumentiert die Entwicklung und bekannte verwandte Arbeiten. Die Autorenangabe bezieht sich auf diese gepflegten Implementierungen; sie beansprucht nicht die Erfindung allgemeiner Frage- oder Faktenprüfungsmethoden.

Autorenname, SetupKit-Link, MIT-Kennung und vollständiger Lizenztext bleiben auch in jeder SKILL.md erhalten und begleiten daher eine einzeln kopierte Datei.

Englisch ist die maßgebliche Quelle. Die README-Übersetzungen beschreiben dieselben Skills; jeder Skill hat eine einzige englische SKILL.md.
