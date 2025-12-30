# 🧬 Clonando Repositórios Git  
## Guia Completo para QA 

---

## 🎯 Objetivo

**Ao final deste capítulo, você será capaz de:**

- Entender o que é clonar um repositório
- Clonar projetos via HTTPS e SSH
- Trabalhar corretamente com repositórios do time
- Evitar erros comuns de iniciantes
- Atuar com segurança como QA Pleno ou Sênior

---

## 🧠 O que é clonar um repositório?

**Clonar um repositório significa:**

> Copiar um projeto que está no GitHub/GitLab/Bitbucket para sua máquina local,
> mantendo TODO o histórico de commits, branches e versões.

🔹 Diferente de baixar ZIP:
- Mantém histórico
- Permite atualizar o código
- Permite trabalhar com branches
- Permite enviar commits (se autorizado)

---

## 🧩 Quando um QA precisa clonar um repositório?

Situações reais:

- Automatizar testes (Cypress, Robot, Playwright)
- Rodar o projeto localmente
- Testar novas funcionalidades
- Validar correções de bugs
- Executar pipelines de CI/CD
- Analisar Pull Requests

👉 QA clona repositórios diariamente.

---

## 🛠️ Pré-requisitos

Antes de clonar, verifique:

- Git instalado
- Acesso ao repositório
- Terminal aberto (Git Bash, CMD ou PowerShell)

**Verificar versão do Git:**

```bash
git --version
```
---
| Tipo  | Quando usar          |
| ----- | -------------------- |
| HTTPS | Iniciante, simples   |
| SSH   | Profissional, seguro |


---

## 🔰 Clone via HTTPS 
- Quando usar?

- Primeiro contato com Git

- Repositórios públicos

- Estudos iniciais

**Passo 1 — Copiar o link HTTPS**
```bash
https://github.com/empresa/projeto-qa.git
```

**Passo 2 — Escolher a pasta**
```bash
cd Documentos
```

**Passo 3 — Clonar o repositório**
```bash
git clone https://github.com/empresa/projeto-qa.git
```
**Saída esperada:**
```bash
Cloning into 'projeto-qa'...
```

**Passo 4 — Entrar no projeto**
```bash
cd projeto-qa
```

**Passo 5 — Conferir status**
```bash
git status
```

**Resultado esperado:**
```bash
On branch main
nothing to commit, working tree clean
```
✅ Clone concluído com sucesso.

---

## 🔰 🚀 Clone via SSH 
- Quando usar?

- Projetos corporativos

- Repositórios privados

- Automação e CI/CD

- Ambientes profissionais

**Verificar se já existe chave SSH**
```bash
ls ~/.ssh
```
Se existir id_rsa.pub ou id_ed25519.pub, a chave já existe.

**Criar chave SSH (se necessário)**
```bash
ssh-keygen -t ed25519 -C "seu-email@empresa.com"
```

**Pressione ENTER para todas as perguntas.**

**Copiar chave pública**
```bash
cat ~/.ssh/id_ed25519.pub
```
Copie todo o conteúdo.

## Adicionar chave no GitHub/GitLab
- Settings

- SSH Keys

- Add new key

- Colar chave

- Salvar

**Clonar via SSH**
```bash
git clone git@github.com:empresa/projeto-qa.git
```

## 📂 Estrutura após o clone
```bash
projeto-qa/
├── src/
├── tests/
├── README.md
├── package.json
└── .git/
```
**⚠️ A pasta .git NÃO deve ser alterada.**

## 🔄 Atualizando o projeto antes de testar
**Sempre execute:**
```bash
git pull
```

Evita:

- Testar código desatualizado

- Reportar bug já corrigido

- Automatizar versão errada

## 🌿 Trabalhando com branches
**Ver branch atual:**
```bash
git branch
```
**Ver branches remotas:**
```bash
git branch -r
```
**Trocar de branch:**
```bash
git checkout develop
```
**ou**

```bash
git switch develop
```

## 🧠 Boas práticas para QA

- Sempre rodar git pull antes de testar

- Verificar a branch correta

- Ler o README do projeto

- Nunca testar código desatualizado

- Nunca apagar a pasta .git

## ❌ Erros comuns de iniciantes

- Baixar ZIP em vez de clonar

- Testar sem atualizar o código

- Não saber em qual branch está

- Clonar um repositório dentro de outro

- Alterar a pasta .git

