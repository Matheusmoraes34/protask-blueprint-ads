# 1. Visão e Escopo do "ProTask"

## 1.1. O Problema
Equipes de estudantes e pequenos grupos de desenvolvimento lutam para gerenciar o progresso de projetos sem ferramentas complexas e caras. A comunicação sobre "quem está fazendo o quê" é muitas vezes informal e se perde.

## 1.2. A Visão (A Solução)
O "ProTask" será uma aplicação web *single-page* (SPA) leve e rápida que permite aos usuários criar projetos, adicionar tarefas a esses projetos e acompanhar o status de cada tarefa (Kanban). O foco é a simplicidade e a velocidade.

## 1.3. Escopo do Produto (Metas Principais - MVP)

-   [ ] **Autenticação:** Usuários podem se cadastrar com nome, e-mail e senha.
-   [ ] **Login:** Usuários podem se autenticar para obter um token de acesso (JWT).
-   [ ] **Projetos (CRUD):** Usuários logados podem criar, listar, editar e excluir seus próprios projetos.
-   [ ] **Tarefas (CRUD):** Dentro de um projeto, usuários podem criar, listar e excluir tarefas.
-   [ ] **Kanban:** Usuários podem atualizar o status de uma tarefa (ex: 'A Fazer' -> 'Fazendo').

## 1.4. Fora do Escopo (Não-Metas para esta versão)
Para garantir a entrega no prazo, **NÃO** iremos implementar:
-   [ ] Chat em tempo real.
-   [ ] Upload de arquivos anexos.
-   [ ] Relatórios avançados ou gráficos de Gantt.
-   [ ] Integração com calendário (Google/Outlook).
-   [ ] Atribuição de tarefas para *outros* usuários (apenas auto-atribuição).
