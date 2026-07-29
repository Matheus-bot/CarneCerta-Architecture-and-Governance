# ADR-001 — Adoção de Arquitetura Modular

## Status

Accepted

---

# Contexto

O CarneCerta foi concebido como um ecossistema composto por diferentes soluções, cada uma responsável por atender necessidades específicas dos usuários e do negócio.

Entre os módulos previstos estão:

- CarneCerta Web;
- CarneCerta Mobile;
- CarneCerta Insights;
- CarneCerta IoT.

A evolução do projeto exigia uma arquitetura que permitisse desenvolver e manter esses módulos de forma independente.

---

# Problema

Uma arquitetura monolítica concentraria todas as responsabilidades em um único sistema, aumentando o acoplamento entre componentes e dificultando:

- manutenção;
- evolução do projeto;
- reutilização de funcionalidades;
- escalabilidade;
- organização do código.

---

# Decisão

Foi adotada uma arquitetura modular, organizada em módulos independentes, cada um com responsabilidades bem definidas.

Cada módulo poderá evoluir individualmente, mantendo compatibilidade com o restante do ecossistema por meio de integrações previamente definidas.

---

# Estrutura Adotada

```text
CarneCerta

├── Web
├── Mobile
├── Insights
└── IoT
```

Cada módulo possui objetivos específicos:

| Módulo | Responsabilidade |
|--------|------------------|
| CarneCerta Web | Interface principal da plataforma e experiência do usuário. |
| CarneCerta Mobile | Disponibilizar funcionalidades em dispositivos móveis. |
| CarneCerta Insights | Processamento analítico e Business Intelligence. |
| CarneCerta IoT | Integração com dispositivos inteligentes e sensores. |

---

# Benefícios

A adoção da arquitetura modular proporciona:

- baixo acoplamento entre módulos;
- alta coesão;
- evolução independente dos componentes;
- facilidade de manutenção;
- escalabilidade;
- reutilização de componentes;
- organização da documentação técnica.

---

# Consequências

## Positivas

- Maior organização da solução;
- Facilidade para adicionar novos módulos;
- Melhor manutenção do código;
- Evolução incremental do ecossistema.

## Negativas

- Maior necessidade de padronização entre módulos;
- Necessidade de documentar integrações e responsabilidades de cada componente.

---

# Decisões Relacionadas

- ADR-002 — Adoção da Arquitetura de Dados (OLTP + Data Warehouse)
- ADR-003 — Adoção do Star Schema
- ADR-004 — Arquitetura do CarneCerta Insights
- ADR-005 — Acessibilidade como Princípio Arquitetural