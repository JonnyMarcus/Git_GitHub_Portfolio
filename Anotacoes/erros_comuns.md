# Git — Erros Comuns e Soluções

## Introdução

Durante o uso do Git é comum encontrar erros relacionados a:
- branches
- commits
- conflitos
- repositórios remotos
- autenticação
- versionamento

Este arquivo reúne erros comuns e suas soluções.

---

# Erro: not a git repository

## Mensagem

```bash
fatal: not a git repository
```

---

## Motivo

A pasta atual não foi inicializada com Git.

---

## Solução

Inicializar repositório:

```bash
git init
```

---

# Erro: nothing to commit

## Mensagem

```bash
nothing to commit, working tree clean
```

---

## Motivo

Não existem alterações para commit.

---

## Solução

Modificar algum arquivo antes de executar:

```bash
git commit
```

---

# Erro: failed to push some refs

## Mensagem

```bash
failed to push some refs
```

---

## Motivo

O repositório remoto possui commits diferentes do local.

---

## Solução

Atualizar projeto:

```bash
git pull origin main
```

Depois enviar novamente:

```bash
git push origin main
```

---

# Erro: remote origin already exists

## Mensagem

```bash
remote origin already exists
```

---

## Motivo

Já existe um remoto chamado origin.

---

## Solução

Remover remoto antigo:

```bash
git remote remove origin
```

Adicionar novamente:

```bash
git remote add origin URL
```

---

# Erro: pathspec did not match

## Mensagem

```bash
error: pathspec 'feature-login' did not match any file(s) known to git
```

---

## Motivo

A branch não existe.

---

## Solução

Listar branches:

```bash
git branch
```

Criar branch:

```bash
git switch -c feature-login
```

---

# Erro: merge conflict

## Mensagem

```bash
CONFLICT (content): Merge conflict
```

---

## Motivo

Duas branches modificaram a mesma parte do arquivo.

---

## Solução

Abrir o arquivo e resolver manualmente:

```txt
<<<<<<< HEAD
codigo atual
=======
codigo da branch
>>>>>>> feature-login
```

Depois:

```bash
git add .
git commit
```

---

# Erro: detached HEAD

## Mensagem

```bash
You are in 'detached HEAD' state
```

---

## Motivo

Você acessou diretamente um commit específico.

---

## Solução

Voltar para branch principal:

```bash
git switch main
```

---

# Erro: permission denied

## Mensagem

```bash
Permission denied
```

---

## Motivo

Problema de autenticação ou permissões.

---

## Solução

Verificar:
- login GitHub
- token de acesso
- chave SSH
- permissões do repositório

---

# Erro: src refspec main does not match any

## Mensagem

```bash
src refspec main does not match any
```

---

## Motivo

Ainda não existe commit na branch.

---

## Solução

Criar primeiro commit:

```bash
git add .
git commit -m "commit inicial"
```

Depois:

```bash
git push -u origin main
```

---

# Erro: repository not found

## Mensagem

```bash
Repository not found
```

---

## Motivo

URL incorreta ou falta de permissão.

---

## Solução

Verificar URL:

```bash
git remote -v
```

Alterar URL:

```bash
git remote set-url origin URL
```

---

# Erro: merge aborted

## Mensagem

```bash
Automatic merge failed
```

---

## Motivo

Conflito durante merge.

---

## Solução

Resolver conflitos manualmente e finalizar:

```bash
git add .
git commit
```

---

# Erro: local changes would be overwritten

## Mensagem

```bash
Your local changes would be overwritten
```

---

## Motivo

Existem alterações locais antes de pull/merge.

---

## Solução

Salvar alterações:

```bash
git stash
```

Depois:

```bash
git pull
```

Restaurar alterações:

```bash
git stash pop
```

---

# Erro: branch already exists

## Mensagem

```bash
fatal: A branch named 'feature-login' already exists
```

---

## Motivo

A branch já foi criada anteriormente.

---

## Solução

Trocar para ela:

```bash
git switch feature-login
```

---

# Erro: updates were rejected

## Mensagem

```bash
Updates were rejected because the remote contains work that you do not have locally
```

---

## Motivo

O remoto possui commits ausentes localmente.

---

## Solução

Atualizar repositório:

```bash
git pull origin main
```

Depois:

```bash
git push origin main
```

---

# Erro: cannot open output file

## Mensagem

```bash
Permission denied
```

---

## Motivo

Arquivo está em uso.

---

## Solução

Fechar:
- executável
- terminal
- editor
- processo relacionado

---

# Dicas Importantes

- Fazer commits frequentes
- Utilizar branches organizadas
- Verificar `git status`
- Atualizar antes de push
- Resolver conflitos com calma
- Manter backup do projeto

---

# Comandos Úteis para Diagnóstico

## Ver estado

```bash
git status
```

---

## Ver histórico

```bash
git log --oneline
```

---

## Ver branches

```bash
git branch
```

---

## Ver remotos

```bash
git remote -v
```

---

# Resumo

Erros no Git fazem parte do aprendizado. Saber identificar e resolver problemas é uma habilidade importante para qualquer desenvolvedor.