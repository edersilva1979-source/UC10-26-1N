# 🏢 Desafio de Git e GitHub

## Projeto: Sistema de Gestão da Empresa Horizonte

**Disciplina:** Git e GitHub  
**Modalidade:** Trabalho obrigatoriamente individual  
**Papel do estudante:** Desenvolvedor contratado  
**Entrega:** Repositório público individual no GitHub, histórico de desenvolvimento e documentação

**Regra de autoria:** cada aluno deverá criar, manter e apresentar seu próprio repositório, seus commits, suas branches e seus Pull Requests. Não é permitido entregar trabalho em dupla, compartilhar o repositório de outro aluno ou reutilizar o histórico de terceiros. O código HTML disponibilizado pelo professor é material didático autorizado para todos.

---

## 📖 A história: seu primeiro contrato

A **Horizonte Soluções**, uma empresa fictícia que comercializa produtos e presta serviços, cresceu rapidamente. Atualmente, seus colaboradores controlam clientes, produtos, pedidos e relatórios por meio de anotações e planilhas separadas. O resultado são cadastros duplicados, informações desencontradas e dificuldades para acompanhar a operação.

A diretora da empresa, **Marina**, decidiu contratar um desenvolvedor para criar o protótipo de um **Sistema de Gestão Empresarial**. O sistema deverá apresentar páginas simples, navegáveis, com informações fictícias e uma identidade visual coerente. Nesta etapa, a empresa está avaliando principalmente **a organização do trabalho, o versionamento, a revisão do código e a qualidade das entregas**.

> 💬 **Mensagem de Marina ao desenvolvedor:** Precisamos acompanhar a evolução do sistema, entender o que mudou em cada entrega e conseguir voltar a uma versão anterior quando necessário. Não basta apresentar as telas prontas. Queremos conhecer o caminho percorrido por você.

### 🎬 Cena 1. A reunião de contratação

O professor assume o papel de cliente e apresenta a necessidade. Você é o único desenvolvedor responsável pelo projeto. Antes de desenvolver qualquer página, organize o ambiente de trabalho e definam como vão registrar cada etapa no Git e no GitHub.

**Missão:** criar um projeto local, iniciar o controle de versões, conectá-lo a um repositório remoto e documentar o trabalho desde o começo.

---

## 🎯 Objetivos de aprendizagem

Ao concluir o projeto, você deverá demonstrar que consegue:

1. Criar e organizar um repositório local e seu correspondente no GitHub.
2. Registrar alterações com commits pequenos e mensagens significativas.
3. Trabalhar com **pelo menos seis branches de trabalho**, sendo **quatro de funcionalidades** e **duas de correção**.
4. Integrar alterações por meio de merges e Pull Requests.
5. Identificar e resolver **um conflito local** e **um conflito durante a integração de um Pull Request**.
6. Utilizar um arquivo de apresentação do projeto e um arquivo de exclusão de itens do versionamento.
7. Criar **quatro tags de versão** e publicar **quatro releases no GitHub**.
8. Conferir o histórico, sincronizar as branches e apresentar evidências do processo.

**Regra principal:** este é um desafio de aplicação. As instruções explicam **o que fazer, em qual sequência e como conferir o resultado**, mas não fornecem os comandos Git prontos. **Os códigos HTML e CSS são fornecidos integralmente** para copiar e colar no VS Code. Consultem anotações, materiais das aulas e a documentação oficial para escolher a sintaxe correta.

---

## 🧩 O produto que a empresa espera

O protótipo deverá conter, no mínimo, cinco páginas HTML conectadas por links ou menu, e uma folha de estilos compartilhada:

| Área | Necessidade apresentada pela empresa | Entrega esperada |
| --- | --- | --- |
| Painel inicial | Visualizar uma apresentação do sistema | Página inicial com título, menu e resumo das funcionalidades |
| Clientes | Consultar informações básicas dos clientes | Página de cadastro ilustrativo com campos adequados |
| Produtos | Organizar itens comercializados | Página com formulário e uma pequena relação fictícia de produtos |
| Pedidos | Acompanhar solicitações | Página com dados de um pedido ilustrativo e seu status |
| Relatórios | Observar resultados da operação | Página com indicadores ou tabela de dados simulados |

**Importante:** não é necessário desenvolver backend ou banco de dados. Os formulários e indicadores são ilustrativos, não salvam informações. O foco da avaliação é Git e GitHub, e não a construção de um sistema funcional em produção.

**Dica de projeto:** adotem nomes consistentes para pastas e arquivos. Antes de criar um link entre páginas, verifiquem se o destino existe e se o nome foi digitado corretamente.

---

## 🗂️ Etapa 1. Preparar a empresa para começar

1. Criem na área de trabalho uma pasta chamada **gestao_horizonte**.
2. Abram essa pasta no VS Code e preparem o repositório Git local.
3. Criem o arquivo `index.html` e a folha `css/estilo.css` conforme os códigos completos oferecidos na seção de implementação, mais adiante. Confiram se a página abre corretamente no navegador.
4. Registrem a primeira versão do projeto no histórico local.
5. Criem no GitHub um repositório chamado **gestao_horizonte** e vinculem o projeto local a ele.
6. Publiquem a branch principal no repositório remoto.

**💡 Dica Git:** antes de registrar um commit, existe um comando que mostra quais arquivos foram alterados e quais estão preparados. Outro comando seleciona as alterações que entrarão no próximo registro. Usem os dois conscientemente.

**✅ Como conferir:** a página inicial deve aparecer no GitHub e o histórico deve identificar quem fez a primeira entrega e por quê.

---

## 📝 Etapa 2. Documentar o projeto com README.md

A diretora Marina deseja entender o projeto sem precisar abrir cada arquivo. Criem um **README.md** na raiz do repositório, escrito para uma pessoa que está conhecendo o sistema pela primeira vez.

O documento deverá apresentar:

* Nome do projeto e descrição breve do problema da empresa.
* Objetivo do protótipo e funcionalidades previstas.
* Tecnologias utilizadas e requisitos para visualizar as páginas.
* Orientações para obter o projeto e abri-lo localmente.
* Visão geral das pastas e módulos.
* Explicação resumida do fluxo de branches adotado.
* Situação atual do desenvolvimento e próximas entregas.
* Nome do aluno responsável, turma e data.
* Histórico resumido das versões e link para as releases.

### 💡 O que torna um README realmente útil?

* Comecem explicando **para que serve** o sistema, não apenas quais linguagens foram usadas.
* Criem títulos objetivos e uma ordem fácil de acompanhar.
* Evitem prometer recursos que ainda não existem. Identifiquem o que está concluído e o que está planejado.
* Usem imagens ou capturas de tela próprias, quando ajudarem a entender o projeto.
* Confiram se os links internos e externos funcionam.
* Revisem o arquivo após cada release importante. Documentação desatualizada compromete a entrega.

**✅ Como conferir:** alguém que não participou das aulas deve conseguir compreender o propósito do repositório e como visualizar o protótipo apenas lendo o README.

---

## 🧹 Etapa 3. Preparar o .gitignore

Durante o desenvolvimento, podem surgir arquivos temporários, configurações pessoais do editor e outros itens que não precisam fazer parte do projeto compartilhado.

1. Criem o arquivo **.gitignore** na raiz do projeto.
2. Pesquisem quais arquivos temporários são comuns no seu ambiente de desenvolvimento.
3. Configurem regras apropriadas e justifiquem ao professor pelo menos três decisões.
4. Criem um arquivo temporário de teste e verifiquem se a regra escolhida evita que ele entre no próximo commit.

**💡 Dicas:** o .gitignore não serve para esconder senhas que já foram publicadas. Nunca registrem credenciais reais no repositório. Além disso, arquivos já rastreados podem exigir uma providência adicional para deixarem de ser acompanhados pelo Git.

**✅ Como conferir:** o arquivo temporário escolhido não deve aparecer entre os itens que serão enviados ao repositório.

---

## 🌿 Etapa 4. Organizar seis branches de trabalho

O projeto adotará a **main** como branch estável e a **develop** como branch de integração. Além delas, criem **seis branches de trabalho**, com a distribuição abaixo.

| Tipo | Nome sugerido | Responsabilidade |
| --- | --- | --- |
| Funcionalidade 1 | `feature/clientes` | Criar a página do módulo de clientes |
| Funcionalidade 2 | `feature/produtos` | Criar a página do módulo de produtos |
| Funcionalidade 3 | `feature/pedidos` | Criar a página do módulo de pedidos |
| Funcionalidade 4 | `feature/relatorios` | Criar a página do módulo de relatórios |
| Correção 1 | `fix/menu` | Corrigir um problema intencional na navegação |
| Correção 2 | `fix/visual` | Corrigir uma inconsistência intencional de apresentação |

**Atenção:** são **seis branches de trabalho, além da main e da develop**. Você poderá criar branches adicionais para os conflitos, desde que documente sua finalidade.

### Como trabalhar em cada funcionalidade

Para cada uma das quatro branches de funcionalidade:

1. Partam da versão mais recente da **develop**.
2. Criem a branch da tarefa e confirmem que ela está ativa.
3. Criem o arquivo HTML correspondente, copiando o código completo da seção de implementação. Não antecipem a criação das outras páginas nesta branch.
4. Façam pelo menos dois commits com mudanças distintas e mensagens que descrevam o trabalho realizado. Sugestão: primeiro o arquivo da página; depois uma melhoria real e identificável no conteúdo ou no README. Não dividam artificialmente um arquivo idêntico em dois commits.
5. Enviem a branch ao GitHub.
6. Abram um Pull Request com destino à **develop**.
7. Descrevam o que foi implementado, quais arquivos mudaram e como a alteração foi verificada.
8. Revisem as diferenças exibidas pelo GitHub, integrem a contribuição e atualizem a versão local da develop antes de iniciar a próxima tarefa.

**💡 Dica Git:** existe um comando para identificar a branch atual e outro para visualizar as alterações registradas ao longo do tempo. Consultem ambos antes e depois de cada integração.

**💡 Dica de revisão:** o Pull Request não é somente um botão de aprovação. Ele registra o motivo da alteração, permite comparar versões e torna a revisão verificável.

---

## 💻 Códigos completos para usar no VS Code

Nesta atividade, **você não precisa inventar o HTML**. Seu desafio técnico é controlar as versões e comprovar o fluxo profissional de desenvolvimento. Copie os arquivos abaixo exatamente nos locais indicados, **cada um na etapa e na branch correspondente**. Eles compartilham um único CSS e foram projetados para funcionar sem bibliotecas externas.

**Estrutura final esperada** (os arquivos surgirão progressivamente, e não todos no primeiro commit):

```text
gestao_horizonte/
├── index.html
├── clientes.html
├── produtos.html
├── pedidos.html
├── relatorios.html
├── css/
│   └── estilo.css
├── README.md
└── .gitignore
```

### Código inicial, na main: `css/estilo.css`

Crie a pasta `css` e salve este arquivo **antes** de iniciar as branches de funcionalidades.

```css
/* Identidade visual da Horizonte Soluções */
:root { color-scheme: light; --azul: #112846; --azul2: #1e4675; --dourado: #dfaa47; --fundo: #f3f6fb; --texto: #23324a; --borda: #d9e3f0; }
* { box-sizing: border-box; }
body { margin: 0; background: var(--fundo); color: var(--texto); font-family: Arial, Helvetica, sans-serif; line-height: 1.55; }
.topo { background: linear-gradient(120deg, var(--azul), var(--azul2)); color: white; padding: 24px max(24px, calc((100vw - 1080px)/2)); }
.marca { color: white; font-size: 1.5rem; font-weight: 800; text-decoration: none; }
.subtitulo { margin: 4px 0 18px; color: #dbe7fa; }
.menu { display: flex; flex-wrap: wrap; gap: 8px; }
.menu a { color: white; text-decoration: none; padding: 9px 13px; border-radius: 7px; background: #ffffff1b; }
.menu a:hover, .menu a[aria-current="page"] { background: var(--dourado); color: #1b2840; }
.conteudo { max-width: 1080px; margin: 32px auto; padding: 0 20px; }
.hero { padding: 28px; background: white; border-left: 6px solid var(--dourado); border-radius: 12px; box-shadow: 0 5px 20px #11284612; }
.hero h1 { margin: 0 0 8px; color: var(--azul); }
.grade { display: grid; grid-template-columns: repeat(auto-fit, minmax(220px, 1fr)); gap: 16px; margin-top: 20px; }
.cartao, .painel { background: white; padding: 22px; border: 1px solid var(--borda); border-radius: 12px; }
.cartao h2, .painel h2 { font-size: 1.12rem; color: var(--azul); margin-top: 0; }
.cartao a { color: #14579b; font-weight: bold; }
.formulario { display: grid; grid-template-columns: repeat(auto-fit, minmax(230px, 1fr)); gap: 14px; }
.campo { display: flex; flex-direction: column; gap: 5px; }
.campo label { font-weight: bold; font-size: .92rem; }
.campo input, .campo select, .campo textarea { padding: 11px; border: 1px solid #becbdc; border-radius: 7px; font: inherit; width: 100%; }
.campo.largo { grid-column: 1 / -1; }
.botao { background: var(--azul2); border: 0; color: white; padding: 11px 16px; border-radius: 7px; font-weight: bold; cursor: pointer; }
.aviso { background: #fff6df; border-left: 4px solid var(--dourado); padding: 10px 14px; margin: 16px 0; }
.tabela { width: 100%; border-collapse: collapse; min-width: 560px; }
.tabela th, .tabela td { text-align: left; border-bottom: 1px solid var(--borda); padding: 11px; }
.tabela th { background: #e8eef8; color: var(--azul); }
.rolagem { overflow-x: auto; }
.selo { display: inline-block; background: #e3f3e8; color: #216237; padding: 4px 9px; border-radius: 999px; font-weight: bold; }
.rodape { color: #63738b; text-align: center; padding: 24px; font-size: .88rem; }
@media (max-width: 600px) { .topo { padding: 22px 18px; } .conteudo { margin: 20px auto; } }
```

### Código inicial, na main: `index.html`

Crie a página inicial no primeiro marco do projeto. Alguns links inicialmente apontarão para páginas que serão construídas nas próximas branches. Isso é esperado.

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="Protótipo acadêmico do sistema de gestão Horizonte Soluções">
  <title>Painel Inicial | Horizonte Soluções</title>
  <link rel="stylesheet" href="css/estilo.css">
</head>
<body>
  <header class="topo">
    <a class="marca" href="index.html">Horizonte Soluções</a>
    <p class="subtitulo">Sistema de Gestão Empresarial</p>
      <nav class="menu" aria-label="Navegação principal">
        <a href="index.html" aria-current="page">Início</a>
        <a href="clientes.html">Clientes</a>
        <a href="produtos.html">Produtos</a>
        <a href="pedidos.html">Pedidos</a>
        <a href="relatorios.html">Relatórios</a>
      </nav>
  </header>
  <main class="conteudo">
    <section class="hero">
      <h1>Painel Inicial</h1>
      <p>Acompanhe os principais setores da empresa em um único lugar.</p>
    </section>
    <section class="grade" aria-label="Módulos disponíveis">
      <article class="cartao"><h2>👥 Clientes</h2><p>Consulte e organize cadastros.</p><a href="clientes.html">Acessar clientes</a></article>
      <article class="cartao"><h2>📦 Produtos</h2><p>Visualize o catálogo da empresa.</p><a href="produtos.html">Acessar produtos</a></article>
      <article class="cartao"><h2>🧾 Pedidos</h2><p>Acompanhe pedidos ilustrativos.</p><a href="pedidos.html">Acessar pedidos</a></article>
      <article class="cartao"><h2>📊 Relatórios</h2><p>Consulte os indicadores simulados.</p><a href="relatorios.html">Acessar relatórios</a></article>
    </section>
    <p class="aviso">Este projeto é demonstrativo. Os módulos serão adicionados progressivamente pelas branches.</p>
  </main>
  <footer class="rodape">© 2026 Horizonte Soluções. Protótipo educacional com dados fictícios.</footer>
</body>
</html>
```

### Na branch `feature/clientes`: `clientes.html`

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="Protótipo acadêmico do sistema de gestão Horizonte Soluções">
  <title>Cadastro de Clientes | Horizonte Soluções</title>
  <link rel="stylesheet" href="css/estilo.css">
</head>
<body>
  <header class="topo">
    <a class="marca" href="index.html">Horizonte Soluções</a>
    <p class="subtitulo">Sistema de Gestão Empresarial</p>
      <nav class="menu" aria-label="Navegação principal">
        <a href="index.html">Início</a>
        <a href="clientes.html" aria-current="page">Clientes</a>
        <a href="produtos.html">Produtos</a>
        <a href="pedidos.html">Pedidos</a>
        <a href="relatorios.html">Relatórios</a>
      </nav>
  </header>
  <main class="conteudo">
    <section class="hero">
      <h1>Cadastro de Clientes</h1>
      <p>Mantenha organizadas as informações básicas dos clientes.</p>
    </section>
    <section class="painel" aria-labelledby="titulo-form">
      <h2 id="titulo-form">Novo cliente</h2>
      <form class="formulario" onsubmit="return false;">
        <div class="campo"><label for="nome">Nome completo</label><input id="nome" name="nome" required placeholder="Ex.: Ana Ribeiro"></div>
        <div class="campo"><label for="email">Email</label><input id="email" name="email" type="email" required placeholder="ana@exemplo.com"></div>
        <div class="campo"><label for="telefone">Telefone</label><input id="telefone" name="telefone" type="tel" placeholder="(51) 99999 9999"></div>
        <div class="campo"><label for="cidade">Cidade</label><input id="cidade" name="cidade" placeholder="Porto Alegre"></div>
        <div class="campo largo"><button class="botao" type="button" title="Demonstração sem armazenamento">Cadastrar (demonstração)</button></div>
      </form>
      <p class="aviso">Formulário ilustrativo. Os dados não são gravados.</p>
    </section>
    <section class="painel" aria-labelledby="lista-clientes" style="margin-top:18px">
      <h2 id="lista-clientes">Clientes de exemplo</h2>
      <div class="rolagem"><table class="tabela"><thead><tr><th>ID</th><th>Nome</th><th>Cidade</th><th>Situação</th></tr></thead>
      <tbody><tr><td>101</td><td>Ana Ribeiro</td><td>Porto Alegre</td><td>Ativo</td></tr><tr><td>102</td><td>Bruno Costa</td><td>Canoas</td><td>Ativo</td></tr></tbody></table></div>
    </section>
  </main>
  <footer class="rodape">© 2026 Horizonte Soluções. Protótipo educacional com dados fictícios.</footer>
</body>
</html>
```

**Seu trabalho:** depois do primeiro commit, faça uma melhoria pequena e verdadeira na própria página e registre outro commit antes de abrir o Pull Request.

### Na branch `feature/produtos`: `produtos.html`

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="Protótipo acadêmico do sistema de gestão Horizonte Soluções">
  <title>Cadastro de Produtos | Horizonte Soluções</title>
  <link rel="stylesheet" href="css/estilo.css">
</head>
<body>
  <header class="topo">
    <a class="marca" href="index.html">Horizonte Soluções</a>
    <p class="subtitulo">Sistema de Gestão Empresarial</p>
      <nav class="menu" aria-label="Navegação principal">
        <a href="index.html">Início</a>
        <a href="clientes.html">Clientes</a>
        <a href="produtos.html" aria-current="page">Produtos</a>
        <a href="pedidos.html">Pedidos</a>
        <a href="relatorios.html">Relatórios</a>
      </nav>
  </header>
  <main class="conteudo">
    <section class="hero">
      <h1>Cadastro de Produtos</h1>
      <p>Cadastre visualmente itens e consulte o catálogo fictício.</p>
    </section>
    <section class="painel"><h2>Novo produto</h2>
      <form class="formulario" onsubmit="return false;">
        <div class="campo"><label for="descricao">Descrição</label><input id="descricao" name="descricao" required placeholder="Monitor 24 polegadas"></div>
        <div class="campo"><label for="categoria">Categoria</label><select id="categoria" name="categoria"><option>Informática</option><option>Escritório</option><option>Acessórios</option></select></div>
        <div class="campo"><label for="estoque">Estoque</label><input id="estoque" name="estoque" type="number" min="0" value="0"></div>
        <div class="campo"><label for="preco">Preço estimado (R$)</label><input id="preco" name="preco" type="number" min="0" step="0.01" placeholder="0,00"></div>
        <div class="campo largo"><button class="botao" type="button" title="Demonstração sem armazenamento">Cadastrar (demonstração)</button></div>
      </form><p class="aviso">A tela não modifica o estoque real nem persiste dados.</p>
    </section>
    <section class="painel" style="margin-top:18px"><h2>Catálogo demonstrativo</h2>
      <div class="rolagem"><table class="tabela"><thead><tr><th>Código</th><th>Produto</th><th>Estoque</th><th>Valor</th></tr></thead>
      <tbody><tr><td>P01</td><td>Monitor 24 polegadas</td><td>12</td><td>R$ 780,00</td></tr><tr><td>P02</td><td>Teclado sem fio</td><td>28</td><td>R$ 120,00</td></tr></tbody></table></div>
    </section>
  </main>
  <footer class="rodape">© 2026 Horizonte Soluções. Protótipo educacional com dados fictícios.</footer>
</body>
</html>
```

**Seu trabalho:** faça uma segunda alteração identificável e registre a evolução separadamente.

### Na branch `feature/pedidos`: `pedidos.html`

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="Protótipo acadêmico do sistema de gestão Horizonte Soluções">
  <title>Gestão de Pedidos | Horizonte Soluções</title>
  <link rel="stylesheet" href="css/estilo.css">
</head>
<body>
  <header class="topo">
    <a class="marca" href="index.html">Horizonte Soluções</a>
    <p class="subtitulo">Sistema de Gestão Empresarial</p>
      <nav class="menu" aria-label="Navegação principal">
        <a href="index.html">Início</a>
        <a href="clientes.html">Clientes</a>
        <a href="produtos.html">Produtos</a>
        <a href="pedidos.html" aria-current="page">Pedidos</a>
        <a href="relatorios.html">Relatórios</a>
      </nav>
  </header>
  <main class="conteudo">
    <section class="hero">
      <h1>Gestão de Pedidos</h1>
      <p>Acompanhe os pedidos e seus estágios de atendimento.</p>
    </section>
    <section class="grade">
      <article class="cartao"><h2>Pedidos em aberto</h2><p><strong>03</strong> pedidos fictícios aguardam atendimento.</p></article>
      <article class="cartao"><h2>Pedido em destaque</h2><p>Número 0007 • Cliente Ana Ribeiro</p><span class="selo">Em separação</span></article>
    </section>
    <section class="painel" style="margin-top:18px"><h2>Consultar pedido</h2>
      <form class="formulario" onsubmit="return false;">
        <div class="campo"><label for="numero">Número do pedido</label><input id="numero" name="numero" placeholder="0007"></div>
        <div class="campo"><label for="situacao">Situação desejada</label><select id="situacao" name="situacao"><option>Pendente</option><option>Em separação</option><option>Enviado</option><option>Concluído</option></select></div>
        <div class="campo largo"><button type="button" class="botao">Pesquisar (demonstração)</button></div>
      </form><p class="aviso">Busca e situação são ilustrativas, sem processamento de pedidos.</p>
    </section>
    <section class="painel" style="margin-top:18px"><h2>Últimos pedidos</h2><div class="rolagem"><table class="tabela"><thead><tr><th>Pedido</th><th>Cliente</th><th>Valor</th><th>Status</th></tr></thead>
    <tbody><tr><td>0007</td><td>Ana Ribeiro</td><td>R$ 900,00</td><td>Em separação</td></tr><tr><td>0008</td><td>Bruno Costa</td><td>R$ 120,00</td><td>Pendente</td></tr></tbody></table></div></section>
  </main>
  <footer class="rodape">© 2026 Horizonte Soluções. Protótipo educacional com dados fictícios.</footer>
</body>
</html>
```

**Seu trabalho:** registre uma melhoria posterior, com uma mensagem que explique o motivo da mudança.

### Na branch `feature/relatorios`: `relatorios.html`

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="Protótipo acadêmico do sistema de gestão Horizonte Soluções">
  <title>Relatórios Gerenciais | Horizonte Soluções</title>
  <link rel="stylesheet" href="css/estilo.css">
</head>
<body>
  <header class="topo">
    <a class="marca" href="index.html">Horizonte Soluções</a>
    <p class="subtitulo">Sistema de Gestão Empresarial</p>
      <nav class="menu" aria-label="Navegação principal">
        <a href="index.html">Início</a>
        <a href="clientes.html">Clientes</a>
        <a href="produtos.html">Produtos</a>
        <a href="pedidos.html">Pedidos</a>
        <a href="relatorios.html" aria-current="page">Relatórios</a>
      </nav>
  </header>
  <main class="conteudo">
    <section class="hero">
      <h1>Relatórios Gerenciais</h1>
      <p>Consulte uma visão consolidada e simulada da operação.</p>
    </section>
    <section class="grade">
      <article class="cartao"><h2>Clientes ativos</h2><p><strong>128</strong> cadastros simulados</p></article>
      <article class="cartao"><h2>Produtos</h2><p><strong>42</strong> itens simulados</p></article>
      <article class="cartao"><h2>Pedidos do mês</h2><p><strong>19</strong> pedidos simulados</p></article>
      <article class="cartao"><h2>Faturamento estimado</h2><p><strong>R$ 18.450,00</strong> em dados fictícios</p></article>
    </section>
    <section class="painel" style="margin-top:18px"><h2>Resumo mensal fictício</h2><div class="rolagem"><table class="tabela"><thead><tr><th>Mês</th><th>Pedidos</th><th>Receita simulada</th></tr></thead>
      <tbody><tr><td>Agosto</td><td>12</td><td>R$ 10.200,00</td></tr><tr><td>Setembro</td><td>15</td><td>R$ 13.100,00</td></tr><tr><td>Outubro</td><td>19</td><td>R$ 18.450,00</td></tr></tbody></table></div>
      <p class="aviso">Valores inventados para fins educacionais, não calculados pelo sistema.</p>
    </section>
  </main>
  <footer class="rodape">© 2026 Horizonte Soluções. Protótipo educacional com dados fictícios.</footer>
</body>
</html>
```

**Seu trabalho:** confirme que a tabela apresenta os valores esperados, depois faça um ajuste real em outro commit.

### O que será feito nas branches `fix/menu` e `fix/visual`?

Aqui não há um novo arquivo para simplesmente copiar. Essas duas branches devem conter **correções feitas por você** nos arquivos anteriores. Para `fix/menu`, identifique e corrija um destino de link intencionalmente alterado. Para `fix/visual`, identifique e corrija uma regra visual alterada de propósito no CSS. Registre o problema antes da correção e teste a solução. **Não altere a branch principal diretamente.**

### Como testar sem backend

Abra `index.html` no navegador. Verifique a navegação, a organização visual, a leitura das tabelas e os campos dos formulários. Os botões demonstrativos **não gravam, pesquisam ou alteram dados**. Não afirme que o sistema possui funcionalidades que não foram implementadas.

**Importante:** você recebeu os arquivos fonte, não as soluções do exercício de Git. Todas as decisões sobre inicialização, branches, stage, commits, push, merge, Pull Requests, tags, releases e conflitos continuam sendo suas.

---

## 🛠️ Etapa 5. Executar as duas correções

A equipe de testes da empresa encontrou dois problemas. O cliente quer que ambos sejam tratados em branches próprias, sem misturar as correções com as novas funcionalidades.

### Chamado 01. Menu com destino incorreto

Na branch **fix/menu**, introduzam de forma controlada ou identifiquem um link incorreto no menu e corrijam esse comportamento. Registrem o estado anterior e o resultado da correção. Depois, submetam um Pull Request para a develop.

### Chamado 02. Inconsistência de visual

Na branch **fix/visual**, corrijam um problema de contraste, alinhamento ou padronização visual observado em pelo menos uma página. Registrem a melhoria em commit próprio e submetam outro Pull Request para a develop.

**💡 Dica:** em uma correção, expliquem o problema e o resultado esperado. Uma mensagem genérica como alteração no site não conta ao avaliador o que foi consertado.

---

## ⚔️ Etapa 6. Resolver um conflito local

O cliente enviou duas solicitações incompatíveis para modificar **a mesma linha ou o mesmo pequeno trecho do título da página inicial**. O objetivo é criar um conflito verdadeiro para treino.

1. Partam de um ponto comum no histórico e escolham duas branches envolvidas no exercício.
2. Na primeira branch, modifiquem o texto do título e registrem a mudança.
3. Sem incorporar essa alteração, mudem o **mesmo trecho** de forma diferente na segunda branch e registrem a mudança.
4. Tentem integrar as alterações localmente.
5. Inspecionem o arquivo que o Git sinalizar como conflituoso.
6. Decidam qual texto final atende melhor ao pedido da empresa e resolvam o trecho manualmente no VS Code.
7. Confirmem que não sobraram marcações de conflito, concluam a integração e testem a página.

**💡 Dica Git:** procurem no arquivo as marcações que separam a versão atual da versão recebida. Não apaguem trechos sem analisar o conteúdo dos dois lados. Se o problema parecer confuso, verifiquem o estado do repositório antes de tentar outras ações.

**📸 Evidências obrigatórias:** captura do conflito antes da resolução e captura do arquivo corrigido, além do registro da integração no histórico. Utilize duas branches temporárias criadas de um mesmo commit, ou documente cuidadosamente outras duas branches, sem prejudicar os Pull Requests de funcionalidades.

---

## ☁️ Etapa 7. Criar e resolver um conflito no GitHub

Agora o gerente técnico quer observar como você lida com uma divergência entre branches remotas durante um Pull Request.

1. Após concluir o conflito local, sincronizem o projeto com o GitHub e confirmem que a **main** e a **develop** estejam em um estado conhecido.
2. Partindo de um mesmo ponto do histórico, façam uma alteração no mesmo trecho de uma página em duas branches diferentes, sem integrar imediatamente uma à outra.
3. Enviem as duas alterações ao GitHub.
4. Abram ou mantenham um Pull Request com destino à branch que recebeu a primeira alteração.
5. Verifiquem se o GitHub identifica que a integração não pode ser feita automaticamente.
6. Abram a ferramenta de resolução de conflitos do GitHub **quando ela estiver disponível**, comparem as versões e preparem o texto final.
7. Concluam a resolução, revisem os arquivos e finalizem a integração.
8. Caso o GitHub não permita resolver o conflito pela interface, resolvam a divergência localmente e atualizem a branch do Pull Request.
9. Atualizem o repositório local e verifiquem se a versão final está correta.

**💡 Dica importante:** alterações feitas sequencialmente e já sincronizadas podem não provocar conflito. Para reproduzir o problema, ambas precisam divergir a partir de um ponto comum e alterar o mesmo trecho de maneira incompatível.

**📸 Evidências obrigatórias:** tela do Pull Request com conflito, resolução realizada e Pull Request integrado. Para o conflito remoto, prefira duas branches temporárias diferentes das seis obrigatórias, derivadas do mesmo ponto de partida. Isso preserva o histórico principal do sistema.

---

## 🏷️ Etapa 8. Planejar quatro versões com tags

A empresa deseja identificar marcos claros do desenvolvimento. Crie **quatro tags de versão**, cada uma apontando para um commit que represente a entrega correspondente.

| Versão sugerida | Marco | Conteúdo mínimo esperado |
| --- | --- | --- |
| `v0.1.0` | Protótipo inicial | Página inicial, README inicial e estrutura do projeto |
| `v0.2.0` | Cadastros | Módulos de clientes e produtos integrados |
| `v0.3.0` | Operação | Módulos de pedidos e relatórios integrados |
| `v1.0.0` | Entrega final | Correções, conflitos resolvidos e documentação revisada |

**Atenção ao planejamento:** a versão `v1.0.0` deve ser marcada **após integrar develop à main**, no commit final estável. As versões anteriores precisam apontar para commits correspondentes aos marcos, preferencialmente commits já integrados à develop. Cada tag precisa corresponder ao estado real do sistema naquele marco. Criem as tags nos commits apropriados, durante o desenvolvimento, ou identifiquem posteriormente os commits corretos no histórico. Não criem quatro tags sobre o mesmo commit final.

**💡 Dica Git:** uma tag identifica um ponto específico do histórico. Procurem os recursos do Git que permitem listar tags, consultar os commits aos quais elas apontam e publicá-las no repositório remoto. Para releases formais, pesquisem a vantagem das tags anotadas.

---

## 📦 Etapa 9. Publicar quatro releases

Depois que as quatro tags estiverem disponíveis no GitHub, publiquem **quatro releases**, vinculando cada uma à sua respectiva tag.

Cada release deverá informar:

* Nome e número da versão.
* O que entrou naquela entrega.
* Erros corrigidos, quando aplicável.
* Funcionalidades ainda não implementadas ou limitações conhecidas.
* Orientação breve para obter ou visualizar o protótipo.

**💡 Dica GitHub:** tag e release não são sinônimos. A tag marca um commit no histórico, enquanto a release é a publicação da versão no GitHub, com título, notas e arquivos associados. Verifiquem essa diferença na interface.

**✅ Como conferir:** a área de releases deverá apresentar quatro versões, em ordem coerente, cada uma vinculada a uma tag distinta.

---

## 🚀 Etapa 10. Entregar a versão estável

1. Confiram se todos os Pull Requests previstos para **develop** foram integrados.
2. Revisem as páginas e testem os links de navegação.
3. Atualizem o README com as funcionalidades realmente concluídas e as versões publicadas.
4. Preparem um Pull Request de **develop** para **main**.
5. Revisem as diferenças antes de integrar e confirmem que a main representará a entrega estável.
6. Atualizem a cópia local e confirmem que não existem alterações pendentes.
7. Verifiquem se a tag e a release final apontam para o commit desejado da entrega estável.

**💡 Dica:** não confundam enviar uma branch com integrar essa branch. Uma branch pode existir no GitHub sem que suas alterações tenham sido incorporadas à main.

---

## 🔎 Etapa 11. Auditoria do professor

Na apresentação final, o professor poderá pedir que você mostre:

* Como identificar a branch ativa e conferir arquivos alterados.
* Como localizar os commits de uma tarefa específica.
* Como distinguir a cópia local do repositório remoto.
* Onde aparecem os Pull Requests e suas respectivas branches de origem e destino.
* Qual foi a decisão tomada na resolução dos dois conflitos.
* Como localizar as quatro tags e as quatro releases.
* Por que determinados arquivos foram incluídos no .gitignore.
* Como o README ajuda outro desenvolvedor a assumir o projeto.

**Não é necessário decorar todos os comandos.** É necessário entender o que cada operação realiza e saber localizar a instrução adequada quando precisar executá-la.

---

## ✅ Lista de verificação da entrega

Marquem cada item somente depois de confirmar o resultado no GitHub:

- [ ] Repositório **gestao_horizonte** publicado no GitHub.
- [ ] Branches principais **main** e **develop** existentes.
- [ ] Quatro branches `feature/` criadas, publicadas e utilizadas.
- [ ] Duas branches `fix/` criadas, publicadas e utilizadas.
- [ ] Pelo menos seis Pull Requests de tarefas, com histórico verificável.
- [ ] Pull Request final da develop para a main integrado.
- [ ] Um conflito local provocado e resolvido, com evidências.
- [ ] Um conflito em Pull Request provocado e resolvido, com evidências.
- [ ] Pelo menos cinco páginas HTML navegáveis.
- [ ] README.md completo e atualizado.
- [ ] .gitignore configurado e testado.
- [ ] Quatro tags distintas publicadas no remoto.
- [ ] Quatro releases publicadas e vinculadas às tags corretas.
- [ ] Commits com mensagens descritivas, distribuídos ao longo do trabalho.
- [ ] Histórico final e links das páginas conferidos.

**Observação:** branches de trabalho podem ser excluídas após o merge, desde que os Pull Requests e demais evidências permaneçam verificáveis. Se isso ocorrer, expliquem a decisão na apresentação.

---

## 📊 Critérios de avaliação

| Critério | Pontuação |
| --- | ---: |
| Organização inicial, repositório e sincronização | 10 |
| Quatro branches de funcionalidades e suas entregas | 20 |
| Duas branches de correção e suas entregas | 10 |
| Pull Requests, revisões e integração em main | 15 |
| Resolução de conflito local | 10 |
| Resolução de conflito no GitHub | 10 |
| Quatro tags e quatro releases coerentes | 10 |
| README.md, .gitignore e documentação | 10 |
| Apresentação e explicação técnica | 5 |
| **Total** | **100** |

**Atenção:** copiar os HTMLs sem criar e demonstrar os históricos de branch, commits e Pull Requests não atende ao objetivo desta avaliação. Criar nomes de branches, tags ou releases sem histórico correspondente não comprova a execução da atividade. O professor avaliará o processo e as evidências.

---

## 📤 O que cada aluno deverá entregar

1. Link do seu repositório GitHub **gestao_horizonte**, criado em sua própria conta.
2. Links dos Pull Requests de funcionalidades, correções e entrega final.
3. Links das quatro releases publicadas.
4. Pasta de evidências com capturas dos dois conflitos e de suas resoluções.
5. README final contendo seu nome, turma e a descrição das tarefas realizadas.
6. Apresentação individual demonstrando a navegação do protótipo e o histórico de trabalho.

---

## 🧠 Questões para reflexão

1. Por que a empresa preferiu desenvolver funcionalidades em branches separadas?
2. Qual a diferença entre registrar uma alteração, enviá-la ao GitHub e integrá-la à main?
3. O que pode causar um conflito de merge mesmo quando duas pessoas trabalham no mesmo projeto sem alterar os mesmos arquivos?
4. Por que nem toda divergência entre branches provoca um conflito?
5. Quais riscos surgem quando um desenvolvedor publica uma release sem conferir o commit da tag?
6. O que torna a documentação útil para um novo colaborador?
7. Como os Pull Requests ajudam a justificar decisões técnicas, mesmo em um trabalho individual?
8. O que você faria de maneira diferente para organizar um próximo projeto profissional?

---

## 📚 Onde pesquisar sem receber a solução pronta

* [Documentação oficial do Git](https://git-scm.com/docs)
* [Livro Pro Git](https://git-scm.com/book/pt-br/v2)
* [Documentação do GitHub sobre Pull Requests](https://docs.github.com/pt/pull-requests)
* [Documentação do GitHub sobre releases](https://docs.github.com/pt/repositories/releasing-projects-on-github)
* [Documentação sobre o README](https://docs.github.com/pt/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-readmes)
* [Documentação sobre .gitignore](https://docs.github.com/pt/get-started/getting-started-with-git/ignoring-files)

---

## 🎓 Encerramento: a aprovação do contrato

Marina receberá o protótipo e avaliará não apenas o resultado visual, mas também **como você organizou, registrou, revisou e entregou o trabalho**.

> Um bom projeto não é aquele em que nunca houve conflito. É aquele em que o desenvolvedor consegue compreender o problema, resolvê-lo e deixar registrado o que aconteceu.

**Desafio final:** apresentem o histórico do GitHub como se estivessem prestando contas a uma empresa real. Explique suas decisões e mostre as evidências. A avaliação será individual e baseada no que você conseguir demonstrar.

**Bom desenvolvimento e boa apresentação individual!** 🚀
