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



colocar uma tabela enorme como um manual
criar 5 cenários de conflito e pedir para os alunos resolverem
cenários mais complexos


## PRÁTICA (1): um repositório remoto / vários respositórios locais

### Considere que você tem um repositório no Github e deseja desenvolvê-lo no PC pessoal e no computador da empresa.

#### (a) No dia D+0 você cria o projeto no PC pessoal e sobe uma cópia no Github.
#### (b) No dia D+1 você cria e apaga arquivos do seu projeto usando seu PC pessoal.
#### (c) No D+2 você cria e apaga arquivos do seu projeto usando o PC da empresa.

### Quais os comandos ```git``` básicos e obrigatórios de cada etapa (a), (b) e (c) para fazer essas alterações, evitar conflitos e manter tudo sincronizado no menor tempo possível? Coloque-os em ordem e justifique. Como você resolve os conflitos usando o VSCode?

### O grupo precisa fazer as simulações ao vivo


## PRÁTICA (2): manipulando o histórico com responsabilidade (Git Avançado)

### Você está trabalhando em um projeto de software junto com uma colega. Ambos utilizam o GitHub para manter o repositório sincronizado. Durante o desenvolvimento, ocorrem situações comuns no mundo real: múltiplos commits confusos, necessidade de aplicar hotfixes pontuais, troca de branch com trabalho em andamento, e conflito entre alterações locais e remotas. Sua missão será limpar o histórico, manter o projeto organizado e colaborar de forma segura, usando comandos poderosos do Git.


### Aplicar comandos avançados do Git — como rebase, stash, cherry-pick, reset e revert — em um cenário colaborativo simulado, compreendendo os riscos e benefícios de manipular o histórico de commits e responder:


#### (a) Por que é importante limpar e organizar o histórico de commits antes de enviar o código para o repositório remoto?
#### (b) Em que situações o git rebase -i pode ser mais vantajoso do que o uso do merge?
#### (c) Qual é a utilidade do comando git stash em um fluxo de trabalho ágil?
#### (d) Em que cenário o uso de stash pode evitar perda de produtividade durante o desenvolvimento?
#### (e) Por que o git cherry-pick é útil quando precisamos aplicar uma correção feita em uma branch para outra?
#### (f) Qual o risco de usar cherry-pick em vez de merge para transferir commits entre branches?
#### (g) Em qual situação o comando git reset --soft é preferível ao git revert?
#### (h) Quando o git revert é a melhor opção em projetos colaborativos?
#### (i) Quais são as principais diferenças entre reset e revert em termos de efeito no histórico de commits?
#### (j) Como o VS Code pode ser utilizado para resolver conflitos de merge de forma visual?
#### (k) O que pode acontecer se um rebase for feito depois de um push já realizado para o GitHub? Como evitar esse problema?


