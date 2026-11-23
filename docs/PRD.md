# Documento de Requisitos del Producto (PRD)

| Campo | Valor |
| --- | --- |
| Alumno | Laura Camacho |
| Proyecto n.º | Conversor Bs/USD con histórico |
| Sitio de referencia | XE Currency Converter |
| Compañero revisor | Pendiente |
| URL desplegada | (se completa en el Sprint 5) |

## 1. Problema

Los usuarios en Venezuela necesitan consultar de manera rápida y precisa la tasa de cambio entre Bolívares (Bs) y Dólares (USD), así como revisar su comportamiento histórico por fecha o rango. Muchas opciones existentes son lentas, tienen exceso de publicidad o no resultan cómodas desde el teléfono móvil.

## 2. Usuarios

- **Usuario principal:** Personas, comerciantes y profesionales que necesitan convertir montos entre Bs y USD rápidamente en su día a día desde el móvil o la web.
- **Usuario secundario:** Usuarios o estudiantes que desean consultar tasas históricas por fecha y observar su tendencia.

## 3. Objetivo y métrica de éxito

Un usuario consulta la tasa, convierte un monto entre Bs y USD y revisa el histórico en menos de 5 segundos desde su dispositivo, manteniendo `npm run check` en verde.

## 4. Alcance del MVP y funcionalidades (`src/`)

1. **Conversión interactiva Bs/USD y USD/Bs:** Cálculo bidireccional de montos y visualización de tasa en la interfaz web (`src/app/web/` y `src/app/`).
2. **Consulta y ordenamiento de histórico por fecha:** Gestión de registros históricos y ordenamiento cronológico (`src/shared/algorithms/sort.ts` y `src/tasks/`).
3. **Búsqueda rápida de tasa histórica por fecha:** Búsqueda eficiente de tasas en series históricas (`src/shared/algorithms/search.ts`).
4. **Caché y estructuras de apoyo:** Almacenamiento en memoria y estructuras de datos para acceso rápido (`src/shared/structures/`).
5. **Gráfica histórica en HTML5 Canvas:** Representación visual de la evolución de la tasa en la vista web (`src/app/web/index.html`, `src/app/web/main.ts`, `src/app/web/styles.css`).
6. **API, configuración y registro de operaciones:** Endpoints, configuración y logs del servidor (`src/app/create-app.ts`, `src/app/server.ts`, `src/shared/config.ts`, `src/shared/logger.ts`, `src/shared/operation-log.ts`).

## 5. Requisitos

- **Funcionales:**
  - Convertir montos de Bs a USD y de USD a Bs.
  - Consultar tasas históricas por fecha y visualizar su evolución.
  - Mantener el flujo de tareas/registros base del proyecto (`src/tasks/`).
- **No funcionales:**
  - Interfaz responsive utilizable desde teléfono móvil.
  - Código tipado en TypeScript que pase `npm run check` (`lint`, `typecheck` y `test`).
