# Desafio 02. Iniciando aplicação

Crie uma aplicação do zero utilizando Express.

Nessa aplicação configure as seguintes ferramentas:

- Sucrase + Nodemon;
- ESLint + Prettier + EditorConfig;
- Sequelize (Utilize PostgresSQL ou MySQL);

Durante esse desafio você dará início a um novo projeto no Bootcamp, esse projeto será desenvolvido aos poucos até o fim da sua jornada onde você terá uma aplicação completa envolvendo back-end, front-end e mobile.

Esse projeto também será utilizado para a certificação do bootcamp, então bora pro código!

## Aplicação

A aplicação que iremos dar início ao desenvolvimento a partir de agora é um app agregador de eventos para desenvolvedores chamado Meetapp (um acrônimo à Meetup + App).

Nesse primeiro desafio vamos criar algumas funcionalidades básicas que aprendemos ao longo das aulas até aqui.

## Funcionalidades

Abaixo estão descritas as funcionalidades que você deve adicionar em sua aplicação.

### Autenticação

Permita que um usuário se autentique em sua aplicação utilizando e-mail e senha.

- A autenticação deve ser feita utilizando JWT.
- Realize a validação dos dados de entrada;

### Cadastro e atualização de usuários

Permita que novos usuários se cadastrem em sua aplicação utilizando nome, e-mail e senha.

Para atualizar a senha, o usuário deve também enviar um campo de confirmação com a mesma senha.

- Criptografe a senha do usuário para segurança.
- Realize a validação dos dados de entrada;

## Entrega

Esse desafio **não precisa ser entregue** e não receberá correção, mas você pode ver o resultado do código do desafio aqui: https://github.com/Rocketseat/bootcamp-gostack-desafio-02

Após concluir o desafio, adicionar esse código ao seu Github é uma boa forma de demonstrar seus conhecimentos para oportunidades futuras.

“Não espere para plantar, apenas tenha paciência para colher”!

## Resolução

### Configurando ambiente
``$ yarn add express`` <br>
``$ yarn add nodemon -D`` <br>
``$ yarn add sucrase nodemon -D`` <br>
``$ yarn add eslint -D`` <br>
``$ yarn add prettier eslint-config-prettier eslint-plugin-prettier -D`` <br>
``$ yarn eslint --init`` <br>
``$ yarn eslint --fix src --ext .js`` <br>

Configurar [.eslintrc.js](.eslintrc.js) <br>
Criar [.prettierrc](.prettierrc) <br>
Criar [.editorconfig](.editorconfig) <br>

### Sequelize
``$ yarn add sequelize`` <br>
``$ yarn add sequelize-cli -D`` <br>
``$ yarn add pg pg-hstore`` <br>

Criar [.sequelizerc](.sequelizerc)

#### Utilizando Sequelize

##### Criar migration
``$ yarn sequelize migration:create=create-users`` (Migration de criação da tabela users)
##### Executar migrations
``$ yarn sequelize db:migrate``
##### Desfazer migrations
``$ yarn sequelize db:migrate:undo`` (Desfaz a última migration) <br>
``$ yarn sequelize db:migrate:undo:all`` (Desfaz todas as migrations)

### Adicionais
``$ yarn add bcryptjs`` <br>
``$ yarn add jsonwebtoken`` <br>

Schema validation: <br>
``$ yarn add yup`` <br>

Código fonte da resolução do desafio se encontra na pasta [src](/src).
