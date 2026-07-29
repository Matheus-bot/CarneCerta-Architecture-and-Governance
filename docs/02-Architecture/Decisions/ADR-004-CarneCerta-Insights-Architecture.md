# ADR-004 — Arquitetura do Módulo CarneCerta Insights

## Status

Accepted

---

# Contexto

O **CarneCerta Insights** é o módulo responsável pela camada analítica do ecossistema CarneCerta.

Seu objetivo é transformar dados operacionais em informações estratégicas, apoiando gestores na tomada de decisão por meio de indicadores, consultas analíticas e dashboards.

Para atender esse objetivo, foi definida uma arquitetura separada do ambiente operacional, baseada em um processo ETL e em um Data Warehouse.

---

# Problema

Os módulos operacionais do CarneCerta são responsáveis por registrar transações do sistema.

Executar consultas analíticas diretamente sobre esses dados aumentaria a complexidade das consultas, dificultaria a manutenção e poderia impactar o desempenho das aplicações.

Além disso, era necessário criar uma estrutura preparada para crescimento futuro da camada analítica.

---

# Decisão

Foi adotada uma arquitetura composta por cinco camadas independentes:

1. Banco Operacional;
2. Processo ETL;
3. Data Warehouse;
4. Camada Analítica;
5. Visualização em Power BI.

Cada camada possui responsabilidades específicas e pode evoluir independentemente das demais.

---

# Arquitetura Adotada

```mermaid
flowchart LR

OLTP["Banco Operacional"]

ETL["ETL"]

DW["Data Warehouse"]

Analytics["Consultas Analíticas"]

PowerBI["Power BI"]

OLTP --> ETL

ETL --> DW

DW --> Analytics

Analytics --> PowerBI
```

---

# Organização das Camadas

## Banco Operacional

Responsável pelo armazenamento das informações utilizadas pelos módulos operacionais do ecossistema.

Exemplos:

- clientes;
- produtos;
- vendas;
- itens de venda.

---

## Processo ETL

Responsável por:

- extrair os dados;
- transformar informações;
- padronizar registros;
- carregar o Data Warehouse.

---

## Data Warehouse

Responsável pelo armazenamento analítico.

Foi adotado o modelo **Star Schema**, composto por tabelas fato e dimensões.

---

## Camada Analítica

Responsável pelas consultas SQL utilizadas para responder perguntas de negócio, como:

- produtos mais vendidos;
- faturamento por categoria;
- ticket médio;
- lucro por período;
- evolução das vendas.

---

## Power BI

Responsável pela apresentação visual dos indicadores por meio de dashboards.

---

# Princípios Arquiteturais

A arquitetura do CarneCerta Insights segue os seguintes princípios:

- separação entre ambiente operacional e analítico;
- arquitetura em camadas;
- modelagem dimensional;
- baixo acoplamento;
- escalabilidade;
- facilidade de manutenção;
- documentação contínua.

---

# Benefícios

A arquitetura adotada oferece:

- melhor desempenho para consultas analíticas;
- organização da camada de dados;
- facilidade para evolução do Data Warehouse;
- integração com ferramentas de Business Intelligence;
- reutilização das consultas analíticas.

---

# Consequências

## Positivas

- Ambiente analítico independente;
- Melhor organização dos scripts SQL;
- Facilidade para expansão do modelo dimensional;
- Consultas mais eficientes para dashboards.

## Negativas

- Dependência do processo ETL para atualização dos dados;
- Maior quantidade de componentes para manutenção.

---

# Decisões Relacionadas

- ADR-001 — Adoção de Arquitetura Modular
- ADR-002 — Adoção da Arquitetura de Dados (OLTP + Data Warehouse)
- ADR-003 — Adoção do Star Schema