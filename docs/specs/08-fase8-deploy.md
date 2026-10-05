---
fase: 8
titulo: Deploy — Cloudflare Pages / Netlify con subdominio gratis
estado: definida
depende_de: [7]
---

# Fase 8 — Deploy: publicación con subdominio gratis

## Objetivo

Sitio online en hosting gratuito con deploy automático desde GitHub, más
instrucciones para conectar un dominio propio cuando el usuario lo decida.

## Alcance

### Incluye

- Push completo del repo (ramas `main` y `dev`) a github.com/jhuazjp/e3d
- Conectar el repo a Cloudflare Pages o Netlify (elegir uno)
- Build de producción en el hosting desde la rama `main`
- Subdominio gratis asignado (`tusitio.pages.dev` o `tusitio.netlify.app`)
- Documentación de los pasos para apuntar un dominio propio después
  (nameservers o DNS + HTTPS automático)
- Nota sobre cómo publicar cambios: merge `dev` → `main`

### No incluye

- Compra de dominio (decisión pendiente del usuario)
- Email con dominio propio
- Checkout / pagos

## Entradas / Salidas

- **Entradas**: repo en GitHub con sitio verificado (build OK)
- **Salidas**: URL pública accesible + guía de dominio propio en el README

## Criterios de aceptación básicos

- El sitio responde en la URL del subdominio con el build correcto
- Cada merge a `main` dispara deploy automático
- README documenta cómo conectar dominio propio (pasos y costos)

## Dependencias

- Fase 7 (sitio completo y documentado); cuenta gratuita en el hosting elegido

## Refinamiento — PENDIENTE

<!-- Se completa con `/refine-spec 8` justo antes de implementar. -->
