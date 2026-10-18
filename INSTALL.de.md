# SetupKit-Skills installieren

[English](INSTALL.md) · [Español](INSTALL.es.md) · [Português (Brasil)](INSTALL.pt.md) · [日本語](INSTALL.ja.md) · Deutsch · [Français](INSTALL.fr.md) · [Русский](INSTALL.ru.md) · [简体中文](INSTALL.zh.md)

Mit [Clarify](skills/setupkit-clarify/README.de.md) wird aus einer unklaren Anfrage ein Arbeitsauftrag. [Fact Check](skills/setupkit-fact-check/README.de.md) prüft Aussagen und Belege. Lies vor der Installation die ausgewählte SKILL.md.

Diese Anleitung behandelt die Installation in einem Projekt. Verwende für den ersten Versuch ein neues, leeres Testprojekt. Eine Kontoverbindung, ein API-Schlüssel oder eine kostenpflichtige Modell-API gehören nicht zu diesen Schritten. Die Kosten und Berechtigungen deines Assistenten gelten weiterhin.

## Vor der Installation

1. Wähle einen oder beide Skills und den gewünschten Assistenten.
2. Prüfe dessen Zielordner und die gemeinsamen Projektordner `.agents/skills/setupkit-clarify` und `.agents/skills/setupkit-fact-check`. Ist ein gleichnamiger Ordner vorhanden, halte an und entscheide gesondert über das Update. Überschreibwarnungen erfassen möglicherweise nicht alle gemeinsamen Ziele.
3. Wähle den Projektumfang. Mehrere Assistenten verwenden `.agents/skills`; andere Assistenten im Projekt können die dort abgelegten Dateien ebenfalls entdecken.

## Skills CLI

Die [Originaldokumentation der Skills CLI](https://github.com/vercel-labs/skills/blob/13e4063a1cf913f5606d57d42ab83a86f5001e04/README.md) nennt unter anderem Codex, Claude Code, Cursor, Gemini CLI, OpenCode, Windsurf und GitHub Copilot. Das Manifest des untersuchten Repositorys verlangt Node.js 22.20.0 oder neuer. Verwende die Laufzeit, die deine gewählte Version voraussetzt.

Öffne ein Terminal im vorgesehenen Projektordner. `npx` lädt das Installationsprogramm herunter und führt es aus; prüfe vorher das Originalpaket.

Beide Skills:

```bash
npx skills add etsarkov/setupkit-ai \
  --skill setupkit-clarify \
  --skill setupkit-fact-check
```

Nur Clarify:

```bash
npx skills add etsarkov/setupkit-ai --skill setupkit-clarify
```

Nur Fact Check:

```bash
npx skills add etsarkov/setupkit-ai --skill setupkit-fact-check
```

Wähle den Assistenten und den Projektumfang. Prüfe alle vorausgewählten Optionen, Pfade und die abschließende Übersicht vor der Bestätigung. Brich ab, wenn ein vorhandener Skill ohne gesondert vereinbartes Update ersetzt würde. Diese Beispiele lassen die Bestätigung aktiviert.

Um ein Ziel anzugeben, ergänze dessen Kennung, etwa `--agent cursor`, `--agent gemini-cli` oder `--agent opencode`. Die [Originaltabelle](https://github.com/vercel-labs/skills/blob/13e4063a1cf913f5606d57d42ab83a86f5001e04/README.md#supported-agents) nennt weitere Kennungen und Ziele.

Beispielhafte Projektziele im untersuchten Installationscode:

| Ziel des Installers | Projektverzeichnis |
|---|---|
| Codex, Cursor, Gemini CLI, OpenCode, GitHub Copilot | `.agents/skills/` |
| Claude Code | `.claude/skills/` |
| Windsurf | `.windsurf/skills/` |

Die Tabelle beschreibt die Zielzuordnung des Installers. Sie belegt keinen SetupKit-Test in jedem Assistenten. Die obigen Befehle legen keine Version fest; eine spätere Ausgabe kann vom untersuchten Quelltext abweichen.

## Alternative für Codex

Wenn skill-installer in deiner Codex-Umgebung verfügbar ist, öffne das Zielprojekt und sende:

```text
$skill-installer Installiere SetupKit Clarify und SetupKit Fact Check aus:
https://github.com/etsarkov/setupkit-ai/tree/main/skills/setupkit-clarify
https://github.com/etsarkov/setupkit-ai/tree/main/skills/setupkit-fact-check
Installiere nur für dieses Projekt. Lasse vorhandene Skills unverändert. Ist eine Projektinstallation nicht möglich, erkläre die Einschränkung, ohne Dateien zu ändern.
```

Für einen einzelnen Skill gib nur dessen Namen und URL an. Die Anfrage beschreibt den gewünschten Umfang; bestätige das tatsächliche Ziel, bevor du Dateiänderungen zulässt. Bietet der Installer nur eine benutzerweite Installation an, halte an und wähle eine geeignete Projektmethode. Siehe die [offizielle Codex-Anleitung](https://learn.chatgpt.com/docs/build-skills).

## Manuelle Installation und Claude Code

Lade das Repository-Archiv von GitHub herunter und entpacke es außerhalb der Ordner, in denen dein Assistent Skills entdeckt. Lies die ausgewählten SKILL.md-Dateien. Kopiere nur die gewählten Ordner aus `skills/` in das vom Assistenten dokumentierte Projektverzeichnis und behalte Namen und Inhalt bei. Prüfe zuerst spezifische und gemeinsame Ziele; ersetze keinen vorhandenen Ordner ohne gesonderte Updateentscheidung.

Codex im Projekt:

```text
.agents/skills/setupkit-clarify/SKILL.md
.agents/skills/setupkit-fact-check/SKILL.md
```

Claude Code im Projekt:

```text
.claude/skills/setupkit-clarify/SKILL.md
.claude/skills/setupkit-fact-check/SKILL.md
```

Für einen einzelnen Skill genügt dessen Ordner. Behalte mitkopierte README-Übersetzungen und alle Autoren- und Lizenzhinweise in SKILL.md. Beginne in Claude Code nach der Erkennung eine Nachricht mit `/setupkit-clarify` oder `/setupkit-fact-check`. Siehe die [offizielle Claude-Code-Dokumentation](https://code.claude.com/docs/en/skills).

Prüfe bei anderen Assistenten den offiziellen Erkennungspfad und die Aufrufmethode. Halte je Skill eine Kopie der Anweisungen vor; eine Pfadanpassung erfordert keine Übersetzung oder Umschreibung von SKILL.md.

## Ergebnis prüfen

1. Prüfe in der Skill-Liste oder Erkennungsansicht, ob die gewählten Kennungen im Projektumfang erscheinen. Starte bei Bedarf eine neue Aufgabe oder den Assistenten neu.
2. Probiere ein Beispiel aus [Clarify](skills/setupkit-clarify/README.de.md) oder [Fact Check](skills/setupkit-fact-check/README.de.md). Prüfe, ob der gewünschte Skill tatsächlich geladen wurde.
3. Vergleiche das Ergebnis mit dem Zweck des Beispiels. Clarify soll nur nach fehlenden wesentlichen Informationen fragen. Fact Check soll Beleglücken und eine passende Entscheidung zeigen, bei Bedarf einschließlich BLOCK.

## Kompatibilität und Berechtigungen

Dateiaufbau und Befehlsmuster wurden anhand gespeicherter Originaldokumentation und Quelltexte geprüft. Der Testumfang konkreter Versionen steht unten; für die anderen aufgeführten Assistenten liefern diese Tests keinen Nachweis eines nativen SetupKit-Aufrufs. Ein Installerziel belegt keine identische Auslösung, Werkzeuge, Quellenzugriffe, Berechtigungen oder Prüfqualität.

Für zeitabhängige Aussagen benötigt Fact Check Zugriff auf aktuelle Quellen. Fehlen wesentliche Belege, bleibt die Aussage ungeklärt. Das Paket enthält und installiert keinen Humanizer; Fact Check kann ohne ihn laufen.

Laden, Ausführung und Berechtigungen kontrolliert der Assistent. Ein Skill oder eine PASS-Entscheidung erlaubt weder Veröffentlichung noch Versand, Ausgaben, Installation oder Kontoverbindung. Teile nur Materialien, die du dem gewählten Assistenten geben darfst, und prüfe seine Bedingungen zur Datenverarbeitung.

## Geprüfter Testmodus

Am 18. Oktober 2026 wurde die Projektinstallation durch Kopieren mit npm/npx 11.6.2 und Skills CLI 1.7.2 in neuen macOS-Projekten geprüft. Beide Skills wurden in Codex 0.163.0-alpha.10.2 (gpt-6.1-sol) und OpenCode 2.0.22 (gpt-5.6-sol) ausdrücklich aufgerufen, mit einem vorhandenen ChatGPT-Abonnement. Die synthetischen Tests behandelten unvollständige/vollständige Aufträge sowie unbelegte/korrekte Aussagen.

Im Test waren npm-Lebenszyklusskripte deaktiviert.

Geprüfter nichtinteraktiver Kopierbefehl für Codex:

```bash
npx --yes skills@1.7.2 add etsarkov/setupkit-ai --skill setupkit-clarify --skill setupkit-fact-check --agent codex --copy --yes --json
```

Ersetze für das geprüfte OpenCode-Ziel `codex` durch `opencode`. Nutze diesen Modus ohne Bestätigungen nur, nachdem du Skills, Projektumfang und sämtliche Zielordner selbst geprüft hast. Die vorherigen Beispiele behalten die Bestätigung bei.

Diese Tests prüfen keine interaktiven Vorauswahlen, keinen standardmäßigen Symlink-Modus, keine globale Installation, automatische Auslösung, Live-Web-Faktenprüfung oder anderen Assistentenversionen. Sie garantieren keine Ausgabequalität für jede Aufgabe.

## Autor und Lizenz

Autor und Maintainer: [Eugene Tsarkov](https://www.linkedin.com/in/etsarkov/). Teil von [SetupKit](https://github.com/etsarkov/setupkit-ai), mit Unterstützung von OpenAI Codex entwickelt. Diese beiden Skills verwenden die [MIT-Lizenz](skills/LICENSE); siehe [Herkunft](skills/PROVENANCE.md). Der Hauptleitfaden von SetupKit hat eine eigene Lizenz, beschrieben in der [Repository-README](README.md#author-and-reuse).

Englisch ist die maßgebliche Fassung. Diese Übersetzung behält Anweisungen, Kennungen und Grenzen bei.
