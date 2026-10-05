---
fase: 7
titulo: SEO y documentación — Meta, sitemap, README
estado: definida
depende_de: [4]
---

# Fase 7 — SEO y documentación

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
- Dominio propio (Fase 8)

## Entradas / Salidas

- **Entradas**: sitio con catálogo y cotizador funcionando (fases 4–6)
- **Salidas**: build con sitemap; README que permite mantener el sitio sin la IA

## Criterios de aceptación básicos

- Cada página tiene title y description propios
- El build genera `sitemap.xml` y `robots.txt`
- README permite a alguien nuevo editar un producto y un precio

## Dependencias

- Fase 4 (páginas); conviene después de Fase 6 para documentar todo

## Refinamiento — PENDIENTE

<!-- Se completa con `/refine-spec 7` justo antes de implementar. -->
