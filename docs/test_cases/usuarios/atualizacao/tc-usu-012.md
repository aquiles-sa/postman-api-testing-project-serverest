# TC-USU-012 - Atualizar usuário inexistente com email já existente

| Item                     | Valor                                                                                                                                    |
| ------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------- |
| **ID**                   | TC-USU-012                                                                                                                               |
| **Condição Relacionada** | CND-USU-017                                                                                                                              |
| **Prioridade**           | Alta                                                                                                                                     |
| **Tipo de Teste**        | Funcional - Negativo                                                                                                                     |
| **Objetivo**             | Validar que a API permita a edição de um usuário com identificador inexistente, desde que o email não tenha sido previamente registrado. |
| **Método HTTP**          | `PUT`                                                                                                                                    |
| **Endpoint**             | `/usuarios/{_id}`                                                                                                                        |

---

## Pré-condições

- API disponível

- Usuário cadastrado previamente

---

## Massa de Teste

```json
{
  "nome": "Fulano da Silva",
  "email": "beltrano@qa.com.br",
  "password": "teste",
  "administrador": "true"
}
```

---

## Passos

1. Enviar uma requisição HTTP `PUT` para o endpoint `/usuarios/{_id}`,

2. Informar um identificador `_id` inexistente no caminho do parâmetro do endpoint,

3. Informar um email que já tenha sido registrado anteriormente,

4. Executar a requisição.

---

## Resultado Esperado

- Status Code `401`

- A resposta deve conter a mensagem `Este email já está sendo utilizado`
