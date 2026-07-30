# Development Guidelines

## Objetivo

Este documento reúne as diretrizes gerais de desenvolvimento adotadas no ecossistema CarneCerta.

Seu objetivo é garantir consistência, qualidade, segurança e facilidade de manutenção durante todo o ciclo de vida do software.

---

# Princípios de Desenvolvimento

Todo desenvolvimento deve seguir os seguintes princípios:

- simplicidade;
- legibilidade;
- modularidade;
- reutilização de código;
- baixo acoplamento;
- alta coesão;
- documentação contínua.

---

# Planejamento

Antes de iniciar uma nova funcionalidade, recomenda-se:

- compreender o requisito de negócio;
- avaliar impactos na arquitetura;
- verificar ADRs relacionados;
- definir a estratégia de implementação.

---

# Desenvolvimento

Durante a implementação:

- seguir os padrões definidos em `coding-standards.md`;
- manter responsabilidades bem definidas;
- evitar duplicação de código;
- utilizar nomes claros e descritivos;
- escrever código de fácil manutenção.

---

# Versionamento

Toda alteração deve:

- ser desenvolvida em uma branch específica;
- utilizar Commits Semânticos;
- seguir o fluxo definido em `git-workflow.md`.

---

# Revisão de Código

Antes da integração, verificar:

- funcionamento da funcionalidade;
- conformidade com os padrões do projeto;
- ausência de código desnecessário;
- atualização da documentação, quando aplicável.

---

# Documentação

Sempre que uma alteração impactar a arquitetura, o funcionamento ou a utilização do sistema:

- atualizar a documentação correspondente;
- registrar novas decisões arquiteturais por meio de ADRs, quando necessário.

---

# Qualidade

Priorizar:

- código limpo;
- componentes reutilizáveis;
- tratamento adequado de erros;
- facilidade de manutenção;
- consistência entre os módulos.

---

# Acessibilidade

Todos os módulos do ecossistema devem considerar os princípios definidos no ADR-005.

Sempre que aplicável:

- utilizar HTML semântico;
- garantir navegação por teclado;
- manter contraste adequado;
- fornecer alternativas textuais para conteúdos visuais;
- desenvolver interfaces acessíveis para diferentes perfis de usuários;
- considerar recursos voltados à comunidade surda, incluindo suporte à tradução para Libras na plataforma Web.

---

# Evolução Contínua

As práticas descritas neste documento deverão ser revisadas periodicamente, acompanhando a evolução tecnológica do ecossistema CarneCerta e as necessidades do projeto.

---

# Documentos Relacionados

- coding-standards.md
- git-workflow.md
- branching-strategy.md
- ADR-005 — Accessibility by Design
- ADR-006 — Git Workflow e Estratégia de Branches
- ADR-007 — Padronização da Documentação Técnica