# Git — Comandos Básicos

## O que é Git

Git é um sistema de controle de versão utilizado para rastrear alterações em projetos e organizar o desenvolvimento de software.

---

# Fluxo do Git

```txt
Working Directory
↓
Staging Area
↓
Repository
```

- Working Directory → arquivos modificados
- Staging Area → arquivos preparados
- Repository → commits salvos

---

# git init

Inicializa um repositório Git.

```bash
git init
```

Cria a pasta oculta:

```txt
.git/
```

---

# git status

Mostra o estado atual do repositório.

```bash
git status
```

Exibe:
- arquivos modificados
- branch atual
- arquivos preparados para commit

---

# git add

Adiciona arquivos para a Staging Area.

Adicionar todos:

```bash
git add .
```

Adicionar arquivo específico:

```bash
git add arquivo.txt
```

---

# git commit

Cria um snapshot do projeto.

```bash
git commit -m "mensagem"
```

Exemplo:

```bash
git commit -m "feat: adiciona sistema de login"
```

---

# Conventional Commits

Padrão profissional de commits.

```bash
feat: nova funcionalidade
fix: correção de erro
docs: documentação
refactor: reorganização
test: testes
```

---

# git log

Mostra o histórico de commits.

```bash
git log
```

---

# git clone

Clona um repositório remoto.

```bash
git clone URL
```

Exemplo:

```bash
git clone https://github.com/usuario/repositorio.git
```

---

# git remote

Conecta o projeto local ao GitHub.

Ver remotos:

```bash
git remote -v
```

Adicionar remoto:

```bash
git remote add origin URL
```

Exemplo:

```bash
git remote add origin https://github.com/usuario/repositorio.git
```

---

# git push

Envia commits para o GitHub.

```bash
git push -u origin main
```

---

# git pull

Baixa atualizações do repositório remoto.

```bash
git pull
```

---

# git branch

Cria e lista branches.

Criar branch:

```bash
git branch feature-login
```

Listar branches:

```bash
git branch
```

---

# git switch

Troca de branch.

```bash
git switch feature-login
```

Criar e entrar na branch:

```bash
git switch -c feature-dashboard
```

---

# git merge

Une branches.

```bash
git merge feature-login
```

---

# git stash

Salva alterações temporariamente.

```bash
git stash
```

---

# git reset

Volta alterações ou commits.

```bash
git reset --hard HEAD~1
```

---

# git revert

Desfaz commits criando um novo commit.

```bash
git revert HASH
```

---

# Fluxo Básico

```bash
git init
git status
git add .
git commit -m "docs: commit inicial"
git remote add origin URL
git push -u origin main
```

---

# Boas Práticas

- Fazer commits pequenos
- Utilizar mensagens claras
- Organizar branches
- Atualizar README
- Versionar frequentemente
- Não trabalhar diretamente na main