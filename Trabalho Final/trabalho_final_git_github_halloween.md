# 🎃 Trabalho Final de Git e GitHub

## Portal Halloween: filmes e séries de terror

**Modalidade:** individual  
**Projeto local:** `Trab_final`  
**Repositório no GitHub:** `Trab_final`  
**Ferramentas:** Git, GitHub, VS Code e navegador

## 🎯 Objetivo

Você foi contratado para organizar o versionamento de um pequeno portal sobre filmes e séries de Halloween. Sua tarefa é criar as páginas fornecidas, registrar as alterações com Git e publicar o projeto no GitHub usando branches, commits, merges, Pull Requests, tags e releases.

**Atenção:** este exercício não apresenta os comandos Git. Você deverá escolher e executar os comandos aprendidos nas aulas. Os códigos HTML estão prontos para copiar e colar no VS Code.

## Observação IMPORTANTE antes de começar
| Tag      | Quando criar                                                                                                       | Release no GitHub             |
| -------- | ------------------------------------------------------------------------------------------------------------------ | ----------------------------- |
| `v0.1.0` | Na `main`, apontando para o commit inicial com `index.html`, `Readme.md` e `.gitignore`, antes das funcionalidades | **Versão inicial do portal**  |
| `v1.0.0` | Na `main`, após a integração completa da `develop`, com as funcionalidades e correção                              | **Portal Halloween completo** |



# Agora vamos começar (leia com atenção até o final)


## Antes da Prática, vamos responder as questões no sistema, segue o link

# https://edersilva1979-source.github.io/Desafio_Git_GitHub_Halloween_Protegido_por_Senha/

## Assim que concluir, chame o professor para verificar

---

## 1. Prepare o projeto

1. Crie uma pasta chamada `Trab_final` na sua Área de Trabalho (Desktop).
2. Abra a pasta no VS Code.
3. Transforme essa pasta em um repositório Git.
4. Confira se a branch principal se chama `main`. Caso esteja com outro nome, ajuste para `main`.
5. Crie na raiz os arquivos `index.html`, `Readme.md` e `.gitignore`.
6. Preencha os arquivos conforme as orientações a seguir.
7. **Para cada arquivo criado, faça a adição ao controle de versão (ADD) e um commit próprio, com mensagem que explique o que foi feito.** Não reúna os três arquivos em um único commit.

### Arquivo `index.html`

Copie todo o código a seguir. Ele será a página inicial do portal.

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Portal Halloween | Filmes de Terror</title>
  <style>
    :root { color-scheme: dark; }
    * { box-sizing: border-box; }
    body { margin: 0; font-family: Arial, sans-serif; background: #10101b; color: #f6f0e8; }
    header { background: #21132f; padding: 24px 8%; border-bottom: 3px solid #f28c28; }
    .topo { display: flex; align-items: center; justify-content: space-between; gap: 20px; flex-wrap: wrap; }
    .marca { margin: 0; color: #ffb04b; font-size: 1.8rem; }
    nav a { color: #fff; margin-right: 18px; text-decoration: none; font-weight: bold; }
    nav a:hover, nav a:focus { color: #ffb04b; }
    .hero { padding: 85px 8%; text-align: center; background: linear-gradient(135deg, #3c1c4f, #17111d); }
    .hero h2 { font-size: clamp(2rem, 5vw, 3.5rem); margin: 0 0 16px; }
    .hero p { max-width: 650px; margin: 0 auto 28px; line-height: 1.6; }
    .botao { display: inline-block; background: #ff9c32; color: #1b1026; padding: 13px 22px;
             border-radius: 9px; font-weight: bold; text-decoration: none; }
    main { max-width: 1100px; margin: auto; padding: 44px 20px; }
    h3 { color: #ffb04b; }
    .grade { display: grid; grid-template-columns: repeat(auto-fit, minmax(230px, 1fr)); gap: 20px; }
    .card { background: #211a2d; padding: 24px; border: 1px solid #493457; border-radius: 14px; }
    .card span { font-size: 2.5rem; }
    .card p { line-height: 1.6; color: #d9d1e1; }
    footer { text-align: center; padding: 25px; background: #21132f; color: #cfc3d9; }
  </style>
</head>
<body>
  <header>
    <div class="topo">
      <h1 class="marca">🎃 Portal Halloween</h1>
      <nav aria-label="Navegação principal">
        <a href="index.html">Início</a>
        <a href="series.html">Séries</a>
        <a href="cadastro.html">Cadastro</a>
      </nav>
    </div>
  </header>

  <section class="hero">
    <h2>Uma noite de arrepiar! 👻</h2>
    <p id="mensagem-destaque">Descubra filmes assustadores para sua maratona de Halloween.</p>
    <a class="botao" href="series.html">Explorar séries</a>
  </section>

  <main>
    <h3>🍿 Filmes para entrar no clima</h3>
    <div class="grade">
      <article class="card">
        <span>🏚️</span>
        <h4>A Casa da Colina</h4>
        <p>Uma sugestão fictícia de suspense sobre os mistérios de uma antiga mansão.</p>
      </article>
      <article class="card">
        <span>🌕</span>
        <h4>Noite de Lua Cheia</h4>
        <p>Uma história fictícia de criaturas e acontecimentos inexplicáveis.</p>
      </article>
      <article class="card">
        <span>🕯️</span>
        <h4>O Último Sussurro</h4>
        <p>Uma indicação fictícia para quem gosta de mistérios e sustos.</p>
      </article>
    </div>
  </main>

  <footer>Projeto educacional de Git e GitHub | Portal Halloween 🎃</footer>
</body>
</html>
```

### Arquivo `Readme.md`

Escreva o README com suas próprias palavras. Ele deverá apresentar **nome do projeto, objetivo, tecnologias utilizadas, estrutura dos arquivos, como abrir o portal, descrição das branches, estratégia de Pull Requests e histórico de versões**.

**Dicas para um bom README:** use um título objetivo, separe os assuntos por subtítulos, explique como testar o site abrindo o `index.html`, inclua capturas de tela se desejar e revise a ortografia. Um visitante deve entender o projeto sem precisar perguntar ao autor.

### Arquivo `.gitignore`

Crie o arquivo para indicar quais itens locais não precisam entrar no repositório, como arquivos temporários do editor, pastas de cache e arquivos de configuração pessoal que não fazem parte do projeto. **Não ignore os arquivos HTML nem o README.**

> **Ponto de controle:** neste momento, os três arquivos devem estar registrados em commits separados na `main`. Verifique o histórico antes de continuar.

## 2. Crie a branch `develop`

1. Crie a branch `develop` a partir da `main`.
2. Passe a trabalhar na `develop`.
3. Confirme que o `index.html`, `Readme.md` e `.gitignore` estão disponíveis.
4. Não faça alterações desnecessárias: essa branch servirá para integrar as funcionalidades.

**Dica:** antes de trabalhar em qualquer branch, confirme em qual branch você está. Esse cuidado evita commits no lugar errado.

## 3. Desenvolva a branch `feature/series`

1. Partindo da `develop`, crie a branch `feature/series` e entre nela.
2. Crie o arquivo `series.html` na raiz do projeto.
3. Copie o código completo abaixo e teste a página no navegador.
4. Faça **ADD e COMMIT exclusivamente desse arquivo**, com uma mensagem adequada.
5. Mantenha a branch para integração posterior.

### Arquivo `series.html`

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Séries de Terror | Portal Halloween</title>
  <style>
    * { box-sizing: border-box; }
    body { margin: 0; font-family: Arial, sans-serif; color: #f5effa; background: #10101b; }
    header { padding: 24px 8%; background: #21132f; border-bottom: 3px solid #ff9c32; }
    .topo { display: flex; justify-content: space-between; align-items: center; flex-wrap: wrap; gap: 18px; }
    h1, h2 { color: #ffb04b; }
    nav a { color: #fff; margin-right: 18px; text-decoration: none; font-weight: bold; }
    nav a:hover { color: #ffb04b; }
    main { max-width: 1100px; margin: auto; padding: 50px 20px; }
    .intro { color: #d4c8de; line-height: 1.6; }
    .grade { display: grid; grid-template-columns: repeat(auto-fit, minmax(240px, 1fr)); gap: 20px; margin-top: 30px; }
    article { border: 1px solid #544064; background: #22192e; border-radius: 14px; padding: 25px; }
    .icone { font-size: 3rem; }
    .tipo { color: #ffbb68; font-weight: bold; font-size: .85rem; }
    article p { line-height: 1.6; color: #ded4e4; }
    footer { text-align: center; background: #21132f; padding: 24px; color: #d7c9e2; }
  </style>
</head>
<body>
  <header>
    <div class="topo">
      <h1>📺 Séries de Terror</h1>
      <nav aria-label="Navegação principal">
        <a href="index.html">Início</a>
        <a href="series.html">Séries</a>
        <a href="cadastro.html">Cadastro</a>
      </nav>
    </div>
  </header>

  <main>
    <h2>Maratona para noites sombrias 🌙</h2>
    <p class="intro">Conheça três séries de terror e suspense para explorar o gênero.</p>
    <section class="grade" aria-label="Sugestões de séries">
      <article>
        <div class="icone">🔦</div>
        <h3>Stranger Things</h3>
        <p class="tipo">Mistério e ficção científica</p>
        <p>Um grupo de jovens enfrenta eventos sobrenaturais em uma pequena cidade.</p>
      </article>
      <article>
        <div class="icone">🏚️</div>
        <h3>A Maldição da Residência Hill</h3>
        <p class="tipo">Terror sobrenatural</p>
        <p>Uma família lida com lembranças perturbadoras de uma antiga casa.</p>
      </article>
      <article>
        <div class="icone">🖤</div>
        <h3>Wandinha</h3>
        <p class="tipo">Mistério e fantasia sombria</p>
        <p>Uma estudante investiga acontecimentos misteriosos em sua escola.</p>
      </article>
    </section>
  </main>

  <footer>Portal Halloween | Página de séries 🎃</footer>
</body>
</html>
```

## 4. Desenvolva a branch `feature/cadastro`

1. Volte para a `develop`.
2. Crie a branch `feature/cadastro` **a partir da `develop`**, e não da `feature/series`.
3. Crie o arquivo `cadastro.html` na raiz do projeto.
4. Copie o código abaixo e teste os campos e as validações no navegador.
5. Faça **ADD e COMMIT desse arquivo**, com uma mensagem adequada.

### Arquivo `cadastro.html`

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Cadastro | Portal Halloween</title>
  <style>
    * { box-sizing: border-box; }
    body { margin: 0; background: #10101b; color: #f8f2fb; font-family: Arial, sans-serif; }
    header { padding: 24px 8%; background: #21132f; border-bottom: 3px solid #ff9c32; }
    .topo { display: flex; align-items: center; justify-content: space-between; gap: 20px; flex-wrap: wrap; }
    h1, h2 { color: #ffb04b; }
    nav a { color: #fff; text-decoration: none; margin-right: 18px; font-weight: bold; }
    nav a:hover { color: #ffb04b; }
    main { max-width: 720px; margin: 45px auto; padding: 0 20px; }
    form { border-radius: 16px; background: #241a31; padding: 30px; border: 1px solid #513b63; }
    label { display: block; margin: 17px 0 7px; font-weight: bold; }
    input, select, textarea { width: 100%; padding: 13px; border: 1px solid #79668b;
      border-radius: 8px; background: #14101c; color: #fff; font: inherit; }
    textarea { min-height: 100px; resize: vertical; }
    button { margin-top: 24px; border: 0; padding: 14px 22px; border-radius: 9px;
      background: #ff9c32; color: #21132f; font-size: 1rem; font-weight: bold; cursor: pointer; }
    button:hover { background: #ffc16f; }
    .aviso { color: #d1c5dc; font-size: .9rem; line-height: 1.6; }
    #resultado { color: #b0f2bb; font-weight: bold; margin-top: 16px; }
    footer { text-align: center; padding: 24px; background: #21132f; color: #d7c9e2; }
  </style>
</head>
<body>
  <header>
    <div class="topo">
      <h1>🦇 Clube do Halloween</h1>
      <nav aria-label="Navegação principal">
        <a href="index.html">Início</a>
        <a href="series.html">Séries</a>
        <a href="cadastro.html">Cadastro</a>
      </nav>
    </div>
  </header>

  <main>
    <h2>Cadastre seu interesse 👻</h2>
    <p>Conte o que você gosta de assistir. Este formulário é uma demonstração educacional.</p>
    <form id="formCadastro">
      <label for="nome">Nome completo</label>
      <input id="nome" name="nome" type="text" maxlength="100" required>

      <label for="email">E-mail</label>
      <input id="email" name="email" type="email" maxlength="150" required>

      <label for="preferencia">Qual seu gênero favorito?</label>
      <select id="preferencia" name="preferencia" required>
        <option value="">Escolha uma opção</option>
        <option value="Terror sobrenatural">Terror sobrenatural</option>
        <option value="Suspense">Suspense</option>
        <option value="Ficção científica">Ficção científica</option>
        <option value="Mistério">Mistério</option>
      </select>

      <label for="comentario">Conte sua indicação favorita</label>
      <textarea id="comentario" name="comentario" maxlength="500"
        placeholder="Qual filme ou série você recomenda?"></textarea>

      <button type="submit">Registrar interesse</button>
      <p class="aviso">Demonstração: os dados não são enviados, armazenados ou compartilhados.</p>
      <p id="resultado" role="status" aria-live="polite"></p>
    </form>
  </main>

  <footer>Portal Halloween | Cadastro demonstrativo 🎃</footer>
  <script>
    document.getElementById('formCadastro').addEventListener('submit', function (evento) {
      evento.preventDefault();
      document.getElementById('resultado').textContent =
        'Interesse registrado nesta demonstração! Nenhum dado foi enviado.';
      this.reset();
    });
  </script>
</body>
</html>
```

> **Importante:** o formulário é uma simulação na própria página. Ele não possui banco de dados, não envia e-mails nem armazena informações. Não apresente essa demonstração como um cadastro real.

## 5. Crie a branch `fix/correcao` e provoque um conflito

Nesta etapa você demonstrará que sabe identificar e resolver conflitos. Siga a ordem rigorosamente.

1. Volte para a `develop`.
2. Crie a branch `fix/correcao` a partir da `develop`.
3. Abra o `index.html` e encontre o parágrafo com `id="mensagem-destaque"`.
4. **Na `fix/correcao`**, substitua somente o texto desse parágrafo por: **Confira nossa seleção especial de filmes e séries de terror para o Halloween.**
5. Salve o arquivo, faça **ADD e COMMIT** com mensagem de correção.
6. Volte para a `develop`, sem integrar a `fix/correcao`.
7. **Na `develop`**, substitua o texto do **mesmo parágrafo** por: **Prepare a pipoca e descubra histórias assustadoras para a noite de Halloween.**
8. Salve, faça **ADD e COMMIT** com outra mensagem coerente.
9. Agora tente integrar a branch `fix/correcao` na `develop` por meio de um **merge local**.
10. Como as duas branches alteraram a mesma linha de maneiras diferentes, deverá ocorrer um conflito. Abra o `index.html` no VS Code, examine as duas versões e escreva **uma frase final que aproveite as ideias das duas alterações**.
11. Remova as marcações de conflito do arquivo, salve, registre a resolução e conclua o merge com um commit, quando necessário.
12. Teste novamente o `index.html` no navegador.

**Dicas:** não apague o arquivo para eliminar o conflito. Entenda o que cada alteração pretendia fazer. Confira se não restaram marcas de conflito e se o HTML continua válido. Se o merge ocorrer sem conflito, reveja se os dois commits realmente modificaram a mesma linha em branches diferentes antes da integração.

## 6. Publique no GitHub

1. No GitHub, crie um repositório com o nome exato `Trab_final`.
2. Deixe o repositório remoto **sem README, sem `.gitignore` e sem licença inicial**, pois você já preparou os arquivos localmente.
3. Conecte o projeto local ao repositório remoto do GitHub.
4. Envie todas as branches: `main`, `develop`, `feature/series`, `feature/cadastro` e `fix/correcao`.
5. Verifique no GitHub se as cinco branches aparecem e se os commits foram publicados.

**Atenção:** publicar uma branch não significa integrá-la. O envio ao repositório remoto e o merge são operações diferentes.

## 7. Integre as funcionalidades com Pull Requests

Faça as integrações pelo GitHub, deixando registrado o processo de revisão:

1. Abra um Pull Request da `feature/series` para a `develop`.
2. Confira os arquivos e conclua a integração.
3. Abra outro Pull Request da `feature/cadastro` para a `develop`.
4. Confira os arquivos e conclua a integração.
5. A correção da `fix/correcao` **já foi integrada localmente na `develop`**, na etapa 5. Não crie outro Pull Request de correção sem novas alterações, pois não haverá diferenças a integrar.
6. Atualize a `develop` local para obter as integrações feitas no GitHub e verifique se os três arquivos HTML estão presentes.
7. Abra um Pull Request da `develop` para a `main` e conclua a integração.
8. Atualize sua `main` local com a versão final do GitHub.

**Dica:** revise sempre a branch de origem e a de destino antes de confirmar um Pull Request. Evite apagar branches antes de verificar se o trabalho foi concluído e publicado.

## 8. Tags e releases

Crie exatamente duas versões identificadas por tags:

| Tag | Quando criar | Release no GitHub |
| --- | --- | --- |
| `v0.1.0` | Na `main`, apontando para o commit inicial com `index.html`, `Readme.md` e `.gitignore`, antes das funcionalidades | **Versão inicial do portal** |
| `v1.0.0` | Na `main`, após a integração completa da `develop`, com as funcionalidades e correção | **Portal Halloween completo** |

1. Identifique no histórico da `main` o commit correspondente à versão inicial.
2. Crie a tag `v0.1.0` apontando para esse commit histórico.
3. Crie a tag `v1.0.0` apontando para o commit final da `main`.
4. Envie as **duas tags** ao GitHub.
5. Na área de Releases do GitHub, publique uma release para cada tag.
6. Escreva uma descrição objetiva do que está disponível em cada versão.

**Atenção:** uma tag identifica um commit específico; uma release apresenta uma versão do projeto no GitHub. Não mova a `v0.1.0` para o commit final. As duas versões precisam representar momentos diferentes do desenvolvimento.

## 9. Atualize o README e revise o projeto

1. Na `main`, atualize o `Readme.md` para apresentar o resultado final, as páginas implementadas, o processo de branches, a correção de conflito e as duas versões publicadas.
2. Faça **ADD e COMMIT apenas dessa atualização do README** e publique a alteração no GitHub.
3. Confira se o site abre pelo `index.html` e se os links levam a `series.html` e `cadastro.html`.
4. Verifique se não existem alterações locais sem commit.
5. Confira o histórico completo das branches e os Pull Requests no GitHub.

**Observação sobre as versões:** a atualização documental realizada depois da `v1.0.0` não altera a tag já criada. Se desejar que o README final esteja incluído no conteúdo da release `v1.0.0`, faça essa atualização **antes** de criar a tag `v1.0.0` na etapa 8.

## ✅ Lista de verificação

- [ ] Pasta `Trab_final` criada no Desktop e Git inicializado.
- [ ] `index.html`, `Readme.md` e `.gitignore` criados e registrados em commits separados.
- [ ] Branches `main`, `develop`, `feature/series`, `feature/cadastro` e `fix/correcao` criadas.
- [ ] `series.html` criado com ADD e COMMIT próprios.
- [ ] `cadastro.html` criado com ADD e COMMIT próprios.
- [ ] Alterações conflitantes realizadas na `fix/correcao` e `develop`.
- [ ] Conflito local resolvido e merge concluído.
- [ ] Todas as branches publicadas no repositório `Trab_final`.
- [ ] Pull Requests das duas features para `develop` concluídos.
- [ ] Pull Request de `develop` para `main` concluído.
- [ ] Tags `v0.1.0` e `v1.0.0` publicadas.
- [ ] Duas releases criadas e descritas no GitHub.
- [ ] README atualizado e links do portal testados.

## 📤 Entrega individual


**Mensagem final:** o objetivo não é decorar comandos. É demonstrar que você sabe selecionar a operação adequada, acompanhar o histórico de versões, corrigir conflitos e publicar um projeto organizado. Bom trabalho! 🎃
