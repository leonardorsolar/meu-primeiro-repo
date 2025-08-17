# Integração GitHub + GitHub Actions para iniciantes

## 1️⃣ Objetivo da Integração

-   Automatizar tarefas repetitivas do projeto.
-   Exemplo simples: **testar código automaticamente sempre que alguém fizer um push**.
-   Benefício: aprende conceitos de CI/CD (Integração Contínua e Entrega Contínua) sem complicações.

---

## 2️⃣ Passo a Passo Simples

### a) Criar um repositório no GitHub

1. Entrar no GitHub.
2. Criar novo repositório (ex: `meu-projeto-tarefas`).
3. Inicializar com **README.md** e **.gitignore** (opcional, se usar linguagem como Node.js ou Python).

---

### b) Criar workflow do GitHub Actions

1. No repositório, clicar em **Actions**.
2. Selecionar **Simple workflow** (template básico).
3. GitHub cria automaticamente a pasta:

    ```
    .github/workflows/main.yml
    ```

4. Exemplo de workflow simples para **Node.js**:

    ```yaml
    name: Teste Node.js

    on:
        push:
            branches: [main]
        pull_request:
            branches: [main]

    jobs:
        build:
            runs-on: ubuntu-latest

            steps:
                - uses: actions/checkout@v3
                - name: Configurar Node.js
                  uses: actions/setup-node@v3
                  with:
                      node-version: "18"
                - run: npm install
                - run: npm test
    ```

> Esse workflow faz:
>
> -   Sempre que houver um push na branch `main`, ele:
>
>     1. Clona o repositório
>     2. Instala dependências (`npm install`)
>     3. Roda os testes (`npm test`)

---

### c) Comitar e testar

1. Commit e push do arquivo `main.yml`.
2. Acessar **Actions** e ver o workflow rodando automaticamente.
3. Se houver erro, a tela do GitHub mostra detalhes do que falhou.

---

## 3️⃣ Possíveis Extensões para Iniciantes

-   **Linting automático:** verificar erros de sintaxe.
-   **Deploy simples:** enviar arquivos para GitHub Pages.
-   **Testes básicos em Python, Node.js ou Java.**

---

💡 **Dica:** Para um aluno iniciante, o mais importante é:

-   Entender que o workflow **roda automaticamente**.
-   Ver que cada commit aciona testes ou verificações.
-   Começar simples antes de automatizar deploys ou pipelines complexos.

---
