---
description: Refina la spec de una fase (definida → refinada) sin tocar código
agent: build
---

Refina la spec indicada: $ARGUMENTS

1. Localiza el archivo en `docs/specs/` por número de fase (`NN-*`) o por nombre.
   Si no existe o no queda claro a cuál se refiere, detente y lista las specs disponibles.
2. Lee `docs/specs/TEMPLATE.md` y `docs/spec.md` (decisiones globales de negocio).
3. Si el estado ya es `refinada` o `implementada`, dilo y pregunta si desea re-refinar.
4. Rellena la sección `## Refinamiento` de la spec con:
   - Detalles técnicos concretos: archivos a crear/modificar con rutas exactas
   - Lista ordenada de tareas pequeñas y verificables
   - Criterios de aceptación testables (comportamiento observable, no vagos)
   - Datos de ejemplo o placeholders necesarios
   - Riesgos, supuestos y preguntas abiertas para el usuario
5. Actualiza el frontmatter a `estado: refinada`.
6. NO toques código ni archivos fuera de `docs/specs/`.
7. Resume los cambios realizados y pide la aprobación del usuario antes de
   continuar (el siguiente paso será `/implement-spec <n>`).
