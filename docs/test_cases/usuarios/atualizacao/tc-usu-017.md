# TC-USU-017 - Atualizar usuário com administrador sem valor

| Item                     | Valor                                                                                     |
| ------------------------ | ----------------------------------------------------------------------------------------- |
| **ID**                   | TC-USU-017                                                                                |
| **Condição Relacionada** | CND-USU-021                                                                               |
| **Prioridade**           | Alta                                                                                      |
| **Tipo de Teste**        | Funcional - Negativa                                                                      |
| **Objetivo**             | Validar que a API não permita a edição de um usuário com o campo `administrador` ausente. |
| **Método HTTP**          | `PUT`                                                                                     |
| **Endpoint**             | `/usuarios/{_id}`                                                                         |

---

## Pré-condições

- API disponível

- Usuário cadastrado previamente

---

## Massa de Teste

```json
{
    "nome": "Lucas de Oliveira",
    "email": "lucasoli20@qa.com.br",
    "password": "respon",
    "administrador": ""
}
```

---

## Passos

1. Enviar uma requisição HTTP `PUT` para o endpoint `/usuarios/{_id}`,

2. Informar o identificador `_id` do usuário a ser editado,

3. Não preencher o campo `administrador`,

4. Preencher os outros campos restantes,

5. Executar a requisição.

---

## Resultado Esperado

- Status Code `400`

- A resposta deve conter a mensagem `administrador deve ser 'true' ou 'false'`
