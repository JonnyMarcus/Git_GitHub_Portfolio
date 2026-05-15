# Git — .gitignore

## O que é

O `.gitignore` é um arquivo utilizado para informar ao Git quais arquivos ou pastas não devem ser versionados.

---

# Objetivos

- evitar arquivos desnecessários
- ignorar arquivos temporários
- proteger dados sensíveis
- manter projeto organizado

---

# Criar arquivo

```txt
.gitignore
```

---

# Exemplo Básico

```txt
node_modules/
build/
dist/
*.exe
*.log
.env
```

---

# O que significa

## Ignorar pasta

```txt
node_modules/
```

---

## Ignorar extensão

```txt
*.log
```

Ignora todos arquivos `.log`

---

## Ignorar arquivo específico

```txt
config.txt
```

---

# Exemplos Comuns

## Python

```txt
__pycache__/
*.pyc
venv/
.env
```

---

## C/C++

```txt
*.exe
*.o
*.out
build/
```

---

## VS Code

```txt
.vscode/
```

---

## Linux

```txt
*.swp
```

---

# Arquivos Sensíveis

Nunca enviar:

```txt
.env
senhas.txt
tokens.txt
```

---

# Como Funciona

O Git ignora arquivos listados no `.gitignore`.

Esses arquivos:
- não aparecem no git status
- não entram em commits
- não são enviados ao GitHub

---

# Exemplo Completo

```txt
# executáveis
*.exe
*.out

# logs
*.log

# vscode
.vscode/

# python
__pycache__/
venv/

# variáveis de ambiente
.env

# build
build/
dist/
```

---

# Importante

O `.gitignore` funciona apenas para arquivos que ainda não estão sendo rastreados pelo Git.

---

# Remover Arquivo do Rastreamento

```bash
git rm --cached arquivo.txt
```

---

# Exemplo

```bash
git rm --cached .env
```

Depois adicionar ao `.gitignore`.

---

# Verificar Arquivos Ignorados

```bash
git status
```

Arquivos ignorados não aparecerão.

---

# Boas Práticas

- Utilizar `.gitignore` desde o início
- Ignorar executáveis
- Ignorar builds
- Proteger arquivos sensíveis
- Ignorar dependências temporárias

---

# Benefícios

- Projeto mais limpo
- Segurança
- Melhor organização
- Menor tamanho do repositório
- Workflow profissional

---

# Resumo

O `.gitignore` é essencial para impedir que arquivos desnecessários, temporários ou sensíveis sejam versionados no Git.