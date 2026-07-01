# Preparación para Código Abierto

Este documento registra los valores predeterminados recomendados de lanzamiento público para
Agentic Patterns.

## Evaluación de Tarea

Veredicto: `REVISE` hasta que la licencia esté finalizada y los inicios rápidos traducidos
tengan una revisión humana.

Alcance: documentación del repositorio, catálogo de patrones, plantillas de GitHub, i18n,
flujo de trabajo de contribución y posicionamiento público.

Riesgo principal: el proyecto está inspirado en flujos de trabajo agénticos reales, por lo
que los documentos públicos deben evitar exponer prompts propietarios, detalles privados de
harness, datos de clientes, nombres de repositorios privados y transcripciones internas de
flujos de trabajo.

## Posicionamiento

Mejor opción: presentar Agentic Patterns como un lenguaje de patrones para el trabajo con IA
guiado por humanos, no como una colección de prompts. El coding es el primer dominio maduro,
pero el catálogo también cubre generación de imágenes, escritura, diseño, video/medios,
investigación y análisis.

## Licencia

Decisión actual:

- Documentación, catálogo de patrones, prompts y notas de campo: CC BY 4.0.
- Código, esquemas y artefactos de software aprobados: MIT.

## Etapa de Lanzamiento

Mejor opción: publicar el primer lanzamiento público como `v0.1.0` con lenguaje de etapa
semilla. Evitar presentar los patrones en borrador como mejores prácticas validadas.

## Política de Evidencia y Privacidad

Mejor opción: requerir ejemplos sintéticos, sanitizados o explícitamente públicos. Tratar
la filtración accidental de prompts privados, datos de clientes, URLs privadas o detalles de
flujos de trabajo propietarios como sensible a la seguridad.

## CI

Para este repositorio público basado en Markdown, el CI puede comenzar con lint de markdown
y verificación de enlaces una vez que los validadores públicos estén aprobados.

## Contribuciones

Requerir que los PRs incluyan:

- resumen de cambios de documentos o patrones visibles para el usuario
- comandos de verificación
- impacto en evidencia/privacidad
- impacto en i18n
- enlaces a issues relacionados

## Checklist de Publicación

1. Finalizar los archivos de licencia.
2. Confirmar que `README.md`, `CONTRIBUTING.md`, `SECURITY.md`, `CODE_OF_CONDUCT.md`, `CHANGELOG.md` y
   `RELEASE.md` están presentes.
3. Confirmar que existen plantillas de issues y PRs.
4. Ejecutar las revisiones y verificaciones públicas aprobadas.
5. Revisar los inicios rápidos de `docs/i18n/`.
6. Buscar términos privados, URLs privadas, credenciales y nombres de repositorios internos.
7. Crear un release de GitHub con lenguaje de etapa semilla.

## Checklist de Decisiones

| Elemento | Mejor Opción | Estado |
| --- | --- | --- |
| Promesa del producto | Lenguaje de patrones para trabajo con IA guiado por humanos | Documentado |
| Licencia | CC BY 4.0 para docs + MIT para código | Presente |
| README | Alcance, catálogo, validación, higiene de evidencia | Presente |
| Changelog | Estilo Keep a Changelog con `Unreleased` | Presente |
| Contributing | Expectativas de patrón, evidencia, i18n | Presente |
| Security | Informes de filtración privada y automatización insegura | Presente |
| Código de conducta | Política ligera aplicada por mantenedores | Presente |
| Plantillas de issues | Propuesta de patrón presente; se recomiendan más plantillas | Parcial |
| Plantilla de PR | Resumen, validación, i18n, impacto en privacidad | Presente |
| CI | Verificaciones públicas de markdown/enlaces | Aún no presente |
| Proceso de release | Checklist semilla `v0.1.0` | Presente |

## Criterios de Aceptación

- Los documentos públicos explican qué es el proyecto y qué no es.
- Los mantenedores tienen instrucciones de lanzamiento y rollback.
- Los contribuidores tienen expectativas de configuración, validación, patrones, privacidad e i18n.
- Existen inicios rápidos localizados y afirman que los documentos en inglés siguen siendo la fuente de verdad.
- No se requieren detalles propietarios de soluciones para entender o contribuir patrones.
