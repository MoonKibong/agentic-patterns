# Raíces del Lenguaje de Patrones

Agentic Patterns no pretende ser una colección de trucos de prompts. Su modelo más profundo
proviene de la tradición del lenguaje de patrones: nombrar problemas recurrentes, describir
las fuerzas que los hacen difíciles, registrar un núcleo de solución reutilizable y hacer
que esa solución sea comunicable entre personas y herramientas.

## Christopher Alexander

Christopher Alexander y colaboradores desarrollaron la tradición arquitectónica del lenguaje
de patrones en obras como *A Pattern Language: Towns, Buildings, Construction* y *The Timeless
Way of Building*. Sus patrones describían problemas recurrentes en ciudades, edificios y
habitaciones, junto con soluciones que podían reutilizarse sin copiarse mecánicamente.

La idea importante para este proyecto no es el dominio de la construcción en sí. Es la función
social y cognitiva de un lenguaje de patrones:

- Un patrón da nombre a una situación de diseño recurrente.
- Registra las fuerzas y los tradeoffs que hacen la situación difícil.
- Describe una forma de solución, no un guion rígido.
- Permite que expertos y no expertos se comuniquen sobre decisiones de diseño.
- Los patrones se componen en un lenguaje, de modo que diseños más grandes pueden construirse
  a partir de movimientos más pequeños con nombre.

Ese último punto importa. Un catálogo de consejos aislados no es aún un lenguaje. Un lenguaje
de patrones se vuelve útil cuando los patrones se invocan entre sí, se restringen entre sí y
dan a una comunidad palabras compartidas para el trabajo repetido.

## Patrones de Diseño GoF

El movimiento de patrones de diseño en software adaptó esta idea al software orientado a
objetos. El libro de la Gang of Four, *Design Patterns: Elements of Reusable Object-Oriented
Software*, popularizó el formato entre los ingenieros de software catalogando soluciones
recurrentes con nombre como Factory Method, Adapter, Composite, Decorator, Observer y Strategy.

El catálogo GoF realizó varias contribuciones prácticas que importan aquí:

- Los patrones se convirtieron en una herramienta de comunicación para la revisión de diseño.
- Los nombres de patrones comprimieron discusiones de diseño complejas.
- La estructura reutilizable se separó de los detalles de implementación únicos.
- Los tradeoffs y la aplicabilidad se convirtieron en parte del juicio de ingeniería.
- El vocabulario compartido mejoró la colaboración entre equipos.

La lección no es que los flujos de trabajo agénticos deban copiar las categorías GoF. La
lección es que la práctica repetida se vuelve más poderosa cuando se nombra, estructura,
critica y enseña.

## Por Qué el Trabajo Agéntico Necesita un Lenguaje de Patrones

El agentic coding ha hecho visible la necesidad primero. Los desarrolladores redescubren
repetidamente las mismas preguntas de flujo de trabajo:

- ¿Qué contexto debe recibir el agente?
- ¿Cuándo debe el agente planificar antes de actuar?
- ¿Qué herramientas puede usar, y con qué límites de aprobación?
- ¿Cuándo un revisor o bucle de crítica justifica su costo?
- ¿Qué estado debe sobrevivir la compactación de chat, transferencia o reinicio?

Las mismas preguntas aparecen fuera del coding:

- La generación de imágenes necesita briefs, referencias, control de variaciones, crítica y selección.
- La escritura necesita voz, esquema, continuidad, crítica y revisión.
- La generación de diseño necesita restricciones, revisión de viabilidad, transferencia de
  artefactos y aprobación humana.
- El trabajo de video y medios necesita storyboards, ledgers de continuidad, gates de render
  y procedencia.
- La investigación necesita ledgers de fuentes, verificaciones de afirmaciones, anclajes de
  citas y bucles de revisión.

Por esto el proyecto usa "trabajo con IA guiado por humanos" en lugar de solo "agentic coding".
El coding es el primer dominio maduro, pero el lenguaje de patrones subyacente es más amplio.

## Los Patrones Como Conocimiento Operativo Memético

Los patrones son meméticos en el sentido práctico: son unidades culturales compactas que
pueden transmitirse, modificarse y recombinarse. Un buen patrón ayuda a una comunidad a
recordar una solución útil sin requerir que cada persona repita el descubrimiento original.

Los agentic patterns son especialmente meméticos porque median entre humanos y sistemas de IA.
No solo le dicen a los humanos qué hacer. También dan forma a lo que un agente de IA puede
reconocer, elegir y ejecutar.

En este proyecto, un patrón debe ayudar a responder:

- ¿Cuál es la situación recurrente?
- ¿Qué fuerzas la hacen difícil?
- ¿Qué movimiento reutilizable ayuda?
- ¿Qué evidencia o ejemplos lo respaldan?
- ¿Cuándo no debe usarse?
- ¿Cómo puede un agente reconocerlo y aplicarlo?

## El Juicio Humano Sigue Siendo Central

Los sistemas de IA son potentes identificadores de patrones, pero no poseen el objetivo. Los
humanos aportan propósito, gusto, memoria, contexto social, juicio ético y la capacidad de
decidir cuándo debe romperse un patrón.

El objetivo de Agentic Patterns no es, por tanto, automatizar el juicio humano para eliminarlo.
Es hacer que las partes reutilizables del juicio humano sean lo suficientemente legibles para
que las personas y los agentes puedan colaborar mejor.

## Notas de Fuentes

- Christopher Alexander, Sara Ishikawa, Murray Silverstein, et al., *A Pattern Language: Towns,
  Buildings, Construction*, Oxford University Press, 1977.
- Christopher Alexander, *The Timeless Way of Building*, Oxford University Press, 1979.
- Erich Gamma, Richard Helm, Ralph Johnson, John Vlissides, *Design Patterns: Elements of Reusable
  Object-Oriented Software*, Addison-Wesley, 1994.
- El Hillside Group y la comunidad Pattern Languages of Programs continuaron la tradición de
  patrones de software a través de talleres de escritura y conferencias de patrones.

Puntos de entrada públicos útiles:

- [A Pattern Language](https://en.wikipedia.org/wiki/A_Pattern_Language)
- [Pattern language](https://en.wikipedia.org/wiki/Pattern_language)
- [Design Patterns](https://en.wikipedia.org/wiki/Design_Patterns)
- [The Hillside Group](https://en.wikipedia.org/wiki/The_Hillside_Group)
- [Pattern Languages of Programs](https://en.wikipedia.org/wiki/Pattern_Languages_of_Programs)
