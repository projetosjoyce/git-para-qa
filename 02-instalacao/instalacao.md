# 🚀 Guia Definitivo de Git para QA
Do **Júnior** ao **Sênior** Manual Prático e Executável

Este manual ensina Git na prática, com foco em QA:
testes manuais, automação, evidências, colaboração em time e boas práticas reais de mercado.

---

## 📋 Pré-requisitos

Antes de começar, você precisará de:
* 💻 Um computador (Windows, macOS ou Linux).
* 🌐 Acesso à internet.
* 🖥️ Um terminal (Git Bash, PowerShell ou Terminal).
* 👤 Uma conta no [GitHub](https://github.com).

> 💡 **Importante:** Você **não precisa saber programar** para usar Git como QA.

---

## 🛠️ 1. Instalação (Windows)

1. Baixe o instalador no site oficial: [git-scm.com](https://git-scm.com).
2. Execute o arquivo e siga o fluxo **"Next"** (as opções padrão são suficientes).
3. Após instalar, valide se deu certo abrindo o terminal e digitando:

```bash
git --version
``` 

**Saída esperada:** git version 2.xx.x

##  ⚙️ 2. Configuração Inicial (Obrigatória)
O Git precisa saber quem é você para registrar a autoria dos testes e melhorias nos scripts.

##  Configure seu nome
```bash
git config --global user.name "Seu Nome Completo"
``` 
##  Configure seu e-mail (use o mesmo do GitHub)
```bash
git config --global user.email "seu-email@exemplo.com"
``` 

##  📂 3. Entendendo o Repositório

Um repositório é onde o Git faz toda a mágica do controle de qualidade e histórico.

**Local:** Onde você desenvolve e executa seus scripts de teste.

**Remoto:** Onde o time colabora e armazena o código (GitHub/GitLab).

## 🏗️ 4. Criando seu Primeiro Repositório
Siga estes passos no terminal para iniciar um projeto do zero:

## 1. Crie a pasta do projeto
```bash
mkdir meu-projeto-de-testes
``` 
## 2. Entre na pasta
```bash
cd meu-projeto-de-testes
``` 
## 3. Inicialize o Git
```bash
git init
``` 

>⚠️ **Atenção**: Isso criará uma pasta oculta **.git. Nunca a apague**, pois ela contém todo o histórico de versões dos seus testes..


## 🔄 5. O Fluxo de Trabalho do QA
No dia a dia, você repetirá este ciclo constantemente para garantir rastreabilidade, histórico e colaboração em time.

Visão geral do fluxo
```bash
Alterar arquivos
↓
git status
↓
git add
↓
git commit
↓
git push

``` 

## 5.1 Ver o status
Sempre verifique o que mudou antes de agir:
```bash
git status
``` 

> **💡 Dica QA:**
Esse comando evita subir: **arquivos errados**, **evidências incompletas** e **scripts quebrados**

## 5.2 Adicionar arquivos (Stage)
Prepare os arquivos para serem salvos no próximo **checkpoint**.
```bash
git add nome-do-arquivo.txt  # Para um arquivo específico
git add .                    # Para todos os arquivos da pasta
```
## 5.3 Salvar a alteração (Commit)
Crie um ponto na história com uma mensagem clara sobre o que foi feito:
```bash
git commit -m "feat: adiciona script de login para o Cypress"
``` 

> **💡 Boas mensagens de commit ajudam**: **auditorias**, **rastreabilidade** e **entendimento do time**

## 5.4 Enviar para o repositório remoto (Push)
Agora você envia suas alterações para o repositório remoto (GitHub).
```bash
git push
``` 
> **⚠️ Atenção para iniciantes:**
Se você não rodar o git push, seu trabalho:

**fica só na sua máquina**

**não aparece no GitHub**

**não fica visível para o time**

## 🏆 A Regra de Ouro do Git
Para não errar a ordem, memorize:
```bash
git status
git add
git commit
git push
``` 
Ou, de forma resumida:
git add ➡️ git commit ➡️ git push









