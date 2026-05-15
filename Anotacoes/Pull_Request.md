# GitHub — Pull Requests

## O que é um Pull Request

Pull Request (PR) é uma solicitação para integrar alterações de uma branch em outra.

Normalmente:
- feature → develop
- develop → main

---

# Objetivos do Pull Request

- Revisar código
- Discutir alterações
- Validar funcionalidades
- Manter qualidade do projeto
- Integrar branches

---

# Estrutura do Workflow

```txt
main
 └── feature/login
        ↓
   Pull Request
        ↓
      merge
```

---

# Fluxo Completo

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

## 3. Enviar branch

```bash
git push origin feature-login
```

---

## 4. Abrir Pull Request no GitHub

Comparando:

```txt
feature-login → main
```

---

# Estrutura de um Pull Request

Um PR geralmente possui:

- título
- descrição
- commits
- arquivos alterados
- comentários
- reviewers

---

# Exemplo de Título

```txt
feat: adiciona sistema de login
```

---

# Exemplo de Descrição

```txt
Implementa autenticação utilizando email e senha.

Inclui:
- validação
- tratamento de erros
- organização da interface

Closes #12
```

---

# Code Review

Antes do merge, o código pode ser revisado por outros desenvolvedores.

Objetivos:
- encontrar erros
- melhorar código
- manter padrão
- validar lógica

---

# Merge do Pull Request

Após aprovação:

```txt
Pull Request → Merge
```

As alterações entram na branch principal.

---

# Tipos de Merge

## Merge Commit

Mantém histórico completo.

---

## Squash Merge

Une commits em um único commit.

Muito utilizado para manter histórico limpo.

---

## Rebase Merge

Reescreve histórico de forma linear.

---

# Atualizar Pull Request

Continuar trabalhando normalmente:

```bash
git add .
git commit -m "fix: corrige validação"
git push
```

O PR será atualizado automaticamente.

---

# Relacionar Issue

No Pull Request:

```txt
Closes #12
Fixes #12
```

---

# Branches Profissionais

```txt
main
develop
feature/login
feature/dashboard
hotfix/api
release/v1.0
```

---

# Boas Práticas

- Criar PRs pequenos
- Utilizar títulos claros
- Explicar alterações
- Fazer code review
- Relacionar Issues
- Evitar commits desorganizados

---

# Exemplos de Pull Requests

```txt
feat: adiciona dashboard
fix: corrige erro na API
docs: atualiza documentação
refactor: reorganiza autenticação
```

---

# Benefícios do Pull Request

- Melhor qualidade de código
- Organização profissional
- Revisão de alterações
- Histórico limpo
- Trabalho colaborativo

---

# Resumo

Pull Requests são essenciais para workflows modernos, integração de funcionalidades e desenvolvimento profissional utilizando GitHub.