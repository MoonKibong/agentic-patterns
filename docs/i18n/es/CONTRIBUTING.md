# Guía de Contribución

Agentic Patterns está destinado a convertirse en un catálogo compartido de práctica reutilizable.
Las contribuciones deben hacer que el trabajo repetido entre humanos e IA sea más fácil de
reconocer, discutir y ejecutar.

## Formas de Contribuir

- Añade un nuevo patrón usando [patterns/_template.md](../../../patterns/_template.md).
- Mejora los ejemplos, la aplicabilidad o los modos de fallo de un patrón existente.
- Añade notas de campo de sesiones reales de agentic coding.
- Construye herramientas que validen, indexen, recomienden o empaqueten patrones para agentes.
- Propón una taxonomía de catálogo mejor.

## Antes de Añadir un Patrón

Pregúntate si la entrada es realmente un patrón:

- ¿Resuelve un problema recurrente?
- ¿Puede otra persona aplicarlo en una situación similar?
- ¿Son visibles los tradeoffs?
- ¿Puede un agente reconocer cuándo usarlo?
- ¿Hay al menos alguna evidencia o experiencia concreta detrás de él?

Si la respuesta aún no es clara, añade una nota de campo o un patrón en borrador en lugar de
presentarlo como algo establecido.

## Notas de Campo

Usa [field-notes/_template.md](../../../field-notes/_template.md) cuando una observación es
útil pero aún no es lo suficientemente estable para convertirse en un patrón.

Las buenas notas de campo registran:

- La forma de la tarea.
- La configuración del agente.
- Lo que ocurrió.
- Lo que mejoró o falló.
- Qué patrón puede estar emergiendo.
- Qué evidencia haría el patrón más sólido.

## Higiene de Evidencia

No contribuyas detalles propietarios de soluciones. La evidencia del patrón debe ser una de:

- Ejemplos sintéticos que preserven la estructura del problema.
- Notas de campo sanitizadas con detalles privados eliminados.
- Ejemplos públicos de repositorios abiertos, papers, posts de blog o hilos de issues.
- Observaciones generalizadas sin identificadores privados.

Nunca incluyas datos de clientes, credenciales, URLs privadas, nombres de repositorios
privados, texto de prompts internos ni transcripciones completas de flujos de trabajo propietarios.

## Proceso de Entrada de Patrón

1. Copia `patterns/_template.md` al directorio de categoría correspondiente.
2. Rellena el bloque de metadatos.
3. Escribe el patrón en términos operativos.
4. Incluye al menos un ejemplo.
5. Incluye los modos de fallo conocidos y las contraindicaciones.
6. Enlaza los patrones relacionados.
7. Actualiza [catalog/README.md](../../../catalog/README.md).

## Documentación Localizada

Los inicios rápidos localizados en docs/i18n/ son puntos de entrada públicos.
Al cambiar la descripción del proyecto, las categorías principales, el lenguaje de
seguridad/privacidad o el flujo de trabajo de contribución, actualiza los inicios rápidos
localizados o indica en el pull request por qué no se necesita actualización de traducción.

Si no puedes actualizar un idioma con confianza, mantén el cambio en la fuente en inglés
pequeño y solicita revisión de traducción.

## Estándar de Evidencia

La evidencia puede ser ligera al principio, pero debe ser honesta.

La evidencia útil incluye:

- Un flujo de trabajo repetido observado en múltiples tareas.
- Una comparación antes/después.
- Un extracto de transcripción o incidente resumido.
- Un resultado de test, resultado de revisión o defecto evitado.
- Una convención local que sobrevivió el uso repetido.

Evita afirmaciones vagas como "funciona mejor" sin explicar qué mejoró.

## Tono

Escribe para humanos capaces y agentes capaces. Sé directo, específico y humilde sobre la
incertidumbre.

Este proyecto no debe convertirse en una lista de trucos de prompts inspiracionales. Debe
convertirse en un lenguaje de patrones práctico.
