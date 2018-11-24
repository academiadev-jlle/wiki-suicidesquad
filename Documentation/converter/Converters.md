Converters são utilizados para mapear os valores inteiros armazenados no banco de dados para seus respectivos atributos categóricos das entidades. Todos possuem a estrutura:
* `Integer convertToDatabaseColumn(< Enum > enum)`: retorna o índice numérico correspondente ao `enum` passado, ou `null` caso `enum` seja `null`;
* `< Enum > convertToEntityAttribute(Integer id)`: retorna um `enum` com o atributo correspondente ao índice `id`, ou `null` caso `id` seja `null`.

### Converters atualmente suportados
* CastracaoConverter
* CategoriaConverter
* ComprimentoPeloConverter
* CorConverter
* PorteConverter
* RaçaConverter
* SexoPetConverter
* SexoUsuarioConverter
* SituacaoConverter
* TipoConverter
* VacinacaoConverter