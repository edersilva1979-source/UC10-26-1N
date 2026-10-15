# Exercício prático de Git: Branches e Merge

**Tema:** Criação de branches, registro de commits e integração de arquivos na branch `develop`.

## Objetivo da atividade

Nesta atividade, nós vamos criar um pequeno projeto HTML e praticar o fluxo de trabalho com Git. Vamos inicializar um repositório, criar as branches `develop`, `feature/cadastro` e `fix/cadastro`, registrar as alterações com `git add` e `git commit` e, por fim, integrar as duas branches de trabalho na `develop`.

**Ferramentas:** Git, terminal (Git Bash ou terminal do VS Code) e Visual Studio Code.

> **Atenção:** Executaremos os comandos na ordem apresentada. Antes de trocar de branch, vamos garantir que todas as mudanças foram salvas em commits.

## Etapa 1. Criar a pasta do projeto no Desktop chamada "aula_merge"

Agora vamos abrir a pasta no VS Code:

```bash
code .
```

Se o comando `code .` não estiver disponível, podemos abrir o VS Code e selecionar **Arquivo > Abrir Pasta**, escolhendo `aula_merge`.

## Etapa 2. Inicializar o Git

No terminal, dentro da pasta `aula_merge`, vamos executar:

```bash
git init
```

Para verificar se estamos em um repositório Git:

```bash
git status
```

## Etapa 3. Criar o arquivo index.html

No VS Code, vamos criar um arquivo chamado **`index.html`** na raiz do projeto e copiar o seguinte código:

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pagina nova</title>
</head>
<body>
    <h1>Exercicio de Git</h1>
</body>
</html>
```

Observe que o `<title>` contém **Pagina nova** e o `<body>` contém apenas o título **Exercicio de Git**, conforme solicitado.

Vamos salvar o arquivo e registrar nosso primeiro commit:

```bash
git add index.html
git commit -m "Cria pagina inicial do exercicio"
```

Vamos conferir:

```bash
git status
```

O esperado é que não existam alterações pendentes.

## Etapa 4. Criar a branch develop

Agora vamos criar uma branch chamada `develop` e mudar para ela:

```bash
git switch -c develop
```

Para visualizar as branches:

```bash
git branch
```

O asterisco (`*`) deve aparecer ao lado da branch `develop`.

## Etapa 5. Criar a branch feature/cadastro

A partir da `develop`, vamos criar a branch em que desenvolveremos o formulário:

```bash
git switch -c feature/cadastro
```

No VS Code, vamos criar o arquivo **`Cadastro.html`** na raiz do projeto e copiar este formulário:

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cadastro de Usuario</title>
</head>
<body>
    <h1>Cadastro de Usuario</h1>

    <form action="#" method="get">
        <label for="nome">Nome:</label>
        <input type="text" id="nome" name="nome" required>
        <br><br>

        <label for="email">Email:</label>
        <input type="email" id="email" name="email" required>
        <br><br>

        <label for="telefone">Telefone:</label>
        <input type="tel" id="telefone" name="telefone">
        <br><br>

        <button type="submit">Cadastrar</button>
        <button type="reset">Limpar</button>
    </form>
</body>
</html>
```

> Este é um formulário HTML de treinamento. Ele não salva os dados em banco de dados nem envia informações para um servidor.

Após salvar o arquivo, vamos verificar, adicionar e registrar a alteração:

```bash
git status
git add Cadastro.html
git commit -m "Adiciona formulario HTML de cadastro"
```

## Etapa 6. Criar a branch fix/cadastro

Para manter as duas branches de trabalho independentes, primeiro vamos voltar à `develop`:

```bash
git switch develop
```

Agora vamos criar a branch de correção:

```bash
git switch -c fix/cadastro
```

No VS Code, vamos criar o arquivo **`correcao.html`**, na raiz do projeto, com o conteúdo abaixo:

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Registro de Correcao</title>
</head>
<body>
    <h1>Registro de Correcao</h1>
    <p>Arquivo criado para praticar a branch fix/cadastro.</p>
    <p>Esta pagina representa um ajuste separado da nova funcionalidade.</p>
</body>
</html>
```

Neste exercício, o arquivo representa um ajuste separado para praticarmos a integração. Não estamos alterando o formulário criado na outra branch.

Vamos salvar e fazer o commit:

```bash
git status
git add correcao.html
git commit -m "Adiciona pagina de registro de correcao"
```

## Etapa 7. Realizar o merge das duas branches na develop

Primeiro, vamos voltar à branch que receberá as alterações:

```bash
git switch develop
```

### 7.1. Integrar feature/cadastro

```bash
git merge feature/cadastro
```

O Git deve incorporar o arquivo `Cadastro.html` à `develop`.

### 7.2. Integrar fix/cadastro

```bash
git merge fix/cadastro
```

O Git deve incorporar o arquivo `correcao.html` à `develop`.

> **Importante:** `git merge` integra commits existentes. Quando o merge é concluído normalmente, não precisamos executar `git add` e `git commit` outra vez. Se houver conflitos, precisaremos resolvê-los e concluir o merge conforme as instruções exibidas pelo Git. No nosso exercício, como cada branch cria um arquivo diferente, não esperamos conflitos.

## Etapa 8. Conferir o resultado

Vamos executar:

```bash
git status
git branch
git log --oneline --graph --all --decorate
```

Na branch `develop`, a pasta deverá conter:

```text
aula_merge/
├── index.html
├── Cadastro.html
└── correcao.html
```

Todos os três arquivos devem estar disponíveis na `develop`, e o comando `git status` deverá indicar que não há mudanças pendentes.

Para conferir especificamente os arquivos registrados no último commit da branch atual:

```bash
git ls-tree -r --name-only HEAD
```

## Desafio complementar

Sem apagar as branches, vamos responder:

1. Qual é a função do comando `git add`?
2. Qual é a diferença entre `git commit` e `git merge`?
3. Por que voltamos para a `develop` antes de criar a `fix/cadastro`?
4. Qual branch deve estar ativa quando executamos os merges do exercício?
5. O que o comando `git log --oneline --graph --all` mostra?

## Critérios de entrega

Vamos apresentar ao professor:

1. A pasta `aula_merge` com os três arquivos HTML.
2. As branches `develop`, `feature/cadastro` e `fix/cadastro`.
3. Um commit para cada uma das três etapas de criação de arquivos.
4. A branch `develop` contendo os arquivos das duas branches após os merges.
5. O resultado de `git status` e `git log --oneline --graph --all --decorate`.

**Concluímos o exercício quando conseguimos demonstrar que as duas branches de trabalho foram integradas à `develop` sem perder os arquivos criados.**

---

**Material de apoio para aula prática de Git e GitHub.**

**Prof. Éder Silva**
