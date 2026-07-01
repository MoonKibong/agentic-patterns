# Hygiène des preuves

Les Agentic Patterns doivent être utiles sans exposer des détails de solutions propriétaires.

Le catalogue peut être ancré dans la pratique tout en protégeant les prompts privés, les harnais,
les dépôts, les clients, les identifiants, les transcriptions et les mécanismes internes de
workflow.

## Règle

Publiez le pattern, pas l'incident privé.

Les exemples doivent révéler la structure réutilisable :

- La forme du problème.
- Les forces et les compromis.
- La procédure.
- Les sorties attendues.
- Les modes d'échec.
- Le style de vérification.

Les exemples ne doivent pas révéler des détails d'implémentation privés.

## Types de preuves sûres

- Exemples synthétiques qui préservent la structure du workflow.
- Notes de terrain assainies avec les identifiants privés supprimés.
- Exemples publics provenant de dépôts open source, de papiers, de docs, de billets de blog ou de
  fils de tickets.
- Observations agrégées énoncées sans détails identifiants.

## Ne pas publier

- Données client.
- Identifiants, jetons ou URLs privées.
- Noms de dépôts privés.
- Texte de prompt interne non destiné à être public.
- Logique de harnais propriétaire complète.
- Transcriptions complètes de workflows de projets privés.
- Direction produit, stratégie commerciale ou détails d'implémentation non publiés.

## Comment assainir une note de terrain

1. Remplacer les noms de projets par des noms génériques tels que `web app`, `API service` ou
   `agent runner`.
2. Remplacer les chemins de fichiers par des chemins représentatifs tels que
   `src/billing/service.ts`.
3. Supprimer les identifiants, noms d'hôtes, numéros de tickets privés et noms de branches privées.
4. Résumer les transcriptions plutôt que de les citer.
5. Conserver la condition d'échec ou de succès pertinente pour le pattern.
6. Ajouter une note indiquant que l'exemple est synthétique ou assaini.

## Politique d'exemples synthétiques

Les exemples synthétiques sont encouragés. Ils doivent être suffisamment réalistes pour guider
l'action, mais ils n'ont pas besoin de correspondre à un workflow privé réel.

Un bon exemple synthétique :

- Contient des fichiers, des rôles ou des commandes concrets.
- Exerce les forces du pattern.
- Montre ce que l'agent doit produire.
- Évite les secrets spécifiques au projet.

Les mauvais exemples synthétiques sont trop vagues pour être exécutés, comme « améliorer le code »
ou « utiliser un meilleur prompt ».
