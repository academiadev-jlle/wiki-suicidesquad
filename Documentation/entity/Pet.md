# Pet Entity
Entidade de pet que estende `AuditableEntity`. Define a estruturação dos objetos Pet e mapeamento para a database.

## Anotações
* [`@Data`](https://projectlombok.org/features/Data): geração automática de getters, setters e construtores;
* [`@EqualsAndHashCode`](https://projectlombok.org/features/EqualsAndHashCode): implementa os métodos `equals` e `hashcode` para a classe;
* [`@AllArgsConstructor`](https://projectlombok.org/features/constructor): cria construtor com todos os campos;
* [`@NoArgsConstructor`](https://projectlombok.org/features/constructor): cria construtor vazio;
* [`@Builder`](https://projectlombok.org/features/Builder): cria um método `build()`, que permite acesso a uma classe `PetBuilder`. Essa classe possui um método para cada atributo, que faz a atribuição e retorna o próprio `PetBuilder`. Possui também um método `build()`, que retorna a entidade original construída;
* [`@Entity`](https://javaee.github.io/javaee-spec/javadocs/javax/persistence/Entity.html): especifica a classe como sendo uma entidade de persistência na database;
* [`@Table`](https://javaee.github.io/javaee-spec/javadocs/javax/persistence/Table.html): especifica a tabela da database onde será persistida esta entidade;
* [`@JsonIgnoreProperties`](https://fasterxml.github.io/jackson-annotations/javadoc/2.6/com/fasterxml/jackson/annotation/JsonIgnoreProperties.html): suprime serialização de propriedades do json que contém as propriedades desta classe.

## Atributos
* Enums:
  * `Tipo tipo`: espécie do pet;
  * `Porte porte`;
  * `Raça raça`;
  * `ComprimentoPelo comprimentoPelo`;
  * `SexoPet sexo`;
  * `Categoria categoria`situação do Pet, entre *perdido*, *achado* ou *para adoção*;
  * `Vacinacao vacinacao`;
  * `Castracao castracao`;
* `Localizacao localizacao`: localização do pet;
* `Set<Cor> cores`: conjunto de cores do pet;
* `List<Registro> registros`: histórico de alterações do status do pet;
* `String nome`: nome do pet (2 a 80 caracteres);
* `String descricao`: descricao da situação do pet (máximo de 255 caracteres);
* `Usuario usuario`: usuário que realizou a postagem do anúncio.

## Métodos
* `void addCor(Cor cor)`: inclui nova cor ao atributo `Set<Cor> cores`;
* `void addRegistro(Registro registro)`: inclui nova alteração do status do pet ao histórico;
* `void setRegistros(List<Registro> registros`: inclui lista de atualizações ao histórico do pet.