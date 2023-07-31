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

# Enviando o Projeto para o Github com .gitignore

Agora que nosso código está pronto, vamos enviá-lo para o Github. Antes disso, precisamos garantir que não enviaremos todos os arquivos para o repositório, especialmente os que contêm informações confidenciais. Para isso, criaremos um novo arquivo chamado ".gitignore" dentro da pasta do projeto.

## Criando o Arquivo .gitignore

1. Crie um novo arquivo chamado ".gitignore" dentro da pasta principal do projeto (alura-space).
2. Acesse o site gitignore.io e digite "Django" para obter o padrão de arquivos que não devem ser enviados ao Github.
3. Selecione todo o conteúdo gerado no gitignore.io (com "Ctrl + A") e copie (com "Ctrl + C").
4. Cole o conteúdo copiado no arquivo ".gitignore" que você criou no passo 1 (com "Ctrl + V").

Obs: É importante batizar os arquivos como ".env" e "venv" exatamente como estão no padrão do gitignore.io, para que eles não sejam enviados ao Github.

## Iniciando o Repositório Local e Realizando o Commit

1. No terminal, pare o servidor pressionando "Ctrl + C".
2. Inicie um repositório local com o comando `git init`.
3. Execute o comando `git add .` para adicionar todos os arquivos ao repositório. Os arquivos que não serão enviados ao Github serão exibidos em cinza na barra lateral do terminal.
4. Realize o commit com o comando `git commit -m "projeto alura space"`.

## Enviando o Projeto para o Github

1. Crie um novo repositório no Github clicando em "+ > New repository" e dê o nome "alura_space".
2. No repositório criado, clique na seção "...or create a new repository on the command line" para obter o comando `git remote add origin <link_do_seu_repositório>`.
3. Copie o comando `git remote add origin <link_do_seu_repositório>` e execute-o no terminal.
4. Em seguida, execute o comando `git push origin master` para enviar o código para o Github.

Após realizar esses passos, o código será enviado para o Github. Ao acessar o repositório no Github, você verá que a Secret Key e outros objetos confidenciais não foram enviados, garantindo a segurança do projeto.

Parabéns! Seu projeto agora está versionado no Github e pronto para colaboração e compartilhamento.

# Criando um App Django para a Galeria de Imagens - Parte 1

Apesar de termos iniciado o projeto, sempre que subimos o servidor, a página exibida ainda mostra o foguete. Agora, queremos visualizar uma página diferente, onde exibiremos "Alura Space" na tela.

## Criando um Novo App "Galeria"

Vamos criar outros "pedaços" para compor nosso projeto, cada um com funcionalidades específicas. Esses "pedaços" são chamados de apps. Um projeto pode conter vários apps, e cada app pode ter suas próprias funcionalidades.

1. Pare o servidor pressionando "Ctrl + C".
2. Ative a venv com o comando: `source venv/bin/activate.fish` (ou o comando correspondente ao seu sistema operacional).
3. Execute o comando `python manage.py help` para visualizar uma série de comandos relacionados ao "manage.py".
4. Para criar um novo app chamado "galeria", utilize o comando: `python manage.py startapp galeria`. Isso criará uma pasta chamada "galeria" dentro da pasta "alura-space" com os arquivos iniciais necessários para o app.

## Configurando o App "Galeria" no Projeto

Agora que o app "galeria" foi criado, precisamos configurá-lo para fazer parte do nosso projeto.

1. Abra o arquivo "settings.py" localizado em "setup > settings.py".
2. Role a página até encontrar a seção "INSTALLED_APPS".
3. No final da lista em "INSTALLED_APPS", adicione `'galeria',` para sinalizar que o app "galeria" faz parte do nosso projeto.

```python
INSTALLED_APPS = [
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',
    'galeria',
]
```

## Verificando o App no Servidor

Vamos voltar ao servidor e executar o comando:

```
python manage.py runserver
```

Agora, o servidor voltará a funcionar, mas, se acessarmos a página no navegador, ainda encontraremos a página indesejada. Isso ocorre porque ainda não configuramos o app "galeria" para apresentar algo na tela.

No próximo vídeo, aprenderemos a implementar funcionalidades no app "galeria" para que ele possa exibir conteúdo na página.

Esperamos que essas etapas tenham sido claras e que você possa prosseguir com o desenvolvimento do app "galeria" com sucesso.

# Exibindo "Alura Space" na Tela com o App "Galeria"

Agora que criamos, configuramos e instalamos o app "galeria", queremos exibir "Alura Space" na tela.

## Configurando a View para Exibir "Alura Space"

1. Acesse o arquivo "galeria > views.py", que é responsável por exibir informações na tela.
2. Importe a forma de responder às requisições utilizando o código `from django.http import HttpResponse`.
3. Crie a função `index` utilizando o `def`, que será responsável pela página principal da aplicação. Ela receberá o parâmetro `request` para que possamos responder às requisições.
4. Dentro da função `index`, retorne o conteúdo que queremos exibir na tela utilizando o módulo `HttpResponse`. Por exemplo: `return HttpResponse('<h1>Alura Space</h1>')`.

```python
from django.http import HttpResponse

def index(request):
    return HttpResponse('<h1>Alura Space</h1>')
```

Se atualizarmos a página no navegador após essas alterações, ainda não veremos a mensagem "Alura Space" na tela, porque precisamos configurar as rotas.

## Configurando as Rotas no Arquivo "urls.py"

1. Acesse o arquivo "setup > urls.py", que cuida das rotas do projeto.
2. No início do código, é possível ver um extenso comentário de tudo que podemos fazer. Podemos ignorá-lo ou, como faz o instrutor no vídeo, apagá-lo.
3. Crie um novo path dentro de `urlpatterns`. Ele será `path('', index)`.
4. Importe a função `index` no arquivo "urls.py" inserindo `from galeria.views import index` na linha 3 do código.
5. O resultado deve ser parecido com o código abaixo:

```python
from django.contrib import admin
from django.urls import path
from galeria.views import index

urlpatterns = [
    path('admin/', admin.site.urls),
    path('', index),
]
```

Ao abrir o servidor e atualizar o navegador, o código será carregado automaticamente e a página exibirá "Alura Space" em formato de cabeçalho H1.

### Adicionando um Parágrafo na Página

Se desejamos adicionar um parágrafo abaixo do cabeçalho H1, basta editar a função `index` no arquivo "views.py" e adicionar uma tag `<p>` com o texto "Bem vindo ao espaço":

```python
from django.http import HttpResponse

def index(request):
    return HttpResponse('<h1>Alura Space</h1><p>Bem vindo ao espaço</p>')
```

Ao atualizar a página no navegador novamente, encontraremos o novo parágrafo de texto exibido.

No próximo vídeo, aprenderemos a isolar as URLs para tornar nosso projeto mais organizado.

# Renderizando Página HTML no App "Galeria"

Nós não queremos desenvolver toda a nossa aplicação dentro de "galeria > views.py", no retorno de `HttpResponse`. Queremos criar uma página HTML e renderizá-la na tela.

## Configurando o Diretório de Templates

Para renderizar a página HTML, precisamos informar ao nosso projeto onde ficam os arquivos de templates. Vamos acessar o arquivo "setup > settings.py" e rolar a página até a seção `TEMPLATES`, na linha 58 do código.

1. Ao lado de `'DIRS'`, informaremos o local dos arquivos HTML utilizando `os.path.join()`:

```python
'DIRS': [os.path.join(BASE_DIR, 'templates')],
```

2. Criaremos a pasta "templates" dentro da pasta "alura-space". Esta pasta será o local dos arquivos de templates.

## Criando um Arquivo de Template HTML

Dentro da pasta "templates", criaremos um novo arquivo chamado "index.html". Adicionaremos o código base inicial:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Alura Space</title>
</head>
<body>
    <h1>Nossa... deu certo mesmo!</h1>
</body>
</html>
```

## Renderizando a Página HTML na View

Vamos à "galeria > views.py" e faremos as seguintes alterações:

1. Removeremos o `HttpResponse` na linha 5 e a importação de `from django.shortcuts import render` na linha 2.
2. Adicionaremos a propriedade `render` para o retorno da função `index`, passando como parâmetros `request`, que será sempre o primeiro parâmetro, e o arquivo que queremos exibir entre strings. No nosso caso, é "index.html".

```python
from django.shortcuts import render

def index(request):
    return render(request, 'index.html')
```

## Testando a Renderização no Navegador

Após executar o servidor com o comando `python manage.py runserver`, volte ao navegador e atualize a página. Você verá a mensagem "Nossa... deu certo mesmo!" sendo exibida.

Agora que temos uma página HTML renderizada, podemos criar todo o nosso código utilizando esse template. Por exemplo, abaixo da tag `<h1>`, podemos adicionar um parágrafo `<p>` com o texto "RECEBA!!!!":

```html
<body>
    <h1>Nossa... deu certo mesmo!</h1>
    <p>RECEBA!!!!</p>
</body>
```

Ao atualizar o navegador novamente, encontraremos essa nova alteração.

Dessa forma, conseguimos isolar o código HTML em um único lugar. Agora podemos sempre pedir que a view renderize essa página, porque dissemos para nossas configurações de template que todos os códigos HTML ficarão dentro da pasta "templates".

No próximo vídeo, aprenderemos a isolar as URLs para tornar nosso projeto ainda mais organizado.

Esperamos que essas etapas tenham sido claras e que você possa continuar desenvolvendo o app "Alura Space" com sucesso.

# Alterando o Visual do Projeto Django

Nosso próximo desafio é alterar o visual do nosso projeto Django.

## Organizando os Arquivos HTML e CSS

Na atividade anterior a este vídeo, temos os arquivos HTML e CSS do projeto finalizado do Alura Space disponíveis para download.

1. Para começar, abriremos nosso projeto Django. Para manter nosso código mais organizado e isolado, vamos criar, dentro da pasta "templates", a pasta "galeria". Dentro dela, colocaremos o arquivo "index.html" que, até agora, estava na pasta "templates".

2. Ao voltarmos ao navegador e atualizarmos a página, nos depararemos com uma mensagem de erro que informa que o template "index.html" não existe. Isso acontece porque não informamos sua existência ao arquivo "galeria > migrations > view.py".

3. Vamos adicionar "galeria" ao retorno da função "index":

```python
from django.shortcuts import render

def index(request):
    return render(request, 'galeria/index.html')
```

4. Após essa alteração, se atualizarmos o navegador novamente, o código voltará a funcionar corretamente.

## Importando Estilos CSS

Agora vamos acessar o arquivo "index.html" do código disponibilizado na tarefa anterior. Com a ajuda de "Ctrl + A", vamos selecionar todo o código. Vamos copiá-lo, com "Ctrl + C", e voltar ao arquivo "templates/galeria > index.html".

5. Selecionaremos todo o código presente no arquivo "templates/galeria > index.html" com "Ctrl + A" e substituiremos pelo código que acabamos de copiar. Em seguida, salvaremos a alteração.

6. Ao voltar ao navegador e atualizar a página, veremos as informações do Alura Space em um HTML bem estruturado, mas ainda sem nenhum estilo.

## Instalando Arquivos Estáticos na Aplicação

No próximo vídeo, aprenderemos a instalar arquivos estáticos na aplicação para que possamos importar e utilizar os estilos CSS no nosso projeto.

Esperamos que essas etapas tenham sido claras e que você esteja animado(a) para continuar personalizando o visual do app "Alura Space".

# Carregando os Arquivos Estáticos da Aplicação

Agora vamos carregar os arquivos estáticos da aplicação. O caminho será similar ao dos arquivos HTML.

1. Na linha 61 de "setups > settings.py", informamos que há uma pasta onde manteremos todos os nossos códigos HTML. Faremos um processo semelhante, mas para indicar o caminho dos arquivos estáticos.

2. Vamos descer a página até chegarmos à linha 122, onde lemos `STATIC_URL = 'static/'`. Vamos informar a pasta que receberá esses arquivos, escrevendo, na linha 124, `STATICFILES_DIRS`, passando o caminho `os.path.join`, com os parâmetros `BASE_DIR, 'setup/static'`.

3. Precisamos passar também o caminho absoluto para que o diretório consiga pegar os arquivos estáticos. Para isso, vamos inserir a "raiz" dos caminhos com `STATIC_ROOT`, com o caminho `os.path.join(BASE_DIR, 'static')`:

```python
STATIC_URL = 'static/'

STATICFILES_DIRS = [
    os.path.join(BASE_DIR, 'setup/static')
]

STATIC_ROOT = os.path.join(BASE_DIR, 'static')
```

4. Na pasta "setup", criaremos uma pasta chamada "static". Agora criamos o diretório que servirá para a manipulação dos arquivos estáticos.

5. Vamos copiar, por isso, os arquivos das pastas "assets" e "styles" e levá-los para a pasta "setup > static".

6. No terminal, vamos executar `python manage.py runserver` para rodar o servidor.

7. De volta ao navegador, ao atualizarmos a página, nada mudará. Apesar disso, já temos os arquivos estáticos dentro da aplicação.

8. Agora vamos executar o comando `python manage.py collectstatic` para solicitar que o Django manipule os arquivos estáticos da aplicação, para que possamos visualizá-los.

9. Depois de executarmos o comando, perceberemos a criação de uma pasta chamada "static", relacionada ao `STATIC_ROOT` que criamos. Agora, já podemos usar os arquivos estáticos no Django. Se rodarmos o servidor outra vez, com `python manage.py runserver`, não vamos notar alterações no projeto.

10. Para realizar as alterações, vamos acessar "templates/galeria > index.html". Vamos adicionar o código `{% load static %}`, que solicita o carregamento dos arquivos estáticos, à primeira linha do arquivo.

11. Vamos carregar, inicialmente, o arquivo "style.css", cujo caminho é "static > styles > style.css". Na linha 13 do código, vamos adicionar `{% static '/styles/style.css' %}` após o `href`.

```html
<link rel="stylesheet" href="{% static '/styles/style.css' %}">
```

12. Ao atualizarmos o projeto no navegador, veremos que o estilo da aplicação começou a mudar.

No próximo vídeo, adicionaremos as imagens que estão faltando.

Esperamos que essas etapas tenham sido claras e que você esteja animado(a) para continuar personalizando o visual do app "Alura Space".

# Alura Space - Documentação para Adição de Arquivos Estáticos

Nesta documentação, explicaremos como adicionar arquivos estáticos ao projeto "Alura Space" utilizando a linguagem Django. Os arquivos estáticos incluem imagens, folhas de estilo CSS e scripts JavaScript que são carregados no navegador sem a necessidade de processamento do servidor. Vamos seguir os passos abaixo para adicionar os arquivos estáticos:

## Passo 1: Identificação dos Arquivos Estáticos

Antes de prosseguir, identifique todos os arquivos estáticos que deseja adicionar ao projeto. Neste exemplo, adicionaremos arquivos de imagens e folhas de estilo CSS.

## Passo 2: Configuração do Caminho para Arquivos Estáticos

Para informar ao Django onde estão localizados os arquivos estáticos, precisamos configurar o caminho no arquivo "settings.py".

1. Abra o arquivo "settings.py" localizado na pasta "setup".
2. Procure a seção `STATIC_URL` (linha 61).
3. Adicione a linha `STATICFILES_DIRS = [os.path.join(BASE_DIR, 'setup/static')]` (linha 124) para especificar o diretório onde os arquivos estáticos estão armazenados.

Exemplo:
```python
STATIC_URL = 'static/'

STATICFILES_DIRS = [
        os.path.join(BASE_DIR, 'setup/static')
]
```

## Passo 3: Adição dos Arquivos Estáticos no Template

Agora, podemos adicionar os arquivos estáticos aos nossos templates para que sejam renderizados no navegador.

1. Abra o arquivo "index.html" localizado na pasta "templates/galeria".
2. Adicione o código `{% load static %}` na primeira linha do arquivo para carregar os arquivos estáticos.
3. Em seguida, utilize a tag `{% static %}` para especificar o caminho para os arquivos estáticos.

Exemplo:
```html
{% load static %}
<!DOCTYPE html>
<html>
<head>
    <!-- Adicione outros metadados aqui -->
    <link rel="stylesheet" href="{% static '/styles/style.css' %}">
</head>
<body>
    <!-- Adicione o conteúdo do corpo aqui -->
    <img src="{% static '/assets/logo/Logo(2).png' %}" alt="Logo da Alura Space">
</body>
</html>
```

## Passo 4: Execução do Comando "collectstatic"

Após adicionar os arquivos estáticos, é necessário executar o comando `collectstatic` para que o Django possa manipulá-los corretamente.

1. Abra o terminal e navegue até a pasta raiz do projeto.
2. Execute o comando `python manage.py collectstatic`.

## Conclusão

Após seguir esses passos, os arquivos estáticos serão adicionados ao projeto "Alura Space" e serão exibidos corretamente no navegador. Repita o processo para adicionar outras imagens, folhas de estilo ou scripts JavaScript conforme necessário.

Agora você possui uma aplicação com visual mais atraente e dinâmico, tornando a experiência do usuário ainda mais agradável.

**Observação:** As linhas específicas de código podem variar de acordo com a estrutura e organização do seu projeto. Lembre-se de sempre adaptar os caminhos e nomes de arquivos conforme a sua configuração.

Esperamos que esta documentação tenha sido útil e que você tenha sucesso na adição de arquivos estáticos ao seu projeto Django!


# Alura Space - Documentação para Carregar Página "imagem.html"

Nesta documentação, explicaremos como carregar a página "imagem.html" na aplicação "Alura Space" utilizando a linguagem Django. A página "imagem.html" contém informações sobre uma imagem específica e será renderizada quando acessarmos a rota 'imagem/'.

## Passo 1: Criar o Arquivo "imagem.html"

1. Acesse a pasta "templates/galeria".
2. Crie um novo arquivo chamado "imagem.html".
3. Copie o conteúdo disponibilizado pelo instrutor ou insira o código HTML desejado para a página "imagem.html".

## Passo 2: Criar a Função "imagem" em "views.py"

1. Acesse o arquivo "views.py" localizado na pasta "galeria".
2. Adicione a função "imagem" que receberá o argumento "request" e retornará a renderização do template "imagem.html".

Exemplo:
```python
from django.shortcuts import render

def index(request):
    return render(request, 'galeria/index.html')

def imagem(request):
    return render(request, 'galeria/imagem.html')
```

## Passo 3: Configurar a Rota para "imagem.html"

1. Acesse o arquivo "urls.py" localizado na pasta "galeria".
2. Importe a função "imagem" para utilizá-la na rota.
3. Adicione uma nova rota com o caminho 'imagem/' que aponta para a função "imagem".

Exemplo:
```python
from django.urls import path
from galeria.views import index, imagem

urlpatterns = [
    path('', index),
    path('imagem/', imagem)
]
```

## Passo 4: Carregar os Arquivos Estáticos

Para garantir que os arquivos estáticos, como folhas de estilo CSS, sejam carregados corretamente na página "imagem.html", siga os passos descritos anteriormente na documentação sobre adição de arquivos estáticos.

## Conclusão

Após seguir esses passos, a página "imagem.html" estará configurada e será carregada corretamente quando acessarmos a rota 'imagem/'. Certifique-se de que os arquivos estáticos também estão carregados para garantir a correta exibição da página com o estilo adequado.

Agora você possui uma aplicação "Alura Space" com a funcionalidade de exibir informações detalhadas sobre uma imagem específica. Continue explorando e aprimorando sua aplicação!

**Observação:** Lembre-se de sempre adaptar os caminhos e nomes de arquivos conforme a sua configuração e estrutura do projeto. A documentação pode variar dependendo das versões do Django e da organização do código.