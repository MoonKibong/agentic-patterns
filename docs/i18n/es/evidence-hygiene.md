# Higiene de Evidencia

Agentic Patterns debe ser útil sin exponer detalles propietarios de soluciones.

El catálogo puede basarse en experiencia real, pero se deben proteger los prompts privados,
harnesses, repositorios, clientes, credenciales, transcripciones y mecánicas internas de
flujos de trabajo.

## Principio

Haz públicos los patrones, no los incidentes privados.

Los ejemplos deben mostrar la siguiente estructura reutilizable:

- La forma del problema.
- Fuerzas y tradeoffs.
- Procedimiento.
- Salida esperada.
- Modos de fallo.
- Estilo de verificación.

Los ejemplos no deben mostrar detalles de implementación privada.

## Tipos de Evidencia Seguros

- Ejemplos sintéticos que preserven la estructura del flujo de trabajo.
- Notas de campo sanitizadas con identificadores privados eliminados.
- Ejemplos públicos de repositorios de código abierto, papers, docs, blogs, hilos de issues, etc.
- Observaciones agregadas con información de identificación eliminada.

## Qué No Publicar

- Datos de clientes.
- Credenciales, tokens, URLs privadas.
- Nombres de repositorios privados.
- Texto de prompts internos no destinados a ser públicos.
- Lógica completa de harness propietario.
- Transcripción completa de flujo de trabajo de proyectos privados.
- Dirección de producto, estrategia de negocio, detalles de implementación no publicados.

## Sanitización de Notas de Campo

1. Reemplaza los nombres de proyectos con nombres genéricos como `web app`, `API service`, `agent runner`.
2. Reemplaza las rutas de archivos con rutas representativas como `src/billing/service.ts`.
3. Elimina credenciales, nombres de host, números de issues privados, nombres de ramas privadas.
4. Resume las transcripciones en lugar de citarlas directamente.
5. Conserva las condiciones de éxito/fallo relevantes para el patrón.
6. Indica que el ejemplo es sintético o sanitizado.

## Política de Ejemplos Sintéticos

Los ejemplos sintéticos son bienvenidos. No necesitan coincidir con un flujo de trabajo
privado real, pero deben ser lo suficientemente específicos para ser ejecutables.

Un buen ejemplo sintético:

- Incluye archivos, roles y comandos concretos.
- Expone las fuerzas del patrón.
- Muestra qué salida debe producir el agente.
- Evita secretos específicos del proyecto.

Un mal ejemplo sintético es demasiado vago, como "mejorar el código".
