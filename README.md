# Nasam Geek TCG — Monorepo

Plataforma e-commerce orientada a la compra y venta de cartas individuales (Singles) y productos TCG, construida sobre una arquitectura escalable de microservicios.

## Arquitectura del Sistema

El sistema utiliza una arquitectura orientada a microservicios desacoplados:

- **Frontend:** Next.js (App Router) + Tailwind CSS.
- **Backend Services:** NestJS + TypeScript.
- **API Gateway:** Traefik (Reverse Proxy, Rate Limiting y SSL).
- **Base de Datos & Auth:** Supabase (PostgreSQL con Row Level Security).
- **Contenedores:** Docker & Docker Compose.

## DevSecOps & Calidad

Este proyecto cuenta con integración continua (CI/CD) mediante GitHub Actions:
- **Gitleaks:** Detección automática de secretos y API keys expuestas.
- **ESLint Strict:** Control estricto de sintaxis y reglas de TypeScript.
- **Trivy:** Escaneo de vulnerabilidades en imágenes Docker.

## Requisitos Previos

- [Docker Desktop](https://www.docker.com/) (con motor WSL2 activo).
- [Node.js](https://nodejs.org/) v20+.
- [Git](https://git-scm.com/).

## Estrategia de Ramas (Gitflow)

- `main`: Entorno de Producción.
- `qa`: Entorno de Pruebas y Certificación de Calidad.
- `dev`: Entorno de Desarrollo Activo.