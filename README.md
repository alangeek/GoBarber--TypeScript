<h1 align="center">
  <img alt="GoBarber" title="gobarber" src="github/logo.svg" width="200px" />
</h1>

<h3 align="center">
  GoBarber: back-end, front-end web e mobile
</h3>



<h3 align="center">
  <a href="https://insomnia.rest/run/?label=GoBarber&uri=https%3A%2F%2Fraw.githubusercontent.com%2Fhugo-marcelo%2Fgobarber-ts%2Fmaster%2Fbackend%2FInsomnia.json" target="_blank"><img src="https://insomnia.rest/images/run.svg" alt="Run in Insomnia"></a>
</h3>

## :gear: Back-end

### :information_source: Deploy

- https://gobarber-ts-api.herokuapp.com

### :information_source: Instruções Back-end

#### :whale: Executando com Docker Compose

```bash
# instalar os contâineres da API, PostgreSQL, MongoDB e Redis
docker-compose up -d
```

#### :whale: Executando com Docker localmente

```bash
# instalar PostgreSQL - Banco de dados principal
docker run --name gobarber -e POSTGRES_PASSWORD=docker -p 5432:5432 -d postgres

# instalar MongoDB - Banco de dados para notificações
docker run --name mongodb -p 27017:27017 -d -t mongo

# instalar Redis - Banco de dados para filas
docker run --name redis -p 6379:6379 -d -t redis:alpine

# instalar os pacotes e dependências
yarn
```

---

#### Executando back-end

```bash

# criar estrutura do banco de dados Postgres
yarn typeorm migration:run

# iniciar servidor da aplicação
yarn dev:server

```

---

## :computer: Front-end

### :information_source: Deploy

- https://gobarber-ts-web.herokuapp.com

### :information_source: Instruções Front-end

```bash
#instalar os pacotes e dependências
yarn

# iniciar a aplicação web
yarn start
```

---

## :iphone: Mobile

### :information_source: Instruções Mobile (iOS)

```bash
#instalar os pacotes e dependências
yarn

# iniciar o aplicativo no emulador do iOS
yarn ios
```

### :information_source: Instruções Mobile (Android)

```bash
#instalar os pacotes e dependências
yarn
```

Alterar a variável baseURL em `/src/services/api.js` colocando o ip local ou do emulador

```bash
# inicializar o aplicativo no emulador do Android
yarn android
```

---

## :memo: Licença

Esse projeto está sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.

---

## :clap: Obrigado

[Rocketseat](https://rocketseat.com.br/) pelo bootcamp!
