# CustomUserDetailsService
Classe que implementa a interface [`UserDetailsService`](https://docs.spring.io/spring-security/site/docs/4.2.6.RELEASE/apidocs/org/springframework/security/core/userdetails/UserDetailsService.html) do spring.

## Anotações
* [`@Component`](https://docs.spring.io/spring-framework/docs/current/javadoc-api/org/springframework/stereotype/Component.html): anotação do Spring para indicar que a classe é um componente elegível para detecção automática/injeção.

## Atributos
* `UsuarioRepository usuarioRepository`: declara a variável de acesso ao repositório.

## Construtor
* `CustomUserDetailsService(UsuarioRepository usuarioRepository)`: inicializa a variável do repositório para o repositório `usuarioRepository` informado.

## Métodos
* `UserDetails loadUserByUsername(String username)`: retorna um `UserDetails` com o username (de fato, com o email) solicitado. Lana uma exceção `UsernameNotFoundException` caso o usuário não seja encontrado.