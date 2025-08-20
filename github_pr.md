# Pull Request (PR)

**Pull Request (PR)** é o processo usado para propor, revisar e integrar mudanças em um repositório Git (geralmente no GitHub, GitLab ou Bitbucket).

---

## 🔄 Fluxo do Pull Request

### 1. **Criação de uma Branch**

-   Você não trabalha direto na branch principal (`main` ou `master`).
-   Cria uma nova branch para a sua tarefa/feature/correção:

    ```bash
    git checkout -b feature/nova-funcionalidade
    ```

### 2. **Implementação das mudanças**

-   Faz alterações no código.
-   Testa localmente.
-   Cria commits explicando o que foi feito:

    ```bash
    git add .
    git commit -m "Implementa nova funcionalidade X"
    ```

### 3. **Envio da branch para o repositório remoto**

-   Envia sua branch para o servidor remoto (GitHub, GitLab etc.):

    ```bash
    git push origin feature/nova-funcionalidade
    ```

### 4. **Abertura do Pull Request**

-   No repositório (GitHub/GitLab), abre um **Pull Request (PR)** da sua branch → para a branch principal (`main`) ou outra branch de destino.
-   No PR, você descreve:

    -   O que foi feito
    -   Por que foi feito
    -   Como testar

### 5. **Revisão do Código**

-   Outros membros da equipe analisam seu PR.
-   Podem:

    -   Aprovar ✅
    -   Pedir mudanças 🔄
    -   Fazer comentários 💬

### 6. **Ajustes e Atualizações**

-   Se houver pedidos de mudanças, você altera o código na mesma branch, faz novos commits e dá `push`.
-   O PR se atualiza automaticamente.

### 7. **Testes Automáticos (CI/CD)**

-   Muitas equipes configuram pipelines (ex.: GitHub Actions, GitLab CI, Jenkins).
-   O código só pode ser aprovado se os testes passarem.

### 8. **Merge do PR**

-   Quando aprovado, o PR é integrado (merge) à branch de destino.
-   Tipos de merge comuns:

    -   **Merge commit** → mantém histórico completo
    -   **Squash and merge** → junta commits em um só
    -   **Rebase and merge** → aplica commits em linha limpa

### 9. **Branch pode ser excluída**

-   Após o merge, geralmente a branch é apagada para manter o repositório organizado.

---

## ⚙️ Resumindo em Fluxo Visual

1. Criar branch →
2. Fazer alterações →
3. Commitar →
4. Push →
5. Abrir PR →
6. Revisão →
7. Ajustes →
8. Aprovação →
9. Merge →
10. Branch excluída
