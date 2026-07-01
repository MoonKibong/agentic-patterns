# Tendencias del Trabajo Agéntico 2026

Esta nota resume señales públicas recientes sobre agentic coding y flujos de trabajo creativos
adyacentes. Usa la salida de investigación de Gemini como entrada, pero solo registra aquí
afirmaciones que son seguras, útiles y que están verificadas desde fuentes públicas o
claramente enmarcadas como pistas de investigación.

## Resumen Ejecutivo

El agentic coding se está convirtiendo en la biblioteca de patrones inicial más concreta para
el trabajo con IA guiado por humanos: los repositorios, shells, tests, revisiones de código,
sandboxes y pull requests hacen visibles el contexto y la verificación. Los mismos primitivos
están apareciendo en flujos de trabajo de generación de imágenes, escritura, diseño,
video/medios e investigación:

- paquetes de contexto y briefs delimitados
- agentes o subagentes específicos de rol
- protocolos de uso de herramientas
- bucles generate-critique-refine
- bucles plan-execute-verify-review
- estado durable y artefactos de transferencia
- seguimiento de procedencia y citas
- gates de aprobación humana
- wrappers de seguridad y gobernanza

El catálogo debe, por tanto, mantenerse organizado en torno a primitivos reutilizables,
mientras que las páginas de dominio muestran cómo esos primitivos aplican al coding,
generación de imágenes, escritura, diseño, video/medios e investigación.

## Notas de Fuentes Verificadas

| Fuente | Fecha | Relevancia |
| --- | --- | --- |
| [OpenAI, Introducing Codex](https://openai.com/index/introducing-codex/) | 2025 | Codex presenta ejecución de tareas en la nube para ingeniería de software, reforzando la delegación de tareas en sandbox, contexto de repositorio, ejecución de tests y flujos de trabajo estilo PR. |
| [OpenAI Agents SDK Docs](https://openai.github.io/openai-agents-python/) | 2025-2026 | Documenta agentes, handoffs, guardrails, tracing y herramientas como primitivos de primera clase. |
| [Anthropic Claude Code Subagents](https://docs.anthropic.com/en/docs/claude-code/sub-agents) | 2025-2026 | Describe subagentes específicos de tarea con ventanas de contexto separadas, prompts personalizados y permisos de herramientas. |
| [Anthropic Claude Code Hooks](https://docs.anthropic.com/en/docs/claude-code/hooks) | 2025-2026 | Muestra puntos de control deterministas alrededor del comportamiento del agente, útiles para gates de aprobación y gobernanza de herramientas. |
| [Model Context Protocol Introduction](https://modelcontextprotocol.io/introduction) | 2025-2026 | Enmarca MCP como una forma estándar para que las aplicaciones expongan herramientas y contexto a los modelos de lenguaje. |
| [Google A2A Protocol](https://developers.googleblog.com/en/a2a-a-new-era-of-agent-interoperability/) | 2025 | Muestra el creciente interés en la interoperabilidad y delegación entre agentes. |
| [arXiv: The 2025 AI Agent Index](https://arxiv.org/abs/2602.17753) | 2026 | Examina los sistemas de agentes de IA y refuerza la necesidad de evaluar las capacidades y los patrones de despliegue de los agentes. |
| [arXiv: VideoAgent](https://arxiv.org/abs/2606.23327) | 2026 | Demuestra la descomposición agéntica para flujos de trabajo de edición de video. |
| [HKUDS ViMax](https://github.com/HKUDS/ViMax) | 2026 | Repositorio público para generación agéntica de video a partir de entradas de texto/historia, útil como pista de investigación para pipelines de medios. |

## Tendencia: La Ingeniería de Contexto se Convierte en una Superficie de Producto

Los sistemas agénticos tratan cada vez más el contexto como entrada estructurada en lugar de
historial de chat. Los agentes de coding usan archivos del repositorio, instrucciones, texto
de issues, tests y estado del entorno. Los sistemas creativos necesitan briefs equivalentes:
referencias, restricciones de estilo, anclajes de continuidad, audiencia, entregables y
criterios de evaluación.

Impacto en el catálogo:

- Mantener [Paquete de Contexto (Context Packet)](../../../../patterns/context/context-packet.md) como el patrón general.
- Añadir [Paquete de Brief Creativo (Creative Brief Packet)](../../../../patterns/context/creative-brief-packet.md) para dominios creativos.
- Considerar futuros patrones `Reference Board`, `Source Ledger` y `Context Compactor`.

## Tendencia: Los Agentes se Envuelven en Harnesses

El cambio importante no son solo los modelos más potentes. Los sistemas útiles envuelven los
modelos con planificación, ejecución, crítica, verificación, guardrails, tracing y gates de
aprobación. En coding esto aparece como plan-execute-test-review. En trabajo creativo aparece
como brief-generate-critique-refine-select.

Impacto en el catálogo:

- Mantener bucles explícitos de revisión y verificación para software y otro trabajo verificable.
- Añadir [Generar-Criticar-Refinar (Generate-Critique-Refine)](../../../../patterns/harness/generate-critique-refine.md) para trabajo creativo y exploratorio.
- Añadir futuros patrones `Rubric Review`, `Human Approval Gate` y `Guardian Gate`.

## Tendencia: Los Protocolos de Herramientas y la Interoperabilidad de Agentes Importan

MCP y los protocolos agente-a-agente muestran que los flujos de trabajo agénticos dependen
cada vez más de límites de capacidad explícitos. Las herramientas y los sistemas externos
deben ser descubribles, delimitados, auditados y seguros de usar.

Impacto en el catálogo:

- Mantener [Contrato de Uso de Herramientas (Tool-Use Contract)](../../../../patterns/tool/tool-use-contract.md).
- Añadir futuros patrones `Capability Manifest`, `Approval Boundary` y `Sandbox Gate`.

## Tendencia: El Trabajo Creativo Necesita Patrones de Ciclo de Vida de Artefactos

Los flujos de trabajo de imágenes, escritura, diseño y video generan artefactos intermedios:
briefs, referencias, esquemas, tableros de estilo, imágenes candidatas, storyboards, planes de
escenas, tablas de crítica y assets finales. Esos artefactos necesitan transferencia, procedencia,
versionado y aprobación humana.

Impacto en el catálogo:

- Añadir páginas de dominio en lugar de dividir el catálogo principal demasiado pronto.
- Añadir futuros patrones `Artifact Handoff`, `Provenance Ledger`, `Variation Ladder`,
  `Style Lock` y `Continuity Ledger`.

## Higiene de Fuentes

La salida de investigación de Gemini incluía pistas útiles, pero este repositorio no debe
tratar las citas generadas como verificadas por defecto. Para documentación pública:

- preferir fuentes primarias y documentación oficial
- marcar los elementos no verificados como pistas
- no citar flujos de trabajo privados
- usar ejemplos sintéticos cuando la evidencia pública revelaría métodos propietarios
