# Git — git clone

## O que é

O comando `git clone` é utilizado para copiar um repositório remoto para o computador local.

Ele baixa:
- arquivos
- commits
- branches
- histórico
- configurações do projeto

---

# Sintaxe

```bash
git clone URL
```

---

# Exemplo

```bash
git clone https://github.com/usuario/repositorio.git
```

---

# O que acontece

O Git:
- cria uma pasta do projeto
- conecta ao repositório remoto
- baixa todo histórico
- configura o remote origin

---

# Estrutura

```txt
GitHub Repository
        ↓
git clone
        ↓
Projeto Local
```

---

# Clonar em pasta específica

```bash
git clone URL nome-da-pasta
```

---

# Exemplo

```bash
git clone https://github.com/usuario/repositorio.git meu-projeto
```

---

# Verificar remoto após clone

```bash
git remote -v
```

---

# Resultado

```txt
origin  https://github.com/usuario/repositorio.git (fetch)
origin  https://github.com/usuario/repositorio.git (push)
```

---

# Fluxo Básico

## 1. Clonar projeto

```bash
git clone URL
```

---

## 2. Entrar na pasta

```bash
cd repositorio
```

---

## 3. Verificar estado

```bash
git status
```

---

# Boas Práticas

- Clonar repositórios organizados
- Ler README antes de modificar
- Atualizar projeto com git pull
- Criar branches para novas funcionalidades

---

# Resumo

O `git clone` é utilizado para copiar um repositório remoto completo para o ambiente local, incluindo histórico e configurações Git.