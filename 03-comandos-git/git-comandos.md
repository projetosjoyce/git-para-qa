# 🧩 03. Comandos Git Essenciais para QA

Este capítulo ensina como o Git funciona na prática, usando exemplos reais do dia a dia de QA: testes manuais, automação, correção de scripts e trabalho em equipe.

---

💡 **Objetivo:**
Ao final, você deve:

- Entender o que o Git faz
- Saber qual comando usar em cada situação
- Não ter medo de errar comandos básicos



## ENTENDENDO O QUE ESTÁ ACONTECENDO
Se você **nunca usou Git**, comece daqui.
Nada aqui exige conhecimento prévio.


📌 **git status** —> Entender o estado do seu trabalhov
```bash
git status
```
🧠 **O que esse comando faz** (explicação simples)
> **Ele responde à pergunta: “O que mudou no meu projeto desde a última vez que salvei?”**

💡 **O Git mostra:**

- Arquivos que você modificou

- Arquivos novos

- Arquivos que já estão prontos para serem salvos **(commit)**

---
**📂 Exemplo real de QA**

Você tem um projeto com testes automatizados e altera o arquivo:
```bash
cypress/e2e/login.spec.js
```
Depois disso, ao rodar **git status**, o Git mostra algo como:
```bash
modified: cypress/e2e/login.spec.js
```
Isso significa:
👉 O arquivo mudou, **mas ainda não foi salvo no histórico do Git.**

📍 **Quando usar**

-  Antes de qualquer commit
- Sempre que terminar uma alteração
- Quando algo der errado e você não souber o motivo

**⚠️ Erro comum de iniciante**

> Fazer commit sem saber o que está sendo commitado.

**👉 Regra prática:**
> Nunca use git add ou git commit sem rodar git status antes.
  
---

📌 **git add** —> Dizer ao Git o que você quer salvar
```bash
git add login.spec.js
```
ou
```bash
git add .
```
**🧠 O que esse comando faz**
O Git funciona em etapas.
Alterar um arquivo não significa que ele será salvo automaticamente.
**git add** significa:
> “Git, eu quero salvar este arquivo no próximo commit.”

**📂 Exemplo real de QA**
Você:
- Corrigiu um teste quebrado em login.spec.js
- Ajustou um seletor
- Rodou os testes e funcionou

Agora você decide **salvar essa correção:**
```bash
git add cypress/e2e/login.spec.js
```
👉 Isso prepara o arquivo para o commit.

**⚠️ Sobre git add .**
```bash
git add .
```
Esse comando adiciona **todos os arquivos alterados.**

📌 Use apenas quando:
- Você sabe exatamente o que mudou
- Conferiu antes com git status

**⚠️ Erro comum de QA**

Adicionar tudo sem olhar e subir:
- Evidência errada
- Arquivo pessoal
- Teste incompleto

---

📌 **git commit** —> Salvar a alteração no histórico
  ```bash
git commit -m "test: corrige validação de login inválido"
```
**🧠 O que é um commit** (sem complicação)

Um commit é como um checkpoint.

> “Nesse momento, o projeto ficou assim.”

O Git guarda:

- O que mudou
- Quem mudou
- Quando mudou
- Por quê (mensagem)

**📂 Exemplo real de QA**

**Antes:** Teste de login quebrava com senha inválida

**Depois:** Teste corrigido

Commit feito com mensagem clara

Se amanhã o teste quebrar de novo, o time consegue:
- Voltar no histórico
- Entender o que foi feito
- Evitar retrabalho

❌ Mensagens ruins (evite): "teste", "ajustes", "alterações"

✅ Mensagens boas: **"test:** adiciona cenário de login inválido",  **"fix:** corrige seletor do botão de login"




