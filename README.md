# Projeto de testes de API - ServeRest

## Sobre o Projeto

Esse projeto se trata de realizar testes manuais e criar testes automatizados utilizando a ferramenta Postman para a API pública do [ServeRest](https://serverest.dev/?lang=pt-BR), além de exercitar a criação de documentação de testes, como um plano de teste, condições de teste, casos de teste, relatórios de defeitos e uma matriz de rastreabilidade de testes.

---

## Objetivo

O objetivo do projeto é avaliar o comportamento funcional dos endpoints dos módulos de Login, Usuário e de Produtos, considerando cenários positivos e negativos, além de organizar os testes através do desenvolvimento de uma suíte de testes automatizada utilizando a ferramenta Postman.

---

## Escopo

O escopo do projeto contém a arquitetura de organização dos três módulos utilizados para testes: **Login**, **Usuários** e **Produtos**.

- **Login**
  - Login com credenciais válidas
  - Login com credenciais inválidas
  - Validações de credenciais

- **Usuários**
  - Cadastro
  - Consulta
  - Atualização
  - Exclusão
  - Validação de credenciais

- **Produtos**
  - Cadastro
  - Consulta
  - Atualização
  - Exclusão
  - Validação de credenciais

---

## Ferramentas Utilizadas

- Postman
- JavaScript Assertions
- Markdown
- Git
- GitHub

---

## Collections e Environment do Postman

As collections exportadas do Postman correspondem aos módulos de Login, Usuários e Produtos. Estão disponíveis em `postman/collections`.

Apenas uma environment foi exportada do Postman. Ela contém variáveis que são utilizadas pelos três módulos e em requisições. Está disponível em `postman/environments`

---

## Documentação

- [Plano de Teste](/docs/test_plan.md)
- [Condições de Teste](/docs/test_conditions.md)
- [Casos de Teste](/docs/test_cases/)
  - [Login](/docs/test_cases/login/)
  - [Usuários](/docs/test_cases/usuarios/)
  - [Produtos](/docs/test_cases/produtos/)
- [Bug Reports](/docs/bug_reports/)
- [Relatório de Execução de Testes](/docs/test_execution_report.md)

---

## Resumo da Execução de Testes

| Item               | Resultado |
| ------------------ | --------- |
| Casos de Teste     | 49        |
| Executados         | 49        |
| Testes Aprovados   | 47        |
| Testes Falhos      | 2         |
| Bugs Identificados | 2         |

---

## Defeitos

| ID      | Bug                                  | Módulo               | Severidade | Status |
| ------- | ------------------------------------ | -------------------- | ---------- | ------ |
| BUG-001 | Status Code retornado incorretamente | Consulta de Usuários | Baixa      | Aberto |
| BUG-002 | Status Code retornado incorretamente | Consulta de Produtos | Baixa      | Aberto |

---

## Evidências

As evidências de defeitos estão localizadas em `postman/evidencias`.

- [BUG-001 - Evidência de Status Code incorreto](/postman/evidencias/bug_001_evidence.png)
- [BUG-002 - Evidência de Status Code incorreto](/postman/evidencias/bug_001_evidence.png)

---

## Limitações

> Os testes foram criados e executados utilizando a API ServRest. Por se tratar de uma API pública e compartilhada, os dados podem sofrer alterações decorrentes da utilização da API por outros usuários. Com o conhecimento disto, foi utilizada uma estratégia para geração dinâmica de dados, visando menor dependência de massas registradas anteriormente.

---

## Conclusão

Este projeto demonstra conhecimento e habilidades de testes de software, especialmente em testes de API e de documentação de testes, exibindo a aplicação das atividades de teste, como o planejamento de teste, análise de teste, modelagem de teste, implementação de teste, execução de teste e conclusão de teste.

Os testes realizados forneceram evidências de comportamentos dos módulos avaliados dentro do escopo definido. Isso não afirma que a API esteja livre de defeitos.

É válido ressaltar que este projeto não está finalizado. O módulo de Carrinhos, exibido na API ServeRest, não está dentro do escopo do projeto.

---

## Autor

QA: Aquiles Araujo | [LinkedIn](https://www.linkedin.com/in/aquiles-araujo-035112251/) <br>
Email: aquiles2ws@gmail.com
