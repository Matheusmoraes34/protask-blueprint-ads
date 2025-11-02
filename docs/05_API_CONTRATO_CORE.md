(Define as "portas" privadas: o que o usuário logado pode fazer.)

```md
# 5. Contrato da API: Core (Projetos e Tarefas)

Endpoints privados que exigem um Token JWT no cabeçalho:
`Authorization: Bearer <seu-token-jwt>`

---

## 5.1. Projetos

### GET /api/v1/projects
- **Descrição:** Lista todos os projetos do usuário autenticado.
- **Response (200 OK):**
  ```json
  [
    { "id": 1, "name": "Projeto Final 4BIM" },
    { "id": 2, "name": "Lista de Compras" }
  ]
