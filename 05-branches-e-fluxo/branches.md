# 🌿 Branches e Fluxo de Trabalho no Git  

## 🎯 Objetivo

Ao final deste capítulo, você será capaz de:

- Entender o que são branches
- Criar, trocar e remover branches
- Trabalhar corretamente no fluxo do time
- Atuar com segurança em Pull Requests
- Evitar erros graves em produção

---

## 🧠 O que é uma branch?

Uma branch é uma **linha paralela de desenvolvimento** dentro do Git.

> Ela permite trabalhar em uma tarefa sem afetar o código principal.

---

## 🌳 Branch principal

Normalmente chamada de:

- `main`
- `master` (legado)

⚠️ **QA NÃO deve trabalhar direto na `main`**, salvo exceções.

---

## 🧩 Branches mais comuns em times reais

| Branch | Função |
|------|-------|
| main | Código em produção |
| develop | Código em validação |
| feature | Nova funcionalidade |
| bugfix | Correção de bug |
| hotfix | Correção urgente |

---

## 🔍 Ver branch atual

```bash
git branch
```

---

## 🔄 Trocar de branch
```bash
git checkout develop
```
**ou**
```bash
git switch develop
```

## ➕ Criar uma nova branch
```bash
git checkout -b feature/testes-login
```
**ou**
```bash
git switch -c feature/testes-login
```

## 🧪 Fluxo real de QA (na prática)

**1. Atualiza o código**
```bash
git pull
```

**2. Vai para a branch correta**
```bash
git checkout develop
```

**3. Executa os testes**

**4. Reporta bugs ou valida correções**

**5. Aprova ou reprova PR**

## 🔀 Merge (visão de QA)
Merge é quando uma branch é unida a outra.

- QA normalmente:

- Valida antes do merge

- Testa após o merge

- Não faz merge sem autorização

## 🧠 Boas práticas
- Sempre confirme a branch antes de testar

- Nunca teste direto na main

- Combine o fluxo com o time

- Documente o que foi testado

## ❌ Erros comuns
- Testar na branch errada

- Esquecer de atualizar (git pull)

- Criar branch sem padrão de nome

- Apagar branch errada
