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
| `git push`                 | Envia os commits locais para o repositório remoto (como o GitHub).       |
| `git pull`                 | Atualiza o repositório local com as mudanças do repositório remoto.      |
| `git fetch`                | Baixa as mudanças do repositório remoto sem aplicar ao seu diretório.    |
| `git merge <branch>`       | Junta uma branch ao branch atual.                                        |
| `git branch`               | Lista as branches existentes no repositório.                             |
| `git checkout <branch>`    | Muda para outra branch.                                                  |
| `git log`                  | Mostra o histórico de commits.                                           |
| `git diff`                 | Mostra as diferenças entre arquivos modificados e os commits anteriores. |
| `git remote -v`            | Lista os repositórios remotos vinculados ao projeto local.               |
