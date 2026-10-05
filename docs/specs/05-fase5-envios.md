---
fase: 5
titulo: Envíos — WhatsApp y email (Web3Forms)
estado: definida
depende_de: [4]
---

# Fase 5 — Envíos: WhatsApp y email (Web3Forms)

## Objetivo

Que la cotización y las consultas lleguen al negocio por dos canales:
WhatsApp con mensaje pre-lleno y formulario por email.

## Alcance

### Incluye

- Botón de WhatsApp: `wa.me/<número>` con resumen pre-lleno de la cotización
  (material, dimensiones, precio estimado, cantidad)
- Formulario de contacto/cotización vía Web3Forms (access key en config)
- Campos: nombre, contacto, mensaje, resumen de la cotización; STL solo si
  el límite gratuito lo permite (si no, el cliente lo adjunta en WhatsApp)
- Validación básica de campos obligatorios
- Estados de éxito/error en el formulario

### No incluye

- Backend propio ni base de datos
- Pasarela de pagos

## Entradas / Salidas

- **Entradas**: resultado del cotizador (Fase 4), número de WhatsApp y
  access key de Web3Forms (los aporta el usuario)
- **Salidas**: mensaje abierto en WhatsApp / email enviado al negocio

## Criterios de aceptación básicos

- El botón de WhatsApp abre chat con el resumen correcto y codificado
- El formulario envía el email o indica claramente qué falta configurar
- El usuario puede usar ambos canales desde la página de cotización

## Dependencias

- Fase 4 (resultado de cotización); número de WhatsApp y clave Web3Forms del usuario

## Refinamiento — PENDIENTE

<!-- Se completa con `/refine-spec 5` justo antes de implementar. -->
