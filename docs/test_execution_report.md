# Relatório de Execução de Testes

## 1. Informações do Documento

| Item      | Valor                          |
| --------- | ------------------------------ |
| Projeto   | ServeRest                      |
| Documento | Relatório de Execução de Testes|
| Versão    | 1.0                            |
| Autor     | Aquiles Araujo                 |
| Data      | 16/08/2026                     |

---

## 2. Objetivo

Relacionar as condições de teste com os respectivos casos de teste, comparar os resultados obtidos com os resultados esperados, demonstrar os status e o relacionar com o relatório de defeito, em caso de falha.

---

## 3. Relatório

### Módulo de Login

| Condição    | Caso de Teste | Resultado Esperado | Resultado Obtido | Status | Bug |
| ----------- | ------------- | ------------------ | ---------------- | ------ | --- |
| CND-LOG-001 | TC-LOG-001    | Status Code 200    | Status Code 200  | PASSOU | --- |
| CND-LOG-002 | TC-LOG-002    | Status Code 401    | Status Code 401  | PASSOU | --- |
| CND-LOG-002 | TC-LOG-006    | Status Code 400    | Status Code 400  | PASSOU | --- |
| CND-LOG-003 | TC-LOG-003    | Status Code 401    | Status Code 401  | PASSOU | --- |
| CND-LOG-004 | TC-LOG-004    | Status Code 400    | Status Code 400  | PASSOU | --- |
| CND-LOG-004 | TC-LOG-005    | Status Code 400    | Status Code 400  | PASSOU | --- |
| CND-LOG-005 | TC-LOG-007    | Status Code 400    | Status Code 400  | PASSOU | --- |

---

### Módulo de Usuários

| Condição    | Caso de Teste | Resultado Esperado | Resultado Obtido | Status     | Bug     |
| ----------- | ------------- | ------------------ | ---------------- | ---------- | ------- |
| CND-USU-006 | TC-USU-001    | Status Code 201    | Status Code 201  | PASSOU     | ---     |
| CND-USU-007 | TC-USU-002    | Status Code 400    | Status Code 400  | PASSOU     | ---     |
| CND-USU-008 | TC-USU-003    | Status Code 400    | Status Code 400  | PASSOU     | ---     |
| CND-USU-009 | TC-USU-005    | Status Code 400    | Status Code 400  | PASSOU     | ---     |
| CND-USU-010 | TC-USU-004    | Status Code 400    | Status Code 400  | PASSOU     | ---     |
| CND-USU-011 | TC-USU-006    | Status Code 400    | Status Code 400  | PASSOU     | ---     |
| CND-USU-012 | TC-USU-007    | Status Code 200    | Status Code 200  | PASSOU     | ---     |
| CND-USU-013 | TC-USU-008    | Status Code 200    | Status Code 200  | PASSOU     | ---     |
| CND-USU-014 | TC-USU-009    | Status Code 404    | Status Code 400  | NÃO PASSOU | BUG-001 |
| CND-USU-015 | TC-USU-010    | Status Code 400    | Status Code 400  | PASSOU     | ---     |
| CND-USU-016 | TC-USU-011    | Status Code 200    | Status Code 200  | PASSOU     | ---     |
| CND-USU-017 | TC-USU-012    | Status Code 201    | Status Code 201  | PASSOU     | ---     |
| CND-USU-017 | TC-USU-013    | Status Code 201    | Status Code 201  | PASSOU     | ---     |
| CND-USU-018 | TC-USU-014    | Status Code 400    | Status Code 400  | PASSOU     | ---     |
| CND-USU-019 | TC-USU-015    | Status Code 400    | Status Code 400  | PASSOU     | ---     |
| CND-USU-020 | TC-USU-016    | Status Code 400    | Status Code 400  | PASSOU     | ---     |
| CND-USU-021 | TC-USU-017    | Status Code 400    | Status Code 400  | PASSOU     | ---     |
| CND-USU-022 | TC-USU-018    | Status Code 200    | Status Code 200  | PASSOU     | ---     |
| CND-USU-023 | TC-USU-019    | Status Code 200    | Status Code 200  | PASSOU     | ---     |

---

### Módulo de Produtos

| Condição    | Caso de Teste | Resultado Esperado | Resultado Obtido | Status     | Bug     |
| ----------- | ------------- | ------------------ | ---------------- | ---------- | ------- |
| CND-PRO-024 | TC-PRO-001    | Status Code 201    | Status Code 201  | PASSOU     | ---     |
| CND-PRO-025 | TC-PRO-002    | Status Code 400    | Status Code 400  | PASSOU     | ---     |
| CND-PRO-026 | TC-PRO-003    | Status Code 400    | Status Code 400  | PASSOU     | ---     |
| CND-PRO-026 | TC-PRO-004    | Status Code 400    | Status Code 400  | PASSOU     | ---     |
| CND-PRO-027 | TC-PRO-005    | Status Code 400    | Status Code 400  | PASSOU     | ---     |
| CND-PRO-028 | TC-PRO-006    | Status Code 400    | Status Code 400  | PASSOU     | ---     |
| CND-PRO-029 | TC-PRO-007    | Status Code 400    | Status Code 400  | PASSOU     | ---     |
| CND-PRO-030 | TC-PRO-008    | Status Code 200    | Status Code 200  | PASSOU     | ---     |
| CND-PRO-031 | TC-PRO-009    | Status Code 200    | Status Code 200  | PASSOU     | ---     |
| CND-PRO-032 | TC-PRO-010    | Status Code 404    | Status Code 400  | NÃO PASSOU | BUG-002 |
| CND-PRO-033 | TC-PRO-011    | Status Code 400    | Status Code 400  | PASSOU     | ---     |
| CND-PRO-034 | TC-PRO-012    | Status Code 200    | Status Code 200  | PASSOU     | ---     |
| CND-PRO-035 | TC-PRO-013    | Status Code 201    | Status Code 201  | PASSOU     | ---     |
| CND-PRO-036 | TC-PRO-014    | Status Code 400    | Status Code 400  | PASSOU     | ---     |
| CND-PRO-037 | TC-PRO-015    | Status Code 400    | Status Code 400  | PASSOU     | ---     |
| CND-PRO-037 | TC-PRO-016    | Status Code 400    | Status Code 400  | PASSOU     | ---     |
| CND-PRO-038 | TC-PRO-017    | Status Code 400    | Status Code 400  | PASSOU     | ---     |
| CND-PRO-039 | TC-PRO-018    | Status Code 400    | Status Code 400  | PASSOU     | ---     |
| CND-PRO-039 | TC-PRO-019    | Status Code 400    | Status Code 400  | PASSOU     | ---     |
| CND-PRO-040 | TC-PRO-020    | Status Code 400    | Status Code 400  | PASSOU     | ---     |
| CND-PRO-041 | TC-PRO-021    | Status Code 200    | Status Code 200  | PASSOU     | ---     |
| CND-PRO-042 | TC-PRO-022    | Status Code 200    | Status Code 200  | PASSOU     | ---     |
| CND-PRO-043 | TC-PRO-023    | Status Code 400    | Status Code 400  | PASSOU     | ---     |
