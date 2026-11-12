# Engenharia de Dados — Schema 1: Dados Públicos

## Projeto AF Sacolas

Este diretório reúne a contribuição de Engenharia de Dados desenvolvida para o projeto AF Sacolas, com foco na obtenção, estruturação, armazenamento e análise de dados públicos para contextualização do mercado de comércio eletrônico brasileiro.

## 1. Objetivo

Utilizar uma base de dados pública para extrair informações relevantes sobre o comércio eletrônico, transformando dados brutos em indicadores que auxiliem na fundamentação e contextualização do projeto AF Sacolas.

## 2. Fonte dos dados

Foi utilizado o **Brazilian E-Commerce Public Dataset by Olist**, disponibilizado publicamente no Kaggle.

A base contém informações históricas sobre pedidos, produtos, pagamentos e clientes do comércio eletrônico brasileiro, abrangendo o período de 2016 a 2018.

- **Fonte:** [Brazilian E-Commerce Public Dataset by Olist — Kaggle](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)

**Observação:** os dados não representam especificamente a comercialização de sacolas. São utilizados como referência para compreender a movimentação do comércio eletrônico e o contexto de mercado relacionado ao projeto.

## 3. Tecnologias utilizadas

- **MySQL:** criação e gerenciamento do banco de dados.
- **SQL:** consultas, agregações e análise dos dados.
- **CSV:** formato dos arquivos de origem.
- **Git e GitHub:** versionamento e documentação do trabalho.

## 4. Estrutura do banco de dados

O banco de dados `schema1_dados_publicos` foi estruturado com quatro tabelas:

| Tabela | Descrição |
|---|---|
| `orders` | Informações dos pedidos |
| `order_items` | Itens associados aos pedidos |
| `order_payments` | Informações dos pagamentos |
| `customers` | Informações geográficas dos clientes |

**Total importado: 415.418 registros.**

## 5. Processamento e análise

O desenvolvimento envolveu:

1. Obtenção dos arquivos CSV da fonte pública.
2. Organização e preparação dos arquivos.
3. Criação do banco de dados relacional no MySQL.
4. Criação das quatro tabelas.
5. Importação dos registros.
6. Desenvolvimento de consultas SQL para extração de indicadores.
7. Interpretação dos resultados obtidos.

Foram utilizadas funções como `SUM()`, `AVG()`, `MAX()`, `MIN()` e `COUNT()`, além de agrupamentos com `GROUP BY`, ordenações e relacionamentos entre tabelas.

## 6. Indicadores analisados

As consultas permitiram investigar:

- Volume financeiro dos produtos comercializados.
- Preço médio, maior e menor preço dos itens.
- Distribuição dos pagamentos por modalidade.
- Quantidade de pedidos e valores movimentados mensalmente.
- Situação dos pedidos.
- Distribuição geográfica das compras por estado.
- Valor médio por pedido em diferentes regiões.

Os resultados detalhados estão disponíveis em [resultados/indicadores.md](resultados/indicadores.md).

## 7. Organização dos arquivos

A contribuição está organizada da seguinte forma:

| Diretório/arquivo | Conteúdo |
|---|---|
| `database/` | Script de criação das tabelas |
| `importacao/` | Script de importação dos arquivos CSV |
| `analises/` | Consultas SQL utilizadas nas análises |
| `resultados/` | Indicadores e interpretação dos resultados |
| `documentacao/` | Documentação técnica e relatório em PDF |

### Principais arquivos

- [Criação das tabelas](database/01_criacao_tabelas.sql)
- [Importação dos dados CSV](importacao/02_importacao_csv.sql)
- [Consultas de análise SQL](analises/03_analises_sql.sql)
- [Resultados das análises](resultados/indicadores.md)
- [Documentação técnica](documentacao/README.md)

## 8. Relação com o projeto AF Sacolas

Os indicadores extraídos fornecem uma contextualização baseada em dados reais sobre o comércio eletrônico brasileiro.

Essas informações contribuem para fundamentar a relevância de uma solução digital voltada à comercialização de sacolas personalizadas, apoiando a compreensão do ambiente comercial no qual o sistema está inserido.

É importante destacar que a base utilizada não contém dados específicos sobre a venda de sacolas. Portanto, os resultados representam o contexto geral do comércio eletrônico, não uma medição direta da demanda pelo produto.

## 9. Considerações metodológicas

- Os valores financeiros apresentados referem-se aos preços dos produtos, exceto na análise de pagamentos.
- Os estados representam a localização dos clientes, não dos vendedores.
- O período analisado é histórico e termina em outubro de 2018.
- O ano de 2018 possui dados parciais, não devendo ser comparado diretamente como um ano completo.
- Os resultados foram obtidos por meio de consultas SQL no MySQL.

## 10. Considerações finais

A utilização de dados públicos permitiu aplicar conceitos de Engenharia de Dados na obtenção, estruturação, armazenamento e análise de informações reais.

O trabalho demonstra como dados disponíveis publicamente podem ser transformados em indicadores úteis para contextualizar e fundamentar o desenvolvimento de um projeto de software.
