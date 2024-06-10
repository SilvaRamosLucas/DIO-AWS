# 📘 Guia de Comandos Git

## Introdução

Git é uma ferramenta poderosa e essencial para controle de versão, amplamente utilizada no desenvolvimento de software. Ela permite que os desenvolvedores colaborem de maneira eficiente e acompanhem as mudanças no código-fonte ao longo do tempo. Abaixo, você encontrará os comandos Git mais importantes, acompanhados de exemplos para ilustrar seu uso.Git is a powerful and essential tool for version control, widely used in software development. It allows developers to collaborate efficiently and track changes in the source code over time. Below, you'll find the most important Git commands, accompanied by examples to illustrate their use.

---

<details>

<summary> Tópicos </summary>

## 📌 Índice

1. [Inicializando um Repositório](#1-inicializando-um-repositório)
2. [Clonando um Repositório](#2-clonando-um-repositório)
3. [Adicionando Mudanças](#3-adicionando-mudanças)
4. [Commit de Mudanças](#4-commit-de-mudanças)
5. [Verificando Status](#5-verificando-status)
6. [Enviando Mudanças](#6-enviando-mudanças)
7. [Recebendo Mudanças](#7-recebendo-mudanças)
8. [Gerenciando Branches](#8-gerenciando-branches)
9. [Trocando de Branches](#9-trocando-de-branches)
10. [Mesclando Branches](#10-mesclando-branches)
11. [Visualizando Histórico de Commits](#11-visualizando-histórico-de-commits)
12. [Gerenciando Repositórios Remotos](#12-gerenciando-repositórios-remotos)
13. [Salvar Mudanças Temporárias](#13-salvar-mudanças-temporárias)
14. [Rebasing de Branches](#14-rebasing-de-branches)
15. [Desfazer Alterações](#15-desfazer-alterações)
16. [Mostrar Diferenças](#16-mostrar-diferenças)
17. [Marcando Commits](#17-marcando-commits)
18. [Cherry-Picking de Commits](#18-cherry-picking-de-commits)
19. [Buscando Mudanças](#19-buscando-mudanças)
20. [Arquivando um Repositório](#20-arquivando-um-repositório)
21. [Gerenciando Submódulos](#21-gerenciando-submódulos)
22. [Configurando o Git](#22-configurando-git)

</details>

---

## ⚙ Comandos

### 1. Inicializando um Repositório

O comando `git init` inicializa um novo repositório Git em um diretório.

```sh
$ mkdir meu_projeto
$ cd meu_projeto
$ git init
```

### 2. Clonando um Repositório

The `git clone` command is used to create a copy of an existing repository.

```sh
$ git clone https://github.com/user/repo.git
```

### 3. Adicionando Mudanças

The `git add` command adds changes in the working directory to the staging area.

```sh
#To add all modified files
$ git add file.txt
$ git add .
```

### 4. Commit de Mudanças

The `git commit` command records the changes added to the staging area in a new commit.

```sh
$ git commit -m "Message describing the changes"
```

### 5. Checking Status

The `git status` command shows the current state of the working directory and the staging area.

```sh
$ git status
```

### 6. Pushing Changes

The `git push` command sends commits from the local repository to a remote repository.

```sh
$ git push origin master
```

### 7. Pulling Changes

The `git pull` command fetches and integrates changes from a remote repository.

```sh
$ git pull origin master
```

### 8. Managing Branches

The `git branch` command allows you to manage branches.

```sh
# List branches
$ git branch

# Create a new branch
$ git branch new-feature

# Delete a branch
$ git branch -d old-branch
```

### 9. Switching Branches

The `git checkout` command is used to switch branches or restore files.

```sh
# Switch to another branch
$ git checkout new-feature

# Create a new branch and switch to it
$ git checkout -b new-feature
```

### 10. Merging Branches

The `git merge` command combines changes from different branches.

```sh
$ git checkout master
$ git merge new-feature
```

### 11. Viewing Commit History

The `git log` command displays the commit history of the repository.

```sh
$ git log

# Show history with diff stats
$ git log --stat
```

### 12. Managing Remote Repositories

The `git remote` command allows you to manage connections to remote repositories.

```sh
# List remote repositories
$ git remote -v

# Add a remote repository
$ git remote add origin https://github.com/user/repo.git

# Remove a remote repository
$ git remote remove origin
```

### 13. Stashing Changes

The `git stash` command temporarily saves uncommitted changes.

```sh
# Save uncommitted changes
$ git stash

# List saved stashes
$ git stash list

# Apply the most recent stash
$ git stash apply

# Apply and remove the most recent stash
$ git stash pop
```

### 14. Rebasing Branches

The `git rebase` command reapplies commits from one branch on top of another.

```sh
$ git checkout my-branch
$ git rebase master
```

### 15. Resetting Changes

The `git reset` command moves the current branch pointer and modifies the staging area and/or working directory.

```sh
# Revert commits but keep changes in the working directory
$ git reset --soft HEAD~1

# Revert commits and changes in the staging area, but keep in the working directory
$ git reset --mixed HEAD~1

# Revert commits and all changes
$ git reset --hard HEAD~1
```

### 16. Showing Differences

The `git diff` command shows the differences between commits, branches, and the working directory.

```sh
# Show differences between the working directory and the staging area
$ git diff

# Show differences between the staging area and the last commit
$ git diff --cached

# Show differences between two branches
$ git diff branch1 branch2
```

### 17. Tagging Commits

The `git tag` command marks specific points in the repository's history.

```sh
# Create an annotated tag
$ git tag -a v1.0 -m "Version 1.0"

# Create a lightweight tag
$ git tag v1.1

# List all tags
$ git tag

# Push tags to the remote repository
$ git push origin --tags
```

### 18. Cherry-Picking Commits
The `git cherry-pick` command applies a specific commit from one branch to another.

```sh
$ git checkout master
$ git cherry-pick abc123
```

### 19. Fetching Changes

The `git fetch` command fetches changes from a remote repository without automatically integrating them.

```sh
$ git fetch origin
```

### 20. Archiving a Repository

The `git archive` command creates a tar or zip file of a repository tree.

```sh
# Create a tar file of the master branch
$ git archive --format=tar master | gzip > project.tar.gz
```

### 21. Managing Submodules

The `git submodule` command manages submodules, which are Git repositories inside another Git repository.

```sh
# Add a submodule
$ git submodule add https://github.com/user/subrepo.git path/to/subrepo

# Initialize submodules
$ git submodule init

# Update submodules
$ git submodule update
```

### 22. Configuring Git

The `git config` command configures Git options and behaviors.

```sh
# Configure username
$ git config --global user.name "Your Name"

# Configure email
$ git config --global user.email "youremail@example.com"

# View all configurations
$ git config --list
```

## ☑ Conclusão

### Esses comandos formam a base do uso diário do Git, permitindo que os desenvolvedores controlem a versão do seu código, colaborem de maneira eficiente e mantenham um histórico claro e detalhado de mudanças no projeto. Dominar esses comandos é essencial para qualquer desenvolvedor que trabalha em equipe ou em projetos de longo prazo. Happy Coding! 🚀

## 📚 Documentação

- [Git](https://git-scm.com/doc)
- [GitHub](https://docs.github.com/en)
- [Markdown](https://www.markdownguide.org/)
