# Patterns d'outils

Les patterns d'outils définissent comment les agents doivent utiliser les commandes shell, les
navigateurs, les serveurs MCP, les APIs, les gestionnaires de paquets, Git et d'autres
fonctionnalités qui peuvent affecter l'état réel.

Utilisez les patterns d'outils lorsque l'agent doit agir via des fonctionnalités externes et que le
rayon d'impact doit être explicite.

## Patterns actuels

- [Contrat d'utilisation des outils (Tool-Use Contract)](../../../../patterns/tool/tool-use-contract.md) :
  définir les outils autorisés, les déclencheurs d'approbation, les actions interdites et les
  attentes en matière de preuves.

## Idées de patterns

- Read-First Tooling.
- Approval Boundary.
- Verification Command.
- External State Guard.

## Catégories associées

- [Patterns de harnais](harness.md)
- [Patterns de prompts](prompt.md)
- [Patterns d'évaluation](evaluation.md)
