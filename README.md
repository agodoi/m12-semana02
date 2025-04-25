# m12-semana02

Esta instrução abordará tópicos essenciais para o domínio completo do Git, incluindo assinatura de commits para garantir autenticidade, criptografia para proteger dados sensíveis e comandos avançados como stash, cherry-pick e bisect. Também explorará as diferenças entre rebase e merge, com foco na organização do histórico de commits e como aplicar rebase interativo para reordenar, mesclar, editar ou remover commits de forma eficaz. A resolução de conflitos será discutida detalhadamente, enfatizando boas práticas para manter a integridade do código durante operações complexas.

- **Git** é um **sistema de controle de versões mais popular** local. Ele permite que você acompanhe mudanças no código, volte a versões anteriores e trabalhe em diferentes ramificações de um projeto no seu próprio computador.

- **GitHub** é uma **plataforma online** que hospeda repositórios Git. Ele facilita a colaboração entre desenvolvedores, permitindo compartilhamento, revisão de código, issues, pull requests, entre outros recursos.

Em ambos, você pode trabalhar em equipe, formando uma única versão estável do projeto.

Resumindo:  
**Git** = ferramenta de versionamento.  
**GitHub** = rede social para projetos versionados com Git.

Git --> é o sistema de controle de versões mais popular, que documenta e armazena todas as alterações ao longo do desenvolvimento do projeto. Foi criado pelo pai do Linux
Github --> é uma rede social de projetos técnicos.


## (1) Configurando o Git

### 1.1 Comandos iniciais para Commits
Abra o Git, e digite 

```
git config --global user.name "seu nome"
```

```
git config --global user.email "seu email"
```

Na tela a seguir, você tem outros códigos que verificam as suas configurações e se precisar mudar o Editor de Textos Padrão faça:

```
git config --global core.editor "path do executável do novo editor"
```

### (2) Comandos do Git

| Comando                     | Descrição                                                                 |
|----------------------------|---------------------------------------------------------------------------|
| `pwd`                      | Mostra o diretório atual (onde você está no terminal).                    |
| `mkdir <nome>`             | Cria uma nova pasta/diretório.                                           |
| `touch <nome_do_arquivo>`  | Cria um novo arquivo vazio.                                              |
| `cd /c`                    | Entra no disco C:\ (útil no Git Bash ou terminal Unix-like no Windows).  |
| `ls`                       | Lista arquivos e diretórios do diretório atual.                          |
| `ls -a`                    | Lista **todos** os arquivos, incluindo ocultos (ex: `.git`).             |
| `git init`                 | Inicializa um novo repositório Git local.                                |
| `git clone <url>`          | Clona um repositório remoto para o ambiente local.                       |
| `git status`               | Mostra o estado atual dos arquivos (modificados, staged, etc.).          |
| `git add <arquivo>`        | Adiciona arquivos ao "staging area" (preparar para commit).              |
| `git commit -m "mensagem"` | Salva as mudanças com uma mensagem descritiva.                           |
| `git push`                 | Envia os commits locais para o repositório remoto.                       |
| `git pull`                 | Baixa o repositório remoto e atualiza o repositório local.               |
| `git fetch`                | Equivale ao PULL, porém baixa as mudanças do repositório remoto sem aplicar ao seu diretório.    |
| `git merge <branch>`       | Junta uma branch ao branch atual.                                        |
| `git branch`               | Lista as branches existentes no repositório.                             |
| `git checkout <branch>`    | Muda para outra branch.                                                  |
| `git log`                  | Mostra o histórico de commits.                                           |
| `git log --oneline`        | Exibe o histórico de commits em formato compacto e simplificado.         |
| `git diff`                 | Mostra as diferenças entre arquivos modificados e os commits anteriores. |
| `git remote -v`            | Lista os repositórios remotos vinculados ao projeto local.               |
| `git config --global`      | Define configurações globais do Git (nome, e-mail, editor, etc.).        |
| `git rebase -i HEAD~N`     | Edita interativamente os últimos N commits (squash, reorder, etc.).      |
| `git reset --soft HEAD~1`  | Desfaz o último commit, mantendo as alterações no staging.               |
| `git checkout HEAD~2`      | Acessa o estado do projeto como estava dois commits atrás.               |


---
### PRÁTICA (1): um repositório remoto com vários respositórios locais (Git básico)

### Fazer em quatro pessoas

**Objetivo**: vamos brincar com comandos básicos de Git

**Contexto:** considere que você tem um repositório no Github e deseja desenvolvê-lo no PC pessoal e no computador da empresa.

**(a)** No dia D+0 você cria o projeto no PC pessoal e sobe uma cópia no Github.

**(b)** No dia D+1 você cria e apaga arquivos do seu projeto usando seu PC pessoal.

**(c)** No D+2 você cria e apaga arquivos do seu projeto usando o PC da empresa.

## ✅ Entregáveis

**(1)** Quais os comandos ```git``` básicos e obrigatórios de cada etapa (a), (b) e (c) para fazer essas alterações, evitar conflitos e manter tudo sincronizado no menor tempo possível? Prepare um log explicativo

**(2)** Coloque-os em ordem e justifique. 

**(3)** Como você resolve os conflitos visualmente usando o VSCode?

**(4)** O grupo precisa fazer essa simulações ao vivo

---
### PRÁTICA (2):

**Objetivos:** vamos simular um cenário profissional onde diferentes funcionalidades são desenvolvidas em branches separadas, integradas via pull request, com o uso consciente de git merge, git diff, resolução de conflitos simples e boas práticas com mensagens de commit.

**Contexto:** você e um(a) colega estão desenvolvendo um site institucional. O repositório principal está hospedado no GitHub. Você criará uma branch para trabalhar na página de contato e sua colega criará uma branch para a página sobre nós. Ao final, vocês deverão unir tudo na branch principal (main), usando boas práticas colaborativas.

**ETAPA 1 - Organização inicial**

**(a)** Crie um novo repositório no GitHub.

**(b)** Clone esse repositório em duas máquinas diferentes (ou duas pastas distintas, simulando dois devs).

**(c)** Crie a estrutura inicial do site (ex: index.html, style.css) e suba para a branch main.

**ETAPA 2 - Trabalho em branches separadas**

**(d)** Em dupla, crie uma branch chamada **feature/contato** e a outra dupla cria a branch **feature/sobre-nos**.
Ambos devem:

**(e)** Criar seus respectivos arquivos HTML.

**(f)** Fazer ao menos 2 commits com mensagens claras.

**(g)** Usar git log --oneline para revisar o histórico.

**(h)** Subir a branch para o GitHub com git push -u origin <nome-da-branch>.

**ETAPA 3 - Integração no GitHub (Pull Request)**

**(i)** Cada dupla abre um pull request no GitHub para a branch main.

**(j)** A outra dupla faz a revisão do PR. 

**(k)** Se não houver conflitos, aceita e faz o merge pelo GitHub.

**ETAPA 4 - Simulando um conflito e resolvendo no VS Code**

**(l)** Ambas duplas alteram a mesma linha no arquivo style.css, em suas branches locais.

**(m)** Uma dupla faz merge com main.

**(n)** A outra, ao tentar o merge, terá um conflito. Resolva o conflito com o editor de conflitos do VS Code.


## ✅ Entregáveis

**(1)** Prints do git log, tela de conflito no VS Code e merges.

**(2)** Print da tela do GitHub com os pull requests e merges aprovados.

**(3)** Uma apresentação explicando:

  **(3.1)** Para que serve uma branch.
  
  **(3.2)** Diferença entre merge automático e com conflito.
  
  **(3.3)** Como o GitHub ajuda na integração entre times.
  
  **(3.4)** Qual foi a principal vantagem de usar branches para dividir tarefas entre colegas?
  
  **(3.5)** O que torna o uso de pull request mais seguro que apenas fazer git push direto na main?
  
  **(3.6)** O que causou o conflito de merge e como você resolveu?
  
  **(3.7)** Quais cuidados você tomaria numa equipe maior, com mais pessoas fazendo commits ao mesmo tempo?

---
### PRÁTICA (3): manipulando o histórico com responsabilidade (Git avançado)

**Objetivos**: aplicar comandos avançados do Git — como rebase, stash, cherry-pick, reset e revert — em um cenário colaborativo simulado, compreendendo os riscos e benefícios de manipular o histórico de commits.

**Contexto:** ocê está trabalhando em um projeto de software junto com uma colega. Ambos utilizam o GitHub para manter o repositório sincronizado. Durante o desenvolvimento, ocorrem situações comuns no mundo real: múltiplos commits confusos, necessidade de aplicar hotfixes pontuais, troca de branch com trabalho em andamento, e conflito entre alterações locais e remotas. Sua missão será limpar o histórico, manter o projeto organizado e colaborar de forma segura, usando comandos poderosos do Git.

## ✅ Entregáveis



**(2)** Por que é importante limpar e organizar o histórico de commits antes de enviar o código para o repositório remoto?

**(3)** Em que situações o git rebase -i pode ser mais vantajoso do que o uso do merge?

**(4)** Qual é a utilidade do comando git stash em um fluxo de trabalho ágil?

**(5)** Em que cenário o uso de stash pode evitar perda de produtividade durante o desenvolvimento?

**(6)** Por que o git cherry-pick é útil quando precisamos aplicar uma correção feita em uma branch para outra?

**(7)** Qual o risco de usar cherry-pick em vez de merge para transferir commits entre branches?

**(8)** Em qual situação o comando git reset --soft é preferível ao git revert?

**(9)** Quando o git revert é a melhor opção em projetos colaborativos?

**(10)** Quais são as principais diferenças entre reset e revert em termos de efeito no histórico de commits?

**(11)** Como o VS Code pode ser utilizado para resolver conflitos de merge de forma visual?

**(12)** O que pode acontecer se um rebase for feito depois de um push já realizado para o GitHub? Como evitar esse problema?
