# Repositorio-GIT

## 🎯 Objetivo

Este repositório tem como objetivo documentar e revisar toda a aprendizagem sobre o **GIT** e **GITHUB** no primeiro ano de ensino de Análise e Desenvolvimento de Sistemas - SENAI

---

## 🌩️ 0. Iniciando o Git

- Baixe o **[GitBash](https://git-scm.com/install/)**, utilizando a própria IDE do Git, ou o **[Git para Windows](https://git-scm.com/install/windows)**, utilizando o Prompt de Comando como IDE.

---

## Com ou Sem Fork?



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

