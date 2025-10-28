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

**Caso DESEJE fazer uma fork de algum repositório existente pule para a [Etapa 4](https://github.com/IsaacIuriO/Repositorio-GIT/blob/main/README.md#-4-criando-a-fork)**

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

Lista as branchs e mostra qual a atual:

```bash
git branch
```
img

--- 

## 🍴 4. Criando a Fork

**Pule para a Etapa 6 se NÃO DESEJAR criar a FORK**

- O _Fork_ é uma função do GITHUB que edita um README já existente, seja seu ou de outra pessoa da plataforma, e recria o seu próprio, sem alterar o original.

<img width="1904" height="476" alt="fork" src="https://github.com/user-attachments/assets/a737e0bf-dc2e-403c-a6c5-89e14b850904" />

- Dê um nome a sua _fork_ e depois crie-a.

<img width="1002" height="691" alt="fork2" src="https://github.com/user-attachments/assets/5d217f27-3115-4737-95de-718fa8d239d3" />

---

## 🍽️ 5. Utilizando a Fork

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

## 🔆 6. GitFluence

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/f534da4f-b766-4cac-b6ff-f3aa314c5197" />

Acesse: [GitFluence](https://www.gitfluence.com/) - Ele é um auxiliador para comandos no Git.

*Como funciona:* Pergunte a ele o que deseja fazer no Git e ele, SOMENTE, te retornará o código.

### Exemplos

Entrada: *"Push the new branch to the remote repository"*
<img width="1022" height="210" alt="ex1" src="https://github.com/user-attachments/assets/eaf5ad11-030c-4c47-847e-4302db2e8451" />
Entrada: *"See all my current branches"*
<img width="1021" height="178" alt="ex2" src="https://github.com/user-attachments/assets/e3b3706b-03b9-480b-b66d-5eb66f59f0fb" />

Entrada: *"Check the status of my files"*
<img width="1025" height="185" alt="ex3" src="https://github.com/user-attachments/assets/3f4e0521-e40f-4d84-a860-c2f87edccbe2" />

Entrada: *"Como ver as configurações atuais"*
<img width="1019" height="170" alt="ex4" src="https://github.com/user-attachments/assets/fb602630-a87d-4f92-b6e9-5eb3ec952f57" />

Entrada: *"Como comparar a nova atualização com a versão antiga"*
<img width="1020" height="174" alt="ex5" src="https://github.com/user-attachments/assets/53a89ac6-cef1-48c0-844d-439b1a95c860" />

_Ps: Você também pode utilizar perguntas em português!_

---

## 7. 

---
