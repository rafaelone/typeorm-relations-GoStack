# Desafio 09: Relacionamentos com banco de dados no Node.js

Nesse desafio, foi proposto criar uma nova aplicação para fixar os conhecimentos sobre o que foi visto até agora no BootCamp GoStack da RocketSeat utilizando Node.js junto ao TypeScript e incluindo o uso de banco de dados com o TypeORM e relacionamentos ManyToMany

## Rotas da aplicação

- **POST /customers:** A rota deve receber name e email dentro do corpo da requisição, sendo o name o nome do cliente a ser cadastrado. Ao cadastrar um novo cliente, ele deve ser armazenado dentro do seu banco de dados e deve ser retornado o cliente criado. Ao cadastrar no banco de dados, na tabela customers ele deverá possuir os campos possuindo os campos name, email, created_at, updated_at.

- **POST /products:** Essa rota deve receber name, price e quantity dentro do corpo da requisição, sendo o name o nome do produto a ser cadastrado, price o valor unitário e quantity a quantidade existente em estoque do produto. Com esses dados devem ser criados no banco de dados um novo produto com os seguitnes campos: name, price, quantity, created_at, updated_at.

- **POST /orders/:** Nessa rota você deve receber no corpo da requisição o customer_id e um array de products, contendo o id e a quantity que você deseja adicionar a um novo pedido. Aqui você deve cadastrar na tabela order um novo pedido, que estará relacionado ao customer_id informado, created_at e updated_at . Já na tabela orders_products, você deve armazenar o product_id, order_id, price e quantity, created_at e updated_at.

- **GET /orders/:id:** Essa rota deve retornar as informações de um pedido específico, com todas as informações que podem ser recuperadas através dos relacionamentos entre a tabela orders, customers e orders_products.
