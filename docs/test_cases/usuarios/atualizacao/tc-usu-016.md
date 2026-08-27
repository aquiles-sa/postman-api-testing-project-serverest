# TC-USU-016 - Atualizar usuário com senha sem valor

| Item                     | Valor                                                                                |
| ------------------------ | ------------------------------------------------------------------------------------ |
| **ID**                   | TC-USU-016                                                                           |
| **Condição Relacionada** | CND-USU-020                                                                          |
| **Prioridade**           | Alta                                                                                 |
| **Tipo de Teste**        | Funcional - Negativa                                                                 |
| **Objetivo**             | Validar que a API não permita a edição de um usuário com o campo `password` ausente. |
| **Método HTTP**          | `PUT`                                                                                |
| **Endpoint**             | `/usuarios/{_id}`                                                                    |

---

## Pré-condições

- API disponível

- Usuário cadastrado previamente

---

## Massa de Teste

```json
{
    "nome": "Eliseu",
    "email": "elis123@qa.com.br",
    "password": "",
    "administrador": "true"
}
```

---

## Passos

1. Enviar uma requisição HTTP `PUT` para o endpoint `/usuarios/{_id}`,

2. Informar o identificador `_id` do usuário a ser editado,

3. Não preencher o campo `password`,

4. Preencher os outros campos restantes,

5. Executar a requisição.

---

## Resultado Esperado

- Status Code `400`

- A resposta deve conter a mensagem `password não pode ficar em branco`
