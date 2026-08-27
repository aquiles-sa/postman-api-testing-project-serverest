# TC-USU-014 - Atualizar usuário com nome sem valor

| Item                     | Valor                                                                              |
| ------------------------ | ---------------------------------------------------------------------------------- |
| **ID**                   | TC-USU-014                                                                         |
| **Condição Relacionada** | CND-USU-018                                                                        |
| **Prioridade**           | Média                                                                              |
| **Tipo de Teste**        | Funcional - Negativa                                                               |
| **Objetivo**             | Validar que a API não permita a edição de um usuário com o campo `nome` sem valor. |
| **Método HTTP**          | `PUT`                                                                              |
| **Endpoint**             | `/usuarios/{_id}`                                                                  |

---

## Pré-condições

- API disponível

- Usuário cadastrado previamente

---

## Massa de Teste

```json
{
    "nome": "",
    "email": "umnovoemail@qa.com.br",
    "password": "testando",
    "administrador": "false"
}
```

---

## Passos

1. Enviar uma requisição HTTP `PUT` para o endpoint `/usuarios/{_id}`,

2. Informar o identificador `_id` do usuário a ser editado,

3. Não preencher o campo `nome`,

4. Preencher os outros campos restantes,

5. Executar a requisição.

---

## Resultado Esperado

- Status Code `400`

- A resposta deve conter a mensagem `nome não pode ficar em branco`
