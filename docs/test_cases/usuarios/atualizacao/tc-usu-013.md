# TC-USU-013 - Atualizar usuário com identificador inexistente

| Item                     | Valor                                                                                                                                                                    |
| ------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **ID**                   | TC-USU-013                                                                                                                                                               |
| **Condição Relacionada** | CND-USU-017                                                                                                                                                              |
| **Prioridade**           | Alta                                                                                                                                                                     |
| **Tipo de Teste**        | Funcional - Positivo                                                                                                                                                     |
| **Objetivo**             | Validar que a API permita a edição de um usuário com identificador inexistente. Caso não haja um usuário com o identificador informado, um novo usuário deve ser criado. |
| **Método HTTP**          | `PUT`                                                                                                                                                                    |
| **Endpoint**             | `/usuarios/{_id}`                                                                                                                                                        |

---

## Pré-condições

- API disponível

- Usuário cadastrado previamente

---

## Massa de Teste

```json
{
    "nome": "Cristiano Pereira",
    "email": "crisperei@qa.com.br",
    "password": "senhaaleatoria",
    "administrador": "true"
}
```

---

## Passos

1. Enviar uma requisição HTTP `PUT` para o endpoint `/usuarios/{_id}`,

2. Informar um identificador `_id` inexistente no caminho do parâmetro do endpoint,

3. Preencher todos os campos,

4. Executar a requisição.

---

## Resultado Esperado

- Status Code `201`

- A resposta deve conter a mensagem `Cadastro realizado com sucesso`
