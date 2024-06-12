# 📘 Guia de Comandos Git

## Introdução

Git é uma ferramenta poderosa e essencial para controle de versão, amplamente utilizada no desenvolvimento de software. Ela permite que os desenvolvedores colaborem de maneira eficiente e acompanhem as mudanças no código-fonte ao longo do tempo. Abaixo, você encontrará os comandos Git mais importantes, acompanhados de exemplos para ilustrar seu uso.

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

O comando `git clone` é usado para criar uma cópia de um repositório existente.

```sh
$ git clone https://github.com/usuario/repo.git
```

### 3. Adicionando Mudanças

O comando `git add` adiciona mudanças no diretório de trabalho para a *Stage Area*

```sh
# Para adicionar todos os arquivos modificados
$ git add arquivo.txt
$ git add .
```

### 4. Commit de Mudanças

O comando `git commit` registra as mudanças adicionadas na *Stage Area* em um novo commit.

```sh
$ git commit -m "Mensagem descrevendo as mudanças"
```

### 5. Verificando Status

O comando `git status` mostra o estado atual do diretório de trabalho e da *Stage Area*.

```sh
$ git status
```

### 6. Enviando Mudanças

O comando `git push` envia commits do repositório local para um repositório remoto.

```sh
$ git push origin master
```

### 7. Recebendo Mudanças

O comando `git pull` busca e integra mudanças de um repositório remoto.

```sh
$ git pull origin master
```

### 8. Gerenciando Branches

O comando `git branch` permiteque você gerencie branches.

```sh
# Listar branches
$ git branch

# Criar uma nova branch
$ git branch nova-funcionalidade

# Delete a branch
$ git branch -d branch-antiga
```

### 9. Trocando de Branches

O comando `git checkout` é usado para trocar de branches ou restaurar arquivos.

```sh
# Trocar para outra branch
$ git checkout nova-funcionalidade

# Criar uma nova branch e trocar para ela
$ git checkout -b nova-funcionalidade
```

### 10. Mesclando Branches

O comando `git merge` combina mudanças de diferentes branches.

```sh
$ git checkout master
$ git merge nova-funcionalidade
```

### 11. Visualizando Histórico de Commits

O comando `git log` exibe o histórico de commits do repositório.

```sh
$ git log

# Mostrar histórico com estatíscas de diff
$ git log --stat
```

### 12. Gerenciando Repositórios Remotos

O comando `git remote` permite que você gerencie conexões com repositórios remotos.

```sh
# Listar repositórios remotos
$ git remote -v

# Adicionar um repositório remoto
$ git remote add origin https://github.com/usuario/repo.git

# Remover um repositório remoto
$ git remote remove origin
```

### 13. Guardar Mudanças Temporariamente

O comando `git stash` salva temporariamente mudanças não comitadas.

```sh
# Salvar mudanças não comitadas
$ git stash

# Listar stashes salvos
$ git stash list

# Aplciar o stash mais recente
$ git stash apply

# Aplicar e remover o stash mais recente
$ git stash pop
```

### 14. Rebasing de Branches

O comando `git rebase` reaplica commits de uma branch  no topo de outra.

```sh
$ git checkout my-branch
$ git rebase master
```

### 15. Resetando Mudanças

O comando `git reset` move o ponteiro da branch atual e modifica a *Stage Area* e/ou o diretório de trabalho.

```sh
# Reverter commits, mas manter mudanças no diretório de trabalho
$ git reset --soft HEAD~1

# Reverter commits e mudanças na Stage Area, mas manter no diretório de trabalho 
$ git reset --mixed HEAD~1

# Reverter commits e todas as alterações
$ git reset --hard HEAD~1
```

### 16. Mostrando Diferenças

O comando `git diff` mostra as diferenças entre commits, branches e o diretório de trabalho.

```sh
# Mostrar diferenças entre o diretório de trabalho e a Stage Area
$ git diff

# Mostrar diferenças entra a Stage Area e o último commit
$ git diff --cached

# Mostrar diferenças entre duas branhces
$ git diff branch1 branch2
```

### 17. Marcando Commits

O comando `git tag` marca pontos específicos no histórico do repositório.

```sh
# Criar uma tag anotada
$ git tag -a v1.0 -m "Versão 1.0"

# Criar uma tag leve
$ git tag v1.1

# Listar todas as tags
$ git tag

# Enviar tags para o repositório remoto
$ git push origin --tags
```

### 18. Cherry-Picking de Commits
O comando `git cherry-pick` aplica um commit específico de uma branch em outra.

```sh
$ git checkout master
$ git cherry-pick abc123
```

### 19. Fetching Changes

O comando `git fetch` busca mudanças de um repositório remoto sem integrá-las automaticamente.

```sh
$ git fetch origin
```

### 20. Arquivando um Repositório

O comando `git archive` cria um arquivo tar ou zip de uma árvore do repositório.

```sh
# Criar um arquivo tar da branch master
$ git archive --format=tar master | gzip > projeto.tar.gz
```

### 21. Gerenciando Submódulos

O comando `git submodule` gerencia submódulos, que são repositórios Git dentro de outro repositório Git.

```sh
# Adicionar um submódulo
$ git submodule add https://github.com/usuario/subrepo.git caminho/para/subrepo

# Inicializar submódulos
$ git submodule init

# Atualizar submódulos
$ git submodule update
```

### 22. Configurando o Git

O comando `git config` configura opções e comportamentos do Git.

```sh
# Configurar nome de usuário
$ git config --global user.name "Seu Nome"

# Configurar email
$ git config --global user.email "seuemail@examplo.com"

# Ver todas as configurações
$ git config --list
```

## ☑ Conclusão

### Esses comandos formam a base do uso diário do Git, permitindo que os desenvolvedores controlem a versão do seu código, colaborem de maneira eficiente e mantenham um histórico claro e detalhado de mudanças no projeto. Dominar esses comandos é essencial para qualquer desenvolvedor que trabalha em equipe ou em projetos de longo prazo. Happy Coding! 🚀

## 📚 Documentação

- [Git](https://git-scm.com/doc)
- [GitHub](https://docs.github.com/en)
- [Markdown](https://www.markdownguide.org/)
