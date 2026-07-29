# ADR-005 — Accessibility by Design

## Status

Accepted

---

# Contexto

O CarneCerta foi concebido com o objetivo de oferecer uma experiência digital acessível para todos os usuários.

Durante a definição da arquitetura do ecossistema, foi identificado que consumidores com deficiência auditiva podem encontrar barreiras de comunicação durante o processo de compra em plataformas digitais.

Diante desse cenário, a acessibilidade passou a ser tratada como um requisito arquitetural do projeto, influenciando decisões de desenvolvimento, interface e experiência do usuário.

---

# Problema

Implementar recursos de acessibilidade apenas após o desenvolvimento da plataforma aumenta o custo de manutenção, dificulta a padronização das interfaces e pode comprometer a experiência dos usuários.

Além disso, soluções pontuais não garantem que a acessibilidade seja aplicada de forma consistente em todos os módulos do ecossistema.

---

# Decisão

Foi adotado o princípio **Accessibility by Design**, incorporando requisitos de acessibilidade desde a concepção do projeto.

Todos os novos módulos e funcionalidades deverão considerar acessibilidade durante as fases de planejamento, arquitetura, desenvolvimento e testes.

O módulo **CarneCerta Web** deverá disponibilizar recursos voltados à inclusão, incluindo suporte à tradução da interface para Libras.

---

# Diretrizes

As decisões de desenvolvimento deverão considerar, sempre que aplicável:

- utilização de HTML semântico;
- contraste adequado entre cores;
- navegação por teclado;
- textos alternativos para imagens;
- compatibilidade com leitores de tela;
- interfaces claras e consistentes;
- suporte à tradução para Libras;
- conformidade gradual com as diretrizes WCAG.

---

# Benefícios

A adoção desse princípio proporciona:

- maior inclusão digital;
- melhor experiência para diferentes perfis de usuários;
- redução de retrabalho;
- padronização dos recursos de acessibilidade;
- evolução contínua da plataforma.

---

# Consequências

## Positivas

- Acessibilidade considerada desde o início do projeto;
- Interfaces mais inclusivas;
- Arquitetura preparada para novas tecnologias assistivas;
- Melhor qualidade da experiência do usuário.

## Negativas

- Necessidade de validações adicionais durante o desenvolvimento;
- Maior atenção aos padrões de acessibilidade durante a implementação.

---

# Decisões Relacionadas

- ADR-001 — Adoção de Arquitetura Modular
- Architecture Overview
- Requirements
- Operations / Accessibility