# Tendances du travail agentique 2026

Cette note résume les signaux publics récents autour du coding agentique et des workflows créatifs
adjacents. Elle utilise la sortie de recherche de Gemini comme point d'entrée, mais n'enregistre
ici que les affirmations qui sont sûres, utiles et soit vérifiées à partir de sources publiques,
soit clairement formulées comme pistes de recherche.

## Résumé exécutif

Le coding agentique est en train de devenir la bibliothèque de patterns précoces la plus concrète
pour le travail IA guidé par des humains : les dépôts, les shells, les tests, la revue de code, les
sandboxes et les pull requests rendent le contexte et la vérification visibles. Les mêmes primitives
apparaissent dans les workflows de génération d'images, d'écriture, de design, de vidéo/médias et
de recherche :

- paquets de contexte et briefs bornés
- agents ou sous-agents spécifiques à un rôle
- protocoles d'utilisation des outils
- boucles generate-critique-refine
- boucles plan-execute-verify-review
- état durable et artefacts de transfert
- suivi de la provenance et des citations
- portes d'approbation humaine
- enveloppes de sécurité et de gouvernance

Le catalogue doit donc rester organisé autour de primitives réutilisables, tandis que les pages de
domaines montrent comment ces primitives s'appliquent au coding, à la génération d'images, à
l'écriture, au design, à la vidéo/médias et à la recherche.

## Notes de sources vérifiées

| Source | Date | Pertinence |
| --- | --- | --- |
| [OpenAI, Introducing Codex](https://openai.com/index/introducing-codex/) | 2025 | Codex présente l'exécution de tâches cloud pour le génie logiciel, renforçant la délégation de tâches en sandbox, le contexte de dépôt, l'exécution de tests et les workflows de type PR. |
| [OpenAI Agents SDK Docs](https://openai.github.io/openai-agents-python/) | 2025-2026 | Documente les agents, les transferts, les garde-fous, le traçage et les outils comme primitives de premier ordre. |
| [Anthropic Claude Code Subagents](https://docs.anthropic.com/en/docs/claude-code/sub-agents) | 2025-2026 | Décrit des sous-agents spécifiques à une tâche avec des fenêtres de contexte séparées, des prompts personnalisés et des permissions d'outils. |
| [Anthropic Claude Code Hooks](https://docs.anthropic.com/en/docs/claude-code/hooks) | 2025-2026 | Montre des points de contrôle déterministes autour du comportement des agents, utiles pour les portes d'approbation et la gouvernance des outils. |
| [Model Context Protocol Introduction](https://modelcontextprotocol.io/introduction) | 2025-2026 | Présente MCP comme une façon standard pour les applications d'exposer des outils et du contexte aux modèles de langage. |
| [Google A2A Protocol](https://developers.googleblog.com/en/a2a-a-new-era-of-agent-interoperability/) | 2025 | Montre l'intérêt croissant pour l'interopérabilité et la délégation agent-à-agent. |
| [arXiv: The 2025 AI Agent Index](https://arxiv.org/abs/2602.17753) | 2026 | Passe en revue les systèmes d'agents IA et renforce le besoin d'évaluer les capacités des agents et les patterns de déploiement. |
| [arXiv: VideoAgent](https://arxiv.org/abs/2606.23327) | 2026 | Démontre la décomposition agentique pour les workflows d'édition vidéo. |
| [HKUDS ViMax](https://github.com/HKUDS/ViMax) | 2026 | Dépôt public pour la génération vidéo agentique à partir d'entrées texte/histoire, utile comme piste de recherche pour les pipelines médias. |

## Tendance : L'ingénierie de contexte devient une surface produit

Les systèmes agentiques traitent de plus en plus le contexte comme une entrée structurée plutôt que
comme un historique de chat. Les agents de coding utilisent les fichiers de dépôt, les instructions,
le texte des tickets, les tests et l'état d'environnement. Les systèmes créatifs ont besoin de
briefs équivalents : références, contraintes de style, ancres de continuité, audience, livrables et
critères d'évaluation.

Impact sur le catalogue :

- Conserver [Paquet de contexte (Context Packet)](../../../../patterns/context/context-packet.md) comme pattern général.
- Ajouter [Paquet de brief créatif (Creative Brief Packet)](../../../../patterns/context/creative-brief-packet.md) pour les domaines créatifs.
- Envisager les futurs patterns `Reference Board`, `Source Ledger` et `Context Compactor`.

## Tendance : Les agents sont enveloppés dans des harnais

Le changement important n'est pas seulement des modèles plus puissants. Les systèmes utiles
enveloppent les modèles avec de la planification, de l'exécution, de la critique, de la
vérification, des garde-fous, du traçage et des portes d'approbation. Dans le coding, cela apparaît
comme plan-execute-test-review. Dans le travail créatif, cela apparaît comme
brief-generate-critique-refine-select.

Impact sur le catalogue :

- Conserver des boucles de révision et de vérification explicites pour les logiciels et autres
  travaux vérifiables.
- Ajouter [Générer-Critiquer-Affiner (Generate-Critique-Refine)](../../../../patterns/harness/generate-critique-refine.md) pour le travail créatif et exploratoire.
- Ajouter les futurs patterns `Rubric Review`, `Human Approval Gate` et `Guardian Gate`.

## Tendance : Les protocoles d'outils et l'interopérabilité des agents sont importants

MCP et les protocoles agent-à-agent montrent que les workflows agentiques dépendent de plus en plus
de limites de capacités explicites. Les outils et les systèmes externes doivent être découvrables,
bornés, audités et sûrs à utiliser.

Impact sur le catalogue :

- Conserver [Contrat d'utilisation des outils (Tool-Use Contract)](../../../../patterns/tool/tool-use-contract.md).
- Ajouter les futurs patterns `Capability Manifest`, `Approval Boundary` et `Sandbox Gate`.

## Tendance : Le travail créatif a besoin de patterns de cycle de vie des artefacts

Les workflows d'images, d'écriture, de design et de vidéo génèrent des artefacts intermédiaires :
briefs, références, plans, tableaux de style, images candidates, storyboards, plans de scènes,
tableaux de critique et assets finaux. Ces artefacts ont besoin de transfert, de provenance, de
versionnage et d'approbation humaine.

Impact sur le catalogue :

- Ajouter des pages de domaines plutôt que de diviser le catalogue principal trop tôt.
- Ajouter les futurs patterns `Artifact Handoff`, `Provenance Ledger`, `Variation Ladder`,
  `Style Lock` et `Continuity Ledger`.

## Hygiène des sources

La sortie de recherche de Gemini comprenait des pistes utiles, mais ce dépôt ne doit pas traiter
les citations générées comme vérifiées par défaut. Pour la documentation publique :

- préférer les sources primaires et les docs officielles
- marquer les éléments non vérifiés comme des pistes
- ne pas citer des workflows privés
- utiliser des exemples synthétiques lorsque les preuves publiques révéleraient des méthodes
  propriétaires
