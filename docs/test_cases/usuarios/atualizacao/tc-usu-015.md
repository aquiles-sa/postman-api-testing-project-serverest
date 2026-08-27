# TC-USU-015 - Atualizar usuário com email sem valor

| Item                     | Valor                                                                               |
| ------------------------ | ----------------------------------------------------------------------------------- |
| **ID**                   | TC-USU-015                                                                          |
| **Condição Relacionada** | CND-USU-019                                                                         |
| **Prioridade**           | Alta                                                                                |
| **Tipo de Teste**        | Funcional - Negativa                                                                |
| **Objetivo**             | Validar que a API não permita a edição de um usuário com o campo `email` sem valor. |
| **Método HTTP**          | `PUT`                                                                               |
| **Endpoint**             | `/usuarios/{_id}`                                                                   |

---

## Pré-condições

- API disponível

- Usuário cadastrado previamente

---

## Massa de Teste

```json
{
    "nome": "Nico De La Hoya",
    "email": "",
    "password": "testesenha10",
    "administrador": "false"
}    
```

## Passos

1. Enviar uma requisição HTTP `PUT` para o endpoint `/usuarios/{_id}`,

2. Informar o identificador `_id` do usuário a ser editado,

3. Não preencher o campo `email`,

4. Preencher os outros campos restantes,

5. Executar a requisição.

---

## Resultado Esperado

- Status Code `400`

- A resposta deve conter a mensagem `email não pode ficar em branco`
