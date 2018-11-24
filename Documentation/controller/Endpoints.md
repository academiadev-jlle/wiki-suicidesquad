A API responde por 4 controladores:
* Controlador do pet
* Controlador do usuário
* Controlador de autenticação via email
* Controlador de autenticação via facebook

### Controlador do pet
* `/pets`
  * `GET`: retorna um objeto *Pageable* com todos os pets presentes no banco de dados;
  * `POST`: realiza a inclusão de um novo pet ao banco. O novo usuario deve ser passado no corpo da requisição como um json, no formato `{"atributo1": "valor", "atributo2": "valor", ...}` conforme atributos da entidade [DTOPet](DTOPet.md).
* `/pets/{idPet}`: retorna o pet com o *id* especificado, caso existente; caso contrário, lança a exceção `ResourceNotFoundException`.

### Controlador do usuário
* `/usuarios`
  * `GET`: retorna um objeto *Pageable* com todos os usuarios presentes no banco de dados;
  * `POST`: realiza a inclusão de um novo usuarioao banco. O novo usuario deve ser passado no corpo da requisição como um json, no formato `{"atributo1": "valor", "atributo2": "valor", ...}` conforme atributos da entidade [DTOUsuario](DTOUsuario.md).
* `/usuarios/{idUsuario}`: retorna o usuario com o *id* especificado, caso existente; caso contrário, lança a exceção `ResourceNotFoundException`.

### Controlador de autenticação via e-mail
* `/auth/email`
  * `POST`: recebe as credenciais (email e senha) como um json(?) . Caso o email e senha providos sejam verificados com sucesso, retorna `stats 200: ok` e o email e token de acesso do usuário no corpo da resposta como um json. Caso a verificação falhe, lança a exceção `BadCredentialsException`.

### Controlador de autenticação via Facebook
* `/auth/facebook/authorization`
	* `GET`: redireciona a request para a API do [facebook](link.da.api);
* `/auth/facebook/callback`
	* `GET`: recebe o código do usuário como parâmetro de URL, e busca as informações do usuário pelo *id* do facebook, caso existente, ou cria um novo usuário com as informações retornadas pela API do [facebook](link.da.api).