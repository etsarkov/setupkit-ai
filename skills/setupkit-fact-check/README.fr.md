# SetupKit Fact Check

Auteur: **[Eugene Tsarkov](https://www.linkedin.com/in/etsarkov/)** · [SetupKit](https://github.com/etsarkov/setupkit-ai) · Licence: **MIT**

[English](README.md) · [Español](README.es.md) · [Português (Brasil)](README.pt.md) · [日本語](README.ja.md) · [Deutsch](README.de.md) · Français · [Русский](README.ru.md) · [简体中文](README.zh.md)

Vérifiez les affirmations et leurs preuves avant de publier.

## Quand l’utiliser

Utilisez Fact Check lorsqu’un texte public est prêt pour la vérification factuelle ou lorsque vous demandez explicitement de vérifier une affirmation. Il distingue faits, expérience personnelle, opinions et hypothèses, examine les preuves disponibles et fournit un relevé concis des affirmations.

La décision est PASS, PASS WITH EDITS ou BLOCK. Une affirmation essentielle sans preuve ou une exigence importante concernant les médias qui reste non résolue conduit à BLOCK.

## Installation

Lisez d’abord les instructions du skill. Pour un premier essai, utilisez un nouveau projet de test vide. Avant d’exécuter la commande, vérifiez les dossiers de skills déjà présents dans les destinations et les emplacements partagés du projet ; décidez séparément de toute mise à jour. Consultez le [guide d’installation commun](../../INSTALL.fr.md).

```bash
npx skills add etsarkov/setupkit-ai --skill setupkit-fact-check
```

Choisissez l’assistant cible et une installation limitée au projet. Vérifiez les options présélectionnées, les destinations et le récapitulatif avant de confirmer. Certains assistants partagent .agents/skills ; d’autres assistants du projet peuvent découvrir les fichiers qui y sont placés.

npx télécharge et exécute l’installateur. Le guide d’installation commun précise les versions et les modes testés ainsi que les limites de compatibilité.

## Exemples

Les extraits et les données sont fictifs ; ils ne décrivent ni des entreprises réelles, ni des résultats mesurés, ni des droits sur des images.

### Préserver le sens d’une citation

**Contenu à vérifier:**

```text
Utilise setupkit-fact-check. Extrait fictif de la source : « Nous envisageons un lancement en juin. » Brouillon : « L’entreprise a lancé le produit. »
```

**Résultat illustratif:** Repère qu’un lancement futur possible est devenu un événement accompli. Remplace l’affirmation par une formulation fidèle et attribuée, comme « L’entreprise indique qu’elle envisage un lancement en juin. » Vérifie toute citation finale à partir de la source fournie.

### Vérifier les pourcentages

**Contenu à vérifier:**

```text
Utilise setupkit-fact-check. Données fictives fournies : avant, 10 conversions pour 100 visites ; après, 12 pour 100. Brouillon : « Le taux de conversion a augmenté de 20 points de pourcentage. »
```

**Résultat illustratif:** Corrige ainsi : « Le taux de conversion est passé de 10% à 12% : 2 points de pourcentage, soit une hausse relative de 20%. » PASS WITH EDITS pour cet exemple arithmétique après vérification de la correction ; ces chiffres ne prouvent ni une mesure réelle, ni une significativité statistique, ni un lien de causalité.

### Vérifier la provenance d’une photo

**Contenu à vérifier:**

```text
Utilise setupkit-fact-check. Un post contient une photo trouvée en ligne. Son auteur, la source originale et l’autorisation pour cet usage sont inconnus.
```

**Résultat illustratif:** Consigne la provenance et l’autorisation manquantes. BLOCK tant que les exigences importantes applicables au média ne sont pas résolues. Demande la source et l’autorisation, ou remplace l’image par un élément dont l’usage prévu est justifié.

## Limites

La vérification dépend des sources et des outils accessibles à votre assistant. Les faits susceptibles de changer exigent une vérification actuelle. PASS évalue le texte et les preuves examinés ; il n’autorise pas la publication et ne remplace pas un conseil professionnel lorsque celui-ci est nécessaire.

Les skills restent soumis aux autorisations et aux règles d’approbation de votre assistant. Ils ne donnent aucun accès aux comptes et n’autorisent ni dépenses, ni envois, ni installations, ni publications.

Utilisez uniquement des éléments que vous êtes en droit de partager avec l’assistant choisi. Vérifiez ses conditions de traitement des données avant de lui fournir des informations confidentielles ou personnelles.

[SKILL.md](SKILL.md) · [SetupKit Skills](../README.fr.md)

## Licence et provenance

[MIT](../LICENSE). Copyright (c) 2026 Eugene Tsarkov. Développés avec l’aide d’OpenAI Codex.

Consultez la [provenance](../PROVENANCE.md) pour l’historique de développement et les travaux connexes connus. L’attribution concerne ces implémentations maintenues ; elle ne revendique pas l’invention des méthodes générales de questionnement ou de vérification des faits.

Le nom de l’auteur, le lien vers SetupKit, l’identifiant MIT et le texte intégral de la licence restent aussi dans chaque SKILL.md et accompagnent donc une copie indépendante.

L’anglais est la source de référence. Les traductions des README décrivent les mêmes skills ; chaque skill possède un seul SKILL.md en anglais.
