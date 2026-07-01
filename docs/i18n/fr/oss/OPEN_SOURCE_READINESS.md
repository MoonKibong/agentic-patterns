# Préparation open source

Ce document enregistre les valeurs par défaut recommandées pour la publication publique d'Agentic
Patterns.

## Évaluation de tâche

Verdict : `REVISE` jusqu'à ce que la licence soit finalisée et que les démarrages rapides traduits
aient fait l'objet d'une révision humaine.

Périmètre : docs du dépôt, catalogue de patterns, templates GitHub, i18n, workflow de contribution
et positionnement public.

Risque principal : le projet est inspiré de vrais workflows agentiques, donc les docs publics
doivent éviter d'exposer des prompts propriétaires, des détails de harnais privés, des données
client, des noms de dépôts privés et des transcriptions de workflows internes.

## Positionnement

Meilleur choix : présenter Agentic Patterns comme un langage de patterns pour le travail IA guidé
par des humains, pas comme une collection de prompts. Le coding est le premier domaine mature, mais
le catalogue couvre aussi la génération d'images, l'écriture, le design, la vidéo/médias, la
recherche et l'analyse.

## Licence

Décision actuelle :

- Documentation, catalogue de patterns, prompts et notes de terrain : CC BY 4.0.
- Code, schémas et artefacts logiciels approuvés : MIT.

## Phase de release

Meilleur choix : publier la première release publique en `v0.1.0` avec un langage en phase
initiale. Éviter de présenter les patterns brouillons comme des meilleures pratiques validées.

## Politique sur les preuves et la confidentialité

Meilleur choix : exiger des exemples synthétiques, assainis ou explicitement publics. Traiter la
fuite accidentelle de prompts privés, de données client, d'URLs privées ou de détails de workflows
propriétaires comme un problème de sécurité.

## CI

Pour ce dépôt public centré sur Markdown, la CI peut commencer par le linting Markdown et les
vérifications de liens une fois que les validateurs publics sont approuvés.

## Contributions

Exiger que les PR incluent :

- un résumé des changements de docs ou de patterns visibles par les utilisateurs
- des commandes de vérification
- l'impact sur les preuves/la confidentialité
- l'impact sur l'i18n
- des liens vers les tickets associés

## Liste de contrôle de publication

1. Finaliser les fichiers de licence.
2. Confirmer la présence de `README.md`, `CONTRIBUTING.md`, `SECURITY.md`, `CODE_OF_CONDUCT.md`,
   `CHANGELOG.md` et `RELEASE.md`.
3. Confirmer l'existence des templates de tickets et de PR.
4. Exécuter les vérifications de révision et de validation publiques approuvées.
5. Réviser les démarrages rapides `docs/i18n/`.
6. Rechercher les termes privés, les URLs privées, les identifiants et les noms de dépôts internes.
7. Créer une release GitHub avec un langage en phase initiale.

## Liste de contrôle des décisions

| Élément | Meilleur choix | Statut |
| --- | --- | --- |
| Promesse produit | Langage de patterns pour le travail IA guidé par des humains | Documenté |
| Licence | Docs CC BY 4.0 + code MIT | Présent |
| README | Périmètre, catalogue, validation, hygiène des preuves | Présent |
| Changelog | Style Keep a Changelog avec `Unreleased` | Présent |
| Contributing | Attentes sur les patterns, preuves, i18n | Présent |
| Security | Rapports de fuite privée et d'automatisation dangereuse | Présent |
| Code de conduite | Politique légère appliquée par les mainteneurs | Présent |
| Templates de tickets | Proposition de pattern présente ; plus de templates recommandés | Partiel |
| Template de PR | Résumé, validation, i18n, impact sur la confidentialité | Présent |
| CI | Vérifications publiques Markdown/liens | Pas encore présent |
| Processus de release | Checklist seed `v0.1.0` | Présent |

## Critères d'acceptation

- Les docs publics expliquent ce qu'est le projet et ce qu'il n'est pas.
- Les mainteneurs disposent d'instructions de release et de rollback.
- Les contributeurs disposent des attentes en matière de configuration, de validation, de patterns,
  de confidentialité et d'i18n.
- Les démarrages rapides localisés existent et indiquent que les docs anglais restent la source de
  vérité.
- Aucun détail de solution propriétaire n'est requis pour comprendre ou contribuer des patterns.
