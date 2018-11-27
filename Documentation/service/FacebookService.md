# FacebookService
Classe com regras de negócio relacionadas à autenticação via Facebook.

## Anotações
*[`@Service`](https://docs.spring.io/spring-framework/docs/current/javadoc-api/org/springframework/stereotype/Service.html): anotação do Spring para indicar que a classe é um serviço.

## Atributos
* `String appId`: inicializado com o valor passado para a anotação [`@Value`](), que corresponde ao id da aplicação fornecido pela API do Facebook;
* `String appSecret`: inicializado com o valor passado para a anotação [`@Value`](), que corresponde à chave da aplicação fornecido pela API do Facebook;
* `String backendRedirectUri`: inicializado com o valor passado para a anotação [`@Value`](), que corresponde ao endereço da aplicação armazenado pela API do Facebook.

## Métodos
* `String createAthorizationURL()`: TODO
* `Optional<String> getAccessToken(String code)`: TODO
* `Optional<User> getUser(String accessToken)`: TODO