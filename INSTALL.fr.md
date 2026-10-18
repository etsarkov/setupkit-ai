# Installer les skills SetupKit

[English](INSTALL.md) · [Español](INSTALL.es.md) · [Português (Brasil)](INSTALL.pt.md) · [日本語](INSTALL.ja.md) · [Deutsch](INSTALL.de.md) · Français · [Русский](INSTALL.ru.md) · [简体中文](INSTALL.zh.md)

Choisissez [Clarify](skills/setupkit-clarify/README.fr.md) pour préciser une demande floue, ou [Fact Check](skills/setupkit-fact-check/README.fr.md) pour examiner les affirmations et leurs preuves. Lisez le SKILL.md choisi avant l’installation.

Ce guide concerne l’installation dans un projet. Pour un premier essai, utilisez un nouveau projet de test vide. Ces instructions ne comprennent aucune connexion de compte, clé API ni API de modèle payante. Les coûts et autorisations de votre assistant continuent de s’appliquer.

## Avant l’installation

1. Choisissez un ou deux skills et l’assistant à utiliser.
2. Vérifiez les dossiers de destination de l’assistant et les dossiers partagés `.agents/skills/setupkit-clarify` et `.agents/skills/setupkit-fact-check`. Si un dossier correspondant existe déjà, arrêtez-vous et décidez séparément de cette mise à jour. Les avertissements d’écrasement peuvent ne pas couvrir toutes les destinations partagées.
3. Choisissez la portée du projet. Plusieurs assistants utilisent `.agents/skills` ; d’autres assistants du projet peuvent découvrir les fichiers qui s’y trouvent.

## Skills CLI

La [documentation d’origine de Skills CLI](https://github.com/vercel-labs/skills/blob/13e4063a1cf913f5606d57d42ab83a86f5001e04/README.md) cite notamment Codex, Claude Code, Cursor, Gemini CLI, OpenCode, Windsurf et GitHub Copilot. Le manifeste du dépôt inspecté exige Node.js 22.20.0 ou une version ultérieure. Utilisez l’environnement requis par la version choisie.

Ouvrez un terminal dans le dossier du projet cible. `npx` télécharge et exécute l’installateur ; examinez le paquet d’origine avant de le lancer.

Les deux skills :

```bash
npx skills add etsarkov/setupkit-ai \
  --skill setupkit-clarify \
  --skill setupkit-fact-check
```

Clarify uniquement :

```bash
npx skills add etsarkov/setupkit-ai --skill setupkit-clarify
```

Fact Check uniquement :

```bash
npx skills add etsarkov/setupkit-ai --skill setupkit-fact-check
```

Choisissez l’assistant et la portée du projet. Vérifiez toutes les options présélectionnées, les chemins et le récapitulatif final avant de confirmer. Annulez si un skill existant devait être remplacé sans mise à jour convenue séparément. Ces exemples conservent la confirmation.

Pour préciser une cible, ajoutez son identifiant, par exemple `--agent cursor`, `--agent gemini-cli` ou `--agent opencode`. Le [tableau d’origine](https://github.com/vercel-labs/skills/blob/13e4063a1cf913f5606d57d42ab83a86f5001e04/README.md#supported-agents) liste d’autres identifiants et destinations.

Exemples de destinations dans le code inspecté :

| Cible de l’installateur | Dossier du projet |
|---|---|
| Codex, Cursor, Gemini CLI, OpenCode, GitHub Copilot | `.agents/skills/` |
| Claude Code | `.claude/skills/` |
| Windsurf | `.windsurf/skills/` |

Ce tableau décrit l’orientation des fichiers par l’installateur ; il ne prouve pas un test SetupKit dans chaque assistant. Les commandes précédentes ne fixent pas de version : une version ultérieure peut différer du code inspecté.

## Autre méthode pour Codex

Si skill-installer est disponible dans votre environnement Codex, ouvrez le projet cible et envoyez :

```text
$skill-installer Installe SetupKit Clarify et SetupKit Fact Check depuis :
https://github.com/etsarkov/setupkit-ai/tree/main/skills/setupkit-clarify
https://github.com/etsarkov/setupkit-ai/tree/main/skills/setupkit-fact-check
Installe-les uniquement pour ce projet. Préserve les skills existants. Si l’installation dans le projet est impossible, explique la limite sans modifier de fichiers.
```

Pour un seul skill, ne gardez que son nom et son URL. La demande exprime la portée souhaitée ; confirmez la destination réelle avant d’autoriser des modifications. Si seule une installation pour tout l’utilisateur est proposée, arrêtez-vous et choisissez une méthode adaptée au projet. Voir le [guide officiel Codex](https://learn.chatgpt.com/docs/build-skills).

## Installation manuelle et Claude Code

Téléchargez l’archive du dépôt depuis GitHub et extrayez-la hors des dossiers où votre assistant découvre les skills. Lisez les SKILL.md sélectionnés. Copiez uniquement leurs dossiers depuis `skills/` vers le dossier du projet documenté par l’assistant, sans changer leurs noms ni leur contenu. Vérifiez d’abord les destinations propres à l’assistant et les destinations partagées ; ne remplacez pas un dossier sans décision de mise à jour séparée.

Codex, portée du projet :

```text
.agents/skills/setupkit-clarify/SKILL.md
.agents/skills/setupkit-fact-check/SKILL.md
```

Claude Code, portée du projet :

```text
.claude/skills/setupkit-clarify/SKILL.md
.claude/skills/setupkit-fact-check/SKILL.md
```

Pour un seul skill, son dossier suffit. Conservez les traductions de README que vous copiez et toutes les mentions d’auteur et de licence dans SKILL.md. Dans Claude Code, après la découverte, commencez un message par `/setupkit-clarify` ou `/setupkit-fact-check`. Voir la [documentation officielle Claude Code](https://code.claude.com/docs/en/skills).

Pour un autre assistant, vérifiez le chemin officiel de découverte et la méthode d’appel. Conservez une copie des instructions de chaque skill ; adapter un chemin ne nécessite ni de traduire ni de réécrire SKILL.md.

## Vérifier le résultat

1. Confirmez que les identifiants choisis apparaissent dans la liste ou la vue de découverte avec la portée du projet. Ouvrez une nouvelle tâche ou redémarrez l’assistant si nécessaire.
2. Essayez un exemple de [Clarify](skills/setupkit-clarify/README.fr.md) ou [Fact Check](skills/setupkit-fact-check/README.fr.md). Vérifiez que le bon skill a réellement été chargé.
3. Comparez le résultat au but de l’exemple. Clarify doit demander seulement les informations importantes manquantes. Fact Check doit montrer les preuves manquantes et une décision adaptée, y compris BLOCK si nécessaire.

## Compatibilité et autorisations

La structure des fichiers et les modèles de commandes ont été comparés à la documentation et au code d’origine enregistrés. Le périmètre des tests sur des versions précises est indiqué ci-dessous ; ces tests ne fournissent pas de preuve d’appel natif de SetupKit dans les autres assistants cités. Une cible d’installation ne démontre pas une activation, des outils, un accès aux sources, des autorisations ou une qualité de revue identiques.

Fact Check a besoin de sources actuelles pour les affirmations sensibles au temps. Si une preuve importante manque, l’affirmation reste non résolue. Le paquet n’inclut et n’installe aucun humanizer ; Fact Check peut fonctionner sans celui-ci.

L’assistant contrôle le chargement, l’exécution et les autorisations. Un skill ou une décision PASS n’autorise ni publication, envoi, dépense, installation, ni connexion de compte. Fournissez seulement les documents que vous avez le droit de partager avec l’assistant choisi et consultez ses conditions de traitement des données.

## Mode de test vérifié

Le 18 octobre 2026, l’installation par copie dans de nouveaux projets macOS a été vérifiée avec npm/npx 11.6.2 et Skills CLI 1.7.2. Les deux skills ont été appelés explicitement dans Codex 0.163.0-alpha.10.2 (gpt-6.1-sol) et OpenCode 2.0.22 (gpt-5.6-sol), avec un abonnement ChatGPT existant. Les tests synthétiques couvraient des demandes incomplètes/complètes et des affirmations non étayées/correctes.

Les scripts de cycle de vie npm étaient désactivés dans l’environnement de test.

Commande non interactive de copie testée pour Codex :

```bash
npx --yes skills@1.7.2 add etsarkov/setupkit-ai --skill setupkit-clarify --skill setupkit-fact-check --agent codex --copy --yes --json
```

Pour la cible OpenCode testée, remplacez `codex` par `opencode`. Utilisez ce mode sans confirmations seulement après avoir vérifié vous-même les skills, la portée du projet et tous les dossiers de destination. Les exemples précédents conservent la confirmation.

Ces tests ne vérifient pas les choix interactifs par défaut, le mode de liens symboliques par défaut, l’installation globale, l’activation automatique, la vérification de sources web en direct ni d’autres versions d’assistants. Ils ne garantissent pas la qualité des résultats pour toute tâche.

## Auteur et licence

Auteur et responsable de maintenance : [Eugene Tsarkov](https://www.linkedin.com/in/etsarkov/). Partie de [SetupKit](https://github.com/etsarkov/setupkit-ai), développée avec l’aide d’OpenAI Codex. Ces deux skills utilisent la [licence MIT](skills/LICENSE) ; voir leur [provenance](skills/PROVENANCE.md). Le guide principal SetupKit a sa propre licence, décrite dans le [README du dépôt](README.md#author-and-reuse).

L’anglais est la version de référence. Cette traduction conserve les mêmes instructions, identifiants et limites.
