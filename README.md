# Projeto DSCatalog - Curso Java Spring Expert

Projeto desenvolvido no decorrer do curso Java Spring Expert.

## Modelo Conceitual
![dscatalog-modelo-conceitual](https://github.com/user-attachments/assets/12deec2b-f3ef-4a86-ab30-3e96c1d0b016)

## Tecnologias utilizadas:
- Spring Boot
- Banco de dados H2
- Banco de dados PostgreSQL
- Jakarta Bean Validation
- JPA/Hibernate
- Spring Security
- OAuth2
- JUnit
- TDD
- Mockito
- MockMvc

## Enpoints:

1. **Gerenciamento de Usuário**:
   - `GET /users`: Permite listar todos os usuários, com dados paginados.
   - `GET /users/{id}`: Permite listar os dados de um usuário.
   - `GET /users/me`: Permite listar os dados do usuário autenticado.
   - `POST /users`: Permite criar um novo usuário.
   - `PUT users/{id}`: Permite atualizar um usuário existente.
   - `DELETE users/{id}`: Permite deletar um usuário.
     
2. **Autenticação**:
   - `POST /oauth2/token`: Permite permite a obtenção de um token  para a autenticação do usuário.
   - `POST /auth/recover-token`: Permite gerar um token para a recuperação da senha informando um email.
   - `PUT /auth/new-password`: Permite cadastrar uma nova senha informando o token gerado no endpoint de recuperação de senha e a nova senha.   

3. **Gerenciamento de categorias**:
   - `GET /categories`: Permite listar todas as categorias de produtos não paginadas.
   - `GET /categories/{id}`: Permite buscar uma categoria por id.
   - `POST /categories`: Permite criar uma nova categoria.
   - `PUT /categories/{id}`: Permite atualizar uma categoria existente.
   - `DELETE /categories/{id}`: Permite deletar uma categoria existente. 

4. **Gerenciamento de produtos**:
   - `GET /products?page=0&size=10&name=gamer&categoryId=1,3&sort=name,desc`: Permite listar todas os produtos paginados, havendo um filtro de produtos por nome ou categorias de produtos pelos ids de categorias. 
   - `GET /products{id}`: Permite listar um produto por id.  
   - `POST /products`: Permite criar um novo produto.
   - `PUT /products/{id}`: Permite atualizar um produto existente.
   - `DELETE /products/{id}`: Permite deletar um produto existente.
