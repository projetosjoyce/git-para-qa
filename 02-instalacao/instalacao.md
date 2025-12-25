# 🚀 Guia de Git para QA: Instalação e Repositórios

Este guia foi criado para que qualquer pessoa — do iniciante ao QA Sênior — entenda o fluxo de versionamento de testes e automação.

---

## 📋 Pré-requisitos

Antes de começar, você precisará de:
* 💻 Um computador (Windows, macOS ou Linux).
* 🌐 Acesso à internet.
* 🖥️ Um terminal (Git Bash, PowerShell ou Terminal).
* 👤 Uma conta no [GitHub](https://github.com).

> 💡 **Nota:** Não é necessário saber programar para versionar seus planos de teste ou scripts de automação.

---

## 🛠️ 1. Instalação (Windows)

1. Baixe o instalador no site oficial: [git-scm.com](https://git-scm.com).
2. Execute o arquivo e siga o fluxo "Next" (as opções padrão são suficientes).
3. Após instalar, valide se deu certo abrindo o terminal e digitando:

```bash
git --version

Saída esperada: git version 2.xx.x

⚙️ 2. Configuração Inicial (Obrigatória)
O Git precisa saber quem é você para registrar a autoria dos testes e melhorias nos scripts.

# Configure seu nome
git config --global user.name "Seu Nome Completo"

# Configure seu e-mail (use o mesmo do GitHub)
git config --global user.email "seu-email@exemplo.com"

📂 3. Entendendo o Repositório
Um repositório é onde o Git faz toda a mágica do controle de qualidade e histórico.

Local: Onde você desenvolve e executa seus scripts de teste.

Remoto: Onde o time colabora e armazena o código (GitHub/GitLab).

🏗️ 4. Criando seu Primeiro Repositório
Siga estes passos no terminal para iniciar um projeto do zero:

# 1. Crie a pasta do projeto
mkdir meu-projeto-de-testes

# 2. Entre na pasta
cd meu-projeto-de-testes

# 3. Inicialize o Git
git init

⚠️ Atenção: Isso criará uma pasta oculta .git. Nunca a apague, pois ela contém todo o histórico de versões dos seus testes.

🔄 5. O Fluxo de Trabalho do QA
No dia a dia, você repetirá este ciclo constantemente para garantir a rastreabilidade:

Passo A: Ver o status
Sempre verifique o que mudou antes de agir:
git status

Passo B: Adicionar arquivos (Stage)
Prepare os arquivos para serem salvos no próximo "checkpoint":

git add nome-do-arquivo.txt  # Para um arquivo específico
git add .                    # Para todos os arquivos da pasta


Passo C: Salvar a alteração (Commit)
Crie um ponto na história com uma mensagem que explique o que foi testado ou alterado:

git commit -m "feat: adiciona script de login para o Cypress"

🏆 A Regra de Ouro
Para não errar a ordem, memorize esta sequência:

git add ➡️ git commit ➡️ git push









