# Django API com Docker Compose

Este projeto implementa uma API RESTful desenvolvida com Django. O projeto utiliza dois ambientes separados configurados com Docker Compose: um para desenvolvimento (**dev**) e outro para produção (**prod**).

## Estrutura do Projeto

- **api_rest/**: Diretório contendo o código principal da API Django.
- **api_root/**: Diretório do projeto Django.
- **venv/**: Ambiente virtual Python (ignorado no repositório).
- **docker-compose-dev.yml**: Arquivo Docker Compose para o ambiente de desenvolvimento.
- **docker-compose-prod.yml**: Arquivo Docker Compose para o ambiente de produção.
- **Dockerfile**: Configuração para criar a imagem Docker da API.
- **requirements.txt**: Lista de dependências Python.

## Requisitos

- [Docker](https://www.docker.com/)
- [Docker Compose](https://docs.docker.com/compose/)
- Python 3.9+

## Configurações

### Docker Compose (Desenvolvimento)
O arquivo `docker-compose-dev.yml` utiliza imagens públicas do Docker Hub para a API e para o banco de dados PostgreSQL.

### Docker Compose (Produção)
O arquivo `docker-compose-prod.yml` utiliza a imagem personalizada `tobizinho100/api-rest:latest`, que é gerada a partir do `Dockerfile` deste projeto.

## Como Usar

Passo a Passo para Desenvolvimento

Certificar de ter o Docker e Docker Compose instalados.

Clonar o repositório:

`git clone https://github.com/Tobizinho100/Trabalho-Pratico-Docker.git`

Naveguar até o diretório do projeto:

`cd seu-repositorio`

Suba o ambiente de desenvolvimento:

`docker-compose -f docker-compose-dev.yml up --build`

A API estará disponível em `http://localhost:8000/api`

Derrubar os conteiners:
`docker-compose -f docker-compose-dev.yml down`


------------------------//------------------------------

Passo a Passo para Produção

Certifique-se de que a imagem da API foi publicada no Docker Hub:

`docker build -t tobizinho100/api-rest:latest`

Suba o ambiente de produção:

`docker-compose -f docker-compose-prod.yml up --build`

A API estará disponível em `http://localhost:8000/api`

Derrubar os conteiners:
`docker-compose -f docker-compose-prod.yml down`

------------------------//------------------------------

## Testes

Para rodar os testes do Django:

`docker-compose -f docker-compose-dev.yml run api python manage.py runserver`

ou

`docker-compose -f docker-compose-prod.yml run api python manage.py runserver`

## Autor

Desenvolvido por Duarte Menezes.

