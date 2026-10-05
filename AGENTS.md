# AGENTS.md — Contexto del proyecto

## Qué es

Sitio web de un negocio personal de impresión 3D (impresora Bambu Lab A1).
Catálogo de productos + cotización rápida de piezas personalizadas desde STL.
Usuario hispanohablante: toda la documentación, specs e interfaz en español.

## Stack (decidido, no reabrir)

- Astro (estático) + Tailwind CSS + JavaScript vanilla — sin React ni Next.js
- Sin backend: análisis del STL y cálculo de precios en el navegador (client-side)
- Envíos de cotización: WhatsApp (wa.me) + email vía Web3Forms
- Hosting: Cloudflare Pages o Netlify (gratis); dominio propio opcional, después
- Repo: github.com/jhuazjp/e3d — `main` = estable/deploy, `dev` = desarrollo

## Reglas duras

1. NO implementar una fase cuya spec no tenga `estado: refinada`. Flujo:
   `/refine-spec <n>` → aprobación del usuario → `/implement-spec <n>`.
2. Verificación obligatoria antes de dar una fase por terminada:
   - `npm run build` sin errores
   - `npm run astro check` sin errores
3. Datos de productos, categorías y precios en `src/data/*.json` — editables sin
   tocar lógica. Toda fórmula de cotización vive en `src/lib/` parametrizada
   por `src/data/pricing-config.json`.
4. Trabajar siempre en la rama `dev`. `main` solo recibe merges de fases
   verificadas.
5. No hacer commit ni push sin que el usuario lo pida explícitamente.
6. Estado de las fases: ver índice en `docs/spec.md`. Cada spec es
   autocontenido: leer solo el de la fase actual (más `docs/specs/TEMPLATE.md`).

## Comandos

- `npm run dev` — servidor de desarrollo (desde Fase 1)
- `npm run build` — build de producción (desde Fase 1)
- `npm run astro check` — tipos/validación (desde Fase 1)

## Convenciones

- Español para docs e interfaz; nombres técnicos (archivos, clases, claves JSON) en inglés.
- Componentes en `src/components/`, páginas en `src/pages/`, datos en `src/data/`.
- Imágenes y estáticos en `public/`.
- Sin comentarios en el código salvo que se pidan explícitamente.
