<p align="center">
  <a href="http://nestjs.com/" target="blank"><img src="https://nestjs.com/img/logo_text.svg" width="320" alt="Nest Logo" /></a>
</p>

[circleci-image]: https://img.shields.io/circleci/build/github/nestjs/nest/master?token=abc123def456
[circleci-url]: https://circleci.com/gh/nestjs/nest

## Description

[Nest](https://github.com/nestjs/nest) framework TypeScript starter repository.

## Installation

```bash
$ npm install
```

## Running the app

```bash
# development
$ npm run start

# watch mode
$ npm run start:dev

# production mode
$ npm run start:prod
```

## Test

```bash
# unit tests
$ npm run test

# e2e tests
$ npm run test:e2e

# test coverage
$ npm run test:cov
```

## anotation

npx @nestjs/cli new <nome do projeto>

dando permissões para o script .sh:
$ chmod +x .\docker\entrypoint.sh

removendo as pastas para testar se o docker gera automatico:
$ rm -rf node_modules dist

rodar o docker-compose:
$ docker-compose up --build

add tsconfig.json:
"include": ["src"],
"exclude": [
"node_modules",
"dist",
".docker"
]

instalando o typeORM no container do projeto
$ docker-compose exec app bash
$ npm install typeORM @nestjs/typeorm --save
$ npm install pg --save
$ npm install @nestjs/config --save

add no package.json a config do typeorm:
$ "typeorm": "ts-node ./node_modules/typeorm/cli.js"

criado migrations:
npm run typeorm entity:create -- -n product

## Support

Nest is an MIT-licensed open source project. It can grow thanks to the sponsors and support by the amazing backers. If you'd like to join them, please [read more here](https://docs.nestjs.com/support).

## Stay in touch

- Author - [Kamil Myśliwiec](https://kamilmysliwiec.com)
- Website - [https://nestjs.com](https://nestjs.com/)
- Twitter - [@nestframework](https://twitter.com/nestframework)

## Tutorials

- https://www.youtube.com/watch?v=qE0jRojtx08&ab_channel=FullCycle
