# Conciliación SIGEP

Microservicio para la conciliación de C-21 y facturas extraídas de SIGEP.

## Arquitectura
- **Backend:** NestJS + TypeORM (PostgreSQL)
- **Frontend:** React + Vite + TanStack Query + TailwindCSS
- **Base de Datos:** Esquema `sigep_rep` (tablas `facturas_excel`, `transacciones`, `documentos`)

## Requisitos
- Node.js 20+
- PostgreSQL 15+
- Variables de entorno configuradas (ver `.env.example`)

## Desarrollo
1. `npm install`
2. `npm run dev:backend` (puerto 3001)
3. `npm run dev:frontend` (puerto 5173)

## Integración con IAM
Este módulo se registra en el menú dinámico del sistema IAM principal.
- El frontend consume `GET /sigep/conciliacion/c21`
- El backend valida el JWT emitido por el IAM (pendiente para producción).
