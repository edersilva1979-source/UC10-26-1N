# Aula 8: GitHub Actions, GitHub Pages e Projeto Final

## Encerramento do Curso de Git e GitHub

### Carga horária

4 horas

### Tema da aula

Automação de verificações com GitHub Actions, publicação do projeto com GitHub Pages, revisão geral do fluxo colaborativo e apresentação do projeto final.

---

## 1. Apresentação da aula

Chegamos à última aula do nosso curso de Git e GitHub. 🎓

Durante as aulas anteriores, eu ensinei você a:

1. Criar repositórios locais.

2. Registrar alterações com commits.

3. Publicar projetos no GitHub.

4. Criar e utilizar branches.

5. Integrar alterações com merge.

6. Abrir e revisar Pull Requests.

7. Resolver conflitos.

8. Recuperar alterações.

9. Organizar tarefas com Issues e Projects.

10. Criar tags e releases.

Nesta aula, vamos concluir o ciclo profissional do projeto.

Primeiro, criaremos uma automação com GitHub Actions.

Essa automação será executada sempre que alguém enviar alterações para a branch principal ou abrir um Pull Request direcionado à `main`.

Depois, publicaremos o `Portal da Turma` com GitHub Pages.

Ao final, cada equipe apresentará:

1. O projeto funcionando.

2. O histórico de desenvolvimento.

3. As branches utilizadas.

4. Os Pull Requests.

5. As Issues.

6. A release criada.

7. A automação executada.

8. O site publicado.

Eu quero que esta aula represente a união de todos os conhecimentos construídos durante o curso.

---

## 2. Objetivos da aula

Nesta aula, eu vou ensinar você a:

1. Entender o conceito de automação.

2. Compreender integração contínua.

3. Compreender entrega e implantação contínuas.

4. Identificar um workflow do GitHub Actions.

5. Entender a função de eventos, jobs e steps.

6. Criar um arquivo YAML.

7. Configurar um workflow para `push`.

8. Configurar um workflow para Pull Requests.

9. Utilizar uma Action pronta.

10. Executar comandos dentro de um workflow.

11. Interpretar o resultado de uma execução.

12. Identificar falhas em uma automação.

13. Corrigir um workflow.

14. Adicionar um badge de status ao README.

15. Entender o GitHub Pages.

16. Configurar uma fonte de publicação.

17. Publicar um site HTML e CSS.

18. Atualizar um site já publicado.

19. Identificar erros comuns de publicação.

20. Revisar o fluxo completo do curso.

21. Preparar o projeto final.

22. Apresentar tecnicamente um repositório.

23. Avaliar a organização do trabalho colaborativo.

24. Realizar uma retrospectiva do projeto.

---

## 3. Resultados esperados

Ao final da aula, você deverá conseguir executar este fluxo:

```text
Criar ou atualizar uma funcionalidade

        ↓

Criar uma branch

        ↓

Criar commits

        ↓

Publicar a branch

        ↓

Abrir um Pull Request

        ↓

Executar a automação

        ↓

Revisar e aprovar

        ↓

Realizar o merge

        ↓

Publicar automaticamente a nova versão do site

        ↓

Apresentar o projeto final
```

O aluno também deverá compreender esta relação:

```text
Git

Controla as versões.
```

```text
GitHub

Hospeda e organiza a colaboração.
```

```text
GitHub Actions

Automatiza verificações e processos.
```

```text
GitHub Pages

Publica o site.
```

---

## 4. Conhecimentos necessários

Para acompanhar esta aula, você deverá conhecer:

1. `git status`.

2. `git add`.

3. `git commit`.

4. `git push`.

5. `git pull`.

6. `git branch`.

7. `git switch`.

8. `git merge`.

9. Branch `main`.

10. Pull Request.

11. Revisão de código.

12. Issues.

13. Releases.

14. Arquivos Markdown.

15. HTML e CSS básicos.

---

## 5. Recursos necessários

1. Computador conectado à internet.

2. Git instalado.

3. Visual Studio Code.

4. Conta no GitHub.

5. Repositório `portal_da_turma`.

6. Branch `main` atualizada.

7. Arquivo `index.html`.

8. Arquivo `README.md`.

9. Pasta `css`.

10. Arquivo `css/estilo.css`.

11. Permissão para configurar GitHub Actions e GitHub Pages.

---

## 6. Organização das quatro horas

### Primeiro momento: 20 minutos

Revisão das sete aulas anteriores e apresentação da aula final.

### Segundo momento: 35 minutos

Introdução à automação, integração contínua e GitHub Actions.

### Terceiro momento: 45 minutos

Criação do primeiro workflow.

### Quarto momento: 25 minutos

Análise de execuções, erros e correções.

### Intervalo: 15 minutos

### Quinto momento: 35 minutos

Configuração e publicação com GitHub Pages.

### Sexto momento: 30 minutos

Preparação da entrega e apresentação final.

### Sétimo momento: 25 minutos

Apresentações das equipes.

### Oitavo momento: 25 minutos

Exercícios, desafios, avaliação e encerramento do curso.

---

# Parte 1: Revisão geral do curso

## 7. O caminho percorrido

Durante o curso, começamos com uma pasta comum.

Depois, transformamos essa pasta em um repositório Git:

```bash
git init
```

Criamos arquivos, verificamos alterações e registramos commits:

```bash
git status

git add .

git commit -m "Cria a estrutura inicial do projeto"
```

Publicamos o projeto:

```bash
git remote add origin URL_DO_REPOSITORIO

git push -u origin main
```

Criamos branches:

```bash
git switch -c feature/pagina_sobre
```

Abrimos Pull Requests, revisamos alterações e realizamos merges.

Também resolvemos conflitos, organizamos Issues e publicamos releases.

Agora vamos automatizar e publicar o resultado final.

---

## 8. Fluxo profissional completo

```text
Issue

        ↓

Branch

        ↓

Desenvolvimento

        ↓

Commits

        ↓

Push

        ↓

Pull Request

        ↓

GitHub Actions

        ↓

Revisão

        ↓

Aprovação

        ↓

Merge

        ↓

Release

        ↓

GitHub Pages
```

Esse fluxo representa uma versão simplificada de processos encontrados em equipes profissionais.

---

## 9. Situação atual do Portal da Turma

Antes de continuar, eu verifico se o projeto possui:

```text
portal_da_turma/

├── .github/
├── css/
│   └── estilo.css
├── index.html
├── sobre.html
├── alunos.html
├── projetos.html
├── contato.html
├── README.md
├── CHANGELOG.md
├── CONTRIBUTING.md
└── LICENSE
```

Nem todos os arquivos são obrigatórios para o GitHub Pages.

Para a publicação básica, precisamos principalmente de:

```text
index.html
```

Os caminhos utilizados pelo HTML também precisam estar corretos.

---

## 10. Preparação inicial

Eu abro o terminal na pasta do projeto e executo:

```bash
git status
```

Depois:

```bash
git switch main
```

Atualizo a branch:

```bash
git pull origin main
```

Verifico o histórico:

```bash
git log --oneline -5
```

A área de trabalho deverá estar limpa antes de começarmos.

---

# Parte 2: O que é automação?

## 11. Conceito

Automação é a execução automática de uma tarefa a partir de regras definidas.

Em vez de depender sempre de uma pessoa para realizar uma verificação, podemos configurar o sistema para executá la.

Exemplos:

1. Verificar se os arquivos obrigatórios existem.

2. Executar testes.

3. Verificar a formatação do código.

4. Compilar uma aplicação.

5. Gerar documentação.

6. Publicar um site.

7. Criar um pacote.

8. Enviar uma notificação.

---

## 12. Exemplo manual

Antes da automação, o professor ou revisor precisaria verificar manualmente:

```text
O index.html existe?

O arquivo CSS existe?

O README existe?

O título principal está presente?

O projeto possui a estrutura esperada?
```

Esse processo precisa ser repetido em cada Pull Request.

---

## 13. Exemplo automatizado

Podemos criar um workflow que execute:

```bash
test -f index.html

test -f README.md

test -f css/estilo.css
```

Se algum arquivo não existir, o workflow falhará.

---

## 14. Por que automatizar?

A automação ajuda a:

1. Reduzir tarefas repetitivas.

2. Detectar problemas mais cedo.

3. Padronizar verificações.

4. Dar retorno rápido ao autor.

5. Evitar que requisitos básicos sejam esquecidos.

6. Aumentar a confiança antes do merge.

7. Registrar o resultado da verificação.

---

## 15. Automação não substitui revisão

Um workflow pode verificar se um arquivo existe.

Ele não compreende completamente:

1. A qualidade do conteúdo.

2. A experiência do usuário.

3. A intenção da tarefa.

4. A clareza da documentação.

5. A adequação visual.

Por isso, utilizamos:

```text
Automação

mais

Revisão humana
```

---

# Parte 3: Integração contínua

## 16. O que é integração contínua?

Integração contínua, também conhecida como CI, é a prática de integrar alterações com frequência e executar verificações automáticas.

A sigla vem de:

```text
Continuous Integration
```

Em um fluxo simples:

```text
Alteração enviada

        ↓

Workflow iniciado

        ↓

Projeto verificado

        ↓

Resultado apresentado
```

---

## 17. Exemplo no nosso curso

Quando um aluno abrir um Pull Request para a `main`, o GitHub Actions verificará:

1. Se `index.html` existe.

2. Se `README.md` existe.

3. Se `css/estilo.css` existe.

4. Se o HTML possui um elemento `<title>`.

5. Se o HTML possui um título `<h1>`.

---

## 18. Benefício no Pull Request

O revisor visualizará um resultado semelhante a:

```text
Verificação do portal

Successful
```

ou:

```text
Verificação do portal

Failed
```

Isso ajuda a decidir se o trabalho está pronto para revisão e integração.

---

# Parte 4: Entrega e implantação contínuas

## 19. Entrega contínua

Entrega contínua organiza o projeto para que ele esteja pronto para publicação depois das verificações.

A sigla costuma aparecer como:

```text
CD
```

Nesse contexto, CD pode representar:

```text
Continuous Delivery
```

---

## 20. Implantação contínua

Implantação contínua significa publicar automaticamente uma alteração aprovada.

Também pode ser chamada:

```text
Continuous Deployment
```

---

## 21. Aplicação no Portal da Turma

Quando um Pull Request for aprovado e integrado à `main`, o GitHub Pages poderá publicar a versão atualizada.

O fluxo será:

```text
Merge na main

        ↓

Nova versão disponível no repositório

        ↓

Publicação do GitHub Pages

        ↓

Site atualizado
```

---

# Parte 5: O que é GitHub Actions?

## 22. Conceito

GitHub Actions é uma plataforma de automação integrada ao GitHub.

Ela permite criar workflows para responder a eventos no repositório.

Um workflow pode ser iniciado por:

1. `push`.

2. Pull Request.

3. Criação de uma Issue.

4. Criação de uma release.

5. Execução manual.

6. Agendamento.

7. Outros eventos suportados.

---

## 23. Onde ficam os workflows?

Os arquivos ficam na pasta:

```text
.github/workflows/
```

Exemplo:

```text
.github/workflows/verificar_portal.yml
```

O arquivo utiliza YAML.

Extensões comuns:

```text
.yml
```

```text
.yaml
```

---

## 24. O que é YAML?

YAML é um formato de texto utilizado para configurações.

Ele organiza informações por indentação.

Exemplo:

```yaml
nome:
  propriedade: valor
```

A quantidade de espaços é importante.

Eu não utilizo tabulações no arquivo YAML.

---

## 25. Estrutura geral de um workflow

```yaml
name: Nome do workflow

on:
  evento:

jobs:
  nome_do_job:
    runs-on: sistema

    steps:
      - name: Nome da etapa
        run: comando
```

---

## 26. Partes principais

```text
name

Nome visível do workflow.
```

```text
on

Eventos que iniciam a execução.
```

```text
jobs

Conjunto de trabalhos executados.
```

```text
runs-on

Ambiente onde o job será executado.
```

```text
steps

Etapas realizadas dentro do job.
```

---

# Parte 6: Eventos do workflow

## 27. Executar em push

```yaml
on:
  push:
```

O workflow será iniciado quando ocorrer um push correspondente à configuração.

---

## 28. Executar em Pull Request

```yaml
on:
  pull_request:
```

O workflow será iniciado em atividades relacionadas a Pull Requests.

---

## 29. Limitar à branch main

```yaml
on:
  push:
    branches:
      - main

  pull_request:
    branches:
      - main
```

Agora, o workflow será executado:

1. Em push para a `main`.

2. Em Pull Requests destinados à `main`.

---

## 30. Execução manual

Podemos acrescentar:

```yaml
on:
  workflow_dispatch:
```

Isso permite iniciar o workflow manualmente pela interface, quando disponível.

---

## 31. Configuração combinada

```yaml
on:
  push:
    branches:
      - main

  pull_request:
    branches:
      - main

  workflow_dispatch:
```

---

# Parte 7: Jobs, runners e steps

## 32. Job

Um job é um conjunto de etapas.

Exemplo:

```yaml
jobs:
  verificar:
```

O identificador do job será:

```text
verificar
```

---

## 33. Runner

Runner é o ambiente que executa o job.

Exemplo:

```yaml
runs-on: ubuntu-latest
```

Nesse caso, o GitHub utilizará um ambiente Ubuntu disponibilizado para a execução.

---

## 34. Steps

Os steps são as etapas do job.

Exemplo:

```yaml
steps:
  - name: Exibir mensagem
    run: echo "Iniciando verificação"
```

---

## 35. Ordem das etapas

As etapas são executadas em sequência.

Se uma etapa obrigatória falhar, as etapas seguintes normalmente não serão executadas, salvo configurações específicas.

---

# Parte 8: Action pronta

## 36. O que é uma Action?

Uma Action é um componente reutilizável.

Podemos utilizar Actions criadas pelo GitHub ou por outros fornecedores.

Para acessar os arquivos do repositório durante o workflow, utilizaremos:

```yaml
uses: actions/checkout@v4
```

---

## 37. Checkout

O checkout disponibiliza o conteúdo do repositório no runner.

Sem essa etapa, nossos comandos não terão automaticamente os arquivos do projeto no diretório de trabalho esperado.

---

## 38. uses e run

```text
uses

Utiliza uma Action pronta.
```

```text
run

Executa um comando.
```

Exemplo:

```yaml
- name: Baixar o código
  uses: actions/checkout@v4
```

```yaml
- name: Listar arquivos
  run: ls -la
```

---

# Parte 9: Criando o primeiro workflow

## 39. Criando a branch

Eu não altero diretamente a `main`.

Executo:

```bash
git switch main

git pull origin main

git switch -c ci/verificacao_portal
```

---

## 40. Criando as pastas

Na raiz do projeto, crio:

```text
.github
```

Dentro dela:

```text
workflows
```

Dentro de `workflows`, crio:

```text
verificar_portal.yml
```

Estrutura:

```text
.github/
└── workflows/
    └── verificar_portal.yml
```

---

## 41. Conteúdo completo

```yaml
name: Verificação do Portal

on:
  push:
    branches:
      - main

  pull_request:
    branches:
      - main

  workflow_dispatch:

jobs:
  verificar_estrutura:
    name: Verificar estrutura do projeto

    runs-on: ubuntu-latest

    steps:
      - name: Baixar arquivos do repositório
        uses: actions/checkout@v4

      - name: Exibir arquivos encontrados
        run: |
          echo "Arquivos do repositório:"
          find . -maxdepth 3 -type f | sort

      - name: Verificar arquivos obrigatórios
        run: |
          test -f index.html
          test -f README.md
          test -f css/estilo.css

      - name: Verificar estrutura mínima do HTML
        run: |
          grep -qi "<title" index.html
          grep -qi "<h1" index.html

      - name: Informar resultado
        run: |
          echo "Estrutura básica verificada com sucesso."
```

---

# Parte 10: Explicando o workflow linha por linha

## 42. Nome

```yaml
name: Verificação do Portal
```

Esse nome aparecerá na área Actions e nos resultados do Pull Request.

---

## 43. Eventos

```yaml
on:
```

Inicia a configuração dos eventos.

---

## 44. Push

```yaml
push:
  branches:
    - main
```

O workflow será executado quando houver um push para a `main`.

---

## 45. Pull Request

```yaml
pull_request:
  branches:
    - main
```

O workflow será executado quando um Pull Request tiver a `main` como base.

---

## 46. Execução manual

```yaml
workflow_dispatch:
```

Permite iniciar o workflow manualmente.

---

## 47. Jobs

```yaml
jobs:
```

Inicia a lista de jobs.

---

## 48. Identificador do job

```yaml
verificar_estrutura:
```

É o identificador interno do job.

Ele não pode conter espaços.

---

## 49. Nome visível

```yaml
name: Verificar estrutura do projeto
```

É o nome apresentado na interface.

---

## 50. Ambiente

```yaml
runs-on: ubuntu-latest
```

Define o runner.

---

## 51. Lista de etapas

```yaml
steps:
```

Inicia as etapas.

---

## 52. Checkout

```yaml
- name: Baixar arquivos do repositório
  uses: actions/checkout@v4
```

Disponibiliza os arquivos no runner.

---

## 53. Bloco de comandos

```yaml
run: |
```

O símbolo `|` permite escrever vários comandos em linhas separadas.

---

## 54. find

```bash
find . -maxdepth 3 -type f | sort
```

Lista arquivos encontrados até a profundidade definida.

---

## 55. test

```bash
test -f index.html
```

Verifica se o arquivo existe.

Se não existir, o comando retorna falha.

---

## 56. grep

```bash
grep -qi "<title" index.html
```

Procura o texto no arquivo.

Opções utilizadas:

```text
q

Não exibe o resultado completo.
```

```text
i

Ignora diferenças entre maiúsculas e minúsculas.
```

---

# Parte 11: Registrando o workflow

## 57. Verificar arquivos

```bash
git status
```

Resultado esperado:

```text
untracked:

.github/workflows/verificar_portal.yml
```

---

## 58. Preparar

```bash
git add .github/workflows/verificar_portal.yml
```

---

## 59. Criar commit

```bash
git commit -m "Adiciona verificação automática do portal"
```

---

## 60. Publicar a branch

```bash
git push -u origin ci/verificacao_portal
```

---

## 61. Abrir Pull Request

Configuração:

```text
base

main
```

```text
compare

ci/verificacao_portal
```

Título:

```text
Adiciona verificação automática do portal
```

---

## 62. Descrição sugerida

```md
## Objetivo

Adicionar uma automação para verificar a estrutura básica do Portal da Turma.

## Alterações realizadas

1. Criação da pasta .github/workflows.
2. Criação do workflow verificar_portal.yml.
3. Verificação dos arquivos obrigatórios.
4. Verificação dos elementos title e h1 no index.html.
5. Configuração para push, Pull Request e execução manual.

## Como testar

1. Abrir o Pull Request.
2. Aguardar a execução do workflow.
3. Acessar os detalhes da verificação.
4. Confirmar que todas as etapas foram concluídas.

## Resultado esperado

O job Verificar estrutura do projeto deve ser concluído com sucesso.
```

---

# Parte 12: Analisando a execução

## 63. Área Actions

Na página do repositório, acesso:

```text
Actions
```

Lá encontrarei:

1. Nome do workflow.

2. Execuções recentes.

3. Branch utilizada.

4. Commit utilizado.

5. Autor.

6. Status.

7. Duração.

---

## 64. Estados possíveis

```text
Queued

Aguardando execução.
```

```text
In progress

Em execução.
```

```text
Success

Concluído com sucesso.
```

```text
Failure

Uma ou mais etapas falharam.
```

```text
Cancelled

Execução cancelada.
```

---

## 65. Abrindo os detalhes

Seleciono a execução.

Depois, abro o job:

```text
Verificar estrutura do projeto
```

Cada etapa poderá ser expandida.

---

## 66. Logs

Os logs mostram:

1. Comandos executados.

2. Arquivos encontrados.

3. Mensagens.

4. Erros.

5. Código de saída.

Eu utilizo os logs para descobrir onde ocorreu a falha.

---

# Parte 13: Provocando uma falha controlada

## 67. Objetivo

Vamos verificar se a automação realmente detecta um problema.

Na branch, renomeio temporariamente:

```text
css/estilo.css
```

para:

```text
css/estilo_antigo.css
```

---

## 68. Registrar a alteração

```bash
git add .

git commit -m "Simula ausência do arquivo de estilos"

git push
```

---

## 69. Resultado esperado

A etapa:

```text
Verificar arquivos obrigatórios
```

deverá falhar porque este comando não será atendido:

```bash
test -f css/estilo.css
```

---

## 70. Interpretando

O erro não significa que o GitHub Actions está quebrado.

Ele significa que a regra encontrou uma estrutura diferente da esperada.

---

## 71. Corrigindo

Restauro o nome:

```bash
git mv css/estilo_antigo.css css/estilo.css
```

Depois:

```bash
git add .

git commit -m "Restaura o arquivo de estilos obrigatório"

git push
```

A mesma proposta será atualizada e o workflow será executado novamente.

---

# Parte 14: Erros comuns em YAML

## 72. Indentação

Incorreto:

```yaml
jobs:
verificar:
runs-on: ubuntu-latest
```

Correto:

```yaml
jobs:
  verificar:
    runs-on: ubuntu-latest
```

---

## 73. Steps sem hífen

Incorreto:

```yaml
steps:
  name: Testar
  run: echo "Teste"
```

Correto:

```yaml
steps:
  - name: Testar
    run: echo "Teste"
```

---

## 74. Misturar tabs e espaços

Eu utilizo espaços.

O editor pode ser configurado para inserir espaços ao pressionar Tab.

---

## 75. Arquivo no local errado

Incorreto:

```text
workflows/verificar.yml
```

Correto:

```text
.github/workflows/verificar.yml
```

---

## 76. Extensão incorreta

Utilizo:

```text
.yml
```

ou:

```text
.yaml
```

---

## 77. Nome de branch incorreto

Se o workflow está limitado à `main`, um push para outra branch não acionará o evento `push` configurado para a `main`.

Porém, um Pull Request destinado à `main` deverá acionar o evento correspondente.

---

# Parte 15: Melhorando a automação

## 78. Verificar links locais básicos

Podemos acrescentar uma etapa simples:

```yaml
- name: Verificar arquivos HTML relacionados
  run: |
    test -f sobre.html
    test -f alunos.html
    test -f projetos.html
```

Essa etapa só deverá ser utilizada quando esses arquivos forem requisitos do projeto.

---

## 79. Verificar marcadores de conflito

Podemos impedir que marcadores sejam publicados:

```yaml
- name: Verificar marcadores de conflito
  run: |
    if grep -R -n -E "^(<<<<<<<|=======|>>>>>>>)" \
      --include="*.html" \
      --include="*.css" \
      --include="*.md" .; then
        echo "Foram encontrados marcadores de conflito."
        exit 1
    fi
```

---

## 80. Workflow completo aprimorado

```yaml
name: Verificação do Portal

on:
  push:
    branches:
      - main

  pull_request:
    branches:
      - main

  workflow_dispatch:

jobs:
  verificar_estrutura:
    name: Verificar estrutura do projeto

    runs-on: ubuntu-latest

    steps:
      - name: Baixar arquivos do repositório
        uses: actions/checkout@v4

      - name: Exibir arquivos encontrados
        run: |
          find . -maxdepth 3 -type f | sort

      - name: Verificar arquivos obrigatórios
        run: |
          test -f index.html
          test -f README.md
          test -f css/estilo.css

      - name: Verificar estrutura mínima do HTML
        run: |
          grep -qi "<title" index.html
          grep -qi "<h1" index.html

      - name: Verificar marcadores de conflito
        run: |
          if grep -R -n -E "^(<<<<<<<|=======|>>>>>>>)" \
            --include="*.html" \
            --include="*.css" \
            --include="*.md" .; then
              echo "Foram encontrados marcadores de conflito."
              exit 1
          fi

      - name: Informar resultado
        run: |
          echo "Portal verificado com sucesso."
```

---

# Parte 16: Segurança no GitHub Actions

## 81. Workflows executam comandos

Um workflow pode:

1. Ler arquivos.

2. Instalar programas.

3. Executar scripts.

4. Acessar recursos conforme as permissões concedidas.

Por isso, eu reviso alterações em workflows com atenção.

---

## 82. Actions externas

Antes de utilizar uma Action de terceiros, eu verifico:

1. Quem mantém a Action.

2. Se o repositório é confiável.

3. Qual versão está sendo utilizada.

4. Quais permissões ela solicita.

5. O que o código executa.

---

## 83. Segredos

Credenciais não devem ser escritas diretamente no YAML.

Incorreto:

```yaml
env:
  SENHA: minha_senha_real
```

Segredos devem ser armazenados nos recursos apropriados do GitHub quando forem necessários.

Nosso workflow não precisa de credenciais.

---

## 84. Princípio da menor permissão

Um workflow deve receber apenas as permissões necessárias.

Para a verificação simples do portal, não precisamos conceder permissões de escrita.

---

# Parte 17: Badge do workflow

## 85. O que é um badge?

Badge é uma pequena imagem exibida no README para mostrar uma informação.

Exemplo:

```text
Status da verificação
```

---

## 86. Adicionando pelo GitHub

Na área do workflow, posso utilizar a opção para criar o badge de status.

O GitHub gera um código Markdown semelhante a:

```md
![Verificação do Portal](ENDERECO_DO_BADGE)
```

---

## 87. Inserindo no README

```md
# Portal da Turma

![Verificação do Portal](ENDERECO_DO_BADGE)
```

> O endereço deverá ser copiado da interface do próprio repositório.

---

## 88. O que o badge comunica?

Ele pode mostrar se a execução mais recente foi:

1. Bem sucedida.

2. Falha.

3. Desconhecida.

O badge não substitui a análise dos logs.

---

# Parte 18: Realizando o merge do workflow

## 89. Revisão

Antes do merge, o revisor verifica:

1. Local correto do arquivo.

2. Indentação.

3. Eventos.

4. Comandos.

5. Actions utilizadas.

6. Resultado da execução.

7. Ausência de credenciais.

---

## 90. Aprovação

Depois da verificação, o revisor aprova.

---

## 91. Merge

Realizamos o merge na `main`.

---

## 92. Nova execução

Como o workflow está configurado para `push` na `main`, o merge deverá iniciar outra execução.

---

## 93. Atualização local

```bash
git switch main

git pull origin main

git fetch --prune origin

git branch -d ci/verificacao_portal
```

---

# Parte 19: O que é GitHub Pages?

## 94. Conceito

GitHub Pages é um serviço que publica sites estáticos a partir de um repositório.

Sites estáticos podem utilizar:

1. HTML.

2. CSS.

3. JavaScript executado no navegador.

4. Imagens.

5. Arquivos de fontes permitidos.

---

## 95. O que não funciona diretamente?

GitHub Pages não executa diretamente aplicações de servidor como:

1. PHP.

2. Java no servidor.

3. Node.js no servidor.

4. Banco de dados PostgreSQL.

5. APIs próprias executadas no servidor.

Nosso Portal da Turma utiliza HTML e CSS, portanto é adequado para publicação estática.

---

## 96. Endereço do site

Um site de projeto normalmente terá um endereço baseado em:

```text
https://NOME_DO_USUARIO.github.io/NOME_DO_REPOSITORIO/
```

O endereço exato será apresentado pelo GitHub depois da publicação.

---

# Parte 20: Preparando o site

## 97. Arquivo de entrada

O projeto deverá possuir:

```text
index.html
```

O nome deve estar em letras minúsculas e com a extensão correta.

---

## 98. Caminhos relativos

Exemplo adequado:

```html
<link rel="stylesheet" href="css/estilo.css">
```

Outro exemplo:

```html
<a href="sobre.html">Sobre</a>
```

---

## 99. Caminho que pode causar problema

```html
<link
    rel="stylesheet"
    href="C:\\Users\\Aluno\\Projeto\\css\\estilo.css"
>
```

Esse caminho existe apenas no computador do aluno.

---

## 100. Cuidado com barra inicial

Em um site de projeto, este caminho:

```html
<a href="/sobre.html">Sobre</a>
```

pode apontar para a raiz do domínio e não para a pasta do repositório.

Para o projeto simples, prefiro:

```html
<a href="sobre.html">Sobre</a>
```

---

## 101. Letras maiúsculas e minúsculas

Estes nomes podem ser tratados como diferentes:

```text
Index.html
```

```text
index.html
```

Se o link aponta para:

```html
<a href="Sobre.html">Sobre</a>
```

mas o arquivo se chama:

```text
sobre.html
```

a navegação pode falhar no site publicado.

---

## 102. Checklist antes da publicação

1. `index.html` existe.

2. O CSS está no caminho correto.

3. As imagens utilizam caminhos relativos.

4. Os nomes correspondem exatamente.

5. Os links foram testados.

6. Não existem credenciais.

7. Não existem marcadores de conflito.

8. A `main` está atualizada.

9. O workflow foi aprovado.

10. O projeto funciona localmente.

---

# Parte 21: Publicando a partir de uma branch

## 103. Configuração didática

Para um projeto HTML e CSS simples, utilizaremos a publicação a partir da branch `main`.

Fonte:

```text
Deploy from a branch
```

Branch:

```text
main
```

Pasta:

```text
/root
```

---

## 104. Acessando as configurações

No repositório:

1. Acesso `Settings`.

2. Localizo `Pages`.

3. Na área de construção e implantação, escolho a fonte.

4. Seleciono a publicação a partir de uma branch.

5. Escolho `main`.

6. Escolho a pasta raiz.

7. Salvo.

Os nomes dos menus podem variar conforme o idioma e atualizações da interface.

---

## 105. Primeira publicação

Depois de salvar, o GitHub iniciará o processo de publicação.

A página poderá levar algum tempo para apresentar a primeira versão.

O status e o endereço serão exibidos na área Pages.

---

## 106. Testando o endereço

Abro o endereço apresentado.

Verifico:

1. Página inicial.

2. Menu.

3. CSS.

4. Imagens.

5. Links internos.

6. Responsividade.

7. Conteúdo.

---

# Parte 22: Atualizando o site publicado

## 107. Criando uma melhoria

Não altero diretamente a `main`.

```bash
git switch main

git pull origin main

git switch -c feature/mensagem_encerramento
```

---

## 108. Alteração

No `index.html`, adiciono:

```html
<section>
    <h2>Curso concluído</h2>

    <p>
        Este portal foi desenvolvido de forma colaborativa
        durante o curso de Git e GitHub.
    </p>
</section>
```

---

## 109. Registro

```bash
git status

git diff

git add index.html

git commit -m "Adiciona mensagem de conclusão do curso"

git push -u origin feature/mensagem_encerramento
```

---

## 110. Pull Request

O workflow será executado.

Depois:

1. Revisamos.

2. Aprovamos.

3. Realizamos o merge.

---

## 111. Nova publicação

Depois do merge na `main`, o GitHub Pages publicará a versão atualizada conforme a fonte configurada.

---

# Parte 23: GitHub Pages com Actions

## 112. Outra possibilidade

O GitHub Pages também pode utilizar um workflow do GitHub Actions como fonte de publicação.

Essa opção é útil quando o site precisa:

1. Ser compilado.

2. Gerar arquivos antes da publicação.

3. Utilizar uma ferramenta de construção.

4. Executar etapas personalizadas.

---

## 113. Escolha para esta aula

Nosso site é formado por arquivos HTML e CSS prontos.

Por isso, utilizaremos:

```text
Publicação a partir da branch
```

Essa escolha mantém a prática simples e ajuda a separar:

```text
Workflow de verificação

GitHub Pages para publicação
```

---

## 114. Evolução futura

Em cursos avançados, podemos criar um workflow específico de implantação usando as Actions oficiais do GitHub Pages.

---

# Parte 24: Erros comuns no GitHub Pages

## 115. Erro 404

Possíveis causas:

1. Publicação ainda não concluída.

2. Branch incorreta.

3. Pasta incorreta.

4. `index.html` ausente.

5. Nome `Index.html` diferente de `index.html`.

6. Repositório ou Pages com configuração incompleta.

---

## 116. CSS não carregado

Possíveis causas:

1. Caminho incorreto.

2. Nome do arquivo diferente.

3. Letras maiúsculas e minúsculas.

4. CSS não foi enviado para a `main`.

5. Link utiliza caminho local do computador.

---

## 117. Imagem não aparece

Verifico:

```html
<img src="img/logo.png" alt="Logotipo">
```

Depois, confirmo se existe:

```text
img/logo.png
```

---

## 118. Link retorna 404

Verifico se o nome do link corresponde ao arquivo.

```html
<a href="projetos.html">Projetos</a>
```

Arquivo esperado:

```text
projetos.html
```

---

## 119. Site antigo

Possíveis causas:

1. O merge ainda não foi realizado.

2. A publicação está em andamento.

3. A página está em cache.

4. A fonte do Pages está em outra branch.

5. A alteração foi feita em uma branch não integrada.

---

## 120. Informações confidenciais

Publicar o site torna os arquivos da fonte acessíveis conforme a visibilidade e o funcionamento do serviço.

Nunca incluo:

1. Senhas.

2. Tokens.

3. Chaves privadas.

4. Dados pessoais não autorizados.

5. Credenciais de banco.

---

# Parte 25: Projeto final

## 121. Nome

```text
Portal da Turma
```

---

## 122. Objetivo

Demonstrar, em um único repositório, os conhecimentos de Git, GitHub, colaboração, versionamento, automação e publicação.

---

## 123. Requisitos do repositório

O projeto deverá possuir:

1. README completo.

2. Histórico de commits organizado.

3. Branch `main`.

4. Branches de funcionalidades.

5. Pull Requests concluídos.

6. Revisões registradas.

7. Issues.

8. Labels.

9. Milestone.

10. GitHub Project.

11. `CONTRIBUTING.md`.

12. `CHANGELOG.md`.

13. Tag de versão.

14. Release.

15. Workflow.

16. Site publicado.

---

## 124. Requisitos do site

O site deverá possuir:

1. Página inicial.

2. Apresentação da turma.

3. Conteúdos estudados.

4. Página de projetos.

5. Navegação funcional.

6. Estilos CSS.

7. Rodapé.

8. Layout organizado.

9. Caminhos relativos.

10. Ausência de dados confidenciais.

---

## 125. Requisitos do workflow

O workflow deverá:

1. Estar em `.github/workflows`.

2. Utilizar YAML válido.

3. Executar em Pull Requests para a `main`.

4. Executar em push para a `main`.

5. Utilizar checkout.

6. Verificar arquivos obrigatórios.

7. Apresentar resultado compreensível.

---

## 126. Requisitos da release final

A equipe deverá possuir uma release semelhante a:

```text
v1.0.0
```

Ela deverá apresentar:

1. Resumo da versão.

2. Funcionalidades.

3. Correções.

4. Documentação.

5. Instruções de acesso.

6. Link do site publicado.

---

# Parte 26: Preparação da apresentação

## 127. Tempo sugerido

Cada equipe terá entre cinco e dez minutos, conforme a quantidade de grupos.

---

## 128. Roteiro

### Etapa 1: Apresentação da equipe

Informar:

1. Integrantes.

2. Nome do projeto.

3. Objetivo.

---

### Etapa 2: Demonstração do site

Apresentar:

1. Página inicial.

2. Navegação.

3. Funcionalidades.

4. Responsividade.

---

### Etapa 3: Demonstração do repositório

Mostrar:

1. README.

2. Estrutura de arquivos.

3. Commits.

4. Branches.

5. Pull Requests.

6. Issues.

7. Project.

---

### Etapa 4: Automação

Mostrar:

1. Arquivo YAML.

2. Eventos.

3. Etapas.

4. Execução bem sucedida.

5. Uma falha corrigida, quando houver.

---

### Etapa 5: Versão e publicação

Mostrar:

1. Tag.

2. Release.

3. Changelog.

4. Endereço do GitHub Pages.

---

### Etapa 6: Aprendizados

Cada integrante deverá citar:

1. Um conhecimento adquirido.

2. Uma dificuldade superada.

3. Uma boa prática que levará para outros projetos.

---

# Parte 27: Retrospectiva

## 129. O que é retrospectiva?

Retrospectiva é uma reunião de reflexão sobre o trabalho realizado.

Ela não serve para procurar culpados.

Serve para identificar:

1. O que funcionou.

2. O que dificultou.

3. O que deve continuar.

4. O que precisa mudar.

5. Qual será o próximo passo.

---

## 130. Perguntas da retrospectiva

### O que funcionou bem?

Exemplos:

```text
As branches evitaram que as alterações se misturassem.
```

```text
Os Pull Requests melhoraram a revisão.
```

---

### O que foi difícil?

Exemplos:

```text
Resolver o primeiro conflito.
```

```text
Entender a diferença entre fetch e pull.
```

---

### O que devemos continuar fazendo?

Exemplos:

```text
Criar commits pequenos.
```

```text
Atualizar a main antes de criar uma branch.
```

---

### O que devemos melhorar?

Exemplos:

```text
Escrever descrições mais completas.
```

```text
Testar todos os links antes da revisão.
```

---

## 131. Registro

Criar uma Issue chamada:

```text
Retrospectiva do projeto final
```

Descrição:

```md
## O que funcionou bem

1.
2.
3.

## O que foi difícil

1.
2.
3.

## O que devemos continuar

1.
2.
3.

## O que devemos melhorar

1.
2.
3.

## Próximos passos

1.
2.
3.
```

---

# Parte 28: Checklist final do projeto

## 132. Repositório

1. O nome está adequado.

2. A descrição está preenchida.

3. O README está atualizado.

4. A estrutura está organizada.

5. Não existem credenciais.

---

## 133. Git

1. Os commits possuem mensagens específicas.

2. Não existem alterações pendentes.

3. A `main` está atualizada.

4. Branches concluídas foram excluídas.

5. O histórico está compreensível.

---

## 134. Colaboração

1. Existem Pull Requests.

2. Existem revisões.

3. Existem aprovações.

4. As Issues possuem responsáveis.

5. O Project mostra o andamento.

---

## 135. Versão

1. Existe tag.

2. Existe release.

3. O changelog está atualizado.

4. A versão segue o padrão escolhido.

---

## 136. Automação

1. O workflow existe.

2. A sintaxe está correta.

3. O workflow executa no Pull Request.

4. O workflow executa na `main`.

5. A execução mais recente foi verificada.

---

## 137. Publicação

1. O Pages está configurado.

2. O site abre.

3. O CSS carrega.

4. Os links funcionam.

5. O endereço está no README.

---

# Parte 29: Exercícios de fixação

## 138. Exercício 1: Conceitos

Responda com suas palavras.

1. O que é automação?

2. O que é integração contínua?

3. O que é GitHub Actions?

4. O que é um workflow?

5. O que é um evento?

6. O que é um job?

7. O que é um step?

8. O que é um runner?

9. Para que serve `actions/checkout`?

10. O que é GitHub Pages?

11. Que tipo de site pode ser publicado diretamente no Pages?

12. Por que a automação não substitui a revisão humana?

---

## 139. Exercício 2: Relacione os conceitos

### Conceitos

```text
A. Workflow

B. Event

C. Job

D. Step

E. Runner

F. Action

G. GitHub Pages

H. Badge
```

### Definições

```text
1. Ambiente que executa o trabalho.

2. Processo automatizado definido em YAML.

3. Pequena imagem que apresenta um status.

4. Serviço de publicação de sites estáticos.

5. Atividade que inicia um workflow.

6. Componente reutilizável.

7. Conjunto de etapas.

8. Etapa individual executada dentro de um job.
```

---

## 140. Exercício 3: Complete o workflow

```yaml
name: Verificação Simples

on:
  __________:
    branches:
      - main

jobs:
  verificar:
    runs-on: __________

    steps:
      - name: Baixar arquivos
        uses: actions/__________@v4

      - name: Verificar index
        run: test -f __________
```

---

## 141. Exercício 4: Identifique o erro

Observe:

```yaml
name: Teste

on:
push:

jobs:
verificar:
  runs-on: ubuntu-latest
  steps:
  - name: Testar
  run: echo "Olá"
```

Responda:

1. Qual é o principal problema?

2. Como corrigir a indentação?

3. Onde o hífen deve aparecer?

---

## 142. Exercício 5: Interprete o workflow

```yaml
name: Verificar README

on:
  pull_request:
    branches:
      - main

jobs:
  documentacao:
    runs-on: ubuntu-latest

    steps:
      - uses: actions/checkout@v4

      - run: test -f README.md
```

Responda:

1. Quando será executado?

2. Qual é o nome do job?

3. Qual runner será utilizado?

4. Qual arquivo será verificado?

5. O que acontece se o arquivo não existir?

---

## 143. Exercício 6: Caminhos do Pages

Classifique como adequado ou inadequado.

```text
css/estilo.css

C:\\Users\\Aluno\\Projeto\\css\\estilo.css

img/logo.png

/sobre.html

sobre.html

Sobre.html quando o arquivo é sobre.html
```

Explique.

---

## 144. Exercício 7: Organize o fluxo

Coloque na ordem correta:

```text
Realizar o merge.

Criar uma branch.

Publicar a nova versão do site.

Criar commits.

Abrir um Pull Request.

Executar o workflow.

Revisar.

Desenvolver a alteração.
```

---

## 145. Exercício 8: Diagnóstico

O site abre, mas o CSS não aparece.

Liste cinco verificações que deverão ser realizadas.

---

## 146. Exercício 9: Projeto final

Para cada item, marque:

```text
Concluído

Em andamento

Não iniciado
```

Itens:

1. README.

2. Issues.

3. Branches.

4. Pull Requests.

5. Workflow.

6. Tag.

7. Release.

8. Pages.

9. Apresentação.

10. Retrospectiva.

---

# Parte 30: Desafios

## 147. Desafio 1: Workflow mínimo

Crie um workflow que verifique apenas:

```text
index.html

README.md
```

Ele deverá executar em Pull Requests para a `main`.

---

## 148. Desafio 2: Verificação de conflito

Acrescente uma etapa que falhe quando encontrar:

```text
<<<<<<<

=======

>>>>>>>
```

em arquivos HTML, CSS ou Markdown.

---

## 149. Desafio 3: Falha e correção

1. Crie uma regra para um arquivo obrigatório.

2. Remova ou renomeie o arquivo.

3. Observe a falha.

4. Abra os logs.

5. Corrija o projeto.

6. Envie um novo commit.

7. Confirme o sucesso.

---

## 150. Desafio 4: Badge

Adicione ao README:

1. Badge do workflow.

2. Link do site.

3. Versão atual.

4. Link da release.

---

## 151. Desafio 5: Página 404

Crie:

```text
404.html
```

A página deverá apresentar:

1. Mensagem de página não encontrada.

2. Link para a página inicial.

3. Estilos compatíveis com o portal.

---

## 152. Desafio 6: Publicação pela pasta docs

Em um repositório de teste:

1. Crie uma pasta `docs`.

2. Coloque um `index.html`.

3. Configure o Pages para publicar da pasta `docs` da `main`.

4. Compare com a publicação pela raiz.

---

## 153. Desafio 7: Execução manual

Adicione:

```yaml
workflow_dispatch:
```

Execute o workflow manualmente e registre:

1. Horário.

2. Branch.

3. Commit.

4. Resultado.

---

## 154. Desafio 8: Workflow com dois jobs

Crie:

```text
verificar_estrutura

verificar_documentacao
```

O primeiro verifica HTML e CSS.

O segundo verifica README, CONTRIBUTING e CHANGELOG.

---

## 155. Desafio 9: Release final

Publique uma release:

```text
v1.0.0
```

Inclua:

1. Resumo.

2. Funcionalidades.

3. Correções.

4. Link do site.

5. Créditos da equipe.

---

## 156. Desafio 10: Apresentação técnica

Prepare uma apresentação de até dez minutos.

Ela deverá demonstrar:

1. Site.

2. Repositório.

3. Histórico.

4. Pull Request.

5. Issue.

6. Workflow.

7. Release.

8. Pages.

9. Aprendizado da equipe.

---

## 157. Desafio 11: Próxima versão

Crie uma milestone:

```text
v1.1.0
```

Adicione três Issues de melhoria.

Exemplos:

1. Adicionar modo escuro.

2. Melhorar responsividade.

3. Criar galeria de projetos.

---

## 158. Desafio 12: Portfólio individual

Cada aluno deverá criar um repositório próprio contendo:

1. README profissional.

2. Um projeto publicado.

3. Histórico organizado.

4. Pelo menos uma release.

5. GitHub Pages.

6. Descrição das tecnologias.

---

# Parte 31: Avaliação final

## 159. Critérios

A avaliação poderá valer 10 pontos.

### Organização do repositório: 1 ponto

Arquivos e documentação estão organizados.

### Histórico Git: 1 ponto

Commits possuem mensagens adequadas.

### Trabalho com branches: 1 ponto

As funcionalidades foram desenvolvidas separadamente.

### Colaboração: 1 ponto

Existem Pull Requests e revisões.

### Planejamento: 1 ponto

Issues e Project foram utilizados.

### Versionamento: 1 ponto

Existe tag, changelog e release.

### Workflow: 2 pontos

A automação funciona e foi compreendida pela equipe.

### GitHub Pages: 1 ponto

O site está publicado e funcional.

### Apresentação: 1 ponto

A equipe explicou o processo com clareza.

---

## 160. Evidências

A equipe deverá apresentar:

1. Link do repositório.

2. Link do site.

3. Link da release.

4. Execução do workflow.

5. Pull Request revisado.

6. Issue concluída.

7. Project atualizado.

8. Histórico de commits.

9. Retrospectiva.

---

# Parte 32: Gabarito

## 161. Gabarito do exercício 1

### Questão 1

Automação é a execução automática de tarefas a partir de regras definidas.

### Questão 2

Integração contínua é a prática de integrar alterações com frequência e executar verificações automáticas.

### Questão 3

GitHub Actions é a plataforma de automação integrada ao GitHub.

### Questão 4

Workflow é um processo automatizado definido em um arquivo YAML.

### Questão 5

Evento é uma atividade que inicia um workflow.

### Questão 6

Job é um conjunto de etapas executadas em um runner.

### Questão 7

Step é uma etapa individual de um job.

### Questão 8

Runner é o ambiente que executa os jobs.

### Questão 9

Disponibiliza os arquivos do repositório no runner.

### Questão 10

GitHub Pages é um serviço para publicação de sites estáticos.

### Questão 11

Sites formados por arquivos estáticos, como HTML, CSS e JavaScript executado no navegador.

### Questão 12

Porque verificações automáticas não compreendem completamente a qualidade, intenção e experiência do usuário.

---

## 162. Gabarito do exercício 2

```text
A corresponde a 2.

B corresponde a 5.

C corresponde a 7.

D corresponde a 8.

E corresponde a 1.

F corresponde a 6.

G corresponde a 4.

H corresponde a 3.
```

---

## 163. Gabarito do exercício 3

```yaml
name: Verificação Simples

on:
  pull_request:
    branches:
      - main

jobs:
  verificar:
    runs-on: ubuntu-latest

    steps:
      - name: Baixar arquivos
        uses: actions/checkout@v4

      - name: Verificar index
        run: test -f index.html
```

---

## 164. Gabarito do exercício 4

O problema principal é a indentação.

Versão corrigida:

```yaml
name: Teste

on:
  push:

jobs:
  verificar:
    runs-on: ubuntu-latest

    steps:
      - name: Testar
        run: echo "Olá"
```

---

## 165. Gabarito do exercício 5

1. Em Pull Requests destinados à `main`.

2. `documentacao`.

3. `ubuntu-latest`.

4. `README.md`.

5. O comando falha e o job será marcado como falha.

---

## 166. Gabarito do exercício 6

### Adequados

```text
css/estilo.css

img/logo.png

sobre.html
```

### Inadequados ou arriscados

```text
C:\\Users\\Aluno\\Projeto\\css\\estilo.css
```

Caminho local do computador.

```text
/sobre.html
```

Pode apontar para a raiz do domínio.

```text
Sobre.html quando o arquivo é sobre.html
```

Diferença entre maiúsculas e minúsculas.

---

## 167. Gabarito do exercício 7

Ordem:

```text
Criar uma branch.

Desenvolver a alteração.

Criar commits.

Abrir um Pull Request.

Executar o workflow.

Revisar.

Realizar o merge.

Publicar a nova versão do site.
```

---

## 168. Gabarito do exercício 8

Possíveis verificações:

1. Caminho informado no `link`.

2. Nome do arquivo.

3. Maiúsculas e minúsculas.

4. Arquivo presente na branch publicada.

5. Publicação concluída.

6. Cache do navegador.

7. Sintaxe do elemento `link`.

---

# Parte 33: Revisão oral

## 169. Perguntas

1. O que é automação?

2. O que significa CI?

3. O que é um workflow?

4. Onde ficam os arquivos de workflow?

5. O que inicia um workflow?

6. O que é um job?

7. O que é um runner?

8. Para que serve checkout?

9. Como identificamos uma falha?

10. O que é GitHub Pages?

11. Por que o `index.html` é importante?

12. Como o site é atualizado?

13. Qual é a diferença entre automação e revisão?

14. Qual foi o principal aprendizado do curso?

---

# Parte 34: Resumo dos arquivos

## 170. Workflow

```text
.github/workflows/verificar_portal.yml
```

---

## 171. Página inicial

```text
index.html
```

---

## 172. Estilos

```text
css/estilo.css
```

---

## 173. Documentação

```text
README.md

CONTRIBUTING.md

CHANGELOG.md
```

---

## 174. Página de erro

```text
404.html
```

---

# Parte 35: Resumo dos comandos

## 175. Preparação

```bash
git switch main

git pull origin main

git status
```

---

## 176. Branch da automação

```bash
git switch -c ci/verificacao_portal
```

---

## 177. Registro

```bash
git add .github/workflows/verificar_portal.yml

git commit -m "Adiciona verificação automática do portal"

git push -u origin ci/verificacao_portal
```

---

## 178. Atualização depois do merge

```bash
git switch main

git pull origin main

git fetch --prune origin

git branch -d ci/verificacao_portal
```

---

## 179. Nova funcionalidade

```bash
git switch -c feature/nome_da_tarefa

git status

git add .

git commit -m "Descrição da alteração"

git push -u origin feature/nome_da_tarefa
```

---

# Parte 36: Fluxo final do curso

## 180. Planejamento

```text
Issue

Label

Responsável

Milestone

Project
```

---

## 181. Desenvolvimento

```bash
git switch main

git pull origin main

git switch -c feature/nome_da_tarefa
```

---

## 182. Registro

```bash
git status

git diff

git add .

git commit -m "Descrição da alteração"

git push
```

---

## 183. Colaboração

```text
Pull Request

GitHub Actions

Revisão

Correções

Aprovação

Merge
```

---

## 184. Entrega

```text
Tag

Release

GitHub Pages
```

---

# Parte 37: Encerramento do curso

## 185. O que aprendemos nesta aula

Nesta aula, eu mostrei como automatizar uma verificação e publicar um site.

Aprendemos que:

```text
Workflow é um processo automatizado.
```

```text
Evento inicia o workflow.
```

```text
Job reúne etapas.
```

```text
Runner executa o trabalho.
```

```text
Step representa uma ação individual.
```

```text
GitHub Pages publica sites estáticos.
```

---

## 186. O que aprendemos no curso

Ao longo das oito aulas, construímos esta sequência:

```text
Controle de versão

Repositório local

Repositório remoto

Commits

Branches

Merge

Pull Requests

Revisão

Conflitos

Recuperação

Issues

Projects

Tags

Releases

Actions

Pages
```

---

## 187. Mais importante do que decorar comandos

Eu não espero que o aluno memorize imediatamente todos os comandos.

Eu espero que ele aprenda a perguntar:

```text
Em qual branch estou?

O que foi alterado?

O que está preparado?

O que está registrado?

O que está publicado?

O que será integrado?

Qual comando corresponde ao estado atual?
```

---

## 188. Continuidade dos estudos

Depois deste curso, o aluno poderá avançar para:

1. Git rebase.

2. Cherry-pick.

3. Estratégias avançadas de branches.

4. Git hooks.

5. Actions com testes automatizados.

6. Deploy em serviços de nuvem.

7. Actions para Java, TypeScript ou Python.

8. Pacotes e registries.

9. Segurança de dependências.

10. Contribuição em projetos de código aberto.

---

## 189. Frase de encerramento

O Git registra como um projeto evoluiu.

O GitHub mostra como uma equipe colaborou.

As Issues registram o que precisava ser feito.

Os Pull Requests registram como as decisões foram revisadas.

As releases registram o que foi entregue.

As automações aumentam a confiança no processo.

E o projeto publicado demonstra o resultado de todo esse trabalho.

Ao concluir este curso, você não aprendeu apenas comandos.

Você aprendeu a organizar mudanças, colaborar com responsabilidade e transformar um conjunto de arquivos em um projeto profissional.

Parabéns pela conclusão! 🚀🎓

---

# Referências

1. Documentação oficial do GitHub Actions  
   https://docs.github.com/pt/actions

2. Introdução ao GitHub Actions  
   https://docs.github.com/pt/actions/get-started/quickstart

3. Sintaxe de workflows  
   https://docs.github.com/pt/actions/writing-workflows/workflow-syntax-for-github-actions

4. Eventos que acionam workflows  
   https://docs.github.com/pt/actions/writing-workflows/choosing-when-your-workflow-runs/events-that-trigger-workflows

5. Documentação do GitHub Pages  
   https://docs.github.com/pt/pages

6. Configuração da fonte de publicação  
   https://docs.github.com/pt/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site

7. Início rápido do GitHub Pages  
   https://docs.github.com/pt/pages/quickstart

8. Uso seguro do GitHub Actions  
   https://docs.github.com/pt/actions/security-for-github-actions/security-guides/security-hardening-for-github-actions

9. Documentação oficial do Git  
   https://git-scm.com/docs
