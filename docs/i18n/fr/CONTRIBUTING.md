# Contribuer

Agentic Patterns est destiné à devenir un catalogue partagé de pratiques réutilisables. Les
contributions doivent rendre le travail humain-IA répété plus facile à reconnaître, discuter et
exécuter.

## Façons de contribuer

- Ajouter un nouveau pattern en utilisant [patterns/_template.md](../../../patterns/_template.md).
- Améliorer les exemples, l'applicabilité ou les modes d'échec d'un pattern existant.
- Ajouter des notes de terrain issues de vraies sessions de coding agentique.
- Construire des outils qui valident, indexent, recommandent ou empaquettent des patterns pour les
  agents.
- Proposer une meilleure taxonomie du catalogue.

## Avant d'ajouter un pattern

Demandez-vous si l'entrée est vraiment un pattern :

- Résout-il un problème récurrent ?
- Une autre personne peut-elle l'appliquer dans une situation similaire ?
- Les compromis sont-ils visibles ?
- Un agent peut-il reconnaître quand l'utiliser ?
- Y a-t-il au moins quelques preuves ou une expérience concrète derrière ?

Si la réponse n'est pas encore claire, ajoutez une note de terrain ou un pattern brouillon plutôt
que de le présenter comme établi.

## Notes de terrain

Utilisez [field-notes/_template.md](../../../field-notes/_template.md) lorsqu'une observation est
utile mais pas encore assez stable pour devenir un pattern.

Les bonnes notes de terrain enregistrent :

- La forme de la tâche.
- La configuration de l'agent.
- Ce qui s'est passé.
- Ce qui s'est amélioré ou a échoué.
- Quel pattern pourrait émerger.
- Quelles preuves renforcerait le pattern.

## Hygiène des preuves

Ne contribuez pas de détails de solutions propriétaires. Les preuves de pattern doivent être l'une
des suivantes :

- Exemples synthétiques qui préservent la structure du problème.
- Notes de terrain assainies avec les détails privés supprimés.
- Exemples publics provenant de dépôts ouverts, de papiers, de billets de blog ou de fils de
  tickets.
- Observations généralisées énoncées sans identifiants privés.

N'incluez jamais de données client, d'identifiants, d'URLs privées, de noms de dépôts privés, de
texte de prompt interne ou de transcriptions complètes de workflows propriétaires.

## Processus d'entrée de pattern

1. Copier `patterns/_template.md` dans le répertoire de catégorie approprié.
2. Remplir le bloc de métadonnées.
3. Rédiger le pattern en termes opérationnels.
4. Inclure au moins un exemple.
5. Inclure les modes d'échec et contre-indications connus.
6. Lier les patterns associés.
7. Mettre à jour [catalog/README.md](../../../catalog/README.md).

## Documentation localisée

Les démarrages rapides localisés dans docs/i18n/ et les miroirs wiki sont des
points d'entrée publics. Lorsque vous modifiez la description du projet, les catégories
principales, le langage de sécurité/confidentialité ou le workflow de contribution, mettez à jour
les démarrages rapides localisés ou indiquez dans la pull request pourquoi aucune mise à jour de
traduction n'est nécessaire.

Si vous ne pouvez pas mettre à jour une langue avec confiance, gardez le changement de source
anglaise petit et demandez une révision de traduction.

## Norme de preuve

Les preuves peuvent être légères au début, mais elles doivent être honnêtes.

Les preuves utiles incluent :

- Un workflow répété observé dans plusieurs tâches.
- Une comparaison avant/après.
- Un extrait de transcription ou un incident résumé.
- Un résultat de test, un résultat de révision ou un défaut évité.
- Une convention locale qui a survécu à une utilisation répétée.

Évitez les affirmations vagues telles que « fonctionne mieux » sans expliquer ce qui s'est amélioré.

## Ton

Écrivez pour des humains compétents et des agents compétents. Soyez direct, spécifique et humble
face à l'incertitude.

Ce projet ne doit pas devenir une liste d'astuces de prompts inspirants. Il doit devenir un langage
de patterns pratique.
