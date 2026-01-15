1. INTRODUÇÃO
Este mini-projeto tem como objetivo aplicar os fundamentos iniciais de
Business Intelligence (BI) a partir da análise de um sistema de informações
de um supermercado fictício denominado Supermercado VivaMais. O trabalho busca compreender como os dados operacionais gerados no dia adia do negócio podem ser organizados e interpretados de forma analítica, apoiando a tomada de decisão. O estudo parte da observação do funcionamento do sistema transacional do supermercado, identificando os principais registros envolvidos no processo de vendas, como produtos, clientes, vendedores, formas de pagamento e datas das transações. A partir dessa visão, o projeto propõe uma reflexão inicial sobre quais informações são relevantes para análise gerencial e como elas podem ser estruturadas em um contexto de Business Intelligence. Este mini-projeto tem caráter introdutório e contextual, servindo como base para o desenvolvimento do raciocínio analítico, sem a aplicação imediata de modelos técnicos ou esquemas dimensionais. O foco está na compreensão do negócio, no entendimento dos dados disponíveis e na construção do pensamento analítico necessário para futuras implementações
de soluções de BI.

2. DESCRIÇÃO DAS TABELAS DO SISTEMA VIVAMAIS
O sistema do Supermercado VivaMais é composto por 14 tabelas que registram as informações operacionais relacionadas ao cadastro de clientes, produtos, fornecedores, vendas, pagamentos e colaboradores. Essas tabelas refletem o funcionamento do negócio e servem como base para análises futuras em um ambiente de Business Intelligence. A seguir, são apresentadas as descrições das tabelas do sistema, organizadas em ordem alfabética.

tbl_categoria
Armazena as categorias dos produtos comercializados pelo supermercado. Essa tabela contém informações como o nome da categoria, sua descrição e o tipo, permitindo a classificação e organização dos produtos no sistema. 

tbl_cliente
Registra os clientes do supermercado, identificando o tipo de cliente (pessoa
física ou pessoa jurídica). Essa tabela funciona como base para os dados
específicos de cada tipo de cliente.

tbl_cliente_pf
Armazena as informações dos clientes pessoa física, como CPF e nome
completo. Está relacionada à tabela tbl_cliente, garantindo a identificação
individual desses clientes. 

tbl_cliente_pj
Armazena os dados dos clientes pessoa jurídica, como CNPJ e razão social. Assim como a tabela de pessoa física, está vinculada à tabela tbl_cliente.

tbl_email
Registra os endereços de e-mail associados aos clientes do supermercado, permitindo o contato e a comunicação com os mesmos. 

tbl_endereco
Armazena os endereços dos clientes, contendo informações como logradouro, número, complemento, cidade, estado e CEP. Essa tabela está associada ao
cadastro de clientes.

tbl_fornecedor
Registra os fornecedores do supermercado, contendo dados como CNPJ, razão social, telefone, e-mail e localização. Essa tabela é fundamental para o
controle de abastecimento de produtos. 

tbl_fornecer_produto
Tabela associativa que registra quais produtos são fornecidos por quais
fornecedores, incluindo informações como preço de custo e prazo de entrega
em dias. Permite analisar custos e logística de fornecimento.

tbl_item_venda
Armazena os itens vendidos em cada venda realizada. Contém informações como o produto vendido, a quantidade, o preço unitário e possíveis descontos aplicados. Essa tabela representa o nível mais detalhado das vendas do sistema. 

tbl_pagamento
Registra os pagamentos relacionados às vendas, incluindo situação do
pagamento, valor, data de vencimento, forma de pagamento e número de parcelas. Está vinculada diretamente à tabela de vendas.

tbl_produto
Armazena os dados dos produtos comercializados pelo supermercado, como nome, preço de venda, unidade de medida, quantidade em estoque, estoque mínimo, status do produto e categoria associada.

tbl_telefone
Registra os números de telefone associados aos clientes, permitindo múltiplos contatos para um mesmo cliente. 

tbl_venda
Armazena as informações gerais das vendas realizadas, como data e hora da
venda, cliente responsável pela compra e o vendedor que efetuou o atendimento. 

tbl_vendedor
Registra os vendedores do supermercado, contendo informações como CPF, nome completo, data de admissão e percentual de comissão. Essa tabela permite o acompanhamento do desempenho comercial.

3. DESCRIÇÃO DO SISTEMA VIVAMAIS
O Sistema Supermercado VivaMais é um sistema transacional desenvolvido para registrar e gerenciar as operações diárias de umsupermercado de pequeno a médio porte. Ele contempla os principais processos do negócio, desde o cadastro de clientes, produtos, fornecedores e vendedores, até o registro de vendas e pagamentos. O sistema permite identificar clientes como pessoas físicas ou jurídicas, armazenando seus dados de contato, endereço, telefone e e-mail. Também mantém o controle dos produtos comercializados, incluindo informações de categoria, preço de venda, unidade de medida, status e quantidade em estoque, possibilitando o acompanhamento do abastecimento
e da disponibilidade dos itens. As vendas realizadas são registradas por meio da identificação do cliente, do vendedor responsável e da data e hora da operação. Cada venda é detalhada em nível de item, permitindo o controle preciso dos produtos vendidos, quantidades, preços unitários e descontos aplicados. Os pagamentos associados às vendas são registrados com informações sobre forma de pagamento, valor, parcelas, vencimento e situação. Além disso, o sistema gerencia os fornecedores e a relação de fornecimento de produtos, armazenando dados como preço de custo e prazo de entrega, o que possibilita análises futuras relacionadas a custos, logística e desempenho dos fornecedores. De forma geral, o sistema VivaMais reflete fielmente a rotina operacional como uma base de dados estruturada e confiável para a extração de informações estratégicas em um ambiente de Business Intelligence.

4. OBJETIVO DO MINI-PROJETO
O objetivo deste mini-projeto é aplicar os fundamentos de Business Intelligence (BI) no contexto do sistema Supermercado VivaMais, utilizando
como base os dados operacionais de vendas, produtos, clientes e pagamentos, com a finalidade de transformar dados transacionais úteis para apoio à tomada de decisão. Busca-se identificar os principais processos de negócio, definir a tabela fato central, reconhecer as dimensões relevantes e estabelecer as métricas principais, respeitando os conceitos de granularidade, fatos e dimensões, conforme a abordagem de modelagem proposta por Ralph Kimball. Por meio deste mini-projeto, busca-se demonstrar como a organização adequada dos dados pode fornecer uma visão analítica do desempenho do supermercado, permitindo análises como volume de vendas, faturamento, comportamento de consumo dos clientes e eficiência comercial, servindo como base futuras implementações de um Data Mart e, posteriormente, de um Data Warehouse corporativo. 
Essa modelagem está alinhada aos conceitos de Data Analytics e Data Warehousing, conforme abordados em plataformas analíticas modernas como Azure Synapse e Power BI.

5. JUSTIFICATIVA PARA O USO DE BUSINESS
INTELLIGENCE (BI)
O Supermercado VivaMais, por meio de suas operações diárias, gera um grande volume de dados relacionados a vendas, produtos, clientes, pagamentos, estoque e atuação dos vendedores. Embora esses dados estejam registrados no sistema transacional, eles se encontram distribuídos em diversas tabelas e estruturados com foco operacional, o que dificulta
análises estratégicas mais profundas. Nesse contexto, o uso de Business Intelligence (BI) torna-se essencial para transformar os dados operacionais em informações organizadas, consolidadas e úteis para a tomada de decisão. A partir de uma abordagem analítica, é possível compreender o comportamento de vendas ao longo do tempo, identificar os produtos mais vendidos, analisar o desempenho por categoria, avaliar formas de pagamento mais utilizadas e acompanhar indicadores financeiros relevantes para o negócio. Além disso, o BI permite uma visão integrada do negócio, conectando dados de diferentes áreas em uma estrutura voltada à análise, e não apenas à operação. Essa visão facilita o acompanhamento de tendências, a identificação de oportunidades de melhoria e o suporte às decisões gerenciais, como controle de estoque, estratégias de precificação, promoções e avaliação de desempenho de vendedores. Portanto, a aplicação de BI no Supermercado VivaMais justifica-se pela necessidade de transformar dados brutos em conhecimento estratégico, apoiando a gestão do negócio de forma mais eficiente, organizada e orientada por dados.

6. PROPOSTA DE ANÁLISE COM BUSINESS
INTELLIGENCE (BI)
A proposta deste mini-projeto consiste em aplicar conceitos fundamentais
de Business Intelligence (BI) sobre os dados do sistema Supermercado
VivaMais, com o objetivo de transformar dados operacionais em informações
analíticas que auxiliem na compreensão do desempenho do negócio. A partir da estrutura do banco de dados existente, a análise será centrada
principalmente nos dados de vendas, permitindo observar padrões de
consumo, comportamento dos clientes, desempenho dos produtos e
resultados financeiros ao longo do tempo. Esses dados, quando organizados
de forma analítica, possibilitam responder perguntas relevantes para a gestão, como:

• Quais produtos possuem maior volume de vendas;
• Quais períodos apresentam maior faturamento;
• Como os descontos impactam o valor final das vendas;
• Qual o desempenho geral do supermercado em termos de quantidade e
valor vendido. 

Nesta etapa, a proposta não envolve a construção de dashboards ou o uso de ferramentas específicas de visualização, mas sim o entendimento do papel dos dados, da organização das informações e da definição de quais elementos são essenciais para uma futura análise analítica mais avançada. Este mini-projeto tem como foco demonstrar a capacidade de identificar dados relevantes, compreender a relação entre fatos e dimensões e estruturar uma visão analítica inicial, servindo como base para projetos futuros mais completos na área de Business Intellingence e Análise de Dados.

7. IDENTIFICAÇÃO DO FATO PRINCIPAL DO SISTEMA
VIVAMAIS
No contexto do Supermercado VivaMais, o processo de negócio central é
a venda de produtos. 
A tabela que melhor representa esse processo, no nível mais detalhado
possível, é:

7.1 Tabela Fato Principal

• tbl_item_venda
Por que ela é a tabela fato?
Porque ela:

• Registra cada item vendido individualmente
• Contém medidas numéricas analisáveis
• Representa o grão mais detalhado da venda

7.2 Grão da Tabela Fato
Uma linha para cada produto vendido em uma venda. Ou seja:

• Se uma venda tem 5 produtos → 5 linhas na tbl_item_venda

7.3 Medidas (Fatos) presentes
• qtde_vendida
• preco_unitario
• desconto_item
• (derivável) valor total do item → qtde_vendida x preco_unitario -desconto_item

Essas medidas são a base para relatórios, análise e indicadores.

8. DIMENSÕES ANALÍTICAS DO VIVAMAIS
As dimensões são tudo aquilo que contextualiza, explica e qualifica a venda. A partir da sua modelagem, temos as seguintes dimensões:

8.1 Dimensão Tempo
Origem:

• tbl_venda.data_hora

Possibilita análises como:

• Vendas por dia, mês, ano
• Horários de pico
• Comparações temporais

8.2 Dimensão Produto
Origem:

7 tbl_produto
• tbl_categoria

Atributos relevantes:

• Nome do produto
• Categoria
• Unidade de medida
• Status do produto

Permite análises como:

• Produtos mais vendidos
• Categorias com maior faturamento
• Produtos com baixo giro

8.3 Dimensão Cliente
Origem:

• tbl_cliente
• tbl_cliente_pf
• tbl_cliente_pj
• tbl_endereco

Viabiliza análises relacionadas a:

• Perfil do cliente (PF ou PJ)
• Localização
• Comportamento de compra

8.4 Dimensão Vendedor
Origem:

• tbl_vendedor
Apoia análises como:

• Desempenho por vendedor
• Comissão x vendas
• Produtividade individual

8.5 Dimensão Pagamento
Origem:

• tbl_pagamento

Possibilita análises como:

• Parcelamentos
• Forma de pagamento mais utilizada
• Situação dos pagamentos

9. RESUMO ANALÍTICO (VISÃO CLARA)
• Fato principal:
• Venda de itens (tbl_item_venda)
• O que é analisado (medidas):
• Quantidade
• Valores
• Descontos
• O que explica a análise (dimensões):
• Tempo
• Produto / Categoria
• Cliente
• Vendedor
• Forma de pagamento

10. IDENTIFICAÇÃO DO FATO E DAS DIMENSÕES
ANALÍTICAS

10.1 Identificação do Fato Principal
Conforme apresentado anteriormente no sistema Supermercado VivaMais, o principal evento de negócio analisado neste mini-projeto é a venda de
produtos aos clientes. A tabela que representa esse evento é a tbl_item_venda, pois é nela que
estão registrados os dados mais relevantes para análise quantitativa do
negócio, como:

• o produto vendido, 
• o preço unitário praticado, 
• a quantidade vendida, 
• e a aplicação de descontos por item. 

Essa tabela é considerada a tabela fato do projeto, uma vez que concentra as métricas mensuráveis que permitem avaliar o desempenho comercial do supermercado. 

10.2 Definição do Grão da Análise.
O grão adotado neste mini-projeto corresponde a:

• Uma linha para cada produto vendido em uma venda. 

Em outras palavras, cada registro na tabela tbl_item_venda representa um
item específico de um cupom de venda, permitindo análises detalhadas e
precisas, como:

• vendas por produto,
• vendas por período, 
• vendas por cliente, 
• vendas por vendedor, 
• impacto de descontos nas vendas. 

A definição desse grão garante flexibilidade analítica e possibilita a
construção de indicadores consistentes para apoio à tomada de decisão. 

10.3 Identificação das Dimensões Analíticas
As dimensões analíticas são as entidades que fornecem contexto ao fato
de venda, permitindo diferentes perspectivas de análise. No sistema
VivaMais, as principais dimensões identificadas são:

• Produto
Permite analisar o desempenho de vendas por produto, categoria, status e
estoque. 
• Cliente
Possibilita análises por tipo de cliente (Pessoa Física ou Jurídica), comportamento de compra e relacionamento. 
• Tempo (Data da Venda)
Derivada da tabela de vendas, permite análise temporais como vendas por
dia, mês, período ou sazonalidade. 
• Vendedor
Viabiliza a avaliação de desempenho individual, produtividade e comissões. 
• Forma de Pagamento
Permite analisar preferências de pagamento, parcelamento e impacto
financeiro nas vendas.

Essas dimensões fornecem a base necessária para futuras análises em
Business Intelligence, mesmo antes da formalização de um modelo
dimensional completo. 

11. VISÃO INICIAL DE MODELAGEM DIMENSIONAL
Star Schema do Supermercado VivaMais

11.1 Conceito Geral da Modelagem Dimensional
A modelagem dimensional é uma técnica utilizada em Business
Intelligence para organizar os dados de forma simples, intuitiva e orientada à
análise. Neste mini-projeto, adota-se uma visão inicial de Star Schema, cujo
objetivo é demonstrar como os dados operacionais do sistema VivaMais
podem ser reorganizados para fins analíticos. O modelo Star Schema é composto por:

• uma tabela fato central, que armazena métricas quantitativas;
• tabelas dimensão, que fornecem contexto e significado aos dados
analisados. 

11.2 Tabela Fato Central
A tabela fato central proposta para o VivaMais é:

• Fato_Vendas (derivada da tbl_item_venda)

Essa tabela representa o evento principal de negócio: a venda de produtos. Ela concentra os principais indicadores que poderão ser utilizados em
análises e dashboards, tais como:

• quantidade vendida, 
• valor unitário, 
• valor total da venda por item, 
• descontos aplicados. 

Cada registro da tabela fato corresponde a um produto vendido em uma
venda, respeitando o grão definido anteriormente. 

11.3 Dimensões Associadas à Fato de Vendas
A partir da tabela fato, são identificadas as dimensões que explicam o
contexto de cada venda:

• Dim_Produto
Derivada da tbl_produto e tbl_categoria. 
Permite análises por produto, categoria, status e características
comerciais. 
• Dim_Cliente
Derivada das tabelas tbl_cliente, tbl_cliente_pf e tbl_cliente_pj. Possibilita análises por tipo de cliente e perfil de compra. 
• Dim_Tempo
Derivada da data e hora da venda (tbl_venda). 
Permite análises temporais como vendas por dia, mês, período ou sazonalidade. 
• Dim_Vendedor
Derivada da tbl_vendedor. 
Permite avaliar desempenho individual, produtividade e impacto de
comissões. 
• Dim_Pagamento
Derivada da tbl_pagamento. 
Possibilita análises por forma de pagamento, parcelamento e situação
financeira.

11.4 Estrutura Conceitual do Star Schema
De forma conceitual, o modelo Star Schema do VivaMais pode ser
descrito como:

• Fato_Vendas no centro do modelo
• Dimensões conectadas diretamente à fato:
    • Dim_Produto
    • Dim_Cliente
    • Dim_Vendedor
    • Dim_Pagamento

Essa estrutura facilita consultas analíticas, melhora a performance em
ambientes de BI e torna os dados mais acessíveis para análises e
visualizações futuras. 

11.5 Considerações sobre a Evolução do Modelo
Esta modelagem representa uma visão inicial, construída com base no
entendimento do sistema e nos fundamentos de Business Intelligence. Em etapas futuras, o modelo poderá ser refinado com:

• ajustes de granularidade, 
• inclusão de novas métricas, 
• criação de Data Marts específicos, 
• e implementação técnica em um Data Warehouse.

12. POSSÍVEIS INDICADORES (KPIs) DO SUPERMERCADO
VIVAMAIS
Os KPIs (Key Performance Indicators) são indicadores estratégicos que
permitem acompanhar o desempenho do supermercado VivaMais, auxiliando
gestores na tomada de decisões baseadas em dados concretos. Com base nas informações do sistema e na proposta de uso de Business
Intelligence, alguns KPIs iniciais que podem ser analisados são:

• **Faturamento Total**
Valor total das vendas realizadas em determinado período. 
• **Quantidade de Vendas Realizadas**
Número total de vendas efetuadas. 
• **Ticket Médio**
Média de valor gasto por cliente em cada compra. 
• **Produtos Mais Vendidos**
Identificação dos produtos com maior volume ou valor de vendas. 
• **Vendas por Período**
Análise de vendas por dia, mês ou ano. 
• **Desempenho por Categoria de Produto**
Avaliação de quais categorias geram maior faturamento. 
• **Vendas por Forma de Pagamentos**
Comparação entre pagamentos em dinheiro, cartão, pix, entre outros. 

Esses indicadores fornecem uma visão clara da saúde financeira e operacional do supermercado.

13. EXEMPLOS DE ANÁLISES E PERGUNTAS DE NEGÓCIO
A utilização de BI no VivaMais possibilita responder a diversas perguntas
estratégicas, como:

• Quais produtos apresentam maior saída em determinados períodos?
• Em quais dias ou meses o faturamento é mais alto?
• Qual é o comportamento de compra dos clientes ao longo do tempo?
• Quais categorias de produtos geram maior receita?
• Qual forma de pagamento é mais utilizada pelos clientes?
• Existem períodos de baixa venda que precisam de ações promocionais?
• Quais produtos podem ser melhor trabalhados em campanhas de marketing?

Essas análises ajudam a transformar dados brutos em informação
estratégica, apoiando decisões mais assertivas.

14. CONSIDERAÇÕES FINAIS DO MINI-PROJETO
Este mini-projeto teve como objetivo apresentar uma visão inicial de
modelagem e análise de dados para o sistema do supermercado VivaMais, utilizando conceitos fundamentais de Banco de Dados e Business Intelligence. Ao longo do documento, foram descritas as tabelas do sistema, os objetivos do projeto, a justificativa para o uso de BI e uma proposta de análise baseada em indicadores e perguntas de negócio. Além disso, foi apresentada uma visão inicial de modelagem dimensional, preparando o caminho para a construção de um Star Schema mais detalhado no futuro. Mesmo sendo um projeto introdutório, o VivaMais demonstra grande potencial para evoluir em análises mais avançadas, contribuindo para melhoria da gestão, aumento de desempenho e tomada de decisões orientadas por dados. Este mini-projeto reforça a importância do BI como ferramenta estratégica e evidencia o papel da análise de dados no contexto empresarial moderno.