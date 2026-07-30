# ADR-008 — Adoção da Arquitetura API-First

## Status

Accepted

---

# Contexto

O ecossistema CarneCerta é composto por diferentes módulos que compartilham informações, como o CarneCerta Web, Mobile, Insights e IoT.

Para garantir integração, escalabilidade e independência entre esses módulos, foi necessário definir uma estratégia de comunicação padronizada.

---

# Problema

A comunicação direta entre módulos aumenta o acoplamento e dificulta a evolução independente de cada aplicação.

Além disso, integrações específicas para cada módulo tornam a manutenção mais complexa.

---

# Decisão

Foi adotada uma abordagem **API-First**, na qual os serviços e contratos de comunicação são definidos antes da implementação dos consumidores.

Os módulos deverão acessar dados e funcionalidades por meio de APIs bem definidas, evitando dependências diretas entre aplicações.

---

# Diretrizes

- comunicação por APIs;
- contratos padronizados;
- baixo acoplamento entre módulos;
- reutilização de serviços;
- documentação das interfaces de integração.

---

# Benefícios

A abordagem API-First proporciona:

- integração simplificada;
- escalabilidade;
- reutilização de serviços;
- evolução independente dos módulos;
- facilidade para integração com sistemas externos.

---

# Consequências

## Positivas

- Maior flexibilidade arquitetural;
- Redução do acoplamento;
- Facilidade para criação de novos módulos;
- Melhor interoperabilidade.

## Negativas

- Necessidade de versionamento das APIs;
- Maior controle sobre contratos de integração.

---

# Decisões Relacionadas

- ADR-001 — Adoção de Arquitetura Modular
- ADR-002 — Adoção da Arquitetura de Dados