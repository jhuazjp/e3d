---
fase: 2
titulo: Datos — Categorías, productos y config de precios
estado: definida
depende_de: [1]
---

# Fase 2 — Datos: categorías, productos y configuración de precios

## Objetivo

Crear la capa de datos editable sin tocar lógica: categorías, 20 productos de
ejemplo y parámetros de cotización.

## Alcance

### Incluye

- `src/data/categories.json` — 5 categorías (PLA, PETG, TPU, Accesorios, Personalizados)
- `src/data/products.json` — 20 productos placeholder (nombre, slug, categoría,
  precio, descripción, imagen placeholder, specs)
- `src/data/pricing-config.json` — precios por gramo, densidades, tarifa de
  máquina/hora, factor de relleno, margen, moneda
- Tipos/lectura de datos para usar en siguientes fases

### No incluye

- Páginas que muestren los datos (Fase 3)
- Motor de cotización (Fase 4)
- Fotos reales (placeholders mientras tanto)

## Entradas / Salidas

- **Entradas**: estructura de la Fase 1, reglas de negocio de `docs/spec.md`
- **Salidas**: tres JSON válidos + forma tipada de consumirlos

## Criterios de aceptación básicos

- Build falla si un JSON es inválido
- 20 productos referencian categorías existentes
- `pricing-config.json` contiene todos los parámetros de la fórmula de cotización

## Dependencias

- Fase 1 (estructura del proyecto)

## Refinamiento — PENDIENTE

<!-- Se completa con `/refine-spec 2` justo antes de implementar. -->
