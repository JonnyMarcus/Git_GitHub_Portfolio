# Git — Comandos Avançados

## Introdução

Os comandos avançados do Git permitem controlar histórico, recuperar alterações, organizar versões e trabalhar de forma mais profissional durante o desenvolvimento.

---

# git stash

## O que faz

Salva alterações temporariamente sem criar commit.

Muito utilizado quando é necessário trocar de branch rapidamente.

---

## Salvar alterações

```bash
git stash
```

---

## Ver stashes salvos

```bash
git stash list
```

---

## Restaurar stash

```bash
git stash apply
```

---

## Restaurar e remover stash

```bash
git stash pop
```

---

# git reset

## O que faz

Volta alterações ou commits.

---

# Reset simples

Remove arquivos da Staging Area:

```bash
git reset
```

---

# Reset para commit anterior

```bash
git reset --soft HEAD~1
```

Mantém alterações no código.

---

# Reset hard

```bash
git reset --hard HEAD~1
```

Remove commits e alterações.

⚠ Cuidado:
pode apagar alterações permanentemente.

---

# git revert

## O que faz

Desfaz um commit criando um novo commit inverso.

Mais seguro que reset em projetos compartilhados.

---

## Exemplo

```bash
git revert HASH
```

---

# git rebase

## O que faz

Reorganiza o histórico de commits.

Muito utilizado para manter histórico limpo.

---

# Exemplo

```bash
git rebase main
```

---

# Diferença entre merge e rebase

## Merge

Cria commit de merge.

```txt
Histórico ramificado
```

---

## Rebase

Reescreve histórico.

```txt
Histórico linear
```

---

# git tag

## O que faz

Cria versões do projeto.

Muito utilizado para releases.

---

# Criar tag

```bash
git tag v1.0
```

---

# Listar tags

```bash
git tag
```

---

# Enviar tags

```bash
git push origin --tags
```

---

# git cherry-pick

## O que faz

Copia commits específicos de outra branch.

---

# Exemplo

```bash
git cherry-pick HASH
```

---

# git reflog

## O que faz

Mostra todo histórico interno do Git.

Permite recuperar commits perdidos.

---

# Exemplo

```bash
git reflog
```

---

# git diff

## O que faz

Mostra diferenças entre alterações.

---

# Ver alterações atuais

```bash
git diff
```

---

# Ver alterações staged

```bash
git diff --staged
```

---

# git show

## O que faz

Exibe detalhes de commits.

---

# Exemplo

```bash
git show HASH
```

---

# git clean

## O que faz

Remove arquivos não rastreados.

---

# Exemplo

```bash
git clean -f
```

---

# git fetch

## O que faz

Baixa alterações do remoto sem aplicar no projeto.

---

# Exemplo

```bash
git fetch
```

---

# git pull

## O que faz

Baixa e aplica alterações automaticamente.

---

# Exemplo

```bash
git pull
```

---

# git remote

## O que faz

Gerencia conexões remotas.

---

# Ver remotos

```bash
git remote -v
```

---

# Alterar URL

```bash
git remote set-url origin URL
```

---

# Remover remoto

```bash
git remote remove origin
```

---

# git blame

## O que faz

Mostra quem alterou cada linha do arquivo.

---

# Exemplo

```bash
git blame arquivo.txt
```

---

# git log avançado

## Histórico resumido

```bash
git log --oneline
```

---

## Histórico gráfico

```bash
git log --graph --oneline --all
```

---

# Fluxo Avançado Profissional

## Criar branch

```bash
git switch -c feature-api
```

---

## Trabalhar normalmente

```bash
git add .
git commit -m "feat: adiciona API"
```

---

## Atualizar branch

```bash
git fetch
git rebase main
```

---

## Enviar alterações

```bash
git push origin feature-api
```

---

# Boas Práticas

- Utilizar rebase com cuidado
- Fazer stash antes de trocar de branch
- Evitar reset hard sem necessidade
- Criar tags para versões importantes
- Manter histórico limpo
- Fazer commits pequenos

---

# Cuidados

## Comandos perigosos

```bash
git reset --hard
git clean -f
git push --force
```

Podem apagar alterações permanentemente.

---

# Resumo

Os comandos avançados do Git permitem maior controle sobre:
- histórico
- branches
- recuperação
- organização
- versionamento
- workflow profissional