---
fase: 1
titulo: Foundation — Scaffold Astro + Tailwind
estado: definida
depende_de: []
---

# Fase 1 — Foundation: Scaffold Astro + Tailwind

## Objetivo

Proyecto Astro con Tailwind instalado, estructura de carpetas base y comandos de
verificación funcionando, sobre la rama `dev`.

## Alcance

### Incluye

- Inicializar Astro (TypeScript, sin plantillas de ejemplo al terminar)
- Tailwind CSS integrado
- Estructura: `src/components/`, `src/pages/`, `src/data/`, `src/lib/`
- Scripts npm: `dev`, `build`, `check` (`astro check`)
- `.gitignore` apropiado (node_modules, dist, .astro)

### No incluye

- Contenido de productos, páginas del catálogo ni lógica de cotización
- Deploy

## Entradas / Salidas

- **Entradas**: estructura de specs y decisiones de `docs/spec.md`
- **Salidas**: `npm run dev` sirve una página base; `npm run build` genera `dist/`

## Criterios de aceptación básicos

- `npm run build` sin errores
- `npm run astro check` sin errores
- Estructura de carpetas creada según lo indicado

## Dependencias

- Ninguna (fase inicial)

## Refinamiento — PENDIENTE

<!-- Se completa con `/refine-spec 1` justo antes de implementar. -->
