# Auditable Entity
Entidade auditável que estende `BaseEntity`. Contém datas de criação e atualização para entidades que herdem seus atributos.

## Anotações
* [`@MappedSuperclass`](https://javaee.github.io/javaee-spec/javadocs/javax/persistence/MappedSuperclass.html): define os mapeamentos existentes na classe como aplicáveis apenas às classes que herdam seus atributos;
* [`@Data`](https://projectlombok.org/features/Data): geração automática de getters, setters e construtores.
* [`@EqualsAndHashCode`](https://projectlombok.org/features/EqualsAndHashCode): implementa os métodos `equals` e `hashcode` para a classe.
* [`@EntityListeners`](https://javaee.github.io/javaee-spec/javadocs/javax/persistence/EntityListeners.html): especifica a classe a ser chamada quando objetos desta classe forem alterados.

## Atributos
* `LocalDateTime createdDate`: data de criação da entidade.
	* [`@CreatedDate`](https://docs.spring.io/spring-data/commons/docs/current/api/org/springframework/data/annotation/CreatedDate.html): declara o campo como sendo uma data de criação para a entidade;
	* [`@Column(updatable = false`](https://javaee.github.io/javaee-spec/javadocs/javax/persistence/Column.html): especifica o campo como sendo uma coluna não atualizável no banco de dados;
	* [`@JsonProperty("created_date")`](https://fasterxml.github.io/jackson-annotations/javadoc/2.6/com/fasterxml/jackson/annotation/JsonProperty.html): especifica o nome da variável que deve ser mapeada para este atributo quando construindo a partir de um `json`;
	* [`@ApiModelProperty(hidden = true)`](http://docs.swagger.io/swagger-core/v1.5.0/apidocs/io/swagger/annotations/ApiModelProperty.html): anotação para vinculação da propriedade com o swagger.
* `LocalDateTime lastModifiedDate`:
	* [`@Column(updatable = true`](https://javaee.github.io/javaee-spec/javadocs/javax/persistence/Column.html): especifica o campo como sendo uma coluna atualizável no banco de dados;
	* [`@JsonProperty("last_modified_date")`](https://fasterxml.github.io/jackson-annotations/javadoc/2.6/com/fasterxml/jackson/annotation/JsonProperty.html): especifica o nome da variável que deve ser mapeada para este atributo quando construindo a partir de um `json`;
	* [`@ApiModelProperty(hidden = true)`](http://docs.swagger.io/swagger-core/v1.5.0/apidocs/io/swagger/annotations/ApiModelProperty.html): anotação para vinculação da propriedade com o swagger.