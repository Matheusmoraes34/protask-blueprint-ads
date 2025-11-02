# 2. Arquitetura e Stack de Tecnologias

## 2.1. Visão Geral da Arquitetura
Adotaremos uma arquitetura de serviços desacoplada (**Multi-Repo**), onde o Front-end (Cliente SPA) é totalmente independente do Back-end (Servidor API). A comunicação será feita exclusivamente via uma API RESTful (JSON).

> **Diagrama Conceitual:**
> `[Usuário (Browser)]` -> `[Vue.js (Vercel)]` -> `[API REST (HTTPS)]` -> `[Spring Boot (Render)]` -> `[Banco de Dados (PostgreSQL)]`

## 2.2. Stack Tecnológica

| Componente | Tecnologia | Repositório | Justificativa |
| :--- | :--- | :--- | :--- |
| **Front-end** | **Vue.js 3 (com Vite)** | `protask-web` | Framework reativo moderno (CLI obrigatório para build). |
| **Back-end** | **Spring Boot 3 (Java 17)** | `protask-api` | Robusto, seguro (Spring Security) e excelente para APIs. |
| **Banco de Dados**| **PostgreSQL** | N/A (Hospedado) | Banco relacional padrão de mercado (usaremos H2 para dev). |
| **Autenticação** | **JWT (JSON Web Tokens)** | N/A (Lógica) | Padrão *stateless* para APIs desacopladas. |

## 2.3. Estratégia de Deploy (CI/CD)
-   O repositório `protask-web` será conectado à **Vercel** (Deploy automático na `main`).
-   O repositório `protask-api` será conectado ao **Render** (Deploy automático na `main`).
