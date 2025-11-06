# Repositorio-GIT

## 🎯 OBJETIVO

Este repositório tem como objetivo documentar e revisar toda a aprendizagem sobre o **GIT** e **GITHUB** no primeiro ano de ensino de Análise e Desenvolvimento de Sistemas - SENAI

---

## 🌩️ INICIANDO O GIT

É necessário apenas dois pré-requisitos antes de estruturar seus projetos:

- Baixe o **[GitBash](https://git-scm.com/install/)**, utilizando a própria IDE do Git, ou o **[Git para Windows](https://git-scm.com/install/windows)**, utilizando o Prompt de Comando como IDE.

### Com ou Sem Fork?

A **fork** pode ser um pré-requisitante. Antes de programar dentro do Git, precisamos decidir se iremos editar um arquivo já existente ou se vamos criar um novo.

Um jeito para editar um README já existente no GITHUB, é utilizando a função **Fork**.

### Fork do Repositório GITHUB

**Caso DESEJE fazer uma fork de algum repositório existente pule para a [Etapa 4](https://github.com/IsaacIuriO/Repositorio-GIT/blob/main/README.md#-4-criando-a-fork)**

**Caso NÃO DESEJE continue lendo este README**

---

### ⚙️ 1. Configuração Inicial

Após abrir o seu espaço de programação é necessário configurar alguns aspectos, para tornar seu projeto mais limpo e organizado.

Registra o nome e email (extremamente necessário para commits), define o *vscode* como IDE principal e verifica se tudo funcionou:

```bash
git config --global user.name "Seu Nome"                  # Definindo nome
git config --global user.email "seuemail@exemplo.com"     # Definindo email
git config --global core.editor "code --wait"             # Definindo vscode como padrão
git config --list                                         # Verificação
```

---

### 📂 2. Cria Repositório (pasta)

```bash
mkdir meu_projeto   # Cria pasta
cd meu_projeto      # Entra na pasta

git init            # Cria repositório local
```
---

### 🌿 3. Branch `master` para `main`

O GIT cria o branch com o nome _master_.

Mas o ideal é utilizar com o nome _main_:

```bash
git branch -m master main          # Muda de main para master
```

Se quiser automatizar **main** como padrão para novos repositórios futuros:

```bash
git config --global init.defaultBranch main            # Padroniza o nome para arquivos novos
```

Lista as branchs e mostra qual a atual:

```bash
git branch          # Lista
```
img

--- 

### 🍴 4. Criando a Fork

**Pule para a Etapa 6 se NÃO DESEJAR criar a FORK**

- O _Fork_ é uma função do GITHUB que edita um README já existente, seja seu ou de outra pessoa da plataforma, e recria o seu próprio, sem alterar o original.

<img width="1904" height="476" alt="fork" src="https://github.com/user-attachments/assets/a737e0bf-dc2e-403c-a6c5-89e14b850904" />

- Dê um nome a sua _fork_ e depois crie-a.

<img width="1002" height="691" alt="fork2" src="https://github.com/user-attachments/assets/5d217f27-3115-4737-95de-718fa8d239d3" />

---

### 🍽️ 5. Utilizando a Fork

Agora com a _fork_ criada, basta utiliza-lá no seu projeto.

- Copie o link

<img width="711" height="299" alt="fork3" src="https://github.com/user-attachments/assets/89a28783-6970-4c9b-ad89-0cf75a08d7cf" />

- Abra o Git 
- Faça as configurações iniciais ([Etapa 1](https://github.com/IsaacIuriO/Repositorio-GIT/blob/main/README.md#%EF%B8%8F-1-configura%C3%A7%C3%A3o-inicial))
- Clone o repositório dentro do Git:

```bash
git clone <URl GitFork>          # Baixa o repositório do Fork no GIT
```

- Acessa a pasta:

```bash
cd git-local          # Entra na pasta do repositório clonado
```

- E crie um _branch_:

```bash
git checkout -b documentacao-colaboracao          # Cria um novo branch, mantendo o main limpo
```

---

### 🕹️ 6. Criando o Primeiro Arquivo

Criando um arquivo de texto:
```bash
echo "Hello, World! Primeiro arquivo no GIT!" > readme.txt      # Cria um arquivo de texto com o conteúdo entre aspas
```

---

### 📊 7. Estados dos Arquivos

Mostrando a condição dos arquivos:
```bash
git status          # Mostra o estado dos arquivos: novos, modificados ou prontos para _commit_.
```

---

### 🦾 8. Staging Area

No **Staging Area**, os arquivos são preparados para o _commit_.

```bash
git add readme.txt       # Adiciona apenas o arquivo mencionado
git add .                # Adiciona todos os arquivos do diretório (pasta)
git status               # Mostra o estado
```
img

---

### ✅ 9. Commit

No **Commit**, os arquivos são salvos no **GIT LOCAL**.

```bash
git commit -m "Primeiro Commit"
```

---

### ✏️ 10. Editar Arquivos

Caso deseje mudar um arquivo salvo:

```bash
echo "Criando uma nova linha" >> readme.txt             # Adiciona uma nova linha no arquivo existente
git status                                              # Verifica o estado do arquivo

git diff                                                # Mostra as diferenças entre uma versão de um arquivo e outro

git add readme.txt                                      # Coloca no Staging Area o arquivo
git commit -m "Atualiza readme.txt com nova linha"      # Salva no repositório e diz o que mudou
```

img

---

### ↩️ 11. Desfazer Mudanças

Caso tenha feito algum erro:

```bash
git restore readme.txt              # Tiram o que foi mudado, antes do staged (add)

git restore --staged readme.txt     # Tiram o que foi mudado, depois do staged (add)
```

---

### 🔍 12. Histórico de Commits

Há alguns comandos que permite ver a ordem cronológica dos _commits_.

```bash
git log                # Específico para ver o histórico dos commits
git log --oneline      # Mostra de forma mais resumida

git show               # Comando versátil para ver algumas propriedades
```

img

---

### ➕ 13. Criar Nova Branch

```bash
git branch                         # Lista as branches existentes

git branch nova_ramificacao        # Cria uma nova branch
```

---

### 🔀 14. Mudar Entre Branches

```bash
git branch                         # Lista as branches existentes

git switch nova_ramificacao        # Alterna de branches, tornando 'nova_ramificacao' como a atual
```

---

### 👌 15. Commits em Outras Branches

É o mesmo processo como todos as outras branches, só que você tem que estar dentro dela para funcionar.

```bash
git switch nova_ramificacao                           # Alterna de branches, tornando 'nova_ramificacao' como a atual

echo "Olá, Mundo! (de novo)" > aleatorio.txt          # Cria arquivo de texto
git add aleatorio.txt                                 # Adiciona no Staging Area
git commit -m "Mais uma mudança"                      # Salva no repositório
```

---

### ☯️ 16. Fusão entre Branches

Antes de fusionar uma _branch_ a outra, é necessário que troque para a _branch_ principal.

```bash
git switch main

git merge nova_ramificacao
```

---

### 🗑️ 17. Excluir Branches

Quer excluir?

```bash
git branch -d nova_ramificacao
```

---

### 🫥 18. Ignorar Arquivos no Commit

O **.gitignore** é uma extensão de arquivo muito especial. Ele permite que você possa escolher de forma geral os arquivos que não serão _commitados_.

Serve bastante para a exclusão de arquivos repetidos ou pesados do seu _backup_.

```bash
echo .gitignore > "node_modules/"
```

---

## 📋 TESTE RÁPIDO

Utilizando todos os comandos listados acima de forma eficiente:

```bash
git config --global user.name "Seu Nome"                  		# Definindo nome
git config --global user.email "seuemail@exemplo.com"    			# Definindo email
git config --global core.editor "code --wait"            			# Definindo vscode como padrão
git config --list                                        			# Verificação

mkdir meu_projeto   										                      # Cria pasta
cd meu_projeto      									                   	    # Entra na pasta

git init            									                        # Cria repositório local

git branch -m master main          							              # Muda de main para master

git config --global init.defaultBranch main           	      # Padroniza o nome para arquivos novos

git branch          										                      # Lista branchs

git clone <URl GitFork>        						                    # Baixa o repositório do Fork no GIT
cd git-local          							                          # Entra na pasta do repositório clonado

git checkout -b documentacao-colaboracao         		          # Cria um novo branch, mantendo o main limpo

echo "Hello, World! Primeiro arquivo no GIT!" > readme.txt    # Cria um arquivo de texto com o conteúdo entre aspas

git status                                                    # Mostra o estado

echo "Criando uma nova linha" >> readme.txt                   # Adiciona uma nova linha no arquivo existente
git status                                                    # Verifica o estado do arquivo

git add readme.txt                                            # Coloca no Staging Area o arquivo

git diff                                                      # Mostra as diferenças entre uma versão de um arquivo e outro

git restore --staged readme.txt     				                  # Tiram o que foi mudado, depois do staged (add)

git commit -m "Atualiza readme.txt com nova linha"            # Salva no repositório e diz o que mudou

echo "Criando uma outra nova linha" >> readme.txt             # Adiciona uma nova linha no arquivo existente de novo

git restore readme.txt             				                    # Tiram o que foi mudado, antes do staged (add)

git diff

git log               						                            # Específico para ver o histórico dos commits
git log --oneline      							   	                      # Mostra de forma mais resumida

git show               					  	                          # Comando versátil para ver algumas propriedades

git branch                         					                  # Lista as branches existentes

git branch nova_ramificacao        							              # Cria uma nova branch
git switch nova_ramificacao                                   # Alterna de branches, tornando 'nova_ramificacao' como a atual

echo "Olá, Mundo! (de novo)" > aleatorio.txt                  # Cria arquivo de texto
git add aleatorio.txt                                        	# Adiciona no Staging Area
git commit -m "Mais uma mudança"                              # Salva no repositório

git switch main									  	                          # Muda pra branch principal

git merge nova_ramificacao 										                # Fusiona

git branch -d nova_ramificacao									              # Exclui branch

echo .gitignore > "node_modules/"							                # Cria um .gitignore
```

---

## 📤 COLABORAÇÃO E COMPARTILHAMENTO

Compartilhar o seu repositório para colaboração de outras pessoas, faz do seu projeto único, regrado e eficiente.

É necessário alguns pré-requisitos, para fazê-lo funcionar:

- GIT instalado.
- Ter, ao menos, uma conta GITHUB para cada membro da colaboração.
- O membro principal deve ter um projeto local e já inicializado ([Etapa 1 - 🌩️ INICIANDO GIT](https://github.com/IsaacIuriO/Repositorio-GIT/blob/main/README.md#%EF%B8%8F-iniciando-o-git)).

---

### 💡 Help - GitFluence

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/f534da4f-b766-4cac-b6ff-f3aa314c5197" />

Acesse: [GitFluence](https://www.gitfluence.com/) - Ele é um website/auxiliador para comandos no Git.

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

_OBS: Você também pode utilizar perguntas em português!_

---
