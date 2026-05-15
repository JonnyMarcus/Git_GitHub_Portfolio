# GitHub — Issues

## O que são Issues

Issues são tarefas, bugs, melhorias ou discussões registradas dentro de um repositório no GitHub.

Elas são utilizadas para:
- reportar erros
- sugerir melhorias
- organizar tarefas
- discutir funcionalidades
- planejar desenvolvimento

---

# Objetivos das Issues

- Organização do projeto
- Controle de tarefas
- Comunicação da equipe
- Registro de bugs
- Planejamento de funcionalidades

---

# Exemplos de Issues

## Bug

```txt
Erro ao realizar login com senha inválida
```

---

## Feature

```txt
Adicionar sistema de autenticação
```

---

## Melhoria

```txt
Melhorar layout do README
```

---

# Estrutura de uma Issue

Uma issue normalmente possui:

- título
- descrição
- labels
- responsável
- comentários
- status

---

# Exemplo de Issue

## Título

```txt
Adicionar sistema de login
```

---

## Descrição

```txt
Criar sistema de autenticação utilizando email e senha.
```

---

# Labels

Labels ajudam a organizar Issues.

---

# Exemplos

```txt
bug
feature
documentation
enhancement
help wanted
good first issue
```

---

# Workflow com Issues

## 1. Criar Issue

```txt
#12 Adicionar dashboard
```

---

## 2. Criar branch

```bash
git switch -c feature/dashboard
```

---

## 3. Trabalhar normalmente

```bash
git add .
git commit -m "feat: adiciona dashboard"
```

---

## 4. Enviar branch

```bash
git push origin feature/dashboard
```

---

## 5. Criar Pull Request

Relacionando a Issue.

---

# Fechar Issue Automaticamente

No commit ou Pull Request:

```txt
Closes #12
Fixes #12
Resolves #12
```

---

# Exemplo

```txt
feat: adiciona dashboard

Closes #12
```

---

# Boas Práticas

- Criar títulos claros
- Explicar problema detalhadamente
- Utilizar labels
- Relacionar Issues com Pull Requests
- Manter organização do projeto

---

# Exemplo de Organização

```txt
#1 Estrutura inicial
#2 Sistema de login
#3 Dashboard
#4 API de usuários
#5 Correção navbar
```

---

# Benefícios das Issues

- Melhor organização
- Histórico do projeto
- Controle de funcionalidades
- Comunicação profissional
- Planejamento de desenvolvimento

---

# Resumo

Issues são fundamentais para organização e gerenciamento profissional de projetos no GitHub.