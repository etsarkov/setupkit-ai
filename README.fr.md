# SetupKit

[English](README.md) · [Español](README.es.md) · [Português (Brasil)](README.pt.md) · [日本語](README.ja.md) · [Deutsch](README.de.md) · Français · [Русский](README.ru.md) · [简体中文](README.zh.md)

Aidez votre IA à comprendre votre façon de travailler. Un guide gratuit vous aide à définir des règles de travail et à avancer sur une tâche concrète dans votre propre conversation avec une IA.

## Pour commencer

1. Copiez le [prompt de départ](prompts/fr.txt).
2. Collez-le dans votre conversation avec une IA et envoyez-le. Demandez à poursuivre en français.
3. Répondez aux questions pertinentes et choisissez une tâche à réaliser ensemble.

Vous pouvez commencer dans votre conversation actuelle. Indiquez à votre assistant quel outil vous utilisez et comment. Si une tâche nécessite un accès supplémentaire, vérifiez d’abord ce qui est possible dans votre conversation actuelle. Vous pouvez continuer manuellement, remettre cette étape à plus tard ou choisir un autre mode de travail. Installer une application ne garantit pas, à lui seul, l’accès aux outils nécessaires.

## Édition actuelle

[Le guide complet](COMPLETE.md) est à la version `0.19.2`, mise à jour le `2026-10-20`. Votre assistant doit poser des questions pertinentes, expliquer leur intérêt et réutiliser les réponses que vous avez déjà données.

S’il ne peut pas lire la source, suivez les [étapes pour fournir le texte complet](docs/getting-started.md#if-the-guide-cannot-be-read). Tout contenu manquant doit être demandé, pas inventé. La page [Compatibilité et limites](docs/compatibility.md) précise ce qui a été vérifié et ce qui ne l’a pas été. Ces documents de référence et le guide faisant autorité sont en anglais.

## Organisation et contexte, si vous le souhaitez

Si cela vous est utile, vous pouvez aussi organiser votre espace de travail actuel et préparer quelques fichiers relus sur vous, vos objectifs et votre travail. Partez de documents que vous avez déjà, comme un CV ou des notes sur les projets de votre choix. Vous décidez des changements à apporter ; vous pouvez passer une question ou la remettre à plus tard.

Lorsque vous reprenez le travail, fournissez votre progression enregistrée ou votre résumé de reprise. Votre assistant pourra ainsi réutiliser les réponses confirmées et examiner les étapes inachevées ou nouvelles qui vous concernent. Les fichiers ne sont enregistrés qu’avec votre accord et les accès dont votre assistant dispose réellement ; leur création ne garantit ni mémoire ni synchronisation automatiques.

## Trier les documents choisis, si cela vous est utile

Demandez à votre assistant de vous aider à trier les fichiers, liens ou notes que vous choisissez. Il peut proposer à quel projet rattacher chaque élément, où le conserver et ce qu’il serait utile de résumer, en gardant les références aux originaux. Relisez la proposition et choisissez ce que vous souhaitez modifier ou remettre à plus tard. Les fichiers ne sont enregistrés ou déplacés qu’avec votre accord et les accès nécessaires ; sinon, vous recevez un plan à suivre manuellement. À la reprise, fournissez le relevé vérifié pour que l’assistant se concentre sur les éléments nouveaux, modifiés ou en attente.

## Skills

- [Clarify](skills/setupkit-clarify/README.fr.md): pose des questions ciblées pour clarifier une tâche avant de commencer.
- [Fact Check](skills/setupkit-fact-check/README.fr.md): vérifie les affirmations, les preuves à l’appui et les exigences liées aux médias avant publication.

Pour installer les deux, lisez d’abord le [guide d’installation commun](INSTALL.fr.md) et vérifiez les dossiers de skills existants. Pour un premier essai, utilisez un nouveau projet de test vide.

```bash
npx skills add etsarkov/setupkit-ai \
  --skill setupkit-clarify \
  --skill setupkit-fact-check
```

Choisissez l’assistant et une installation limitée au projet ; vérifiez les destinations avant de confirmer. npx exécute le programme d’installation. Consultez [la présentation des skills](skills/README.fr.md) pour les limites de compatibilité et les instructions d’installation individuelle.

## Votre travail reste entre vos mains

Aucun compte SetupKit n’est nécessaire. SetupKit ne reçoit pas les réponses que vous donnez à votre assistant. Les coûts, autorisations et règles de traitement des données de votre assistant s’appliquent. Demander un brouillon n’autorise pas à envoyer, publier, installer, connecter un compte ou modifier des fichiers.

## Auteur et réutilisation

Créé par [Eugene Tsarkov](https://www.linkedin.com/in/etsarkov/). Un projet indépendant et gratuit. Le texte du guide est sous licence [CC BY 4.0](LICENSE.md), qui autorise le partage et l’adaptation, y compris à des fins commerciales, selon ses conditions. Citez l’auteur, ajoutez des liens vers le guide original et la licence et indiquez les modifications comme l’exige la licence. Les sept textes d’accompagnement mentionnés dans LICENSE.md sont soumis aux mêmes conditions CC BY 4.0. La configuration du dépôt est exclue de cette autorisation. Aucune licence sur le code, les logos ou les éléments appartenant à des tiers n’est accordée implicitement.

## Retours et langue

Consultez les [consignes de contribution](CONTRIBUTING.md) et la [procédure de signalement des problèmes de sécurité](SECURITY.md). Ne publiez pas de conversations privées, de fichiers ou de secrets dans une issue GitHub. L’anglais est la source de référence ; la conversation guidée peut se dérouler dans la langue de votre choix. Les versions du site ne seront présentées comme disponibles qu’après vérification du parcours complet dans chaque langue.
