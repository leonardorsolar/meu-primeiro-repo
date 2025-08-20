Claro! Aqui está um tutorial básico de **Git sem GitHub**, para iniciantes que querem entender e usar o Git localmente, no computador, sem usar nenhum serviço online.

---

# Tutorial Básico de Git (Sem GitHub) para Iniciantes

## O que é Git?

Git é um sistema de controle de versão que ajuda a acompanhar as mudanças no código, permitindo voltar a versões anteriores, trabalhar em paralelo, e muito mais.

---

## Pré-requisitos

-   Ter o **Git instalado** no seu computador.

Para verificar se já tem Git instalado, abra o terminal e digite:

```bash
git --version
```

Se aparecer a versão, está tudo certo. Se não, instale:

-   [Git para Windows](https://git-scm.com/download/win)
-   [Git para Mac](https://git-scm.com/download/mac)
-   Para Linux use o gerenciador de pacotes da sua distro, ex: `sudo apt install git`

---

## Passo 1: Criar um repositório Git local

Abra o terminal (Prompt de Comando, PowerShell, Terminal do Linux/macOS) e vá para a pasta do seu projeto (ou crie uma nova pasta):

```bash
mkdir meu-projeto
cd meu-projeto
```

Agora inicialize o Git dentro da pasta:

```bash
git init
```

Isso cria uma pasta oculta `.git` que vai controlar todas as versões.

---

## Passo 2: Configurar seu nome e email (primeira vez)

Para identificar quem faz as mudanças, configure seu nome e email assim (só precisa fazer uma vez por computador):

```bash
git config --global user.name "Seu Nome"
git config --global user.email "seuemail@exemplo.com"
```

---

## Passo 3: Criar um arquivo e salvar mudanças

Vamos criar um arquivo simples:

```bash
echo "Olá, mundo!" > arquivo.txt
```

Verifique o status do repositório:

```bash
git status
```

Ele vai mostrar o arquivo `arquivo.txt` como **não rastreado** (untracked).

---

## Passo 4: Adicionar arquivos para controle (stage)

Para dizer para o Git começar a controlar esse arquivo:

```bash
git add arquivo.txt
```

Ou para adicionar todos os arquivos novos/modificados:

```bash
git add .
```

---

## Passo 5: Fazer o commit (salvar uma "foto" do estado atual)

Agora, para salvar a versão atual do seu projeto, faça o commit:

```bash
git commit -m "Mensagem explicando a mudança"
```

Exemplo:

```bash
git commit -m "Criar arquivo inicial com olá mundo"
```

---

## Passo 6: Fazer mudanças e salvar novas versões

Altere o arquivo `arquivo.txt`:

```bash
echo "Segunda linha" >> arquivo.txt
```

Veja o status:

```bash
git status
```

Adicione e faça o commit novamente:

```bash
git add arquivo.txt
git commit -m "Adicionar segunda linha no arquivo"
```

---

## Passo 7: Ver o histórico de commits

Para ver todas as versões salvas (commits):

```bash
git log
```

Use `q` para sair da visualização.

---

## Passo 8: Voltar para um commit anterior

Se quiser voltar para uma versão anterior (exemplo: commit com hash `abc123`):

```bash
git checkout abc123 arquivo.txt
```

Ou para voltar o projeto inteiro para um commit:

```bash
git checkout abc123
```

Atenção: depois de usar o checkout para um commit antigo, seu repositório ficará em modo “detached HEAD”. Para voltar para a última versão da branch principal (geralmente chamada `main` ou `master`):

```bash
git checkout main
```

---

## Passo 9: Criar e mudar para uma nova branch (ramificação)

Branches são como “linhas paralelas de desenvolvimento” para você trabalhar sem bagunçar a principal.

Criar e mudar para uma branch chamada `nova-feature`:

```bash
git checkout -b nova-feature
```

Agora você está nessa branch e pode fazer commits separados.

Para voltar para a branch principal:

```bash
git checkout main
```

---

## Passo 10: Unir branches (merge)

Depois de terminar a feature, volte para a branch principal e una as mudanças:

```bash
git checkout main
git merge nova-feature
```

---

# Comandos úteis extras

-   `git diff` — mostrar mudanças feitas mas ainda não adicionadas ao stage
-   `git reset arquivo.txt` — retirar arquivo do stage
-   `git rm arquivo.txt` — remover arquivo do projeto e stage
-   `git status` — mostrar o que está acontecendo no repositório
-   `git log --oneline` — log compacto dos commits

---

# Considerações finais

-   Git funciona localmente e você não precisa do GitHub para usar.
-   GitHub e outros são só serviços online para guardar e compartilhar seu repositório.
-   É muito importante sempre escrever mensagens claras nos commits.
-   Use branches para organizar seu trabalho e evitar conflitos.

---

# Estudo

https://learngitbranching.js.org/?locale=pt_BR

O site https://learngitbranching.js.org/?locale=pt_BR é uma ferramenta interativa e visual para aprender Git, focada especialmente no uso de branches (ramificações). Ele oferece uma maneira prática e divertida de entender conceitos fundamentais do Git, como commits, merges, rebases e resolução de conflitos, sem precisar instalar nada no seu computador.

https://www.youtube.com/watch?v=6OokP-NE49k

https://www.youtube.com/watch?v=6Czd1Yetaac
