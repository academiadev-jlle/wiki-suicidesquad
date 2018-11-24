# Base Entity
Entidade base que implementa a interface [Serializable](https://docs.oracle.com/javase/8/docs/api/java/io/Serializable.html) e serve de base para todas as demais entidades do pacote.

## Anotações
* [`@MappedSuperclass`](https://javaee.github.io/javaee-spec/javadocs/javax/persistence/MappedSuperclass.html): define os mapeamentos existentes na classe como aplicáveis apenas às classes que herdam seus atributos;
* [`@Data`](https://projectlombok.org/features/Data): geração automática de getters, setters e construtores.

## Atributos
* `PK id`: chave primária a ser utilizada para indexação da entidade.