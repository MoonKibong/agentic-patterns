# Lenguaje de Patrones

Este documento define la estructura y los criterios de calidad para las entradas de Agentic Patterns.

## Definición

Un agentic pattern es una solución reutilizable con nombre para un problema recurrente en el
trabajo entre humanos e IA.

Un patrón puede describir:

- Estructura de prompt.
- Estructura de contexto.
- Harness de planificación o ejecución.
- Bucle de revisión y verificación.
- Contrato de rol de agente.
- Protocolo MCP/herramienta.
- Movimiento de coordinación multiagente.
- Práctica de memoria y gestión de estado.

Los patrones no se limitan a la ingeniería de software. El coding es el dominio inicial
adecuado porque los tests, el repositorio, las herramientas y los bucles de revisión son
claros. Pero la misma estructura aplica a la generación de imágenes, escritura, diseño,
producción de video/medios, investigación y análisis.

## Metadatos del Patrón

Cada patrón comienza con un bloque de metadatos pequeño.

```yaml
---
id: context-packet
name: Context Packet
category: context
status: draft
applies_to:
  - coding agents
  - planning
  - implementation
domains:
  - coding
related:
  - durable-session-state
---
```

`id` debe ser estable y en formato lowercase-hyphen. `domains` es opcional pero recomendado.
Ejemplos: `coding`, `image-generation`, `writing`, `design`, `video-media`,
`research-analysis`, `general`.

## Secciones del Patrón

Usa las siguientes secciones salvo que haya una razón específica para no hacerlo.

### Intent (Intención)

Describe el movimiento reutilizable en una o dos oraciones.

### Also Known As (También Conocido Como)

Otros nombres si los hay.

### Problem (Problema)

El problema recurrente que resuelve este patrón.

### Context (Contexto)

La situación, las precondiciones y los supuestos del entorno donde aplica el patrón.

### Forces (Fuerzas)

Las tensiones que hacen el problema no trivial. Ejemplos:

- Más context puede ayudar al agente, pero demasiado context puede enterrar la señal importante.
- Más autonomy puede acelerar la ejecución, pero una autonomy sin límites puede ocultar riesgos.
- Más agentes pueden paralelizar el trabajo, pero el overhead de coordination puede superar el beneficio.

### Solution (Solución)

La estructura, protocolo, prompt, harness o comportamiento de herramienta reutilizable.

### Agent Recognition Signals (Señales de Reconocimiento del Agente)

Señales observables que indican que un agente debería considerar este patrón.

### Procedure (Procedimiento)

Pasos concretos que puede seguir una persona o un agente.

### Outputs (Salidas)

Artefactos que deberían generarse después de aplicar el patrón.

### Stop Conditions (Condiciones de Parada)

Cuándo detenerse, escalar o cambiar a otro patrón.

### Example (Ejemplo)

Un ejemplo breve y realista. Si el flujo de trabajo real podría exponer detalles de
implementación privada, datos de clientes o mecánicas internas de orquestación, se prefieren
los ejemplos sintéticos.

### Failure Modes (Modos de Fallo)

Formas en que el patrón se aplica incorrectamente.

### Evidence (Evidencia)

Observaciones, notas de campo, tests, resultados de revisión, fuentes públicas, etc.

La evidencia debe ser publicable. Usa resúmenes sanitizados, reproducciones sintéticas o
fuentes públicas; no expongas prompts privados, lógica interna de harness propietario, datos
de clientes, nombres de repositorios privados, credenciales ni transcripciones internas.

### Related Patterns (Patrones Relacionados)

Patrones que se usan juntos, que entran en conflicto o que se reemplazan entre sí.

## Estado del Patrón

- `draft`: tiene potencial pero aún no está estabilizado.
- `candidate`: se ha usado con éxito varias veces y está listo para revisión.
- `accepted`: ha pasado por revisión y está reconocido como parte del catálogo.
- `deprecated`: se mantiene como referencia histórica pero ya no se recomienda.

## Categorías

Categorías iniciales:

- `prompt`: estructuras de instrucción reutilizables.
- `context`: estructura de paquete de contexto.
- `harness`: flujos de trabajo de planificación, ejecución, revisión y verificación.
- `orchestration`: coordinación multiagente y multisesión.
- `tool`: patrones de interacción con MCP, CLI, script y entorno.
- `memory`: patrones de conocimiento durable y estado.
- `evaluation`: cómo juzgar si un patrón funcionó.

Las categorías pueden cambiar a medida que el catálogo madura.

## Higiene de Evidencia

Los ejemplos de patrones deben enseñar la estructura reutilizable, no el incidente privado en sí.

Permitido:

- Ejemplos sintéticos que preserven las fuerzas y el procedimiento.
- Notas de campo sanitizadas con identificadores privados eliminados.
- Referencias públicas de repositorios de código abierto, papers, docs, blogs, hilos de issues, etc.
- Observaciones agregadas como "observado en varias sesiones locales de coding".

Prohibido:

- Nombres de repositorios privados, nombres de clientes, URLs privadas, credenciales, logs.
- Prompts propietarios completos, internos de harness, protocolos MCP/herramienta.
- Transcripciones que revelen dirección de producto no publicada o detalles de implementación interna.

En caso de duda, generaliza el escenario y mantén el patrón operativo.

## Reglas de Nombres

Los nombres de patrones deben ser:

- Cortos.
- Memorables.
- Operativos.
- Suficientemente específicos para distinguir el movimiento.

Evita nombres que solo describan un objetivo, como `Better Coding` o `Good Context`.

## Legibilidad por Máquina

Los archivos de patrones deben seguir siendo útiles como Markdown normal. El bloque de metadatos existe
para que los futuros mantenedores puedan:

- Construir índices.
- Verificar campos faltantes.
- Recomendar patrones a los agentes.
