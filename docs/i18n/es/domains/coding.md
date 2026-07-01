# Coding

El coding es el dominio semilla de Agentic Patterns porque expone artefactos claros:
repositorios, archivos, tests, shells, issues, pull requests, CI y veredictos de revisión.

## Fuerzas Comunes

- Los agentes necesitan suficiente contexto del repositorio sin ahogarse en archivos irrelevantes.
- El uso de herramientas puede mutar el estado local o remoto.
- La revisión y los tests pueden detectar defectos, pero solo cuando se hacen parte del flujo de trabajo.
- Las tareas de larga duración necesitan estado durable y transferencias reanudables.

## Patrones Útiles

- [Paquete de Contexto (Context Packet)](../../../../patterns/context/context-packet.md)
- [Contrato de Rol (Role Contract)](../../../../patterns/prompt/role-contract.md)
- [Contrato de Uso de Herramientas (Tool-Use Contract)](../../../../patterns/tool/tool-use-contract.md)
- [Estado de Sesión Durable (Durable Session State)](../../../../patterns/orchestration/durable-session-state.md)

## Patrones Candidatos

- Human Approval Gate.
- Guardian Gate.
- Provenance Ledger.
- Verification Ladder.
- Context Compactor.
