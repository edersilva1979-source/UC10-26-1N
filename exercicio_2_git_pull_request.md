# Exercício 2: Git, GitHub, Push e Pull Request

**Turma:** 261N  
**Tema:** Controle de versões, branches, repositório remoto e Pull Requests  
**Ferramentas:** Git Bash, Visual Studio Code, navegador e GitHub

## Nosso objetivo

Neste segundo exercício, vamos repetir o processo de criação de um repositório Git, trabalhar com as branches `main`, `develop`, `feature/cadastro` e `fix/cadastro` e avançar para o trabalho remoto no GitHub. No final, vamos enviar as branches com `git push`, abrir dois Pull Requests para integrar as alterações à `develop` e um terceiro Pull Request para integrar a `develop` à `main`.

> **Atenção:** não vamos fazer os merges localmente. Nesta atividade, os merges serão feitos no GitHub, usando Pull Requests. Assim poderemos acompanhar todo o processo de revisão e integração.

## 1. Criando a pasta do projeto na Área de Trabalho

Vamos criar, na Área de Trabalho (Desktop), uma pasta com o nome **Pull_request**. Podemos fazer isso pelo Explorador de Arquivos do Windows.

Depois, vamos abrir essa pasta no VS Code e iniciar um terminal Git Bash dentro dela. Para confirmar onde estamos, executamos:

```bash
pwd
```

O terminal deve indicar o caminho da pasta `Pull_request`.

## 2. Inicializando o Git e criando a branch main

No terminal aberto na pasta do projeto, executamos:

```bash
git init
git branch -M main
```

O primeiro comando inicializa o repositório Git. O segundo define `main` como nome da branch principal.

> Se o Git solicitar sua identificação, configure seu nome e seu email (usando seus próprios dados):
>
> ```bash
> git config --global user.name "Seu Nome"
> git config --global user.email "seuemail@exemplo.com"
> ```

## 3. Criando o arquivo index.html

No VS Code, vamos criar o arquivo `index.html` na raiz da pasta. Vamos copiar o código a seguir:

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

Salvamos o arquivo e executamos:

```bash
git status
git add index.html
git commit -m "Cria pagina inicial do projeto"
```

O `git status` mostra nossas alterações, o `git add` prepara o arquivo e o `git commit` registra a versão.

## 4. Criando a branch develop

Vamos criar uma branch para receber as alterações antes da integração à `main`:

```bash
git switch -c develop
```

Agora vamos conferir:

```bash
git branch
```

O asterisco deve aparecer ao lado da branch `develop`.

## 5. Criando a branch feature/cadastro

A partir da `develop`, vamos criar uma branch para implementar o formulário de cadastro:

```bash
git switch -c feature/cadastro
```

No VS Code, vamos criar o arquivo **Cadastro.html** e copiar o código:

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cadastro de Alunos</title>
</head>
<body>
    <h1>Cadastro de Alunos</h1>
    <form action="#" method="get">
        <label for="nome">Nome:</label><br>
        <input type="text" id="nome" name="nome" required><br><br>

        <label for="email">Email:</label><br>
        <input type="email" id="email" name="email" required><br><br>

        <label for="turma">Turma:</label><br>
        <input type="text" id="turma" name="turma" required><br><br>

        <button type="submit">Cadastrar</button>
        <button type="reset">Limpar</button>
    </form>
</body>
</html>
```

> Este formulário é apenas uma prática de HTML. Ele não grava informações em um banco de dados.

Depois de salvar:

```bash
git status
git add Cadastro.html
git commit -m "Adiciona formulario de cadastro de alunos"
```

## 6. Criando a branch fix/cadastro

Agora vamos voltar para `develop` e criar outra branch independente. **Não vamos partir de `feature/cadastro`**, pois queremos demonstrar duas alterações separadas.

```bash
git switch develop
git switch -c fix/cadastro
```

No VS Code, criamos o arquivo **correcao.html** com o conteúdo:

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Correcoes do Cadastro</title>
</head>
<body>
    <h1>Correcoes do Cadastro</h1>
    <p>Esta pagina registra uma melhoria planejada para o cadastro de alunos.</p>
    <p>Antes de cadastrar um aluno, devemos conferir nome, email e turma.</p>
</body>
</html>
```

Após salvar, vamos registrar a nova alteração:

```bash
git status
git add correcao.html
git commit -m "Adiciona pagina de orientacoes para correcao do cadastro"
```

> **Observação:** a branch `fix/cadastro` representa uma melhoria complementar. Neste exercício, ela cria uma página de orientações, sem modificar diretamente o formulário existente, já que a `feature/cadastro` ainda não foi integrada.

## 7. Criando o repositório remoto no GitHub

Vamos acessar [https://github.com](https://github.com), entrar em nossa conta e seguir os passos:

1. Clicar em **New repository** (Novo repositório).
2. Digitar exatamente o nome **pull_request_261n**.
3. Escolher a visibilidade **Public**, conforme a orientação do professor.
4. **Não** marcar as opções de criação de README, `.gitignore` ou licença, pois já temos um projeto local.
5. Clicar em **Create repository**.

No GitHub, copiamos a URL HTTPS do repositório. O endereço terá um formato parecido com:

```text
https://github.com/SEU_USUARIO/pull_request_261n.git
```

Substituímos `SEU_USUARIO` pelo nosso usuário real do GitHub.

## 8. Conectando nosso projeto ao GitHub

Voltamos ao terminal do VS Code e executamos:

```bash
git remote add origin https://github.com/SEU_USUARIO/pull_request_261n.git
git remote -v
```

O comando `git remote -v` permite conferir o endereço configurado. O GitHub poderá solicitar autenticação no navegador ou por um gerenciador de credenciais.

## 9. Enviando todas as branches com push

Agora vamos publicar cada branch no repositório remoto. Como já registramos os commits, não precisamos fazer novos commits nesta etapa.

```bash
git switch main
git push -u origin main

git switch develop
git push -u origin develop

git switch feature/cadastro
git push -u origin feature/cadastro

git switch fix/cadastro
git push -u origin fix/cadastro
```

O `git push` envia nossos commits ao GitHub. A opção `-u` associa a branch local à correspondente branch remota, simplificando os próximos envios.

No navegador, acessamos o repositório e verificamos se as quatro branches estão disponíveis:

* `main`
* `develop`
* `feature/cadastro`
* `fix/cadastro`

## 10. Primeiro Pull Request: feature/cadastro para develop

No GitHub, vamos integrar o formulário de cadastro à branch de desenvolvimento:

1. Abrir o repositório **pull_request_261n**.
2. Acessar a aba **Pull requests** e clicar em **New pull request**.
3. Definir **base: develop** e **compare: feature/cadastro**.
4. Conferir se a alteração apresentada é a criação de `Cadastro.html`.
5. Clicar em **Create pull request**.
6. Preencher os campos:

   **Título:** `Adiciona formulario de cadastro de alunos`  
   **Descrição:** `Criamos uma pagina HTML com campos de nome, email e turma para exercitar o fluxo de desenvolvimento com branches.`

7. Clicar em **Create pull request** para abrir a solicitação.
8. Conferir os arquivos alterados na aba **Files changed**.
9. Se o GitHub permitir a integração, clicar em **Merge pull request** e depois em **Confirm merge**.

**Importante:** não apagar a branch após o merge. Vamos mantê-la para conferir o histórico da atividade.

## 11. Segundo Pull Request: fix/cadastro para develop

Agora repetimos o processo com a outra branch:

1. Abrir **Pull requests** e clicar em **New pull request**.
2. Definir **base: develop** e **compare: fix/cadastro**.
3. Conferir a inclusão de `correcao.html`.
4. Criar o Pull Request com:

   **Título:** `Adiciona orientacoes de correcao do cadastro`  
   **Descrição:** `Incluimos uma pagina com orientacoes de conferencia dos dados dos alunos.`

5. Revisar os arquivos e concluir com **Merge pull request** e **Confirm merge**.

Agora a branch `develop` no GitHub deve conter `index.html`, `Cadastro.html` e `correcao.html`.

## 12. Terceiro Pull Request: develop para main

Depois de integrar as duas alterações à `develop`, vamos levar o trabalho concluído à branch principal:

1. Abrir **Pull requests** e clicar em **New pull request**.
2. Definir **base: main** e **compare: develop**.
3. Conferir se o Pull Request apresenta os arquivos `Cadastro.html` e `correcao.html`.
4. Criar o Pull Request com:

   **Título:** `Integra cadastro e correcoes na branch principal`  
   **Descrição:** `Reunimos as alteracoes revisadas na develop e estamos integrando o resultado final a main.`

5. Revisar as alterações e clicar em **Merge pull request** e **Confirm merge**.

Concluímos assim nosso fluxo de integração: `feature/cadastro` e `fix/cadastro` foram integradas à `develop`, e a `develop` foi integrada à `main`.

> As ações de merge devem ser feitas no GitHub, não no terminal, para que o histórico mostre os Pull Requests realizados.

## 13. Atualizando nosso repositório local

Os merges aconteceram no GitHub. Por isso, nossas branches locais `develop` e `main` ainda precisam receber essas alterações. Vamos voltar ao terminal:

```bash
git switch develop
git pull origin develop

git switch main
git pull origin main
```

Vamos conferir os arquivos e o histórico:

```bash
git status
git branch -a
git log --oneline --graph --decorate --all
```

O gráfico deve mostrar os commits e, conforme o tipo de merge escolhido no GitHub, também os commits de integração.

## 14. Estrutura final esperada

Na `main` e na `develop`, teremos:

```text
Pull_request/
    index.html
    Cadastro.html
    correcao.html
```

No GitHub, teremos as quatro branches publicadas e **três Pull Requests integrados**:

| Pull Request | Origem | Destino | Resultado esperado |
| --- | --- | --- | --- |
| 1 | `feature/cadastro` | `develop` | Formulário integrado |
| 2 | `fix/cadastro` | `develop` | Página de orientações integrada |
| 3 | `develop` | `main` | Projeto completo integrado |

## 15. Checklist de entrega

Antes de encerrar, vamos conferir:

- [ ] Criamos a pasta `Pull_request` na Área de Trabalho.
- [ ] Inicializamos o Git e criamos `index.html`.
- [ ] Criamos `develop`, `feature/cadastro` e `fix/cadastro`.
- [ ] Registramos os arquivos com `git add` e mensagens adequadas de `git commit`.
- [ ] Criamos no GitHub o repositório `pull_request_261n` sem arquivos iniciais.
- [ ] Enviamos as quatro branches ao GitHub com `git push`.
- [ ] Abrimos e concluímos o Pull Request de `feature/cadastro` para `develop`.
- [ ] Abrimos e concluímos o Pull Request de `fix/cadastro` para `develop`.
- [ ] Abrimos e concluímos o Pull Request de `develop` para `main`.
- [ ] Atualizamos `develop` e `main` locais com `git pull`.
- [ ] Conferimos os três arquivos na `main` do GitHub.

**Entrega ao professor:** enviar o link do repositório remoto e os links dos três Pull Requests concluídos. Se solicitado, anexar capturas de tela das branches e da lista de Pull Requests na aba **Closed**, identificando os que foram integrados.

## 16. Perguntas para fixação

1. Qual é a diferença entre `git add`, `git commit` e `git push`?
2. Para que usamos a branch `develop` neste projeto?
3. Qual é a diferença entre criar uma branch local e publicá-la no GitHub?
4. O que significam `base` e `compare` ao abrir um Pull Request?
5. Por que integramos as branches de trabalho à `develop` antes de abrir o Pull Request para a `main`?
6. Por que executamos `git pull` depois de concluir os merges no GitHub?

## 17. Desafio extra (opcional)

Depois de concluir a atividade principal, vamos criar uma branch `feature/estilo` a partir da `develop`, acrescentar um arquivo `style.css` e vinculá-lo ao `Cadastro.html`. Em seguida, faremos os commits, enviaremos a branch ao GitHub e abriremos outro Pull Request para `develop`.

---

**Bom trabalho, turma!** Neste exercício, praticamos não apenas os comandos do Git, mas também o fluxo de colaboração usado em projetos reais: desenvolver separadamente, publicar, revisar e integrar as alterações.

**Prof. Éder Silva**
