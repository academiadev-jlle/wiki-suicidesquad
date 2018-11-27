# UsuarioService
Classe com as regras de negócio relacionadas aos usuários.

## Anotações
* [`@Repository`](https://docs.spring.io/spring-framework/docs/current/javadoc-api/org/springframework/stereotype/Service.html): anotação do Spring para indicar que a classe é um serviço.

## Atributos
* `UsuarioRepository usuarioRepository`: declara a variável de acesso ao repositório.

## Construtor
* `UsuarioService(UsuarioRepository usuarioRepository)`: inicializa automaticamente a variável do repositório através da anotação  [`@Autowired`](https://docs.spring.io/spring-framework/docs/current/javadoc-api/org/springframework/beans/factory/annotation/Autowired.html).

## Métodos
* `Optional<Usuario> findById(Long id)`: retorna um `Optional` de `Usuario` com o id solicitado;
* `Page<Usuario> findAll(Pageable pageable)`: retorna um `Pageable`de `Usuario` com todos os usuários do repositório;
* `Usuario save(Usuario usuario)`: salva uma nova entidade de `Usuario` ao repositório, e retorna a entidade salva;
* `Optional<Usuario> findByFacebookUserId(string facebookUserId)`: retorna um `Optional` de `Usuario` com o id do facebook solicitado; retorna um optional vazio no caso de `facebookUserId` ser `null`.