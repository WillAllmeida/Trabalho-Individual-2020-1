# Teste

## Critérios de avaliação

### 1. Containerização

A aplicação foi containerizada utilizando Docker e Docker Compose, contendo um arquivo principal docker-compose.yml contendo as instruções dos serviços e dois arquivos Dockerfile (Na pasta client e na api), para instruções específicas de instalação de pacotes.

O comando para subir o ambiente é:

    $ docker-compose up --build


### 2. Integração contínua

A ferramenta principal escolhida para a integração contínua foi o TravisCI, contendo o script para build tanto da API quanto do Client e de seus respectivos testes.

A coleta de métricas de qualidade foi feita utilizando o CodeClimate, e o mesmo tornou-se um dos critérios para alguma branch ser mergada na master.

Badge com o nível de manutenibilidade mensurado pela ferramenta
[![Maintainability](https://api.codeclimate.com/v1/badges/87d3e9ee6d535eb5d8bf/maintainability)](https://codeclimate.com/github/WillAllmeida/Trabalho-Individual-2020-1/maintainability)

De acordo com a submissão de pull requests, são verificadas as condições de passar na pipeline de build/testes do TravisCI e se o código não possui novos bad smells de acordo com o CodeClimate.
