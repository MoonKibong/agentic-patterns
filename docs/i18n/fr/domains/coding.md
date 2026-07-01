# Coding

Le coding est le domaine de démarrage d'Agentic Patterns car il expose des artefacts clairs :
dépôts, fichiers, tests, shells, tickets, pull requests, CI et verdicts de révision.

## Forces communes

- Les agents ont besoin de suffisamment de contexte de dépôt sans être noyés dans des fichiers non
  pertinents.
- L'utilisation des outils peut modifier l'état local ou distant.
- La révision et les tests peuvent détecter des défauts, mais seulement lorsqu'ils font partie du
  workflow.
- Les tâches de longue durée ont besoin d'un état durable et de transferts resumables.

## Patterns utiles

- [Paquet de contexte (Context Packet)](../../../../patterns/context/context-packet.md)
- [Contrat de rôle (Role Contract)](../../../../patterns/prompt/role-contract.md)
- [Contrat d'utilisation des outils (Tool-Use Contract)](../../../../patterns/tool/tool-use-contract.md)
- [État de session durable (Durable Session State)](../../../../patterns/orchestration/durable-session-state.md)

## Patterns candidats

- Human Approval Gate.
- Guardian Gate.
- Provenance Ledger.
- Verification Ladder.
- Context Compactor.
