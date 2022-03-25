### BABEL

Compilador
Transforma código novo em código antigo. Ex: const nome = 'Andre'; vira var nome = 'Andre';.

Browser Suporte
Para que um browser possa suportar algo novo de JavaScript é preciso que ele esteja atualizado, mas nem todo usuário possui a última versão do browser instalada.

Can I Use
O site <a href="https://caniuse.com/" target="_blank">https://caniuse.com/</a> mostra em quais browsers a novidade está disponível ou não.

### POLYFILL VS TRANSPILER

Polyfill
Cria métodos / funções com o mesmo nome das atuais, porém utilizando código antigo para permitir o uso em browsers que não possuem a API.

Transpiler
Transforma código novo em código antigo. Ou seja, transforma const em var.

### INSTALAR BABEL

<a href="https://babeljs.io/docs/en/usage" target="_blank">https://babeljs.io/docs/en/usage</a>

Instala o Babel, as configurações padrões e o loader para o Webpack

```shell
$ npm install --save-dev @babel/core @babel/preset-env @babel/plugin-transform-runtime babel-loader
```

### WEBPACK.CONFIG.JS

```shell
const path = require('path');

module.exports = {
  entry: './js/script.js',
  output: {
    path: path.resolve(__dirname, './'),
    filename: 'main.js',
  },
  module: {
    rules: [
      {
        test: /\.js$/,
        exclude: /node_modules/,
        use: {
          loader: 'babel-loader',
          options: {
            presets: ['@babel/preset-env'],
            plugins: ['@babel/plugin-transform-runtime'],
          },
        },
      },
    ],
  },
};
```

```shell
"scripts": {
  "dev": "webpack --mode development --watch",
  "build": "webpack --mode production"
},
```
