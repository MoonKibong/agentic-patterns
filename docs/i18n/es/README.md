# Wiki de Agentic Patterns

Punto de entrada en español del wiki de Agentic Patterns.

Úsalo como un wiki: parte de la pregunta que tienes, sigue las páginas de categoría y abre
las entradas de patrones individuales cuando necesites detalle operativo.
Los documentos en inglés son la fuente de verdad definitiva; este documento es el espejo en
español de la documentación pública actual.

## Comienza Aquí

- [Resumen del Proyecto](project-brief.md): qué es el proyecto y por qué existe.
- [Raíces del Lenguaje de Patrones](foundations/pattern-language-roots.md): Christopher Alexander, GoF, y
  la motivación para los agentic patterns.
- [Lenguaje de Patrones](pattern-language.md): cómo está estructurada una entrada de patrón.
- [Higiene de Evidencia](evidence-hygiene.md): cómo evitar filtrar detalles privados de soluciones.
- [Tendencias del Trabajo Agéntico](research/2026-agentic-work-trends.md): por qué esto se extiende más allá del coding.
- [Catálogo](../../../catalog/README.md): tabla de patrones actuales.
- [Hoja de Ruta](roadmap.md): hacia dónde va el proyecto.
- [Guía de Contribución](CONTRIBUTING.md): cómo añadir patrones y notas de campo.
- [Preparación para Código Abierto](oss/OPEN_SOURCE_READINESS.md): checklist de publicación.

## Navegar por Objetivo

| Objetivo | Comienza Con |
| --- | --- |
| Entender el proyecto | [Resumen del Proyecto](project-brief.md) |
| Entender las raíces intelectuales | [Raíces del Lenguaje de Patrones](foundations/pattern-language-roots.md) |
| Encontrar un patrón reutilizable | [Catálogo](../../../catalog/README.md) |
| Dar mejor contexto a un agente | [Paquete de Contexto (Context Packet)](../../../patterns/context/context-packet.md) |
| Definir un rol de agente | [Contrato de Rol (Role Contract)](../../../patterns/prompt/role-contract.md) |
| Coordinar trabajo agéntico de larga duración | [Estado de Sesión Durable (Durable Session State)](../../../patterns/orchestration/durable-session-state.md) |
| Limitar uso de shell, MCP o navegador | [Contrato de Uso de Herramientas (Tool-Use Contract)](../../../patterns/tool/tool-use-contract.md) |
| Guiar generación de imágenes, escritura o diseño | [Paquete de Brief Creativo (Creative Brief Packet)](../../../patterns/context/creative-brief-packet.md) |
| Iterar sobre candidatos creativos | [Generar-Criticar-Refinar (Generate-Critique-Refine)](../../../patterns/harness/generate-critique-refine.md) |
| Registrar una observación | [Plantilla de Nota de Campo](../../../field-notes/_template.md) |

## Navegar por Categoría

- [Patrones de Prompt](categories/prompt.md)
- [Patrones de Contexto](categories/context.md)
- [Patrones de Harness](categories/harness.md)
- [Patrones de Herramientas](categories/tool.md)
- [Patrones de Memoria](categories/memory.md)
- [Patrones de Evaluación](categories/evaluation.md)

## Navegar por Dominio

- [Coding](domains/coding.md)
- [Generación de Imágenes](domains/image-generation.md)
- [Escritura y Literatura](domains/writing.md)
- [Generación de Diseño](domains/design.md)
- [Video y Medios](domains/video-media.md)
- [Investigación y Análisis](domains/research-analysis.md)

## Para Agentes

- Lee `AGENTS.md` en la raíz del repositorio antes de editar.
- Preserva el límite público/privado aprobado por los mantenedores antes de cambiar documentos públicos.
- No añadas nombres de patrones privados ni nombres de herramientas locales a documentos públicos.
- Ejecuta el procedimiento de validación del repositorio después de cambiar archivos de patrones.

## Para Contribuidores

- Comienza con la [Guía de Contribución](CONTRIBUTING.md).
- Usa la [Plantilla de Patrón](../../../patterns/_template.md) para patrones nuevos.
- Usa la [Plantilla de Nota de Campo](../../../field-notes/_template.md) para observaciones iniciales.
- Revisa la [Licencia](licensing.md) antes de decisiones de publicación.
- Revisa la [Higiene de Evidencia](evidence-hygiene.md) antes de añadir ejemplos o notas de campo.

## Barra Lateral

La navegación estilo barra lateral está en [_sidebar.md](_sidebar.md).
