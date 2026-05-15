# Git — Branches e Workflow

## O que é uma Branch

Uma branch é uma linha paralela de desenvolvimento dentro do projeto.

Ela permite:
- criar novas funcionalidades
- corrigir erros
- testar mudanças
- trabalhar sem alterar a branch principal

---

# Estrutura Visual

```txt
main
 ├── commit A
 ├── commit B
 └── commit C
       \
        feature-login
          ├── commit D
          └── commit E
```

---

# git branch

Comando utilizado para criar, listar e remover branches.

---

# Listar Branches

```bash
git branch
```

Exemplo:

```bash
* main
  develop
  feature-login
```

O `*` indica a branch atual.

---

# Criar Nova Branch

```bash
git branch nome-da-branch
```

Exemplo:

```bash
git branch feature-login
```

---

# git switch

Utilizado para trocar de branch.

---

# Trocar de Branch

```bash
git switch nome-da-branch
```

Exemplo:

```bash
git switch feature-login
```

---

# Criar e Entrar na Branch

```bash
git switch -c nome-da-branch
```

Exemplo:

```bash
git switch -c feature-dashboard
```

---

# git checkout

Comando antigo utilizado para trocar de branch.

```bash
git checkout feature-login
```

Criar e entrar:

```bash
git checkout -b feature-api
```

---

# git merge

Une alterações de uma branch em outra.

---

# Exemplo de Merge

Voltar para main:

```bash
git switch main
```

Fazer merge:

```bash
git merge feature-login
```

---

# Fluxo Profissional

## 1. Criar branch

```bash
git switch -c feature-login
```

---

## 2. Trabalhar normalmente

```bash
git add .
git commit -m "feat: adiciona sistema de login"
```

---

## 3. Voltar para main

```bash
git switch main
```

---

## 4. Fazer merge

```bash
git merge feature-login
```

---

# git branch -d

Remove uma branch.

```bash
git branch -d feature-login
```

---

# Forçar Remoção

```bash
git branch -D feature-login
```

---

# git branch -m

Renomeia uma branch.

```bash
git branch -m novo-nome
```

---

# Ver Todas as Branches

## Locais

```bash
git branch
```

---

## Remotas

```bash
git branch -r
```

---

## Todas

```bash
git branch -a
```

---

# Branches Profissionais

Exemplos comuns:

```txt
main
develop
feature/login
feature/dashboard
hotfix/api
release/v1.0
```

---

# Tipos de Branch

## main

Branch principal do projeto.

---

## develop

Branch de desenvolvimento.

---

## feature/

Utilizada para novas funcionalidades.

Exemplo:

```txt
feature/login
feature/dashboard
```

---

## hotfix/

Correções urgentes.

Exemplo:

```txt
hotfix/api
```

---

## release/

Preparação de versões.

Exemplo:

```txt
release/v1.0
```

---

# Boas Práticas

- Não trabalhar diretamente na main
- Criar uma branch por funcionalidade
- Fazer commits organizados
- Utilizar nomes claros
- Remover branches concluídas

---

# Exemplos de Nomes

```txt
feature/login
feature/dashboard
fix/navbar
hotfix/api
docs/readme
refactor/auth
```

---

# Erros Comuns

## Erro

```bash
error: pathspec 'feature-login' did not match any file(s) known to git
```

## Motivo

A branch não existe.

## Solução

Listar branches disponíveis:

```bash
git branch
```

---

# Resumo

Branches são fundamentais para organização, desenvolvimento em equipe e workflows profissionais no Git.