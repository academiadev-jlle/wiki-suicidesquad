
# Enums
Classes que contém lista de atributos válidos para as propriedades abaixo:
* Castracao:
	* CASTRADO;
	* NAO_CASTRADO;
	* NAO_INFORMADO.
* Categoria:
	* ACHADO;
	* PARA_ADOCAO;
	* PERDIDO.
* ComprimentoPelo:
	* CURTO;
	* LONGO;
	* MEDIO;
	* SEM_PELO.
* Cor:
	* BRANCO;
	* MARROM;
	* PRETO.
* Porte:
	* GRANDE;
	* MEDIO;
	* PEQUENO.
* Raca:
	* CACHORRO_SRD;
	* EQUINO_SRD;
	* GATO_SRD;
	* LABRADOR;
	* LUSITANO;
	* PERSA;
	* PITBULL;
	* PURO_SANGUE;
	* SIAMES.
* SexoPet:
	* FEMEA;
	* MACHO;
	* NAO_INFORMADO.
* SexoUsuario:
	* FEMININO;
	* MASCULINO;
	* NAO_INFORMADO.
* Situacao:
	* ENCONTRADO;
	* ENTREGUE;
	* PROCURANDO.
* Tipo:
	* CACHORRO;
	* EQUINO;
	* GATO.
* Vacinacao:
	* EM_DIA;
	* NAO_INFORMADO;
	* PARCIAL.

## Construtor
* `Castracao(Integer id)`: inicializa o enum para o id solicitado.

## Métodos
* `Integer getId()`: retorna o ID relativo ao enum;
* `Castracao findById(Integer id)`: retorna um enum com o id solicitado; ou lança a exceção `IllegalArumentException` caso não haja valor para o id.
* `void setRegistros(List<Registro> registros`: inclui lista de atualizações ao histórico do pet.