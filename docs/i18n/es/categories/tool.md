# Patrones de Herramientas

Los patrones de herramientas definen cómo los agentes deben usar comandos de shell,
navegadores, servidores MCP, APIs, gestores de paquetes, Git y otras capacidades que pueden
afectar el estado real.

Usa patrones de herramientas cuando el agente debe actuar a través de capacidades externas y
el radio de impacto debe ser explícito.

## Patrones Actuales

- [Contrato de Uso de Herramientas (Tool-Use Contract)](../../../../patterns/tool/tool-use-contract.md):
  define las herramientas permitidas, los disparadores de aprobación, las acciones prohibidas
  y las expectativas de evidencia.

## Ideas de Patrones

- Read-First Tooling.
- Approval Boundary.
- Verification Command.
- External State Guard.

## Categorías Relacionadas

- [Patrones de Harness](harness.md)
- [Patrones de Prompt](prompt.md)
- [Patrones de Evaluación](evaluation.md)
