# ❌ Erros Comuns no Git  
## E como um QA profissional resolve

---

## 🎯 Objetivo

Apresentar os erros mais comuns cometidos por QAs ao usar Git  
e como evitá-los ou resolvê-los no dia a dia profissional.

---

## ❌ Erro 1 — Testar código desatualizado

### Sintoma
- Bug já foi corrigido, mas continua aparecendo no teste.

### Causa
- QA não atualizou o repositório.

### Solução (CMD / Git Bash)

```bash
git pull
```

## ❌ Erro 2 — Estar na branch errada
Sintoma

Funcionalidade não aparece

Correção não existe no ambiente local

**Verificar branch atual**
```bash
git branch
```

**Corrigir**
```bash
git checkout develop
```
**ou**
```bash
git switch develop
```

## ❌ Erro 3 — Clonar repositório dentro de outro repositório
**Sintoma**

- Git começa a dar erro estranho

- Commits não funcionam corretamente

**Causa**

- git clone executado dentro de um projeto Git

**Solução**

- Apagar a pasta clonada

- Clonar novamente fora de qualquer repositório

##❌ Erro 4 — Apagar ou alterar a pasta .git ##

**Impacto**

- Perda total do histórico

- Projeto deixa de ser um repositório Git

**Regra de ouro**

Nunca mexa na pasta .git

## ❌ Erro 5 — Baixar ZIP em vez de clonar##

**Problema**

- Não consegue atualizar o código

- Não consegue trocar de branch

**Correção**
```bash
git clone <url-do-repositorio>
```

## ❌ Erro 6 — Não saber o fluxo do time##

**Sintoma**

- Testa na branch errada

- Valida código incompleto

**Boa prática**

- Confirmar sempre:

- Branch correta

- Ambiente correto

- Versão correta