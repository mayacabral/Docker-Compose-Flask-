# Docker Compose Flask 

Este projeto demonstra como criar e executar uma aplicação Flask com banco de dados MySQL usando Docker Compose. A aplicação consome uma API externa (Random User) e armazena dados no MySQL.

## Funcionalidades

- **API Flask**: Servidor web em Python com Flask
- **Banco de Dados**: MySQL para persistência de dados
- **Integração**: Consumo de API externa e inserção no banco
- **Docker**: Containerização completa da aplicação

## Pré-requisitos

- Docker
- Docker Compose

## Como Executar

1. **Clone o repositório**:
   ```bash
   git clone https://github.com/seu-usuario/docker-compose-flask.git
   cd docker-compose-flask
   ```

2. **Construa as imagens**:
   ```bash
   docker-compose build
   ```

3. **Execute os containers**:
   ```bash
   docker-compose up -d
   ```

4. **Acesse a aplicação**:
   - API: http://localhost:5000
   - MySQL: localhost:3306

## Endpoints da API

### GET /
Retorna dados aleatórios de usuário da API Random User.

### POST /inserthost
Insere um nome de usuário aleatório no banco de dados MySQL e retorna o nome inserido.

## Estrutura do Projeto

```
docker-compose-flask/
├── docker-compose.yml    # Configuração do Docker Compose
├── config/
│   └── db.env           # Variáveis de ambiente do MySQL
├── flask/
│   ├── Dockerfile       # Dockerfile da aplicação Flask
│   ├── app.py          # Código da aplicação Flask
│   └── requirements.txt # Dependências (não presente, mas pode ser criado)
└── mysql/
    ├── Dockerfile      # Dockerfile do MySQL customizado
    └── schema.sql      # Script de criação do banco
```

## Comandos Úteis

- **Parar os containers**:
  ```bash
  docker-compose down
  ```

- **Ver logs**:
  ```bash
  docker-compose logs -f
  ```

- **Acessar o container do MySQL**:
  ```bash
  docker-compose exec db mysql -u root flaskdocker
  ```

## Tecnologias Utilizadas

- **Flask**: Framework web Python
- **MySQL**: Banco de dados relacional
- **Docker**: Containerização
- **Docker Compose**: Orquestração de containers
- **Requests**: Biblioteca para chamadas HTTP

## Contribuição

1. Fork o projeto
2. Crie uma branch para sua feature (`git checkout -b feature/nova-feature`)
3. Commit suas mudanças (`git commit -am 'Adiciona nova feature'`)
4. Push para a branch (`git push origin feature/nova-feature`)
5. Abra um Pull Request

## Licença

Este projeto é distribuído sob a licença MIT. Veja o arquivo LICENSE para mais detalhes.
