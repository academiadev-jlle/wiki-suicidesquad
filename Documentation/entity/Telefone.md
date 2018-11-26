# Telefone Entity
Entidade de pet que estende `BaseEntity`. Objeto que contém os dados de contato para o anúncio do pet.

## Anotações
* [`@Data`](https://projectlombok.org/features/Data): geração automática de getters, setters e construtores;
* [`@EqualsAndHashCode`](https://projectlombok.org/features/EqualsAndHashCode): implementa os métodos `equals` e `hashcode` para a classe;
* [`@NoArgsConstructor`](https://projectlombok.org/features/constructor): cria construtor vazio;
* [`@Entity`](https://javaee.github.io/javaee-spec/javadocs/javax/persistence/Entity.html): especifica a classe como sendo uma entidade de persistência na database;
* [`@Table`](https://javaee.github.io/javaee-spec/javadocs/javax/persistence/Table.html): especifica a tabela da database onde será persistida esta entidade.

## Atributos
* `Usuario usuario`: usuario que postou do anúncio;
* `String numero`: número do telefone de contato;
* `boolean isWhatsapp`: atributo de verificação de que o telefone é também um contato de WhatsApp.