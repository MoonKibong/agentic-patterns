# Langage de patterns

Ce document définit la structure et le niveau de qualité des entrées Agentic Patterns.

## Définition

Un agentic pattern est une solution nommée et réutilisable à un problème récurrent dans le travail
humain-IA.

Les patterns peuvent décrire :

- Des structures de prompts.
- Des structures de contexte.
- Des harnais de planification ou d'exécution.
- Des boucles de révision et de vérification.
- Des contrats de rôle d'agent.
- Des protocoles MCP/outil.
- Des actions de coordination multi-agents.
- Des pratiques de gestion de la mémoire et de l'état.

Les patterns ne sont pas limités au génie logiciel. Le coding est le premier domaine fort car il
dispose de tests visibles, de dépôts, d'outils et de boucles de révision, mais la même structure
s'applique à la génération d'images, à l'écriture, au design, à la production vidéo/média, à la
recherche, à l'analyse et à d'autres workflows IA guidés par des humains.

## Métadonnées de pattern

Chaque pattern doit commencer par un petit bloc de métadonnées :

```yaml
---
id: context-packet
name: Context Packet
category: context
status: draft
applies_to:
  - coding agents
  - planning
  - implementation
domains:
  - coding
related:
  - durable-session-state
---
```

L'`id` doit être stable, en minuscules et avec des tirets. `domains` est optionnel mais recommandé.
Il décrit où le pattern est utile, par exemple `coding`, `image-generation`, `writing`, `design`,
`video-media`, `research-analysis`, ou `general`.

## Sections d'un pattern

Utilisez ces sections sauf si un pattern a une raison forte de différer.

### Intent

Une ou deux phrases décrivant l'action réutilisable.

### Also Known As

Noms alternatifs optionnels.

### Problem

Le problème récurrent que ce pattern adresse.

### Context

La situation où le pattern s'applique. Inclure les préconditions et les hypothèses d'environnement.

### Forces

Les tensions qui rendent le problème non trivial. Exemples :

- Plus de contexte peut aider l'agent, mais trop de contexte peut noyer le signal important.
- Plus d'autonomie peut accélérer l'exécution, mais une autonomie illimitée peut cacher des risques.
- Plus d'agents peuvent paralléliser le travail, mais le coût de coordination peut dépasser le bénéfice.

### Solution

La structure, le protocole, le prompt, le harnais ou le comportement d'outil réutilisable.

### Agent Recognition Signals

Signaux observables qui devraient amener un agent à considérer le pattern.

### Procedure

Étapes concrètes qu'un humain ou un agent peut suivre.

### Outputs

Artefacts que le pattern doit produire.

### Stop Conditions

Quand arrêter d'appliquer le pattern, escalader ou changer de pattern.

### Example

Un exemple compact et réaliste. Les exemples synthétiques sont préférés lorsqu'un workflow réel
pourrait révéler des détails privés d'implémentation, client, prompt ou d'orchestration.

### Failure Modes

Façons connues dont le pattern peut mal fonctionner.

### Evidence

Résultats observés, notes de terrain, tests, résultats de révision ou autres éléments de soutien.

Les preuves doivent être sûres à publier. Utilisez des résumés assainis, des reproductions
synthétiques ou des sources publiques. Ne pas exposer des prompts privés, de la logique de harnais
propriétaire, des données client, des noms de dépôts privés, des identifiants ou des transcriptions
internes complètes.

### Related Patterns

Patterns qui se composent avec, remplacent ou entrent en conflit avec celui-ci.

## Statut des patterns

- `draft` : prometteur mais pas encore stabilisé.
- `candidate` : utilisé avec succès plus d'une fois et prêt pour la révision.
- `accepted` : révisé et considéré comme faisant partie du catalogue.
- `deprecated` : conservé pour référence historique mais plus recommandé.

## Catégories

Catégories initiales :

- `prompt` : structures d'instructions réutilisables.
- `context` : structures de paquets de contexte réutilisables.
- `harness` : workflows par étapes pour la planification, l'exécution, la révision et la
  vérification.
- `orchestration` : coordination multi-agents et multi-sessions.
- `tool` : patterns d'interaction MCP, CLI, script ou environnement.
- `memory` : patterns de connaissance durable et d'état.
- `evaluation` : façons de juger si un pattern a fonctionné.

Les catégories peuvent évoluer à mesure que le catalogue mûrit.

## Hygiène des preuves

Les exemples de patterns doivent enseigner la structure réutilisable, pas divulguer l'incident
privé qui a inspiré le pattern.

Preuves acceptables :

- Exemples synthétiques qui préservent les forces et la procédure.
- Notes de terrain assainies avec les identifiants privés supprimés.
- Références publiques provenant de dépôts open source, de papiers, de docs, de billets de blog ou
  de fils de tickets.
- Observations agrégées telles que « observé dans plusieurs sessions de coding locales ».

Ne pas inclure :

- Noms de dépôts privés, noms de clients, URLs privées, identifiants ou logs.
- Prompts propriétaires complets, internes de harnais ou protocoles MCP/outil.
- Transcriptions révélant une direction produit non publiée ou des détails d'implémentation internes.

En cas de doute, généraliser le scénario et garder le pattern opérationnel.

## Règles de nommage

Les noms de patterns doivent être :

- Courts.
- Mémorables.
- Opérationnels.
- Suffisamment spécifiques pour distinguer l'action.

Évitez les noms qui décrivent simplement un objectif, comme `Better Coding` ou `Good Context`.

## Lisibilité machine

Les fichiers de patterns doivent rester utiles en tant que Markdown ordinaire. Le bloc de
métadonnées existe pour que les futurs mainteneurs puissent :

- Construire des index.
- Vérifier les champs manquants.
- Recommander des patterns aux agents.
