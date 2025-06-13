# Descrição
Neste projeto foi utilizado o Docker Compose para executar uma aplicação HTML em um Container Apache. 
Você poderá ir além e fazer alterações mais robustas ao seu projeto, estilizando sua página e utilizando 
seus conhecimentos em (HTML, CSS e JS). Você também pode buscar outras formas para executar seu arquivo 
HTML em outras Linguagens de Programação.

### Passo a Passo

- Criar um arquivo YML com as definições de um servidor Apache (httpd); 
- Especificar no arquivo YML o local onde os arquivos da aplicação estarão.
- Subir o arquivo YML e a aplicação para um repositório no GitHub.

### Comandos utilizados

- Acesso ao GitHub para clonar repositório: ``` git clone ```
 
- Criando o diretório do projeto docker: ``` docker-projeto1-dio```

- Abrir o arquivo docker-projeto1-dio para fazer as configurações :``` nano compose.yml```
 ```

Dentro deste arquivo colocar as seguintes configurações:
version: "3.9",
services:
  apache:
  image:httpd:latest
  container_name: my-apache-app
  ports:
  - '8080:80'
  volumes:
  - ./website:/usr/local/apache2/htdocs

  ```


- Após o arquivo nano compose.yml configurado, criasse um diretório para armazenar o site.
- OBS: Criar o novo  ``` mkdir website``` Dentro do diretório docker-projeto1-dio
- Dentro do diretório website criar o arquivo ``` nano index.html``` OBS: O apache só vai considerar os arquivos de HTML, CSS e JavaScript
- Para salvar o arquivo ``` ctrl + O``` depois tecle Enter, e para sair do nano digite ```ctrl x```
- Feche o arquivo ``` nano index.html```
- Instale o docker compose ``` apt install docker-compose```
- Após o docker compose instalado é preciso gerar o arquivo ``` docker-compose up -d```
- Para saber se o container foi iniciado ``` docker container ls```

### Subindo o projeto para o GitHub
```
git init
git remote add origin https://github.com/seu-usuario/docker-apache-html.git
git add .
git commit -m "Projeto HTML com Apache via Docker Compose"
git branch -M main
git push -u origin main
```
  
