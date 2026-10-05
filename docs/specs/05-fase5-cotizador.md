---
fase: 5
titulo: Cotizador STL — Análisis en navegador y estimado de precio
estado: definida
depende_de: [1, 3]
---

# Fase 5 — Cotizador STL: análisis en navegador y estimado de precio

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

- Envío de la cotización (Fase 6)
- Vista 3D del modelo
- Precisión de slicer real (Bambu Studio es la referencia final)

## Entradas / Salidas

- **Entradas**: STL del usuario + `pricing-config.json` (Fase 2); UI sobre los
  componentes de la Fase 3
- **Salidas**: desglose de precio visible en pantalla, sin llamadas de red

## Criterios de aceptación básicos

- STL binario y ASCII de prueba producen volumen y dimensiones coherentes
- Precio calculado con la fórmula de `docs/spec.md` y parámetros editables
- Archivo inválido muestra error claro sin romper la página
- Funciona sin conexión (cálculo local)

## Dependencias

- Fase 1 (estructura) y Fase 3 (diseño); usa `pricing-config.json` de la Fase 2

## Refinamiento — PENDIENTE

<!-- Se completa con `/refine-spec 5` justo antes de implementar. -->
