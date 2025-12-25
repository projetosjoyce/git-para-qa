# ============================================
# GUIA PRÁTICO: INSTALAÇÃO E CRIAÇÃO DE REPOSITÓRIO GIT
# Público: QA
# ============================================


# ------------------------------
# 1️⃣ VERIFICAR SE O GIT ESTÁ INSTALADO
# ------------------------------

git --version

# Saída esperada:
# git version 2.xx.x
# Se não aparecer versão, o Git não está instalado


# ------------------------------
# 2️⃣ CONFIGURAÇÃO INICIAL (OBRIGATÓRIA)
# ------------------------------
# Todo commit precisa de autor (nome e e-mail)

git config --global user.name "Joyce Sena"
git config --global user.email "joyce@email.com"

# Conferindo se salvou corretamente
git config --list

# Saída esperada:
# user.name=Joyce Sena
# user.email=joyce@email.com

# ⚠️ Boa prática:
# Use o MESMO e-mail do GitHub para manter histórico correto


# ------------------------------
# 3️⃣ CRIANDO UM REPOSITÓRIO LOCAL DO ZERO
# ------------------------------

# Criar a pasta do projeto
mkdir git-para-qa

# Entrar na pasta
cd git-para-qa

# Inicializar o Git
git init

# Saída esperada:
# Initialized empty Git repository

# ⚠️ O Git criou a pasta oculta .git
# NUNCA apague essa pasta


# ------------------------------
# 4️⃣ VERIFICANDO O ESTADO DO REPOSITÓRIO
# ------------------------------

git status

# Saída esperada:
# On branch master
# No commits yet
# nothing to commit

# 👉 Esse comando deve ser usado SEMPRE


# ------------------------------
# 5️⃣ CRIANDO UM ARQUIVO DE TESTE
# ------------------------------

echo "Meu primeiro arquivo" > teste.txt

# Conferindo o status
git status

# Saída esperada:
# Untracked files:
#   teste.txt

# Isso significa:
# O arquivo existe
# Mas o Git ainda NÃO está versionando


# ------------------------------
# 6️⃣ ADICIONANDO ARQUIVOS AO CONTROLE DE VERSÃO
# ------------------------------

# Adicionar arquivo específico
git add teste.txt

# OU adicionar tudo
# git add .

# Conferindo novamente
git status

# Saída esperada:
# Changes to be committed:
#   new file: teste.txt


# ------------------------------
# 7️⃣ CRIANDO O PRIMEIRO COMMIT
# ------------------------------

git commit -m "feat: primeiro commit do projeto"

# Saída esperada:
# 1 file changed, 1 insertion(+)

# Agora o projeto já tem histórico


# ------------------------------
# 8️⃣ REGRA DE OURO DO GIT (GRAVE ISSO)
# ------------------------------
# git add  -> adiciona arquivos
# git commit -> salva no histórico
# git push -> envia para o remoto

# ❌ commit sem add = erro
# ❌ push sem commit = erro


# ------------------------------
# 9️⃣ ERROS COMUNS (EXEMPLOS REAIS)
# ------------------------------

# ❌ Erro: tentar commitar sem adicionar arquivos
git commit -m "meu commit"

# Erro:
# nothing to commit

# ✔️ Solução:
git add .
git commit -m "meu commit"


# ❌ Erro: inicializar Git na pasta errada
# Problema:
# Rodar git init dentro de outra pasta versionada
# Criar vários .git sem perceber

# ✔️ Boa prática:
# Um projeto = um repositório


# ------------------------------
# 🔟 VISÃO DE QA
# ------------------------------

# QA Júnior:
# Git ajuda a não perder código

# QA Pleno:
# Git ajuda a rastrear quando o bug surgiu

# QA Sênior:
# Sem Git não existe:
# rastreabilidade
# auditoria
# histórico confiável
# qualidade de processo

