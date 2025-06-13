# Projeto: Aplicação HTML com Apache via Docker Compose

## Descrição
Este projeto utiliza o Docker Compose para executar uma aplicação HTML dentro de um container Apache (httpd). 
Você pode personalizar sua página com HTML, CSS e JavaScript, além de explorar formas alternativas de executar 
aplicações web com outras linguagens de programação.

### Passo a Passo

- Criar um arquivo ```docker-compose.yml``` com a definição do container Apache.
- Especificar no arquivo o caminho local dos arquivos da aplicação.
- Subir o projeto para um repositório no GitHub

  ### Estrutura do projeto
  
- docker-projeto1-dio/
- ├── docker-compose.yml
- └── website/
- └── index.html


# docker-compose.yml (exemplo)

```
version: "3.9"

services:
  apache:
    image: httpd:latest
    container_name: my-apache-app
    ports:
      - "8080:80"
    volumes:
      - ./website:/usr/local/apache2/htdocs
```


### 💡 Dica: O Apache servirá apenas arquivos HTML, CSS e JS colocados dentro do diretório website.


### Criando a estrutura do projeto

```
# Clonando repositório (se já existir)
git clone https://github.com/seu-usuario/docker-apache-html.git

# Criar diretório do projeto
mkdir docker-projeto1-dio && cd docker-projeto1-dio

# Criar arquivo docker-compose.yml
nano docker-compose.yml

# Criar diretório da aplicação
mkdir website && cd website

# Criar o arquivo HTML da aplicação
nano index.html
```

# Comandos adicionais

```
# Salvar arquivo no nano
Ctrl + O, Enter

# Sair do nano
Ctrl + X

# Instalar o Docker Compose (caso necessário)
sudo apt install docker-compose

# Subir o container
docker-compose up -d

# Verificar se o container está rodando
docker ps
```

# Subindo o projeto para o GitHub

```
git init
git remote add origin https://github.com/seu-usuario/docker-apache-html.git
git add .
git commit -m "Projeto HTML com Apache via Docker Compose"
git branch -M main
git push -u origin main
```
