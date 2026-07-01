# Génération d'images

La génération d'images bénéficie des agentic patterns lorsqu'un utilisateur a besoin de plus qu'un
seul prompt : références, continuité de style, variations, critique, sélection et transfert vers
du travail de design ou de médias en aval.

## Forces communes

- Un prompt vague crée des images visuellement plausibles mais mal alignées.
- Les références et les mots de style peuvent entrer en conflit.
- Le goût humain est central et ne doit pas être caché derrière un scoring automatique.
- L'itération peut être coûteuse ou dériver de l'intention originale.

## Patterns utiles

- [Paquet de brief créatif (Creative Brief Packet)](../../../../patterns/context/creative-brief-packet.md)
- [Générer-Critiquer-Affiner (Generate-Critique-Refine)](../../../../patterns/harness/generate-critique-refine.md)
- [État de session durable (Durable Session State)](../../../../patterns/orchestration/durable-session-state.md)
- [Contrat d'utilisation des outils (Tool-Use Contract)](../../../../patterns/tool/tool-use-contract.md)

## Patterns candidats

- Reference Board.
- Style Lock.
- Variation Ladder.
- Provenance Ledger.
- Human Approval Gate.
