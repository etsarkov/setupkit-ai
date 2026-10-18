# SetupKit Clarify

Auteur: **[Eugene Tsarkov](https://www.linkedin.com/in/etsarkov/)** · [SetupKit](https://github.com/etsarkov/setupkit-ai) · Licence: **MIT**

[English](README.md) · [Español](README.es.md) · [Português (Brasil)](README.pt.md) · [日本語](README.ja.md) · [Deutsch](README.de.md) · Français · [Русский](README.ru.md) · [简体中文](README.zh.md)

Transformez une demande floue en un brief qui permet d’avancer.

## Quand l’utiliser

Utilisez Clarify lorsqu’une question sans réponse peut modifier le périmètre, le coût, le risque ou la définition de la réussite. Il utilise le contexte disponible, ne demande que les informations importantes qui manquent et s’arrête dès qu’il en sait assez pour poursuivre.

Le résultat précise le périmètre établi, les hypothèses acceptées, les questions reportées et la prochaine étape.

## Installation

Lisez d’abord les instructions du skill. Pour un premier essai, utilisez un nouveau projet de test vide. Avant d’exécuter la commande, vérifiez les dossiers de skills déjà présents dans les destinations et les emplacements partagés du projet ; décidez séparément de toute mise à jour. Consultez le [guide d’installation commun](../../INSTALL.fr.md).

```bash
npx skills add etsarkov/setupkit-ai --skill setupkit-clarify
```

Choisissez l’assistant cible et une installation limitée au projet. Vérifiez les options présélectionnées, les destinations et le récapitulatif avant de confirmer. Certains assistants partagent .agents/skills ; d’autres assistants du projet peuvent découvrir les fichiers qui y sont placés.

npx télécharge et exécute l’installateur. Le guide d’installation commun précise les versions et les modes testés ainsi que les limites de compatibilité.

## Exemples

Il s’agit d’illustrations, pas de comptes rendus d’exécutions réelles. Les questions ne s’appliquent que si leurs réponses manquent dans le contexte.

### Automatiser un rapport hebdomadaire

**Exemple de demande:**

```text
Utilise setupkit-clarify : notre rapport hebdomadaire me prend trop de temps. Aide-moi à décider quoi automatiser.
```

**Questions possibles:**

- D’où viennent les données du rapport ?
- Qui utilise le rapport et quelle décision doit-il aider cette personne à prendre ?
- Quelles étapes peuvent être automatiques et lesquelles nécessitent ta vérification ?

**Résultat illustratif:** Un processus délimité : données d’entrée, résultat utile, étapes automatiques et points de contrôle humain. Ce brief n’autorise ni la mise en œuvre ni l’envoi du rapport.

### Définir un post de lancement

**Exemple de demande:**

```text
Utilise setupkit-clarify : je veux annoncer le lancement de notre produit. Aide-moi à définir le post avant de l’écrire.
```

**Questions possibles:**

- Qui doit le lire et que doit comprendre cette personne ?
- Quelle est l’idée principale que tu veux transmettre ?
- Quels résultats ou affirmations sur le produit pouvons-nous étayer et quelle réaction souhaites-tu ?

**Résultat illustratif:** Un brief éditorial précisant le lectorat, l’idée de l’auteur, les affirmations étayées et la réaction souhaitée.

## Limites

Les questions des exemples sont illustratives. Clarify n’impose pas de questionnaire fixe et ne redemande pas des réponses déjà disponibles. Une demande simple et suffisamment précise peut avancer sans questions supplémentaires.

Les skills restent soumis aux autorisations et aux règles d’approbation de votre assistant. Ils ne donnent aucun accès aux comptes et n’autorisent ni dépenses, ni envois, ni installations, ni publications.

Utilisez uniquement des éléments que vous êtes en droit de partager avec l’assistant choisi. Vérifiez ses conditions de traitement des données avant de lui fournir des informations confidentielles ou personnelles.

[SKILL.md](SKILL.md) · [SetupKit Skills](../README.fr.md)

## Licence et provenance

[MIT](../LICENSE). Copyright (c) 2026 Eugene Tsarkov. Développés avec l’aide d’OpenAI Codex.

Consultez la [provenance](../PROVENANCE.md) pour l’historique de développement et les travaux connexes connus. L’attribution concerne ces implémentations maintenues ; elle ne revendique pas l’invention des méthodes générales de questionnement ou de vérification des faits.

Le nom de l’auteur, le lien vers SetupKit, l’identifiant MIT et le texte intégral de la licence restent aussi dans chaque SKILL.md et accompagnent donc une copie indépendante.

L’anglais est la source de référence. Les traductions des README décrivent les mêmes skills ; chaque skill possède un seul SKILL.md en anglais.
