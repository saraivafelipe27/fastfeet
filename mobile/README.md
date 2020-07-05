<h1 align="center">
<img src="https://raw.githubusercontent.com/Rocketseat/bootcamp-gostack-desafio-03/master/.github/logo.png">
</h1>

### Aplicativo mobile do Fastfeet

_Esta aplicação foi desenvolvida usando o Expo. [Clique aqui](https://expo.io/learn) para conhecê-lo!_
```bash
# para instalar as dependências
cd mobile
yarn
```

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


