# Projeto Sequelize

Projeto Sequelize é um projeto de exemplo que demonstra o uso do [Sequelize](https://sequelize.org/), um ORM baseado em Promises para Node.js compatível com Postgres, MySQL, MariaDB, SQLite e Microsoft SQL Server. Este repositório contém uma configuração simples para aprendizado e experimentação com o Sequelize, incluindo operações CRUD, definição de modelos e migrações de banco de dados.

## Funcionalidades

- Configuração do ORM Sequelize com Node.js
- Exemplos de modelos e migrações
- Operações CRUD (Create, Read, Update, Delete)
- Configuração de conexão com banco de dados
- Scripts de exemplo para interação com o banco

## Começando

### Pré-requisitos

- [Node.js](https://nodejs.org/) (recomendado v14 ou superior)
- [npm](https://www.npmjs.com/) ou [yarn](https://yarnpkg.com/)
- Um banco de dados relacional (Postgres, MySQL, SQLite, etc.)

### Instalação

1. Clone este repositório:

   ```bash
   git clone https://github.com/bia-cabral/ProjetoSequelize.git
   cd ProjetoSequelize
   ```

2. Instale as dependências:

   ```bash
   npm install
   # ou
   yarn install
   ```

3. Configure a conexão com seu banco de dados na pasta `config` (veja `config/config.json` ou `.env`, se utilizado).

### Uso

- Execute as migrações para criar as tabelas no banco de dados:

  ```bash
  npx sequelize db:migrate
  ```

- Popule o banco com dados iniciais (opcional):

  ```bash
  npx sequelize db:seed:all
  ```

- Inicie a aplicação (depende da sua configuração, por exemplo, um servidor Express):

  ```bash
  npm start
  ```

### Estrutura do Projeto

```
├── config/
│   └── config.json         # Configurações do banco de dados
├── models/
│   └── *.js                # Modelos Sequelize
├── migrations/
│   └── *.js                # Arquivos de migração
├── seeders/
│   └── *.js                # Arquivos de seed
├── index.js                # Ponto de entrada principal
└── README.md
```

### Exemplo de Modelo Sequelize

```js
// models/user.js
module.exports = (sequelize, DataTypes) => {
  const User = sequelize.define('User', {
    name: DataTypes.STRING,
    email: DataTypes.STRING
  });
  return User;
};
```

## Contribuição

Contribuições são bem-vindas! Sinta-se à vontade para abrir uma issue ou enviar um pull request.

## Licença

Este projeto está licenciado sob a licença MIT.

## Contato

Criado por [bia-cabral](https://github.com/bia-cabral) — fique à vontade para entrar em contato!
