# Repositorio-GIT

## 🎯 Objetivo

Este repositório tem como objetivo documentar e revisar toda a aprendizagem sobre o **GIT** e **GITHUB** no primeiro ano de ensino de Análise e Desenvolvimento de Sistemas - SENAI

---

## 🌩️ 0. Iniciando o Git

- Baixe o **[GitBash](https://git-scm.com/install/)**, utilizando a própria IDE do Git, ou o **[Git para Windows](https://git-scm.com/install/windows)**, utilizando o Prompt de Comando como IDE.

---

## Com ou Sem Fork?

Antes de programar dentro do Git, precisamos decidir se iremos editar um arquivo já existente ou não.

Um jeito para se editar um README já existente no GITHUB, é usando a função **Fork**.

## Fork do Repositório

**Caso não deseje fazer uma fork de algum repositório existente pule para a etapa X**

## 🍴 1. Criando a Fork

- O _Fork_ é uma função do GITHUB que edita um README já existente, seja seu ou de outra pessoa da plataforma, e recria o seu próprio, sem alterar o original.

<img width="1904" height="476" alt="fork" src="https://github.com/user-attachments/assets/a737e0bf-dc2e-403c-a6c5-89e14b850904" />

- Dê um nome a sua _fork_ e depois crie-a.

<img width="1002" height="691" alt="fork2" src="https://github.com/user-attachments/assets/5d217f27-3115-4737-95de-718fa8d239d3" />



---

## ⚙️ 2. Configuração Inicial

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

