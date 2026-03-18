# Projeto Backend - API RESTful

API RESTful para gerenciamento de uma aplicação de e-commerce, contemplando operações completas de autenticação, usuários, categorias e produtos.

## Tecnologias

- Node.js
- Express
- Sequelize (ORM)
- MySQL (ou outro banco compatível)
- JWT (autenticação)
- Bcrypt (hash de senhas)
- Dotenv
- Nodemon (dev)

## Arquitetura

O projeto segue uma arquitetura em camadas:

```
src/
├── config/        # Configurações (ex: banco de dados)
├── controllers/   # Camada de controle (requisição/resposta)
├── services/      # Regras de negócio
├── models/        # Modelos do banco (Sequelize)
├── routes/        # Definição das rotas
├── middleware/    # Middlewares (auth, etc.)
├── database/      # Inicialização do banco
├── app.js         # Configuração do app Express
└── server.js      # Inicialização do servidor
```

## Funcionalidades

- Autenticação com JWT
- CRUD de Usuários
- CRUD de Categorias
- CRUD de Produtos
- Relacionamento entre entidades (produtos, imagens, opções)
- Proteção de rotas com middleware de autenticação

## Instalação

```bash
# Clone o repositório
git clone https://github.com/SrGustavoMC/Projeto_Backend.git

# Acesse o diretório
cd Projeto_Backend/project-root

# Instale as dependências
npm install
```

## Configuração

Crie um arquivo `.env` na raiz com base no exemplo:

```
DB_HOST=
DB_USER=
DB_PASS=
DB_NAME=
JWT_SECRET=
PORT=
```

## Execução

```bash
# Desenvolvimento
npm run dev

# Produção
npm start
```

## Endpoints

### Autenticação
- `POST /auth/login`

### Usuários
- `GET /users`
- `POST /users`
- `PUT /users/:id`
- `DELETE /users/:id`

### Categorias
- `GET /categories`
- `POST /categories`
- `PUT /categories/:id`
- `DELETE /categories/:id`

### Produtos
- `GET /products`
- `POST /products`
- `PUT /products/:id`
- `DELETE /products/:id`

## Testes

```bash
npm test
```

Arquivos de teste disponíveis em:

```
tests/
├── category.test.js
├── product.test.js
└── user.test.js
```

## Segurança

- Senhas armazenadas com hash (bcrypt)
- Autenticação baseada em token (JWT)
- Middleware para proteção de rotas privadas

## Considerações

- Projeto estruturado para escalabilidade e manutenção
- Separação clara de responsabilidades (Controller, Service, Model)
- Pronto para integração com frontend ou consumo via API externa
