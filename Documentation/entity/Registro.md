# Registro Entity
Entidade de pet que estende `BaseEntity`. Objeto que contém a situação do pet em determinada data.

## Anotações
* [`@Data`](https://projectlombok.org/features/Data): geração automática de getters, setters e construtores;
* [`@EqualsAndHashCode`](https://projectlombok.org/features/EqualsAndHashCode): implementa os métodos `equals` e `hashcode` para a classe;
* [`@NoArgsConstructor`](https://projectlombok.org/features/constructor): cria construtor vazio;
* [`@Entity`](https://javaee.github.io/javaee-spec/javadocs/javax/persistence/Entity.html): especifica a classe como sendo uma entidade de persistência na database;
* [`@Table`](https://javaee.github.io/javaee-spec/javadocs/javax/persistence/Table.html): especifica a tabela da database onde será persistida esta entidade.

## Atributos
* `Pet pet`: pet ao qual o registro se refere;
* `Situacao situacao`: status do pet no momento de criação do novo registro;
* `LocalDateTime data`: data de alteração do status.