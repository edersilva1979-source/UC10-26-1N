# Exercício 3: Git e GitHub, branches, merge, push, Pull Request e resolução de conflitos

**Curso:** Desenvolvimento de Sistemas  
**Professor:** Éder Silva  
**Projeto local:** `conflitos2`  
**Repositório GitHub:** `conflito2`  
**Branches:** `main` e `feature/nova_pagina`

## Nossa missão

Nesta atividade, nós vamos repetir as etapas fundamentais dos exercícios anteriores: iniciar um repositório, criar um arquivo HTML, registrar commits, trabalhar com branches, fazer merge, enviar o projeto ao GitHub e abrir um Pull Request. A novidade será **provocar e resolver dois conflitos de propósito**: um no computador, utilizando Git e VS Code, e outro durante a integração no GitHub.

> **Atenção:** vamos usar `main` como branch principal. Quando falarmos em voltar para a branch principal, usaremos `main`, não `index`. O arquivo `index.html` é uma página, não o nome de uma branch.

## Antes de começar

Precisamos ter Git instalado, VS Code e uma conta no GitHub. Vamos executar os comandos no terminal do VS Code ou no Git Bash. Em exemplos de código, substitua `SEU_USUARIO` pelo nome da sua conta no GitHub.

Se for a primeira vez que usamos Git neste computador, configure nome e e-mail:

```bash
git config --global user.name "Seu Nome"
git config --global user.email "seuemail@exemplo.com"
```

## Parte 1. Criar a pasta e iniciar o Git

**1.** Na Área de Trabalho, vamos criar uma pasta chamada `conflitos2` e abri-la no VS Code. No terminal aberto dentro dessa pasta, executamos:

```bash
git init
git branch -M main
```

**2.** Criamos o arquivo `index.html` com o seguinte conteúdo:

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
    <p>Estamos aprendendo a trabalhar com branches.</p>
</body>
</html>
```

**3.** Salvamos o arquivo e fazemos nosso primeiro commit:

```bash
git status
git add index.html
git commit -m "Cria pagina inicial do projeto"
```

## Parte 2. Provocar um conflito de merge no computador

### 4. Criar a branch de funcionalidade

```bash
git switch -c feature/nova_pagina
```

Na branch `feature/nova_pagina`, vamos substituir **somente a linha do título `<h1>`** por:

```html
<h1>Bem-vindos a nossa nova pagina de cadastro</h1>
```

Mantemos o restante do arquivo igual. Salvamos e registramos:

```bash
git add index.html
git commit -m "Altera titulo da pagina na feature"
```

### 5. Voltar à main e alterar a mesma linha

```bash
git switch main
```

Na branch `main`, substituímos **a mesma linha do `<h1>`**, mas por outro texto:

```html
<h1>Exercicio pratico de Git e GitHub</h1>
```

Salvamos e registramos:

```bash
git add index.html
git commit -m "Atualiza titulo principal na main"
```

### 6. Fazer o merge e encontrar o conflito

Continuamos na `main` e executamos:

```bash
git merge feature/nova_pagina
```

O Git deverá informar um conflito no arquivo `index.html`, porque alteramos a mesma linha nas duas branches. Isso faz parte do exercício.

O arquivo poderá mostrar algo parecido com:

```html
<<<<<<< HEAD
<h1>Exercicio pratico de Git e GitHub</h1>
=======
<h1>Bem-vindos a nossa nova pagina de cadastro</h1>
>>>>>>> feature/nova_pagina
```

O trecho acima é **apenas um exemplo das marcações de conflito**. Não devemos deixar as linhas `<<<<<<<`, `=======` e `>>>>>>>` no HTML final.

### 7. Resolver o conflito localmente

No VS Code, podemos usar o editor de conflitos ou editar o arquivo manualmente. Nossa decisão será combinar as duas ideias em um único título:

```html
<h1>Exercicio pratico de Git e GitHub: nova pagina de cadastro</h1>
```

Salvamos, verificamos se todas as marcações de conflito desapareceram e concluímos o merge:

```bash
git status
git add index.html
git commit -m "Resolve conflito de titulo entre main e feature"
```

> Se utilizarmos o botão de conclusão de merge do VS Code, devemos conferir `git status` antes de executar outro commit, pois o editor pode já ter registrado a conclusão.

Agora vamos observar nosso histórico:

```bash
git log --oneline --graph --all --decorate
git status
```

**O que esperamos:** a `main` terá a versão resolvida do título, e o histórico mostrará o merge. A branch `feature/nova_pagina` continuará apontando para seu último commit até receber novos commits.

## Parte 3. Criar o repositório remoto no GitHub e enviar as branches

**8.** No GitHub, criamos um repositório com o nome **`conflito2`**. Para não misturar históricos nesta atividade, **não** selecionamos as opções de criar README, `.gitignore` ou licença durante a criação. Copiamos a URL HTTPS do repositório.

**9.** No terminal da pasta local `conflitos2`, vinculamos o repositório. Substitua `SEU_USUARIO`:

```bash
git remote add origin https://github.com/SEU_USUARIO/conflito2.git
git remote -v
git push -u origin main
git push -u origin feature/nova_pagina
```

> O nome da pasta local é `conflitos2` e o nome do repositório remoto é `conflito2`, sem o segundo **s**. Isso é intencional. Para autenticar o envio, siga a solicitação do GitHub no navegador ou utilize um método de autenticação válido. Não informe sua senha pessoal do GitHub como senha do Git no terminal.

No GitHub, vamos confirmar que existem as duas branches: `main` e `feature/nova_pagina`.

## Parte 4. Provocar um novo conflito para o Pull Request no GitHub

Para reproduzir um conflito de Pull Request com segurança, nós faremos **duas alterações novas e divergentes na mesma linha**, uma em cada branch, e enviaremos ambas. Não vamos fazer merge local entre elas desta vez.

### 10. Criar uma nova alteração na feature

```bash
git switch feature/nova_pagina
```

No `index.html` dessa branch, substituímos novamente a linha do `<h1>` por:

```html
<h1>Nova pagina: cadastro de usuarios e clientes</h1>
```

Salvamos e registramos:

```bash
git add index.html
git commit -m "Personaliza titulo de cadastro na feature"
git push origin feature/nova_pagina
```

### 11. Criar outra alteração na main

```bash
git switch main
```

No `index.html` da `main`, substituímos a linha do `<h1>` por:

```html
<h1>Portal principal: exercicios de versionamento</h1>
```

Salvamos e registramos:

```bash
git add index.html
git commit -m "Atualiza titulo do portal principal"
git push origin main
```

**Importante:** não fazemos `git merge` agora. As branches precisam permanecer com alterações conflitantes para observarmos o problema no Pull Request.

### 12. Abrir o Pull Request no GitHub

No repositório `conflito2`, abrimos a aba **Pull requests** e selecionamos **New pull request**. Configuramos:

| Campo | Branch |
|---|---|
| **base**: destino da integração | `main` |
| **compare**: origem da alteração | `feature/nova_pagina` |

Vamos usar como título: **Integra nova pagina de cadastro a main**.

Na descrição, podemos escrever: **Este Pull Request reúne as alterações da nova página e demonstra a resolução de um conflito no arquivo index.html.**

Ao criar o Pull Request, o GitHub deverá indicar que as branches possuem alterações conflitantes e não podem ser mescladas automaticamente.

### 13. Resolver o conflito no GitHub

Se o GitHub exibir o botão **Resolve conflicts**, vamos selecioná-lo. O editor mostrará marcações semelhantes a estas:

```html
<<<<<<< feature/nova_pagina
<h1>Nova pagina: cadastro de usuarios e clientes</h1>
=======
<h1>Portal principal: exercicios de versionamento</h1>
>>>>>>> main
```

A ordem e os nomes mostrados nas marcações podem variar. O importante é localizar **as duas versões da linha `<h1>`**.

Vamos remover as marcações e deixar apenas a versão combinada:

```html
<h1>Portal de versionamento: cadastro de usuarios e clientes</h1>
```

Mantemos a estrutura HTML válida, selecionamos **Mark as resolved** e confirmamos o commit de resolução no próprio GitHub. Depois, voltamos ao Pull Request, conferimos a comparação e usamos **Merge pull request**, seguido da confirmação.

> Dependendo das configurações do repositório e da complexidade do conflito, o botão **Resolve conflicts** pode não aparecer ou estar indisponível. Nesse caso, fazemos a resolução localmente conforme o procedimento alternativo abaixo.

### Alternativa: resolver no VS Code quando o GitHub não permitir

Enquanto o Pull Request estiver aberto, podemos resolver o conflito na branch de origem, sem alterar diretamente a `main`:

```bash
git fetch origin
git switch feature/nova_pagina
git merge origin/main
```

O Git acusará conflito no `index.html`. No VS Code, substituímos as versões conflitantes pela linha combinada:

```html
<h1>Portal de versionamento: cadastro de usuarios e clientes</h1>
```

Salvamos e finalizamos:

```bash
git add index.html
git commit -m "Resolve conflito do Pull Request com a main"
git push origin feature/nova_pagina
```

O GitHub atualizará o Pull Request automaticamente. Após conferir que o conflito foi resolvido, selecionamos **Merge pull request**.

> Escolhemos **um** método de resolução: pelo editor do GitHub ou pela alternativa no VS Code. Não precisamos executar os dois.

## Parte 5. Sincronizar o computador depois do merge remoto

Depois da conclusão do Pull Request no GitHub, a `main` remota estará atualizada. Vamos atualizar nossa `main` local:

```bash
git switch main
git pull origin main
git status
git log --oneline --graph --all --decorate
```

Se quisermos atualizar também nossa branch de trabalho com o conteúdo final da `main`, podemos fazer:

```bash
git switch feature/nova_pagina
git merge main
git push origin feature/nova_pagina
```

Esses três últimos comandos são opcionais e devem ser feitos **somente depois do Pull Request concluído**.

## Estrutura final do projeto

```text
conflitos2/
├── .git/          (pasta interna do Git, normalmente oculta)
└── index.html
```

O mesmo arquivo terá diferentes versões ao longo da atividade. O objetivo não é criar muitos arquivos, mas compreender **histórico, branches, conflito, merge e Pull Request**.

## Conferência final

Vamos verificar se:

- [ ] Criamos a pasta local `conflitos2` na Área de Trabalho.
- [ ] Inicializamos o Git com a branch principal `main`.
- [ ] Criamos o arquivo `index.html`.
- [ ] Registramos o primeiro commit.
- [ ] Criamos `feature/nova_pagina`.
- [ ] Alteramos a mesma linha em duas branches e provocamos um conflito local.
- [ ] Resolvemos o conflito no VS Code e concluímos o merge na `main`.
- [ ] Criamos o repositório `conflito2` no GitHub.
- [ ] Enviamos `main` e `feature/nova_pagina` com `git push`.
- [ ] Fizemos novas alterações conflitantes nas duas branches.
- [ ] Abrimos um Pull Request de `feature/nova_pagina` para `main`.
- [ ] Resolvemos o conflito do Pull Request e concluímos o merge.
- [ ] Atualizamos a `main` local com `git pull`.

## Perguntas de fixação

1. Por que o primeiro `git merge` não foi concluído automaticamente?
2. O que significam as marcações `<<<<<<<`, `=======` e `>>>>>>>`?
3. Qual é a diferença entre resolver um conflito localmente e resolvê-lo durante um Pull Request?
4. Para que serve `git add` depois de resolver um conflito?
5. Por que enviamos as duas branches ao GitHub antes de abrir o Pull Request?
6. Qual é a diferença entre `git push` e `git pull`?
7. O que representam os campos **base** e **compare** no Pull Request?
8. Por que não devemos fazer o segundo merge local antes de abrir o Pull Request?

## Entrega

Cada aluno deverá entregar o **link do repositório `conflito2`**, o **link do Pull Request concluído** e duas capturas de tela: uma demonstrando a resolução do conflito local e outra mostrando a resolução do conflito no GitHub ou o histórico de sua correção no Pull Request.

**Desafio extra:** repita o procedimento criando uma segunda linha de texto no `index.html`, provoque um conflito nela e explique qual versão você decidiu preservar e por quê.

---

**Prof. Éder Silva**  
*Git e GitHub: aprendendo a trabalhar com versões, integrar mudanças e resolver conflitos.*
