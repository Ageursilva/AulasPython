
  

  

##  Guia de Introdução ao Python

  

  

###  1. Configuração do Ambiente

  

  

####  Instalação do VSCode:

  

- Acesse o site oficial do VSCode: [VSCode](https://code.visualstudio.com/)

  

- Baixe a versão adequada para o seu sistema operacional.

  

- Siga as instruções de instalação.

  

  

####  Instalação do Python:

  

- Acesse o site oficial do Python: [Python](https://www.python.org/downloads/)

  

- Baixe a versão mais recente (ou a versão desejada) para o seu sistema operacional.

  

- Durante a instalação, marque a opção "Add Python to PATH" para facilitar o acesso ao Python pelo terminal.

  

- Siga as instruções de instalação.

  

  

###  2. Primeiro Programa

  

  

####  Crie um arquivo `hello.py`:

  

- Abra o VSCode.

  

- Crie um novo arquivo e salve-o como `hello.py`.

  

- No arquivo, escreva o seguinte código:

  

```python

  

print("Olá, mundo!")

  

```

  

  

####  Execute o programa pelo terminal:

  

- Abra o terminal (prompt de comando ou PowerShell).

  

- Navegue até a pasta onde você salvou o arquivo `hello.py` usando o comando `cd`.

  

- Execute o programa com o comando:

  

```python

  

python hello.py

  

```

  

O terminal exibirá a mensagem "Olá, mundo!".

  

  

###  3. Tipos de Dados

  

  

Use a função `type()` para verificar o tipo de um valor:

  

```python

  

print(type(2.5))  # float (número de ponto flutuante)

  

print(type(42))  # int (número inteiro)

  

print(type("Olá"))  # str (string, texto)

  

print(type(True))  # bool (booleano, True ou False)

  

```

  

  

###  4. Variáveis e Tipos de Dados

  

  

####  Declaração de variáveis:

  

```python

  

largura =  10

  

print(largura)

  

```

  

  

####  Cálculo da área de um retângulo:

  

```python

  

base =  2

  

altura =  3

  

area = base * altura

  

print("Área do retângulo:", area)

  

  

# Usando f-strings (Python 3.6+)

  

print(f"Área do retângulo: {area}")

  

```

  

  

####  Declaração de variáveis com tipos explícitos:

  

```python

  

idade:  int  =  30

  

altura:  float  =  1.75

  

nome:  str  =  "Maria"

  

gosta_de_python:  bool  =  True

  

```

  

  

####  Recebendo dados do usuário:

  

```python

  

idade =  int(input("Sua idade: "))

  

print(f"Sua idade é {idade}")

  

```

  

  

###  5. Exemplos de Programas

  

  

####  Cumprimentar o usuário:

  

```python

  

nome =  input("Qual é o seu nome? ")

  

print(f"Olá, {nome}! Prazer em te conhecer.")

  

```

  

  

####  Calcular a área de um retângulo:

  

```python

  

base =  float(input("Digite a base do retângulo: "))

  

altura =  float(input("Digite a altura do retângulo: "))

  

area = base * altura

  

print(f"A área do retângulo é: {area}")

  

```

  

  

####  Converter Celsius para Fahrenheit:

  

```python

  

celsius =  float(input("Digite a temperatura em Celsius: "))

  

fahrenheit =  (celsius *  9/5)  +  32

  

print(f"{celsius}°C equivale a {fahrenheit}°F")

  

```

  

  

###  6. Operadores Aritméticos

  

-  `+` (soma)

  

-  `-` (subtração)

  

-  `*` (multiplicação)

  

-  `/` (divisão)

  

-  `//` (divisão inteira)

  

-  `%` (módulo, resto da divisão)

  

-  `**` (exponenciação)

  

  

###  7. Operadores Lógicos

  

-  `and` (E)

  

-  `or` (OU)

  

-  `not` (NÃO)

  

  

###  8. Ordem de Precedência

  

1. Parênteses `()`

  

2. Exponenciação `**`

  

3. Multiplicação `*`, divisão `/`, divisão inteira `//`, módulo `%` (da esquerda para a direita)

  

4. Soma `+` e subtração `-` (da esquerda para a direita)

  

5. Operadores de comparação (`<`, `>`, `<=`, `>=`, `==`, `!=`)

  

6. Operadores lógicos (`not`, `and`, `or`)

   
 

  

#  Guia para Instalação e Configuração do Git com Chave SSH no GitHub

  

  

##  1. Baixar e Instalar o Git

  

  

- Acesse o site oficial do Git: [https://git-scm.com/](https://git-scm.com/)

  

- Baixe a versão para Windows.

  

- Execute o instalador e siga as instruções. Na maioria dos casos, você pode manter as configurações padrão.

  

  

##  2. Configurar sua Identidade

  

  

- Abra o Git Bash (um terminal que vem com a instalação do Git).

  

- Configure seu nome e email, que serão associados aos seus commits:

  

  

```bash

  

git  config  --global  user.name  "Seu Nome"

  

git  config  --global  user.email  "seu_email@exemplo.com"

  

```

  

##  3. Gerar uma Chave SSH

  

  

Abra o Git Bash: Procure por "Git Bash" no menu Iniciar do Windows e abra-o. Essa é a interface de linha de comando que usaremos para os comandos Git.

  

Gere a chave: Digite o seguinte comando no Git Bash e pressione Enter:

  

```bash

  

ssh-keygen  -t  rsa  -b  4096  -C  "seu_email@exemplo.com"

  

```

  

Confirme o local de salvamento: O Git Bash perguntará onde salvar a chave. Pressione Enter para aceitar o local padrão `(C:\Users\SeuNomeUsuario.ssh\id_rsa).`

  

  

Defina uma senha (opcional): Você pode definir uma senha para proteger sua chave privada. Se fizer isso, precisará digitá-la sempre que usar a chave. Se preferir não usar senha, pressione Enter duas vezes.

  

  

##  4. Adicionar a Chave SSH ao GitHub

  

- Abra o arquivo da chave pública: No Explorador de Arquivos do

Windows, navegue até `C:\Users\SeuNomeUsuario\.ssh` Abra o arquivo `id_rsa.pub` com um editor de texto (como o Bloco de Notas).

- Copie o conteúdo da chave: Selecione todo o texto dentro do arquivo `id_rsa.pub` e copie-o (Ctrl+C).

- Acesse as configurações do GitHub: Abra seu navegador e faça login na sua conta do GitHub. Clique na sua foto de perfil no canto superio rdireito e selecione "Settings" (Configurações).

- Vá para as chaves SSH: No menu lateral esquerdo, clique em "SSH and GPG keys" (Chaves SSH e GPG).

- Adicione a nova chave: Clique no botão verde "New SSH key" (Nova chave SSH).

  

**Preencha os campos:**

  

- Em "Title" (Título), dê um nome descritivo à chave (por exemplo, "Meu PC Windows").

- Em "Key" (Chave), cole o conteúdo da chave pública que você copiou anteriormente.

- Clique em "Add SSH key" (Adicionar chave SSH).

##  Como subir seu repositório no GitHub

 1. Valide se o GIT esta instalado no seu sistema, No seu terminal
    digite o comando `git -v` e cheque se o mesmo mostra a versão do GIT instalada

![enter image description here](https://i.imgur.com/ZEz8PDn_d.webp?maxwidth=760&fidelity=grand)

 2. Acesse o GitHub e crie um novo repositório e copie o linke HTTPS que  vai ser gerado

![enter image description here](https://i.imgur.com/APrzT93_d.webp?maxwidth=760&fidelity=grand)

 3. Abra o seu terminal na pasta onde esta localizado seu projeto
 4. Digite o comando `git init` para iniciar o git neste repositório
 5.  Adicione os arquivos da pasta com o comando `git add .`
 6.   Crie um novo commit para os arquivos que vão subir com o comando `git commit -m "comentário do commit"`
 7. Suba seus arquivos com a URL que pegamos no segundo passo use o comando `git remote add origin URL-DO-PASSO-2`
 8. Autorize o envio com o comando `git push -u origin main`
