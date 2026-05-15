# Desafio 01 — Inicialização e Primeiro Commit

## Objetivo

Aprender a:
- inicializar um repositório Git
- adicionar arquivos
- criar commits
- visualizar histórico

---

# Etapas

## 1. Criar pasta do projeto

```bash
mkdir desafio_git
cd desafio_git
```

---

## 2. Inicializar Git

```bash
git init
```

---

## 3. Criar README

```bash
touch README.md
```

Windows PowerShell:

```powershell
New-Item README.md
```

---

## 4. Verificar estado

```bash
git status
```

---

## 5. Adicionar arquivos

```bash
git add .
```

---

## 6. Criar primeiro commit

```bash
git commit -m "docs: adiciona README inicial"
```

---

## 7. Verificar histórico

```bash
git log --oneline
```

---

# Objetivo Final

Ao concluir este desafio, o usuário deverá compreender o fluxo básico do Git:

```txt
Working Directory
↓
Staging Area
↓
Commit
```

---

# Conceitos Praticados

- git init
- git status
- git add
- git commit
- git log

---

# Resultado Esperado

```txt
[main abc1234] docs: adiciona README inicial
```