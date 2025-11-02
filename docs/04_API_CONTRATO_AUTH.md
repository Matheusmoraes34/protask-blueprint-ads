# 4. Contrato da API: Autenticação

Define os endpoints públicos para gerenciamento de identidade.

**URL Base:** `/api/v1/auth`

---

## POST /api/v1/auth/register

Registra um novo usuário no sistema.

### Request Body (JSON)
```json
{
  "name": "Matheus Moraes",
  "email": "matheus@email.com",
  "password": "senhaForte123"
}
