Endpoints da API

1. Listar Todos os Utilizadores
URL: `http://localhost:8000/api`
Método: GET
Descrição: Retorna todos os utilizadores disponíveis.


2. Criar Novo Utilizador
URL: `http://localhost:8000/api/data/`
Método: POST
Descrição: Adiciona um novo utilizador. Os detalhes devem ser enviados no corpo da requisição.


3. Atualizar Dados de um Utilizador
URL: `http://localhost:8000/api/data/?user={nickname}`
Método: PUT
Descrição: Atualiza os dados do utilizador especificado pelo parâmetro user.


4. Deletar Dados
URL: `http://localhost:8000/api/data/?user={nickname}`
Método: DELETE
Descrição: Remove o utilizador do sistema.