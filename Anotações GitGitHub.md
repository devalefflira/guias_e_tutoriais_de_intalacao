# Anotações Git/GitHub

# Configurações básicas

## Verificando a versão instalada

```bash
git --version
```

## Configurações do usuário / Primeiro Acesso

```bash
git config --global [user.name](<http://user.name>) "Nome"
git config --global user.email "email@email.com"
	git config --global core.editor "your editor"
```

## Configurações da Branch

```bash
git config --global init.defaultBranch main
```

## Verificando as configurações globais

```bash
git config --list
```

## Inicializar um projeto com git

```bash
git init
```

## Consultar o status dos arquivos

```bash
git status
```

## Adicionar os arquivos

```bash
git add .
```

## Comitado o projeto

```bash
git commit -m "Algum comentário(Ex. Primeiro COmmit"
```

## Para consultar os commits

```bash
git log
```

## Para criar uma nova branch

```bash
git branch nome-da-branch
```

## Para alterar a branch

```bash
git checkout nome-da-branch
```

## Para unir duas branches

```bash
git merge nome-da-branch
```

## Para verificar qual a branch ativa

```bash
git branch
```

## Para deletar uma branch

```bash
git branch -d nome-da-branch
```

## Ver todas as modificações no projeto

```bash
git diff
```

## Ver modificações no arquivo específico

```bash
git diff nome-do-arquivo.extensão
```

## Voltar para o estado de Unmodified

```bash
git checkout nome-do-arquivo.extensão
```

## Para voltar arquivos que já estão em um commit utilizamos o comando

```bash
git reset --soft id-commit-anterior
git reset --mixed id-commit-anterior
git reset --hard id-commit-anterior
```

## Adicionar um repositório remoto

```bash
git remote add origin link-repositorio
```

## Verificar o repositório

```bash
git remote
git remote -v
```

## Enviar os snapshots para o Github

```bash
git push -u origin nome-da-branch
```

## Clonar o projeto

```bash
git clone link-do-projeto
```

## Merge

```bash
	git merge nome-da-branch
```

## Rebase

```bash
git rebase nome-da-branch
```

## Visualizar de forma gráfica o merge

```bash
git log --graph
```

## Criar e alterar a branch automaticamente

```bash
git checkout -b nome-da-branch
```

## Stash

```bash
git stash
git stash apply
git stash list
git stash clear
```

### Para incluir arquivos não traqueados com Stash

```bash
git stash --include-untracked
```

## Git Ignore

Ignorar  arquivo na hora de subir o repositório, como no exemplo abaixo.

É necessário criar um arquivo chamado “.gitignore”

## Revert

```bash
git revert id-ultimo-commit
```

## Mostrar detalhes do commit

```bash
git id-do-commit show
```

## Obter do repositório remoto as modificações realizadas, antes de fazer o push - Workflow Centralizado

```bash
git pull origin main --rebase
```

## Resolução de conflitos

```bash
git merge --continue
git rebase --continue
```

## Chave SSH

```bash
ssh-keygen -t ed25519 -C dev.alefflira@gmail.com 
/home/devalefflira/.ssh
cat id_ed25519.pub
```

Copiar a chave pública e colar no GitHub.

```bash
eval $(ssh-agent -s)
ssh-add id_ed25519
```

## Token de Acesso