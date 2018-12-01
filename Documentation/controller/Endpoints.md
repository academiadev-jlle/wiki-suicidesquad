
A API responde por 4 controladores:
* Controlador do pet
* Controlador do usuário
* Controlador de autenticação via email
* Controlador de autenticação via facebook

### Controlador do pet
* `/pets`
  * `POST`: realiza a inclusão de um novo pet ao banco. O novo usuario deve ser passado no corpo da requisição como um json, no formato `{"atributo1": "valor", "atributo2": "valor", ...}` conforme atributos da entidade [PetCreateDTO](DTOPet.md).
* `/pets/search`
	* `GET`: retorna um  `Iterable` de `PetDTO` contendo todos os pets que atenderem aos atributos estipulados no parâmetro `PetSearch`.
* `/pets/{idPet}`
	* `GET`: retorna o pet com o `id` especificado, ou lança a exceção `PetNotFoundException` caso não encontre o id;
	* `PUT`: atualiza um pet já existente com novos valores definidos no [`PetCreateDTO`](PetCreateDTO.md);
	* `DELETE`: remove permanentemente o pet correspondente ao id fornecido.
* `/pets/{idPet}/registros`
	* `POST`: inclui novo [`Registro`](Registro.md) ao pet especificado por `idPet`.

### Controlador do usuário
* `/usuarios`
	* `POST`: inclui novo [`Usuario`](Usuario.md), enviado como um json no corpo da requisição.
* `/usuarios/{idUsuario}`
  * `GET`: retorna um [`UsuarioDTO`](UsuarioDTO.md) correspondente ao `idUsuario` fornecido, ou lança uma exceção `UsuarioNotFoundException` caso não encontre o usuário;
  * `PUT`: realiza a atualização de um usuário existente. Um [`UsuarioEditDTO`](UsuarioEditDTO.md) deve ser fornecido no corpo da requisição;
  * `DELETE`: realiza a deleção permanente de um usuário banco.

### Controlador de autenticação via e-mail
* `/auth/email`
  * `POST`: recebe as credenciais (email e senha) como um json(?) . Caso o email e senha providos sejam verificados com sucesso, retorna `stats 200: ok` e o email e token de acesso do usuário no corpo da resposta como um json. Caso a verificação falhe, lança a exceção `BadCredentialsException`.

### Controlador de autenticação via Facebook
* `/auth/facebook/authorization`
	* `GET`: redireciona a request para a API do [facebook](link.da.api);
* `/auth/facebook/callback`
	* `GET`: recebe o código do usuário como parâmetro de URL, e busca as informações do usuário pelo *id* do facebook, caso existente, ou cria um novo usuário com as informações retornadas pela API do [facebook](link.da.api).