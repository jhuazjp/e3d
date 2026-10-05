---
fase: 4
titulo: Catálogo — Home, listado con filtros y detalle
estado: definida
depende_de: [2, 3]
---

# Fase 4 — Catálogo: home, listado con filtros y detalle

## Objetivo

Páginas públicas del sitio: inicio, catálogo filtrable por categoría y detalle
de producto, con layout compartido.

## Alcance

### Incluye

- Layout: header con navegación, footer con contacto/WhatsApp
- `/` — inicio: destacados, categorías, llamada a cotizar
- `/productos` — listado completo con filtro por categoría
- `/productos/[slug]` — detalle: descripción, specs, precio, CTA
- Componentes: `ProductCard`, `CategoryFilter`, etc., construidos sobre los
  tokens y componentes base de la Fase 3
- Responsive (mobile-first)

### No incluye

- Cotizador (Fase 5), envíos (Fase 6), SEO amplio (Fase 7)

## Entradas / Salidas

- **Entradas**: datos de la Fase 2 y sistema de diseño de la Fase 3
- **Salidas**: 3 rutas renderizando los 20 productos reales de ejemplo

## Criterios de aceptación básicos

- Los 20 productos aparecen listados desde los JSON
- El filtro por categoría muestra/oculta productos sin recargar
- Cada producto tiene página de detalle accesible desde el listado
- Navegable en móvil y escritorio

## Dependencias

- Fase 2 (datos) y Fase 3 (sistema de diseño)

## Refinamiento — PENDIENTE

<!-- Se completa con `/refine-spec 4` justo antes de implementar. -->
