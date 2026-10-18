# SetupKit Skills

Auteur: **[Eugene Tsarkov](https://www.linkedin.com/in/etsarkov/)** · [SetupKit](https://github.com/etsarkov/setupkit-ai) · Licence: **MIT**

[English](README.md) · [Español](README.es.md) · [Português (Brasil)](README.pt.md) · [日本語](README.ja.md) · [Deutsch](README.de.md) · Français · [Русский](README.ru.md) · [简体中文](README.zh.md)

Clarifiez la tâche avant de commencer. Vérifiez les preuves avant de publier.

## Choisir un skill

| Votre situation | Skill | Ce que vous obtenez |
|---|---|---|
| Une demande comporte des lacunes susceptibles de modifier la tâche | [Clarify](setupkit-clarify/README.fr.md) | Des questions ciblées et un périmètre plus clair |
| Un texte public ou une affirmation nécessite une vérification factuelle | [Fact Check](setupkit-fact-check/README.fr.md) | Un relevé des affirmations, les preuves manquantes et une décision de vérification |

Chaque page de skill contient les scénarios d’exemple sélectionnés et un lien vers son SKILL.md complet.

## Installation

Lisez d’abord les instructions du skill. Pour un premier essai, utilisez un nouveau projet de test vide. Avant d’exécuter la commande, vérifiez les dossiers de skills déjà présents dans les destinations et les emplacements partagés du projet ; décidez séparément de toute mise à jour. Consultez le [guide d’installation commun](../INSTALL.fr.md).

```bash
npx skills add etsarkov/setupkit-ai \
  --skill setupkit-clarify \
  --skill setupkit-fact-check
```

Choisissez l’assistant cible et une installation limitée au projet. Vérifiez les options présélectionnées, les destinations et le récapitulatif avant de confirmer. Certains assistants partagent .agents/skills ; d’autres assistants du projet peuvent découvrir les fichiers qui y sont placés.

npx télécharge et exécute l’installateur. Le guide d’installation commun précise les versions et les modes testés ainsi que les limites de compatibilité.

## Utiliser les skills

Une fois le skill chargé par votre assistant, utilisez l’identifiant setupkit-clarify ou setupkit-fact-check. La découverte, l’invocation, l’accès aux sources et les autorisations des outils dépendent de l’environnement ; la prise en charge d’une cible par l’installateur ne prouve pas un comportement identique dans tous les assistants.

Fact Check peut suivre une étape éditoriale telle qu’un humanizer. Un humanizer n’est pas nécessaire ; ce paquet n’en contient pas et n’en installe pas.

Les skills restent soumis aux autorisations et aux règles d’approbation de votre assistant. Ils ne donnent aucun accès aux comptes et n’autorisent ni dépenses, ni envois, ni installations, ni publications.

Utilisez uniquement des éléments que vous êtes en droit de partager avec l’assistant choisi. Vérifiez ses conditions de traitement des données avant de lui fournir des informations confidentielles ou personnelles.

## Licence et provenance

[MIT](LICENSE). Copyright (c) 2026 Eugene Tsarkov. Développés avec l’aide d’OpenAI Codex.

Consultez la [provenance](PROVENANCE.md) pour l’historique de développement et les travaux connexes connus. L’attribution concerne ces implémentations maintenues ; elle ne revendique pas l’invention des méthodes générales de questionnement ou de vérification des faits.

Le nom de l’auteur, le lien vers SetupKit, l’identifiant MIT et le texte intégral de la licence restent aussi dans chaque SKILL.md et accompagnent donc une copie indépendante.

L’anglais est la source de référence. Les traductions des README décrivent les mêmes skills ; chaque skill possède un seul SKILL.md en anglais.
