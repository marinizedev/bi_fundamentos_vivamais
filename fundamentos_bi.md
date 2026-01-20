# Fundamentos de Business Intelligence – VivaMais

## 1. Introdução
Este documento apresenta os fundamentos iniciais de **Business Intelligence (BI)** aplicados ao sistema fictício **VivaMais**, um supermercado modelado previamente em um banco de dados relacional.
O foco deste material é demonstrar o **raciocínio analítico**, a compreensão do negócio e a preparação para **modelagem dimensional**, servindo como base para estudos e evoluções futuras em BI e Analytics.

---

## 2. Objetivo do Mini-Projeto
Aplicar conceitos fundamentais de Business Intelligence a partir de um sistema transacional realista, identificando fatos, dimensões, métricas e perguntas de negócio, com o objetivo de estruturar análises gerenciais e apoiar a tomada de decisão.

---

## 3. Contexto do Sistema VivaMais
O sistema VivaMais representa o funcionamento de um supermercado, contemplando processos de vendas, clientes, produtos, vendedores, formas de pagamento e controle de estoque. 
Os dados transacionais servem como base para a construção de análises históricas e gerenciais, típicas de um ambiente de BI.

---

## 4. Justificativa para Uso de Business Intelligence
Em sistemas operacionais, os dados são registrados para execução das atividades do dia a dia.
O Business Intelligence permite transformar esses dados em **informações estratégicas**, respondendo perguntas como:
- O que vende mais?
- Quando vende mais?
- Quais produtos e categorias geram mais receita?
- Qual o desempenho por vendedor ou forma de pagamento?
Essas análises apoiam decisões de negócio, planejamento e melhoria contínua.

---

## 5. Identificação do Processo Analítico Central

### 5.1 Fato Principal
O processo central analisado é a **venda de produtos**, representada no nível de itens vendidos (item da venda).

### 5.2 Grão
O grão definido é:

> **Uma linha por produto vendido em uma venda.**

Esse nível permite análise detalhadas e agregações flexíveis.

### 5.3 Medidas (Métricas)
Principais medidas asssociadas ao fato de vendas:
- Quantidade vendida
- Preço unitário
- Valor de desconto
- Valor total de item (derivado)

---

## 6. Dimensões Analíticas
As principais dimensões identificadas para análise são:
- **Tempo** (data da venda)
- **Produto** (produto e categoria)
- **Cliente** 
- **Vendedor**
- **Forma de pagamento**
Essas dimensões permitem análises sob diferentes perpectivas do negócio.

---
 
## 7. Visão Inicial de Modelagem Dimensional
A modelagem proposta segue o conceito de **Star Schema**, onde:
- A **tabela fato de vendas** fica no centro
- As **tabelas dimensão** se conectam diretamente a ela
Esta modelagem facilita consultas analíticas, melhora a performance e torna os dados mais intuitivos para análise em ferramentas de BI.

---

## 8. kPIs Propostos
A partir da estrutura analítica, alguns indicadores-chave podem ser definidos:
- Faturamento total
- Ticket médio
- Quantidade de vendas
- Produtos mais vendidos
- Desempenho por categoria
- Distribuição por forma de pagamento

---

## 9. Perguntas de Negócio
Exemplos de perguntas que o BI pode responder:
- Quais produtos têm maior volume de vendas?
- Em quais períodos o faturamento é maior?
- Quais categorias geram mais receita?
- Qual o desempenho de cada vendedor?
- Como os clientes preferem pagar?

---

## 10. Considerações Finais
Este mni-projeto possui caráter **introdutório e conceitual**, com foco no desenvolvimento do pensamento analítico em Business Intelligence.
Ele serve como base para evoluções futuras, como criação de **Data Marts**, **Data Warehouses** e visualizações em ferramentas como **Power BI**.