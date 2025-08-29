# API Flask - Gerenciamento de Usuários

API RESTful simples desenvolvida com Flask para gerenciar usuários com operações CRUD.

## 📋 Informações do Projeto

**Disciplina:** Desenvolvimento de APIs e Microserviços (DAM)  
**Integrantes:** Anna Julia Higa Farincho, Letícia Macedo, Evelyn Mercês  
**Grupo:** 4  
**Instituição:** IMPACTA

## 🚀 Funcionalidades

- **POST /users** - Criar novo usuário
- **GET /users** - Listar todos os usuários
- **GET /users/<id>** - Buscar usuário específico
- **PUT /users/<id>** - Atualizar usuário
- **DELETE /users/<id>** - Deletar usuário

## 🛠️ Tecnologias Utilizadas

- **Python 3.x**
- **Flask 2.3.3**
- **JSON** para troca de dados
- **HTTP Methods** (GET, POST, PUT, DELETE)

## 📦 Instalação e Execução

### Pré-requisitos
- Python 3.7 ou superior
- pip (gerenciador de pacotes Python)

### Passos para instalação

1. **Clone o repositório:**
```bash
git clone https://github.com/EveMerces/API-Simples-com-Flask.git
cd API-Simples-com-Flask
```

2. **Instale as dependências:**
```bash
pip install -r requirements.txt
```

3. **Execute a aplicação:**
```bash
python app.py
```

A API estará disponível em: `http://localhost:5000`

### Testando a API
Você pode testar usando:
- **Postman** (recomendado)
- **cURL** (linha de comando)
- **Insomnia** (alternativa ao Postman)

## 📚 Endpoints da API

### 1. Criar Usuário
**POST** `/users`

**Headers:**
```
Content-Type: application/json
```

**Body (JSON):**
```json
{
    "nome": "João Silva",
    "email": "joao@email.com"
}
```

**Resposta (201 Created):**
```json
{
    "id": 1,
    "nome": "João Silva",
    "email": "joao@email.com"
}
```

### 2. Listar Todos os Usuários
**GET** `/users`

**Resposta (200 OK):**
```json
[
    {
        "id": 1,
        "nome": "João Silva",
        "email": "joao@email.com"
    }
]
```

### 3. Buscar Usuário por ID
**GET** `/users/<user_id>`

**Resposta (200 OK):**
```json
{
    "id": 1,
    "nome": "João Silva",
    "email": "joao@email.com"
}
```

**Resposta (404 Not Found):**
```json
{
    "error": "Usuário não encontrado"
}
```

### 4. Atualizar Usuário
**PUT** `/users/<user_id>`

**Headers:**
```
Content-Type: application/json
```

**Body (JSON):**
```json
{
    "nome": "João Silva Santos",
    "email": "joao.santos@email.com"
}
```

**Resposta (200 OK):**
```json
{
    "id": 1,
    "nome": "João Silva Santos",
    "email": "joao.santos@email.com"
}
```

### 5. Deletar Usuário
**DELETE** `/users/<user_id>`

**Resposta (200 OK):**
```json
{
    "message": "Usuário excluído com sucesso"
}
```

## 📝 Notas Importantes

- **Armazenamento**: Os dados são armazenados em memória e serão perdidos quando a aplicação for reiniciada
- **IDs**: São gerados automaticamente de forma incremental
- **Validação**: A aplicação valida os dados de entrada e retorna códigos de status HTTP apropriados
- **Estrutura**: Projeto desenvolvido em um único arquivo `app.py` para simplicidade

## 🏫 Projeto Acadêmico

Este projeto foi desenvolvido como atividade da disciplina **Desenvolvimento de APIs e Microserviços (DAM)** da **IMPACTA**, implementando conceitos fundamentais de:

- APIs RESTful
- Framework Flask
- Operações CRUD
- Métodos HTTP
- Manipulação de JSON
- Status Codes HTTP

## 🤝 Contribuições

Este é um projeto acadêmico desenvolvido pelo Grupo 4 da disciplina DAM.

---

**Desenvolvido com ❤️ pelo Grupo 4 - IMPACTA**
