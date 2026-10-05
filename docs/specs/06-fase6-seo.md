---
fase: 6
titulo: SEO y documentación — Meta, sitemap, README
estado: definida
depende_de: [3]
---

# Fase 6 — SEO y documentación

## Objetivo

Que el sitio sea encontrable y mantenible: metadatos, sitemap y README con
instrucciones para editar productos, precios y desplegar.

## Alcance

### Incluye

- Título y meta description únicos por página; Open Graph básico
- `sitemap.xml` y `robots.txt` en el build
- Favicon / ícono del sitio
- `README.md`: qué es el proyecto, estructura, cómo editar productos y
  precios, cómo correr en local, cómo desplegar
- `docs/spec.md` actualizado con estados reales de las fases

### No incluye

- Blog, analytics, herramientas de pago por clic
- Dominio propio (Fase 7)

## Entradas / Salidas

- **Entradas**: sitio con catálogo y cotizador funcionando (fases 3–5)
- **Salidas**: build con sitemap; README que permite mantener el sitio sin la IA

## Criterios de aceptación básicos

- Cada página tiene title y description propios
- El build genera `sitemap.xml` y `robots.txt`
- README permite a alguien nuevo editar un producto y un precio

## Dependencias

- Fase 3 (páginas); conviene después de Fase 5 para documentar todo

## Refinamiento — PENDIENTE

<!-- Se completa con `/refine-spec 6` justo antes de implementar. -->
