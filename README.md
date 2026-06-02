# API Ferramentas
Uma API REST simples desenvolvida com **FastAPI** para gerenciamento de ferramentas. 
O projeto permite cadastrar, listar, consultar, atualizar e remover ferramentas através de endpoints HTTP.

🚀 Tecnologias Utilizadas
Python 3
FastAPI
Pydantic
Uvicorn

📋 Funcionalidades
✅ Listar todas as ferramentas
✅ Cadastrar nova ferramenta
✅ Buscar ferramenta por ID
✅ Atualizar ferramenta existente
✅ Remover ferramenta

📂 Estrutura dos Dados

Cada ferramenta possui os seguintes campos:
| Campo     | Tipo   | Descrição               |
| --------- | ------ | ----------------------- |
| id        | int    | Identificador único     |
| nome      | string | Nome da ferramenta      |
| preco     | float  | Preço da ferramenta     |
| descricao | string | Descrição da ferramenta |

Exemplo
```json
{
  "id": 1,
  "nome": "Furadeira",
  "preco": 299.90,
  "descricao": "Furadeira elétrica profissional"
}
```

▶️ Executando a Aplicação
Execute o servidor:
```bash
uvicorn main:app --reload
```

A API estará disponível em:
```text
http://127.0.0.1:8000
```

📖 Documentação Automática
O FastAPI gera documentação automaticamente.
Swagger UI:
```text
http://127.0.0.1:8000/docs
```

🔗 Endpoints
Listar Ferramentas
```http
GET /ferramentas
```

Buscar Ferramenta por ID
```http
GET /ferramentas/{id}
```

Adicionar Ferramenta
```http
POST /ferramentas
```

Exemplo de requisição:
```json
{
  "nome": "Martelo",
  "preco": 49.90,
  "descricao": "Martelo de aço"
}
```

Atualizar Ferramenta
```http
PUT /ferramentas/{id}
```

Deletar Ferramenta
```http
DELETE /ferramentas/{id}
```

Observação

Os dados são armazenados apenas em memória utilizando uma lista Python. Ao reiniciar a aplicação, todas as informações cadastradas serão perdidas.
Desenvolvido para fins de estudo e aprendizado com FastAPI.
