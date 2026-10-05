# Especificación global — Sitio de impresión 3D

> Documento vivo. Las specs por fase viven en `docs/specs/` y se refinan con
> `/refine-spec <n>` justo antes de implementarse. Flujo:
> `definida` → `/refine-spec <n>` → `refinada` → `/implement-spec <n>` → `implementada`.

## Visión

Sitio web "lite" para un negocio personal de impresión 3D (Bambu Lab A1):

- **Catálogo**: ~20 productos en 5 categorías (PLA, PETG, TPU, Accesorios, Personalizados)
- **Personalizados**: el cliente sube un STL → cotización instantánea en el navegador
  → envío de la solicitud por WhatsApp y/o email
- **Escalable**: camino abierto a checkout (Snipcart / Stripe / Mercado Pago) sin rehacer el sitio

## Decisiones técnicas

| Tema | Decisión |
|------|----------|
| Stack | Astro (estático) + Tailwind CSS + JS vanilla |
| Backend | Ninguno inicialmente — todo client-side |
| Cotización STL | Parser propio en el navegador (binario + ASCII), sin librerías pesadas |
| Envíos | WhatsApp (`wa.me` con mensaje pre-lleno) + email vía Web3Forms |
| Hosting | Cloudflare Pages o Netlify (gratis); dominio propio: decidir después |
| Repo | github.com/jhuazjp/e3d — `main` estable/deploy, `dev` desarrollo |
| Idioma | Documentación e interfaz en español |

## Reglas de negocio — Cotización

- `gramos = volumen_STL (cm³) × densidad(material) × factor_relleno`
- `precio = gramos × precio_por_gramo + horas_estimadas × tarifa_máquina + extras`
- Densidades de referencia: PLA 1,24 · PETG 1,27 · TPU 1,21 g/cm³
- Todos los parámetros (precios, densidades, tarifas, margen, moneda) viven en
  `src/data/pricing-config.json` — editables sin tocar la lógica
- El resultado siempre se presenta como **estimado** (el corte exacto lo calcula Bambu Studio)

## Índice de fases

| # | Spec | Estado |
|---|------|--------|
| 1 | [Fase 1 — Foundation](specs/01-fase1-foundation.md) | definida |
| 2 | [Fase 2 — Datos](specs/02-fase2-data.md) | definida |
| 3 | [Fase 3 — Catálogo](specs/03-fase3-catalogo.md) | definida |
| 4 | [Fase 4 — Cotizador STL](specs/04-fase4-cotizador.md) | definida |
| 5 | [Fase 5 — Envíos](specs/05-fase5-envios.md) | definida |
| 6 | [Fase 6 — SEO y docs](specs/06-fase6-seo.md) | definida |
| 7 | [Fase 7 — Deploy](specs/07-fase7-deploy.md) | definida |

Actualizar esta tabla cuando cambie el estado de una spec.
