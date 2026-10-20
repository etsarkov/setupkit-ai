# SetupKit

[English](README.md) · [Español](README.es.md) · [Português (Brasil)](README.pt.md) · [日本語](README.ja.md) · Deutsch · [Français](README.fr.md) · [Русский](README.ru.md) · [简体中文](README.zh.md)

Hilf deiner KI zu verstehen, wie du arbeitest. Ein kostenloser Leitfaden hilft dir, Arbeitsregeln festzuhalten und in deinem eigenen KI-Chat an einer echten Aufgabe zu arbeiten.

## So startest du

1. Kopiere den [Start-Prompt](prompts/de.txt).
2. Füge ihn in deinen KI-Chat ein und sende ihn ab. Bitte darum, das Gespräch auf Deutsch zu führen.
3. Beantworte die passenden Fragen und wähle eine Aufgabe, an der ihr gemeinsam arbeitet.

Du kannst in deinem bisherigen Chat anfangen. Sag deinem Assistenten, welches Tool du nutzt und wie du damit arbeitest. Braucht eine Aufgabe zusätzliche Zugriffsrechte, prüfe zuerst, was dein Chat leisten kann. Du kannst manuell weitermachen, den Schritt auf später verschieben oder einen anderen Arbeitsmodus wählen. Die Installation einer App allein garantiert nicht, dass die nötigen Tools verfügbar sind.

## Aktuelle Ausgabe

[Der vollständige Leitfaden](COMPLETE.md) hat die Version `0.19`, aktualisiert am `2026-10-19`. Dein Assistent soll passende Fragen stellen, ihre Bedeutung erklären und bereits gegebene Antworten weiterverwenden.

Kann die Quelle nicht gelesen werden, folge den [Schritten zum Übermitteln des vollständigen Textes](docs/getting-started.md#if-the-guide-cannot-be-read). Fehlende Inhalte müssen angefordert werden; sie dürfen nicht erfunden werden. Die Seite [Kompatibilität und Grenzen](docs/compatibility.md) erklärt, was geprüft wurde und was nicht. Diese Referenzdokumente und der maßgebliche Leitfaden sind auf Englisch.

## Arbeitsbereich und Kontext nach Bedarf

Wenn es dir hilft, kannst du auch deinen bestehenden Arbeitsbereich ordnen und einige geprüfte Dateien über dich, deine Ziele und deine Arbeit zusammenstellen. Beginne mit vorhandenen Unterlagen, etwa einem Lebenslauf oder ausgewählten Projektnotizen. Du entscheidest, welche Änderungen du möchtest; Fragen kannst du überspringen oder auf später verschieben.

Wenn du weitermachst, bring deinen gespeicherten Fortschritt oder deine Zusammenfassung zum Fortsetzen mit. So kann dein Assistent bestätigte Antworten weiterverwenden und relevante offene oder neue Schritte prüfen. Dateien werden nur mit deiner Zustimmung und den tatsächlich verfügbaren Zugriffsrechten deines Assistenten gespeichert. Allein das Anlegen von Dateien garantiert weder automatische Erinnerung noch Synchronisierung.

## Ausgewählte Materialien ordnen — bei Bedarf

Bitte deinen Assistenten, ausgewählte Dateien, Links oder Notizen mit dir zu ordnen. Er kann vorschlagen, zu welchem Projekt ein Material gehört, wo es liegen sollte und welche Inhalte sich für eine Zusammenfassung eignen. Verweise auf die Originale bleiben erhalten. Prüfe den Vorschlag und entscheide, was geändert oder auf später verschoben wird. Dateien werden nur mit deiner Zustimmung und dem nötigen Zugriff gespeichert oder verschoben; andernfalls erhältst du einen Plan zum manuellen Umsetzen. Bringe beim Fortsetzen die geprüfte Übersicht mit, damit sich der Assistent auf neue, geänderte oder offene Einträge konzentrieren kann.

## Skills

- [Clarify](skills/setupkit-clarify/README.de.md): stellt gezielte Fragen, um eine Aufgabe vor Arbeitsbeginn zu klären.
- [Fact Check](skills/setupkit-fact-check/README.de.md): prüft Aussagen, Belege und Anforderungen an Medien vor der Veröffentlichung.

Lies zur Installation beider Skills zuerst die [gemeinsame Installationsanleitung](INSTALL.de.md) und prüfe vorhandene Skill-Ordner. Nutze für den ersten Versuch ein neues, leeres Testprojekt.

```bash
npx skills add etsarkov/setupkit-ai \
  --skill setupkit-clarify \
  --skill setupkit-fact-check
```

Wähle den Assistenten und die Installation für dieses Projekt; prüfe vor der Bestätigung die Zielpfade. npx führt den Installer aus. Die Kompatibilitätsgrenzen und Einzelanleitungen findest du in [der Skill-Übersicht](skills/README.de.md).

## Deine Arbeit bleibt bei dir

Du brauchst kein SetupKit-Konto. SetupKit erhält keine Antworten, die du deinem Assistenten gibst. Es gelten die Kosten, Berechtigungen und Regeln zur Datenverarbeitung deines Assistenten. Die Bitte um einen Entwurf ist keine Erlaubnis zum Senden, Veröffentlichen, Installieren, Verbinden eines Kontos oder Ändern von Dateien.

## Autor und Weiterverwendung

Erstellt von [Eugene Tsarkov](https://www.linkedin.com/in/etsarkov/). Ein unabhängiges, kostenloses Projekt. Der verfasste Leitfadentext steht unter [CC BY 4.0](LICENSE.md). Die Lizenz erlaubt auch kommerzielles Teilen und Bearbeiten unter ihren Bedingungen. Nenne den Autor, verlinke den ursprünglichen Leitfaden und die Lizenz und kennzeichne Änderungen wie vorgeschrieben. Die sieben in LICENSE.md genannten Begleittexte unterliegen denselben CC-BY-4.0-Bedingungen. Die Konfiguration des Repositories ist von dieser Erlaubnis ausgenommen. Eine Lizenz für Code, Logos oder Materialien Dritter wird nicht stillschweigend gewährt.

## Feedback und Sprache

Sieh dir die [Hinweise für Beiträge](CONTRIBUTING.md) und die [Meldung von Sicherheitsproblemen](SECURITY.md) an. Veröffentliche keine privaten Chats, Dateien oder Geheimnisse in einem GitHub-Issue. Englisch ist die maßgebliche Quelle; das geführte Gespräch kann in deiner gewählten Sprache stattfinden. Sprachversionen der Website werden erst als verfügbar angeboten, wenn der vollständige Ablauf in der jeweiligen Sprache geprüft ist.
