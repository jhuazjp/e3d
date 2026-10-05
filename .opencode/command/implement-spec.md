---
description: Implementa una fase solo si su spec está refinada, con verificación final
agent: build
---

Implementa la spec indicada: $ARGUMENTS

1. Localiza la spec en `docs/specs/` y lee su contenido completo.
2. Si su frontmatter no tiene `estado: refinada`: DETENTE sin implementar nada.
   Indica que primero debe ejecutarse `/refine-spec <n>` y espera instrucciones.
3. Verifica que estás en la rama `dev` (nunca trabajes directo en `main`).
4. Lee `AGENTS.md` y `docs/spec.md` para las reglas y decisiones globales.
5. Implementa las tareas de la sección `## Refinamiento` en orden, de una en una.
6. Al terminar, ejecuta la verificación obligatoria y corrige cualquier error:
   - `npm run build`
   - `npm run astro check`
7. Actualiza el estado de la spec a `implementada`.
8. Presenta un resumen de lo hecho junto con los resultados de la verificación.
   NO hagas commit ni push salvo que el usuario lo pida explícitamente.
