---
fase: 4
titulo: Cotizador STL — Análisis en navegador y estimado de precio
estado: definida
depende_de: [1]
---

# Fase 4 — Cotizador STL: análisis en navegador y estimado de precio

## Objetivo

Página `/cotizar`: el cliente sube un STL y obtiene al instante un estimado de
precio (gramos, dimensiones, tiempo, desglose), todo en el navegador.

## Alcance

### Incluye

- Subida/drag&drop de archivos `.stl` (binario y ASCII)
- Parser propio en `src/lib/`: volumen (tetraedros), dimensiones (bbox), triángulos
- Motor de cotización en `src/lib/` parametrizado por `pricing-config.json`
- Selector de material (PLA/PETG/TPU), cantidad y calidad/acabado
- Resultado: desglose con advertencia de "estimado"
- Manejo de errores: archivo no STL, vacío, corrupto, demasiado grande

### No incluye

- Envío de la cotización (Fase 5)
- Vista 3D del modelo
- Precisión de slicer real (Bambu Studio es la referencia final)

## Entradas / Salidas

- **Entradas**: STL del usuario + `pricing-config.json` (Fase 2)
- **Salidas**: desglose de precio visible en pantalla, sin llamadas de red

## Criterios de aceptación básicos

- STL binario y ASCII de prueba producen volumen y dimensiones coherentes
- Precio calculado con la fórmula de `docs/spec.md` y parámetros editables
- Archivo inválido muestra error claro sin romper la página
- Funciona sin conexión (cálculo local)

## Dependencias

- Fase 1 (estructura); usa `pricing-config.json` de la Fase 2

## Refinamiento — PENDIENTE

<!-- Se completa con `/refine-spec 4` justo antes de implementar. -->
