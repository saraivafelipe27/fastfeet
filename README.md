
<h1 align="center">
  <img alt="Fastfeet" title="Fastfeet" src="https://github.com/Rocketseat/bootcamp-gostack-desafio-03/blob/master/.github/logo.png" width="300px" />
</h1>

<h3 align="center">
Esse desafio faz parte do Desafio Final, que é uma aplicação completa (Back-end, Front-end e Mobile) que é avaliada para emissão do Certificado do Bootcamp GoStack.
</3>

<h1 align="center">
<img src="https://github.com/saraivafelipe27/fastfeet/blob/master/img/image1.jpg" width="70%" heigth="70%" />
</h1>
<h3 align="center">
<img src="https://github.com/saraivafelipe27/fastfeet/blob/master/img/mobile.jpg" width="70%" heigth="70%" />
</h3>

---

## :fire: Iniciando a aplicação :fire:

### :pencil: Requerimentos

_Para rodar a aplicação é necessário que você possua esses três programas:_
* [Git](https://git-scm.com)
* [Node](https://nodejs.org/)
* [Yarn](https://yarnpkg.com/)


### Também foram utilizados três bancos de dados da aplicação
- [Postgres](https://github.com/postgres/postgres)
- [MongoDB](https://www.mongodb.com/)
- [Redis](https://redis.io/)

### Porém, para facilitar, usamos o [Docker](https://www.docker.com/) para rodar os bancos de dados facilmente. Dentro dele siga estes passos:

```bash
# Instale uma imagem do Redis
docker run --name redisfastfeet -p 6379:6379 -d -t redis:alpine

# Instale uma imagem do Postgres
docker run --name fastfeet -e POSTGRES_PASSWORD=fastfeet -p 5432:5432 -d postgres
(Neste caso, seu login e senha será: fastfeet)

# Inicie o Redis
docker start redisfastfeet

# Inicie o Postgres
docker start fastfeet

```
### :open_file_folder: Iniciando o Backend
Agora clone este repositório e instale suas dependências
```bash
# clonando o repositório
git clone https://github.com/saraivafelipe27/fastfeet

# entrando na pasta do backend
cd backend

#instalando as dependências
yarn

```
Para que haja a conexão do backend com o banco de dados, você precisará colocar suas informações no arquivo .env, baseado no .env.example que está dentro do backend. Após isto, no terminal é necessário enviar as migrations para o banco de dados:

```bash
# rodando as migrations para o banco
yarn sequelize db:migrate

# permitindo que haja o administrador no banco
yarn sequelize db:seed:all

# iniciando a aplicação
yarn dev & yarn queue
```

Após estes passos, você poderá iniciar o frontend ou o mobile!

---

### :computer: Frontend do Fastfeet

_Abra um terminal na pasta do frontend e digite:_
```bash
yarn
yarn start
```
_Use estes dados para realizar login na aplicação:_
<blockquote><strong>Email:</strong> admin@fastfeet.com</blockquote>
<blockquote> <strong>Senha:</strong> 123456</blockquote>

___

### :computer: Mobile do Fastfeet

_Esta aplicação foi desenvolvida usando o Expo. [Clique aqui](https://expo.io/learn) para conhecê-lo!_
```bash
# para instalar as dependências
cd mobile
yarn
```
[LinkedIn](https://www.linkedin.com/in/saraivafelipe27/)
_Após isto, você precisa mudar para o ip de sua máquina neste arquivo:_
[api.js](https://github.com/saraivafelipe27/fastfeet/blob/master/mobile/src/services/api.js)
```javascript
  baseURL: 'http://192.168.0.14:3334',
```

_Substitua 192.168.0.14 com o ip de sua máquina._
_Se você quiser usar o Reactotron mude o ip neste arquivo também:_
[ReactotronConfig](https://github.com/saraivafelipe27/fastfeet/blob/master/mobile/src/config/ReactotronConfig.js)
```javascript
  .configure({ host: '192.168.0.14' })
```

_Agora basta rodar a aplicação._
```bash

# para rodar a aplicação
yarn start

___
```
[LinkedIn](https://www.linkedin.com/in/saraivafelipe27/)