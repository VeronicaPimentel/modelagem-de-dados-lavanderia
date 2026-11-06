# 🧺 Modelagem de Dados — Lavanderia Sta. Bárbara

## Sobre o projeto

Este projeto acadêmico, desenvolvido em grupo em 2026 para a disciplina de **Modelagem de Dados**, apresenta a estruturação de um banco de dados para o módulo operacional da Lavanderia Sta. Bárbara.

O trabalho parte da análise de processos reais de uma lavanderia, identificando necessidades de organização das informações, controle de pedidos, cadastro de clientes, identificação de peças, contratação de serviços e acompanhamento de prazos.

A proposta busca transformar registros manuais em uma estrutura de dados organizada, consistente e preparada para uma futura implementação.

## Objetivo

Desenvolver a modelagem conceitual e lógica de um banco de dados capaz de representar os processos operacionais da lavanderia.

**Objetivos específicos:**

- Identificar os principais processos e necessidades do negócio.
- Levantar requisitos funcionais e não funcionais.
- Definir regras de negócio.
- Elaborar o Diagrama Entidade-Relacionamento (DER).
- Converter o modelo conceitual em um modelo lógico relacional.
- Definir chaves primárias e estrangeiras.
- Construir o dicionário de dados.
- Analisar a normalização até a Terceira Forma Normal (3FN).

## Problemas identificados

Durante o levantamento das necessidades da lavanderia, foram identificados:

- Utilização de comandas e registros manuais.
- Ausência de cadastro digital estruturado de clientes.
- Informações sobre preços e prazos concentradas no conhecimento da responsável.
- Dificuldade para acompanhar o andamento dos pedidos.
- Necessidade de organizar o histórico dos atendimentos.

## Estrutura do banco de dados

O modelo lógico relacional foi organizado em **9 tabelas**:

| Tabela | Finalidade |
|---|---|
| `cliente` | Armazena os dados cadastrais dos clientes. |
| `funcionario` | Identifica os funcionários responsáveis pelas operações. |
| `tipo_peca` | Organiza as categorias de peças. |
| `servico` | Registra os serviços oferecidos pela lavanderia. |
| `pedido` | Armazena os pedidos, seus prazos e situações. |
| `item` | Identifica individualmente cada peça de um pedido. |
| `preco_tabelado` | Define preços e prazos por combinação de tipo de peça e serviço. |
| `servico_item` | Registra os serviços contratados para cada peça. |
| `retirada` | Registra a retirada integral de um pedido. |

O modelo contém 46 colunas de dados e utiliza chaves primárias simples e compostas, além de chaves estrangeiras para preservar os relacionamentos.

## Modelagem conceitual

O Diagrama Entidade-Relacionamento (DER) foi desenvolvido com base na **notação de Chen**.

O modelo representa entidades, atributos, relacionamentos e cardinalidades, incluindo uma entidade fraca para identificar individualmente as peças vinculadas a cada pedido.

## Modelagem lógica

O modelo lógico apresenta a conversão das entidades e dos relacionamentos em tabelas relacionais.

Entre as decisões adotadas estão:

- Identificação de cada peça por pedido e sequência.
- Separação entre preço vigente e preço contratado.
- Preservação das condições comerciais aplicadas aos pedidos.
- Utilização de chaves compostas para garantir a identificação dos registros.
- Representação da retirada como um evento único por pedido.

## Normalização

O projeto apresenta a análise das três primeiras formas normais:

- **1FN:** organização dos dados em atributos com valores únicos no domínio adotado.
- **2FN:** análise das dependências funcionais em relações com chaves compostas.
- **3FN:** separação das informações cadastrais e comerciais para reduzir redundâncias e dependências inadequadas, considerando as regras adotadas no projeto.

## Regras de negócio

Entre as principais regras documentadas estão:

- Cada pedido pertence a um cliente.
- Cada peça está vinculada a um pedido e a um tipo de peça.
- Cada peça deve possuir pelo menos um serviço contratado antes do processamento.
- Os valores contratados devem ser preservados mesmo após alterações na tabela de preços.
- O pedido possui situações definidas durante seu ciclo operacional.
- A retirada deve ser única e integral.
- O cancelamento não deve excluir imediatamente o histórico do pedido.

## Documentação

A documentação técnica completa está disponível no arquivo:

 **[Visualizar projeto completo em PDF](Grupo_01.pdf)**

O documento apresenta o levantamento de necessidades, os processos de negócio, os requisitos, as regras, os diagramas, o dicionário de dados, a normalização e as justificativas técnicas.

## Ferramentas e conceitos utilizados

- Modelagem conceitual de dados.
- Diagrama Entidade-Relacionamento (DER).
- Notação de Chen.
- Modelo lógico relacional.
- dbdiagram.io — representação do modelo lógico.
- Microsoft Visio Online — representação do DER.
- Normalização de bancos de dados.
- GitHub — organização e apresentação da documentação.

## Escopo do projeto

O trabalho contempla a modelagem de dados do módulo operacional de pedidos da lavanderia.

Não contempla a implementação de uma aplicação funcional, nem módulos de pagamento, estoque ou logística de entregas.

A documentação constitui uma base para o desenvolvimento futuro de uma solução informatizada.

## Informações acadêmicas

**Disciplina:** Modelagem de Dados  
**Projeto:** Lavanderia Sta. Bárbara  
**Modalidade:** Trabalho acadêmico em grupo  
**Ano:** 2026

---

*Projeto acadêmico desenvolvido para aplicar conhecimentos de análise de requisitos, modelagem conceitual, modelagem relacional e organização de dados.*
