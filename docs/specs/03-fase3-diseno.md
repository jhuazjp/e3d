---
fase: 3
titulo: Diseño — Sistema de diseño inicial
estado: definida
depende_de: [1]
---

# Fase 3 — Diseño: sistema de diseño inicial

## Objetivo

Definir un sistema de diseño (tokens + componentes base + guía) que unifique el
aspecto del sitio y acelere las fases de UI (catálogo, cotizador, contacto).

## Alcance

### Incluye

- Identidad básica propuesta por la IA y **aprobada por el usuario**:
  paleta (primario, acento, neutrales, estados éxito/error), tipografía
  (títulos/cuerpo), escala de espaciado, radios y sombras
- Tokens en Tailwind (variables CSS), sin valores de color hardcodeados en
  componentes
- Componentes base en `src/components/ui/`:
  - `Button` (variantes: primario, secundario, fantasma; estados hover/focus)
  - `Input` / `Select` / `Textarea` con labels y errores
  - `Card` (para productos)
  - `Badge` (categorías/etiquetas)
  - `Section` / `Container` (maquetación de página)
- Guía de estilo `docs/design.md`: tokens, reglas de uso y ejemplos de cada componente

### No incluye

- Página `/styleguide`
- Mockups de páginas completas ni diseño en Figma
- Logo profesional, fotos o animaciones complejas

## Entradas / Salidas

- **Entradas**: scaffold de la Fase 1; propuesta de identidad (paleta y
  tipografía) que el usuario aprueba durante el refinamiento
- **Salidas**: tokens configurados + componentes importables + `docs/design.md`

## Criterios de aceptación básicos

- Paleta y tipografía aprobadas por el usuario antes de implementar
- Componentes usan tokens (cero colores arbitrarios) y son accesibles (focus visible, contraste)
- `docs/design.md` documenta cada componente con ejemplo de uso
- `npm run build` y `npm run astro check` sin errores

## Dependencias

- Fase 1 (estructura). Puede ejecutarse en paralelo con la Fase 2 (datos)

## Refinamiento — PENDIENTE

<!-- Se completa con `/refine-spec 3` justo antes de implementar. -->
