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

# Configurando Idioma Principal e Fuso Horário no Projeto Django

Quando criamos uma aplicação em Django, é possível alterar o idioma principal e o fuso horário utilizados.

### Configurações de Idioma e Fuso Horário

As configurações relacionadas ao idioma da aplicação ficam no arquivo "settings.py", localizado em "setup > settings.py". Vamos abrir esse arquivo e utilizar os atalhos "Ctrl + B" e "Ctrl + J" para minimizá-lo e visualizar melhor seu conteúdo.

Dentro do arquivo "settings.py", encontramos todas as configurações do projeto, incluindo dependências, templates e muito mais. Portanto, precisaremos manipulá-lo bastante durante o desenvolvimento. Nas linhas 106 e 108 do código do arquivo, encontramos as variáveis "LANGUAGE_CODE" e "TIME_ZONE", que são exatamente o que procurávamos.

Ao lado de "LANGUAGE_CODE", encontramos o valor 'en-us', que representa o idioma inglês dos Estados Unidos. Vamos substituí-lo por 'pt-br' para alterar a linguagem da aplicação para o português brasileiro. Em relação ao fuso horário, utilizaremos o valor 'America/Sao_Paulo' para ajustar nosso fuso horário.

### Verificando as Alterações

Após realizar as alterações no arquivo "settings.py", podemos apertar "Ctrl + J" para abrir o terminal novamente. Vamos voltar ao servidor e atualizar a página no navegador. Com isso, veremos que a página exibida já está em português. Além disso, ao verificar as informações de hora, perceberemos que o fuso horário também foi atualizado corretamente.

### Informações Adicionais

Caso queira saber mais sobre o registro de fusos horários no Django 4.1, você pode acessar [este link](https://docs.djangoproject.com/en/4.1/topics/i18n/timezones/). A partir da versão 4 do Django, o pacote responsável pelo registro de horas é o zoneinfo. Em versões anteriores da ferramenta, era utilizado o comando USE_DEPRECATED_PYTZ.

Com essas configurações, o idioma principal e o fuso horário do seu projeto Django estão devidamente ajustados. Isso proporcionará uma melhor experiência para os usuários e facilitará o desenvolvimento em um ambiente mais familiar.

Esperamos que essas informações tenham sido úteis para você configurar corretamente o idioma e o fuso horário do seu projeto Django. Caso tenha alguma dúvida, estamos à disposição para ajudar.

Desejamos sucesso no desenvolvimento da sua aplicação!

Atenciosamente,

Equipe de Instrutores do Curso de Django.

# Versionamento do Projeto Django com Git e Github

Agora que o projeto está configurado com o idioma e horário corretos, precisamos versionar o projeto utilizando o Git e o Github.

## Gerenciamento da Django Secret Key

Por questões de segurança, não devemos enviar todas as partes do código para o Github, principalmente a Django Secret Key. Essa chave secreta não deve ser disponibilizada publicamente, pois é uma informação sensível.

### Removendo a Django Secret Key do Código

Para evitar que a Secret Key seja enviada para o Github, vamos copiá-la utilizando "Ctrl + C" e depois removê-la do código em "setup > settings.py".

### Utilizando Variáveis de Ambiente com python-dotenv

Para evitar o envio da Secret Key e outras informações confidenciais, utilizaremos variáveis de ambiente com a biblioteca python-dotenv. Para começar, no terminal, instalaremos a dependência python-dotenv com o seguinte comando:

```
pip install python-dotenv
```

Em seguida, atualizaremos o arquivo "requirements.txt" com o comando:

```
pip freeze > requirements.txt
```

### Criando e Configurando o Arquivo .env

Criaremos um novo arquivo chamado ".env" na pasta "alura-space". Dentro desse arquivo, inseriremos a Secret Key utilizando o seguinte formato:

```
SECRET_KEY=sua_secret_key_aqui
```

Agora, podemos remover a Secret Key do arquivo "settings.py".

### Carregando as Variáveis de Ambiente no "settings.py"

Voltaremos ao arquivo "settings.py" e importaremos a função `load_dotenv` na linha 13, junto com o `Path`:

```python
from pathlib import Path
from dotenv import load_dotenv
```

Logo abaixo, criaremos a função `load_dotenv()`:

```python
load_dotenv()
```

Na linha 26 do código, onde estava a Secret Key, substituiremos o valor por `str(os.getenv('SECRET_KEY'))`.

### Verificando a Funcionalidade

Após realizar essas alterações, executaremos o servidor com o comando:

```
python manage.py runserver
```

Se atualizarmos a página no navegador, veremos que o projeto funcionará novamente.

### Enviando o Projeto para o Github

Agora, podemos enviar o projeto para o Github, e o arquivo ".env" não será enviado, garantindo que a Secret Key permaneça somente em nosso computador.

Com essas configurações, sua Django Secret Key estará segura, evitando exposição em um repositório público no Github.

Esperamos que esse guia tenha sido útil para você versionar seu projeto Django com segurança. Se tiver alguma dúvida, estamos à disposição para ajudar.

Desejamos um desenvolvimento tranquilo e produtivo do seu projeto!

Atenciosamente,

Equipe de Instrutores do Curso de Django.