# Les racines du langage de patterns

Agentic Patterns n'est pas destiné à être une collection d'astuces de prompts. Son modèle plus
profond vient de la tradition du langage de patterns : nommer les problèmes récurrents, décrire les
forces qui les rendent difficiles, enregistrer une solution de base réutilisable, et rendre cette
solution communicable entre personnes et outils.

## Christopher Alexander

Christopher Alexander et ses collaborateurs ont développé la tradition du langage de patterns
architecturaux dans des œuvres telles que *A Pattern Language: Towns, Buildings, Construction* et
*The Timeless Way of Building*. Leurs patterns décrivaient des problèmes récurrents dans les villes,
les bâtiments et les pièces, ainsi que des solutions pouvant être réutilisées sans être copiées
mécaniquement.

L'idée importante pour ce projet n'est pas le domaine du bâtiment lui-même. C'est la fonction
sociale et cognitive d'un langage de patterns :

- Un pattern donne un nom à une situation de conception récurrente.
- Il enregistre les forces et les compromis qui rendent la situation difficile.
- Il décrit une forme de solution, pas un script rigide.
- Il permet aux non-experts et aux experts de communiquer sur les décisions de conception.
- Les patterns se composent en un langage, de sorte que des conceptions plus grandes peuvent être
  construites à partir de plus petits mouvements nommés.

Ce dernier point est important. Un catalogue de conseils isolés n'est pas encore un langage. Un
langage de patterns devient utile lorsque les patterns se font appel les uns les autres, se
contraignent mutuellement et donnent à une communauté des mots partagés pour un travail répété.

## Patterns de conception GoF

Le mouvement des patterns de conception logicielle a adapté cette idée aux logiciels
orientés-objet. Le livre du Gang of Four, *Design Patterns: Elements of Reusable Object-Oriented
Software*, a rendu le format largement connu des ingénieurs logiciels en cataloguant des solutions
récurrentes nommées telles que Factory Method, Adapter, Composite, Decorator, Observer et Strategy.

Le catalogue GoF a apporté plusieurs contributions pratiques importantes ici :

- Les patterns sont devenus un outil de communication pour la révision de conception.
- Les noms de patterns ont comprimé les discussions de conception complexes.
- La structure réutilisable a été séparée des détails d'implémentation ponctuels.
- Les compromis et l'applicabilité sont devenus une partie du jugement d'ingénierie.
- Le vocabulaire partagé a amélioré la collaboration entre équipes.

La leçon n'est pas que les workflows agentiques doivent copier les catégories GoF. La leçon est
que la pratique répétée devient plus puissante lorsqu'elle est nommée, structurée, critiquée et
enseignée.

## Pourquoi le travail agentique a besoin d'un langage de patterns

Le coding agentique a rendu le besoin visible en premier. Les développeurs redécouvrent
continuellement les mêmes questions de workflow :

- Quel contexte l'agent doit-il recevoir ?
- Quand l'agent doit-il planifier avant d'agir ?
- Quels outils peut-il utiliser, et avec quelles limites d'approbation ?
- Quand une boucle de révision ou de critique se justifie-t-elle ?
- Quel état doit survivre à la compaction du chat, au transfert ou au redémarrage ?

Les mêmes questions apparaissent en dehors du coding :

- La génération d'images a besoin de briefs, de références, de contrôle des variations, de critique
  et de sélection.
- L'écriture a besoin de voix, de plan, de continuité, de critique et de révision.
- La génération de design a besoin de contraintes, de revue de faisabilité, de transfert
  d'artefacts et d'approbation humaine.
- Le travail vidéo et médias a besoin de storyboards, de registres de continuité, de portes de
  rendu et de provenance.
- La recherche a besoin de registres de sources, de vérifications d'affirmations, d'ancres de
  citations et de boucles de révision.

C'est pourquoi le projet utilise « travail IA guidé par des humains » plutôt que seulement
« coding agentique ». Le coding est le premier domaine mature, mais le langage de patterns
sous-jacent est plus large.

## Les patterns comme connaissance opérationnelle mémétique

Les patterns sont mémétiques au sens pratique : ce sont des unités culturelles compactes pouvant
être transmises, modifiées et recombinées. Un bon pattern aide une communauté à mémoriser une
solution utile sans que chaque personne doive répéter la découverte originale.

Les agentic patterns sont particulièrement mémétiques car ils médiatisent entre les humains et les
systèmes IA. Ils ne disent pas seulement aux humains ce qu'ils doivent faire. Ils façonnent aussi
ce qu'un agent IA peut reconnaître, choisir et exécuter.

Dans ce projet, un pattern doit aider à répondre :

- Quelle est la situation récurrente ?
- Quelles forces la rendent difficile ?
- Quel mouvement réutilisable aide ?
- Quelles preuves ou exemples le soutiennent ?
- Quand ne doit-il pas être utilisé ?
- Comment un agent peut-il le reconnaître et l'appliquer ?

## Le jugement humain reste central

Les systèmes IA sont de puissants reconnaisseurs de patterns, mais ils ne possèdent pas l'objectif.
Les humains fournissent le but, le goût, la mémoire, le contexte social, le jugement éthique et la
capacité de décider quand un pattern doit être brisé.

L'objectif d'Agentic Patterns n'est donc pas d'automatiser le jugement humain pour l'éliminer.
C'est de rendre les parties réutilisables du jugement humain suffisamment lisibles pour que les
personnes et les agents puissent mieux collaborer.

## Notes de sources

- Christopher Alexander, Sara Ishikawa, Murray Silverstein, et al., *A Pattern Language: Towns,
  Buildings, Construction*, Oxford University Press, 1977.
- Christopher Alexander, *The Timeless Way of Building*, Oxford University Press, 1979.
- Erich Gamma, Richard Helm, Ralph Johnson, John Vlissides, *Design Patterns: Elements of Reusable
  Object-Oriented Software*, Addison-Wesley, 1994.
- Le Hillside Group et la communauté Pattern Languages of Programs ont poursuivi la tradition des
  patterns logiciels à travers des ateliers d'écrivains et des conférences sur les patterns.

Points d'entrée publics utiles :

- [A Pattern Language](https://en.wikipedia.org/wiki/A_Pattern_Language)
- [Pattern language](https://en.wikipedia.org/wiki/Pattern_language)
- [Design Patterns](https://en.wikipedia.org/wiki/Design_Patterns)
- [The Hillside Group](https://en.wikipedia.org/wiki/The_Hillside_Group)
- [Pattern Languages of Programs](https://en.wikipedia.org/wiki/Pattern_Languages_of_Programs)
