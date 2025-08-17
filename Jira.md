# Fluxo de Trabalho de Dev com Jira – Gerenciador de Tarefas (CRUD)

## 1️⃣ Planejamento Inicial

-   Criar projeto no **Jira** (ex: “Gerenciador de Tarefas”).
-   Definir **epics** (grandes funcionalidades):

    -   Epic 1: CRUD de Tarefas
    -   Epic 2: Autenticação de Usuário
    -   Epic 3: Relatórios e Dashboard

---

## 2️⃣ Backlog

No **backlog do Jira**, adicionar **user stories** para o CRUD de tarefas:

| ID    | História de Usuário                                                                 | Prioridade | Status  |
| ----- | ----------------------------------------------------------------------------------- | ---------- | ------- |
| US001 | Como usuário, quero **criar uma tarefa** para organizar meu trabalho.               | Alta       | Backlog |
| US002 | Como usuário, quero **visualizar minhas tarefas** para acompanhar meu progresso.    | Alta       | Backlog |
| US003 | Como usuário, quero **editar uma tarefa** para corrigir ou atualizar informações.   | Média      | Backlog |
| US004 | Como usuário, quero **deletar uma tarefa** para remover itens que não preciso mais. | Média      | Backlog |

💡 Cada user story terá: descrição detalhada, critérios de aceite e link para tarefas técnicas (sub-tasks).

---

## 3️⃣ Sprint Planning

-   Selecionar histórias do backlog para a sprint (ex: 2 semanas).
-   Estimar esforço (story points ou horas).
-   Criar **tasks e subtasks** para cada história de usuário:

Exemplo para **US001 – Criar Tarefa**:

-   Task 1: Criar endpoint de criação (Backend)
-   Task 2: Criar formulário de criação (Frontend)
-   Task 3: Testes unitários e integração

---

## 4️⃣ Desenvolvimento

-   Desenvolvedores pegam **tasks do Jira** e movem para **“In Progress”**.
-   Cada tarefa deve ter comentários, commits vinculados no Git/GitHub.
-   Durante a sprint, atualizar status no Jira:

    -   In Progress
    -   Code Review
    -   Testing
    -   Done

---

## 5️⃣ Daily Meet

-   Revisar tarefas em andamento.
-   Identificar bloqueios e dependências.
-   Atualizar **status no Jira**.

---

## 6️⃣ Testes e Revisão

-   QA verifica funcionalidades implementadas.
-   Bugs são registrados como novas **issues no Jira**.
-   Desenvolvedor corrige e atualiza status para **Done**.

---

## 7️⃣ Entrega e Retrospectiva

-   Sprint concluída, revisar o que foi feito.
-   Fechar tarefas completas no Jira.
-   Registrar aprendizados e melhorias para a próxima sprint.

---

### 🔄 Fluxo Visual Simplificado:

```
Backlog → Sprint Planning → In Progress → Code Review → Testing → Done
```

-   Cada user story do CRUD segue este fluxo.
-   Jira garante rastreabilidade de cada tarefa do backlog até a entrega.
