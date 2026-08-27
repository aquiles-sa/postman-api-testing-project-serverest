# Condições de Teste

## 1. Informações do Documento

| Item      | Valor              |
| --------- | ------------------ |
| Projeto   | ServeRest          |
| Documento | Condições de teste |
| Versão    | 1.0                |
| Autor     | Aquiles Araujo     |
| Data      | 30/07/2026         |

---

## 2. Objetivo

Identificar todas as condições que serão verificadas durante a execução dos testes da API ServeRest.

---

## 3. Módulo de Login

Exemplo de _Request Body_ de cadastro de usuários: <br>

```json
{
    "email": "fulano@qa.com",
    "password": "teste"
}
```

| ID              | Condição de Teste                            | Prioridade |
| --------------- | -------------------------------------------- | ---------- |
| **CND-LOG-001** | Validar login com credenciais válidas        | Alta       |
| **CND-LOG-002** | Validar login com senha inválida             | Alta       |
| **CND-LOG-003** | Validar login com email inexistente          | Alta       |
| **CND-LOG-004** | Validar login com campos obrigatórios vazios | Alta       |
| **CND-LOG-005** | Validar login com e-mail inválido            | Média      |

--- 

## 4. Módulo de Usuários

Exemplo de _Request Body_ de cadastro de usuários: <br>

```json
{   
    "nome": "Fulano da Silva",
    "email": "beltrano@qa.com.br",
    "password": "teste",
    "administrador": "true"
}
```

### Cadastro de Usuários

| ID              | Condição de Teste                                        | Prioridade |
| --------------- | -------------------------------------------------------- | ---------- |
| **CND-USU-006** | Validar cadastro de usuário com credenciais válidas      | Alta       |
| **CND-USU-007** | Validar cadastro de usuário com e-mail já cadastrado     | Alta       |
| **CND-USU-008** | Validar cadastro de usuário sem nome                     | Média      |
| **CND-USU-009** | Validar cadastro de usuário sem senha                    | Alta       |
| **CND-USU-010** | Validar cadastro de usuário sem e-mail                   | Alta       |
| **CND-USU-011** | Validar cadastro de usuário sem informe de administrador | Alta       |

---

### Consulta de Usuários

| ID              | Condição de Teste                                       | Prioridade |
| --------------- | ------------------------------------------------------- | ---------- |
| **CND-USU-012** | Listar de todos os usuários cadastrados                 | Alta       |
| **CND-USU-013** | Buscar usuário específico por identificador existente   | Alta       |
| **CND-USU-014** | Buscar usuário específico por identificador inexistente | Alta       |
| **CND-USU-015** | Buscar usuário específico por identificador inválido    | Alta       |

---

### Edição de Usuários

| ID              | Condição de Teste                                          | Prioridade |
|:--------------- |:---------------------------------------------------------- | ---------- |
| **CND-USU-016** | Editar todos os campos válidos de um usuário               | Alta       |
| **CND-USU-017** | Editar um usuário com identificador inexistente            | Alta       |
| **CND-USU-018** | Editar um usuário, deixando-o sem nome                     | Média      |
| **CND-USU-019** | Editar um usuário, deixando-o sem e-mail                   | Alta       |
| **CND-USU-020** | Editar um usuário, deixando-o sem senha                    | Alta       |
| **CND-USU-021** | Editar um usuário, deixando-o sem informe de administrador | Alta       |

---

### Exclusão de Usuários

| ID              | Condição de Teste                                   | Prioridade |
| --------------- | --------------------------------------------------- | ---------- |
| **CND-USU-022** | Excluir um usuário pelo identificador               | Alta       |
| **CND-USU-023** | Excluir um usuário por um identificador inexistente | Alta       |

---

## 5. Módulo de Produtos

Exemplo de _Request Body_ de cadastro de produtos: <br>

```json
{
    "nome": "Logitech MX Vertical",
    "preco": 470,
    "descricao": "Mouse",
    "quantidade": 381
}
```

### Cadastro de Produtos

| ID              | Condição de Teste                             | Prioridade |
| --------------- | --------------------------------------------- | ---------- |
| **CND-PRO-024** | Validar cadastro de produto com dados válidos | Alta       |
| **CND-PRO-025** | Validar cadastro de produto sem nome          | Alta       |
| **CND-PRO-026** | Validar cadastro de produto sem preço         | Alta       |
| **CND-PRO-027** | Validar cadastro de produto sem descrição     | Média      |
| **CND-PRO-028** | Validar cadastro de produto sem quantidade    | Alta       |
| **CND-PRO-029** | Validar cadastro de produto duplicado         | Alta       |

--- 

### Consulta de Produtos

| ID              | Condição de Teste                                       | Prioridade |
| --------------- | ------------------------------------------------------- | ---------- |
| **CND-PRO-030** | Listar todos os produtos registrados                    | Alta       |
| **CND-PRO-031** | Buscar produto específico por identificador existente   | Alta       |
| **CND-PRO-032** | Buscar produto específico por identificador inexistente | Alta       |
| **CND-PRO-033** | Buscar produto específico por identificador inválido    | Alta       |

---

### Edição de Produtos

| ID              | Condição de Teste                                 | Prioridade |
| --------------- | ------------------------------------------------- | ---------- |
| **CND-PRO-034** | Editar todas as credenciais válidas de um produto | Alta       |
| **CND-PRO-035** | Editar um produto com identificador inexistente   | Alta       |
| **CND-PRO-036** | Editar um produto, deixando-o sem nome            | Alta       |
| **CND-PRO-037** | Editar um produto, deixando-o sem preço           | Alta       |
| **CND-PRO-038** | Editar um produto, deixando-o sem descrição       | Média      |
| **CND-PRO-039** | Editar um produto, deixando-o sem quantidade      | Média      |
| **CND-PRO-040** | Editar um produto já registrado previamente       | Alta       |

---

### Exclusão de Produtos

| ID              | Condição de Teste                                   | Prioridade |
| --------------- | --------------------------------------------------- | ---------- |
| **CND-PRO-041** | Excluir um produto pelo identificador               | Alta       |
| **CND-PRO-042** | Excluir um produto por um identificador inexistente | Alta       |
| **CND-PRO-043** | Excluir um produto por um identificador inválido    | Alta       |

---

## 6. Resumo

| Módulo      | Quantidade de Condições |
| ----------- | -----------------------:|
| **Login**   | 5                       |
| **Usuário** | 18                      |
| **Produto** | 20                      |
