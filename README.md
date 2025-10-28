# Repositorio-GIT

## 🎯 Objetivo

Este repositório tem como objetivo documentar e revisar toda a aprendizagem sobre o **GIT** e **GITHUB** no primeiro ano de ensino de Análise e Desenvolvimento de Sistemas - SENAI

---

## 🌩️ 0. Iniciando o Git

- Baixe o **[GitBash](https://git-scm.com/install/)**, utilizando a própria IDE do Git, ou o **[Git para Windows](https://git-scm.com/install/windows)**, utilizando o Prompt de Comando como IDE.

## Com ou Sem Fork?

Antes de programar dentro do Git, precisamos decidir se iremos editar um arquivo já existente ou não.

Um jeito para se editar um README já existente no GITHUB, é usando a função **Fork**.

## Fork do Repositório

**Caso DESEJE fazer uma fork de algum repositório existente pule para a etapa 4**

**Caso NÃO DESEJE continue lendo este README**

---

## 1. 

---

## ⚙️ 1. Configuração Inicial

Registra o nome e email (extremamente necessário para commits), define o *vscode* como IDE principal e verifica se tudo funcionou:

```bash
git config --global user.name "Seu Nome"                  # Definindo nome
git config --global user.email "seuemail@exemplo.com"     # Definindo email
git config --global core.editor "code --wait"             # Definindo vscode como padrão
git config --list                                         # Verificação
```

---

## 📂 2. Cria Repositório (pasta)

```bash
mkdir meu_projeto   # Cria pasta
cd meu_projeto      # Entra na pasta

git init            # Cria repositório local
```
---

## 🌿 3. Branch `master` para `main`

O GIT cria o branch com o nome _master_
Mas o ideal é utilizar com o nome _main_:

```bash
git branch -m master main
```

Se quiser automatizar **main** como padrão para novos repositórios futuros:

```bash
git config --global init.defaultBranch main
```

--- 

## 🍴 4. Criando a Fork

**Pule para a Etapa 6 se NÃO DESEJAR criar a FORK**

- O _Fork_ é uma função do GITHUB que edita um README já existente, seja seu ou de outra pessoa da plataforma, e recria o seu próprio, sem alterar o original.

<img width="1904" height="476" alt="fork" src="https://github.com/user-attachments/assets/a737e0bf-dc2e-403c-a6c5-89e14b850904" />

- Dê um nome a sua _fork_ e depois crie-a.

<img width="1002" height="691" alt="fork2" src="https://github.com/user-attachments/assets/5d217f27-3115-4737-95de-718fa8d239d3" />

---

## 🍽️ 5. Utilizando o Fork

- Copie o link
<img width="711" height="299" alt="fork3" src="https://github.com/user-attachments/assets/89a28783-6970-4c9b-ad89-0cf75a08d7cf" />

- Abra o Git 
- Faça as configurações iniciais (etapa 2)
- Clone o repositório dentro do Git
```bash
git clone <URl GitFork>          # Baixa o repositório do Fork
```

- Acessa a pasta
```bash
cd git-local          # Entra na pasta do repositório clonado
```

- E crie um _branch_
```bash
git checkout -b documentacao-colaboracao          # Cria um novo branch, mantendo o main limpo
```

---

## 6. GitFluence
