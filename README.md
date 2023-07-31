# Documentação do PYTHON-DJANGO-CRUDA

Olá!

Seja bem-vindo(a) ao PYTHON-DJANGO-CRUDA! Estou felizes em tê-lo(a) aqui e espero que esta experiência de aprendizado seja incrível, permitindo que juntos vençamos todos os desafios e aprendamos os fundamentos do Django, utilizando a linguagem Python.

## Ambiente de Desenvolvimento

Neste treinamento, utilizaremos o Visual Studio Code (VSCode) como nosso editor de código e o GitHub para o versionamento do código.

Para acompanhar este curso, é recomendado que você tenha o Python instalado em seu sistema. Caso precise de ajuda para a instalação do Python, recomendamos os seguintes links:

- [Passo a passo para instalar o Python no Windows](link_para_instalacao_python_windows)
- [Passo a passo para instalar o Python em outros sistemas operacionais](link_para_instalacao_python_outros_sistemas)

### Instalação do Python e pacotes necessários

Para obtermos os mesmos resultados ao longo das aulas, é essencial que você instale as seguintes versões dos softwares utilizados no curso:

1. **Python 3.10.6**: Siga as instruções de instalação do Python 3.10.6 em [python.org](https://www.python.org/downloads/release/python-3106/) ou utilize o instalador apropriado para o seu sistema operacional.

2. **Pacote pip**: O gerenciador de pacotes pip é necessário para instalar outras bibliotecas no Python. Abra o seu terminal ou prompt de comando de acordo com o seu sistema operacional e utilize os seguintes comandos:

   - Para sistemas Windows:
     ```
     curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py
     python get-pip.py
     ```

   - Para sistemas Mac:
     ```
     curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py
     python3 get-pip.py
     ```

   - Para sistemas Linux:
     ```
     sudo apt install python3-pip
     ```

3. **Ambiente virtual com virtualenv**: Durante o curso, utilizaremos um ambiente virtualizado chamado virtualenv para construir nossos projetos. Para instalá-lo, utilize o seguinte comando:

   ```
   pip install virtualenv
   ```

## Download do Template Front-end

Por fim, para o desenvolvimento do front-end do nosso projeto, você pode fazer o download de um template construído em HTML e CSS que será utilizado. Para obter o template, acesse o link abaixo:

- [Download do Template HTML e CSS](link_para_download_template_frontend)

Esperamos que este guia facilite o seu início no curso de Django 4. Caso tenha alguma dúvida, não hesite em entrar em contato conosco.

Desejamos a você uma jornada de aprendizado prazerosa e produtiva!

# Documentação do Desenvolvimento da Aplicação em Python com Django

Vamos iniciar o desenvolvimento da nossa aplicação em Python utilizando o framework Django.

## Configuração do Ambiente

Antes de começarmos, é necessário garantir que o Python e a Virtualenv estejam instalados em seu sistema operacional. Caso precise de ajuda, siga o passo a passo de instalação nos seguintes links:

- [Passo a passo para instalar o Python no seu sistema operacional](link_para_instalacao_python)
- [Passo a passo para instalar a Virtualenv no seu sistema operacional](link_para_instalacao_virtualenv)

Após a instalação do Python e Virtualenv, criaremos um novo projeto do zero, criando uma nova pasta na área de trabalho e chamando-a de "alura-space". 

### Verificação da Versão do Python e Virtualenv

Para verificar as versões instaladas do Python e Virtualenv, abra o terminal integrado do Visual Studio Code (ou acesse o terminal do seu sistema operacional) e digite os seguintes comandos:

```
python3 --version
virtualenv --version
```

No vídeo, o instrutor utilizou as versões "Python 3.10.5" e "virtualenv 20.16.2".

### Configurando o Ambiente Virtual

Agora, vamos isolar todas as dependências do nosso projeto criando um ambiente virtual com a Virtualenv. Digite o seguinte comando:

```
virtualenv venv
```

Será criada uma pasta chamada "venv" dentro do projeto "alura-space", contendo duas subpastas "bin" e "lib". Essa prática é uma boa forma de organizar nosso ambiente de desenvolvimento.

### Ativando o Ambiente Virtual

Para continuar utilizando o projeto com o ambiente virtual ativado, precisamos ativar a Virtualenv. O comando para ativar varia de acordo com o sistema operacional:

- No macOS, utilize o seguinte comando:
  ```
  source venv/bin/activate
  ```

- No Windows, utilize o seguinte comando:
  ```
  venv\Scripts\Activate
  ```

Ao executar o comando adequado para o seu sistema operacional, você verá a palavra "venv" aparecendo antes de "alura-space" no terminal, indicando que o ambiente virtual foi ativado.

### Desativando o Ambiente Virtual

Caso queira desativar o ambiente virtual futuramente, basta executar o seguinte comando:

```
deactivate
```

### Instalando o Django

Para instalar o Django, utilize o gerenciador de pacotes Pip, que é um programa de gerenciamento de pacotes do Python. Digite o seguinte comando:

```
pip install django
```

Após a instalação, o Django estará disponível para ser utilizado no nosso projeto.

Caso seja necessário atualizar o Pip, o terminal solicitará a execução do comando `pip install --upgrade pip`.

Apesar das instalações realizadas, é normal que as pastas dentro de "venv", no projeto "alura-space", aparentemente não tenham mudado muito.

Com o ambiente configurado e o Django instalado, estamos prontos para começar a desenvolver a nossa aplicação!

Esperamos que este guia tenha sido útil para você iniciar o projeto utilizando Django. Caso tenha alguma dúvida, estamos à disposição para ajudar.

Desejamos a você uma ótima jornada de desenvolvimento com Django!

Atenciosamente,

Equipe de Instrutores do Curso de Django.

# Executando Boas Práticas em Programação com Django

Agora que o Django está instalado, vamos executar uma boa prática em programação para visualizar todas as dependências do projeto e criar um arquivo "requirements.txt" contendo todas as informações necessárias. Isso ajudará a manter o projeto organizado e garantir que outros desenvolvedores possam replicar o ambiente.

### Visualizando e Criando o Arquivo "requirements.txt"

Para visualizar as dependências do projeto e suas versões, execute o seguinte comando no terminal:

```
pip freeze
```

Ele apresentará uma lista de todas as bibliotecas instaladas no ambiente virtual, incluindo a versão do Django, sqlparse e asgiref necessárias para o funcionamento do projeto.

Agora, criaremos o arquivo "requirements.txt" com todas as informações das dependências executando o comando:

```
pip freeze > requirements.txt
```

Dessa forma, teremos um arquivo "requirements.txt" com todas as bibliotecas e suas respectivas versões necessárias para o projeto.

### Iniciando o Projeto Django

Para iniciar o projeto Django, utilizaremos o comando `django-admin startproject setup .` (o ponto "." no final é importante). Isso criará uma pasta chamada "setup" dentro da pasta "alura-space", contendo as configurações iniciais do projeto.

### Acessando o arquivo "manage.py" e Selecionando o Interpretador Python

Agora, vamos acessar o arquivo "manage.py" que acabou de ser criado. Para garantir que utilizaremos a versão correta do Python (da Virtualenv), é importante selecionar o interpretador correto. 

No terminal da IDE, pressione "Ctrl + Shift + P" e escreva "Python: Select Interpreter" na barra que será mostrada. Selecione a opção correspondente à versão do Python da Virtualenv (venv).

### Visualizando o Projeto

Agora, podemos visualizar o projeto executando o comando:

```
python manage.py runserver
```

Isso iniciará o servidor e permitirá que você visualize o projeto. Verifique o terminal para obter a URL do servidor. Ao acessá-la em seu navegador, você verá uma página que indica a instalação bem-sucedida do Django. Essa página é exibida devido ao ambiente de "DEBUG=True".

No próximo vídeo, aprenderemos a configurar o fuso horário e traduzir a página para o português.

Esperamos que essas práticas ajudem você a desenvolver a aplicação em Python utilizando o Django. Caso tenha alguma dúvida, não hesite em entrar em contato conosco.

Desejamos sucesso no desenvolvimento do projeto!

Atenciosamente,

Equipe de Instrutores do Curso de Django.