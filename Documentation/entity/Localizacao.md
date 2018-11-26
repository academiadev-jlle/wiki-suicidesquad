# Localizacao Entity
Entidade de pet que estende `BaseEntity`. Define os atributos referentes à localização do pet anunciado.

## Anotações
* [`@Data`](https://projectlombok.org/features/Data): geração automática de getters, setters e construtores;
* [`@EqualsAdnHashCode`](https://projectlombok.org/features/EqualsAndHashCode): implementa os métodos `equals` e `hashcode` para a classe;
* [`@Entity`](https://javaee.github.io/javaee-spec/javadocs/javax/persistence/Entity.html): especifica a classe como sendo uma entidade de persistência na database;
* [`@Table`](https://javaee.github.io/javaee-spec/javadocs/javax/persistence/Table.html): especifica a tabela da database onde será persistida esta entidade.

## Atributos
* `String bairro`;
* `String cidade`;
* `String uf`.