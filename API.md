# API Documentation


### 1. Listar Todos os Utilizadores
- **URL:** `http://localhost:8000/api`
- **Método:** GET
- **Descrição:** Retorna todos os utilizadores disponíveis.

#### Respostas
- **200 OK:** Lista de utilizadores retornada com sucesso.
- **400 Bad Request:** Requisição malformada.

---

### 2. Criar Novo Utilizador
- **URL:** `http://localhost:8000/api/data/`
- **Método:** POST
- **Descrição:** Adiciona um novo utilizador. Os detalhes devem ser enviados no corpo da requisição.

#### Respostas
- **201 Created:** Utilizador criado com sucesso.
- **400 Bad Request:** Dados de entrada inválidos ou requisição malformada.

---

### 3. Atualizar Dados de um Utilizador
- **URL:** `http://localhost:8000/api/data/?user={nickname}`
- **Método:** PUT
- **Descrição:** Atualiza os dados do utilizador especificado pelo parâmetro `user`.

#### Respostas
- **202 Accepted:** Utilizador atualizado com sucesso.
- **400 Bad Request:** Dados de entrada inválidos ou requisição malformada.
- **404 Not Found:** Utilizador não encontrado.

---

### 4. Deletar Dados de um Utilizador
- **URL:** `http://localhost:8000/api/data/?user={nickname}`
- **Método:** DELETE
- **Descrição:** Remove o utilizador especificado pelo parâmetro `user`.

#### Respostas
- **202 Accepted:** Utilizador deletado com sucesso.
- **400 Bad Request:** Requisição malformada ou dados inválidos.
- **404 Not Found:** Utilizador não encontrado.

--