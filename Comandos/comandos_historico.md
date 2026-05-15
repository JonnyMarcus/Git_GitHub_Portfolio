# Git — Histórico e Controle de Versões

## Introdução

O Git mantém um histórico completo de alterações realizadas no projeto.

Esse histórico permite:
- visualizar commits
- recuperar versões antigas
- identificar alterações
- acompanhar evolução do projeto
- analisar modificações no código

---

# O que é um Commit

Um commit é um snapshot do projeto em determinado momento.

Cada commit possui:
- identificador único (HASH)
- autor
- data
- mensagem
- alterações realizadas

---

# Estrutura Visual

```txt
Commit A → Commit B → Commit C
```

Cada commit representa uma versão do projeto.

---

# git log

## O que faz

Mostra o histórico completo de commits.

---

# Sintaxe

```bash
git log
```

---

# Exemplo

```bash
git log
```

---

# Informações exibidas

- HASH do commit
- autor
- data
- mensagem

---

# git log --oneline

## O que faz

Mostra histórico resumido.

---

# Exemplo

```bash
git log --oneline
```

---

# Resultado

```txt
a81f2c1 feat: adiciona sistema de login
c19e331 docs: atualiza README
91ab212 fix: corrige erro na API
```

---

# git log --graph

## O que faz

Mostra histórico visual de branches e merges.

---

# Exemplo

```bash
git log --graph --oneline --all
```

---

# Exemplo Visual

```txt
* commit-feature
|\
| * commit-login
|/
* commit-main
```

---

# git show

## O que faz

Exibe detalhes de um commit específico.

---

# Sintaxe

```bash
git show HASH
```

---

# Exemplo

```bash
git show a81f2c1
```

---

# Informações exibidas

- alterações realizadas
- autor
- data
- arquivos modificados

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

# Comparar commits

```bash
git diff HASH1 HASH2
```

---

# git reflog

## O que faz

Mostra histórico interno completo do Git.

Permite recuperar commits perdidos.

---

# Exemplo

```bash
git reflog
```

---

# Utilização

Muito utilizado após:
- reset
- rebase
- commits apagados
- alterações perdidas

---

# git blame

## O que faz

Mostra quem modificou cada linha de um arquivo.

---

# Exemplo

```bash
git blame arquivo.txt
```

---

# Resultado

```txt
a81f2c1 (Jonny Marcus) linha modificada
```

---

# git tag

## O que faz

Marca versões importantes do projeto.

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

# Histórico Profissional

Exemplo de evolução:

```txt
v0.1 → estrutura inicial
v0.2 → sistema de login
v0.3 → dashboard
v1.0 → versão estável
```

---

# HASH de Commit

Cada commit possui um identificador único.

Exemplo:

```txt
a81f2c1d91b7e20f9ab92d12
```

O HASH permite:
- localizar commits
- recuperar versões
- fazer revert
- comparar alterações

---

# Recuperar Commit Antigo

## Ver commit

```bash
git checkout HASH
```

---

## Voltar para branch principal

```bash
git switch main
```

---

# Fluxo de Histórico

## Ver histórico

```bash
git log --oneline
```

---

## Ver alterações

```bash
git diff
```

---

## Ver commit específico

```bash
git show HASH
```

---

## Recuperar histórico perdido

```bash
git reflog
```

---

# Boas Práticas

- Fazer commits frequentes
- Utilizar mensagens claras
- Manter histórico organizado
- Evitar commits gigantes
- Utilizar tags em versões importantes

---

# Exemplos de Commits

```bash
feat: adiciona autenticação
fix: corrige erro no login
docs: atualiza README
refactor: reorganiza código
test: adiciona testes
```

---

# Importância do Histórico

O histórico Git é essencial para:
- rastrear alterações
- recuperar código
- trabalhar em equipe
- organizar desenvolvimento
- manter segurança do projeto

---

# Resumo

Os comandos de histórico permitem controlar toda evolução do projeto, sendo fundamentais para versionamento profissional e manutenção organizada do código.