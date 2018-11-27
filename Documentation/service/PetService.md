# PetService
Classe com as regras de negócio relacionadas aos pets.

## Anotações
* [`@Service`](https://docs.spring.io/spring-framework/docs/current/javadoc-api/org/springframework/stereotype/Service.html): anotação do Spring para indicar que a classe é um serviço.

## Atributos
* `PetRepository petRepository`: instancia a variável de acesso ao repositório.

## Construtor
* `PetService(PetRepository petRepository)`: inicializa automaticamente a variável do repositório através da anotação  [`@Autowired`](https://docs.spring.io/spring-framework/docs/current/javadoc-api/org/springframework/beans/factory/annotation/Autowired.html).

## Métodos
* `Optional<Pet> findById(Long id)`: retorna um `Optional` de `Pet` com o id solicitado;
* `Page<Pet> findAll(Pageable pageable)`: retorna um `Pageable`de `Pet` com todos os pets do repositório;
* `Pet save(Pet pet)`: salva uma nova entidade de `Pet` ao repositório, e retorna a entidade salva.