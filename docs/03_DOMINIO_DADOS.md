# 3. Domínio: Modelo de Dados (Entidades)

Este documento define a estrutura das nossas tabelas no banco de dados, representadas como Entidades JPA (ex: `User.java`).

## 3.1. Entidade: `User`
Representa quem acessa o sistema.
- Tabela: `users`

| Coluna | Tipo (Java/SQL) | Restrições | Descrição |
| :--- | :--- | :--- | :--- |
| `id` | `Long` / `BIGINT` | PK, Auto-incremento | Identificador único |
| `name` | `String` / `VARCHAR(100)`| Not Null | Nome de exibição do usuário |
| `email` | `String` / `VARCHAR(255)`| Not Null, Unique | E-mail de login (único) |
| `password_hash` | `String` / `VARCHAR(255)`| Not Null | Senha criptografada (BCrypt) |

## 3.2. Entidade: `Project`
Representa um projeto (um agrupador de tarefas).
- Tabela: `projects`

| Coluna | Tipo (Java/SQL) | Restrições | Descrição |
| :--- | :--- | :--- | :--- |
| `id` | `Long` / `BIGINT` | PK, Auto-incremento | Identificador único |
| `name` | `String` / `VARCHAR(100)`| Not Null | Nome do projeto |
| `owner_id` | `User` / `BIGINT` | FK (users.id), Not Null | Chave estrangeira para o dono |

## 3.3. Entidade: `Task`
Representa uma tarefa individual.
- Tabela: `tasks`

| Coluna | Tipo (Java/SQL) | Restrições | Descrição |
| :--- | :--- | :--- | :--- |
| `id` | `Long` / `BIGINT` | PK, Auto-incremento | Identificador único |
| `title` | `String` / `VARCHAR(255)`| Not Null | O título da tarefa |
| `status` | `String` (Enum) | Not Null | `TODO`, `IN_PROGRESS` ou `DONE` |
| `project_id` | `Project` / `BIGINT` | FK (projects.id), Not Null | Chave estrangeira para o projeto |
