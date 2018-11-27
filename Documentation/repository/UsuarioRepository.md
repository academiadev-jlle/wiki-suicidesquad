# UsuarioRepository
Interface para acesso aos dados dos Usuarios. Estende `JpaRepository`.

## Anotações
* [`@Repository`](https://docs.spring.io/spring-framework/docs/current/javadoc-api/org/springframework/stereotype/Repository.html): anotação do Spring para indicar que a classe é um repositório.

## Métodos Abstratos
* `Optional<Usuario> findByEmail(String email)`: busca, no repositório, usuários com o email especificado. Retorna um `Optional` de `Usuario`;
* `Optional<Usuario> findByFacebookUserId(String facebookUserId)`: busca, no repositório, usuários com o id especificado. Retorna um `Optional`de `Usuario`.