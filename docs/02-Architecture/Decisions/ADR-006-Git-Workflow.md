# ADR-006 — Adoção do Git Workflow e Estratégia de Branches

## Status

Accepted

---

# Contexto

O desenvolvimento do ecossistema CarneCerta envolve múltiplos módulos, documentação técnica e evolução contínua do código-fonte.

Era necessário definir uma estratégia de versionamento que garantisse organização, rastreabilidade e estabilidade durante o desenvolvimento.

---

# Problema

A ausência de um fluxo de trabalho definido pode causar:

- conflitos entre alterações;
- dificuldade para identificar mudanças;
- perda de histórico;
- redução da qualidade do código;
- dificuldade na colaboração.

---

# Decisão

Foi adotado um Git Workflow baseado em branches com responsabilidades bem definidas.

Cada alteração deverá ser desenvolvida em uma branch específica antes de ser integrada à branch principal.

---

# Estratégia de Branches

| Branch | Finalidade |
|---------|------------|
| `main` | Versões estáveis do projeto. |
| `develop` | Integração das funcionalidades em desenvolvimento. |
| `feature/*` | Desenvolvimento de novas funcionalidades. |
| `fix/*` | Correção de bugs. |
| `docs/*` | Atualizações da documentação. |
| `release/*` | Preparação de novas versões. |
| `hotfix/*` | Correções críticas em produção. |

---

# Fluxo de Desenvolvimento

```text
feature/*
      │
      ▼
develop
      │
      ▼
release/*
      │
      ▼
main
```

---

# Boas Práticas

- utilizar Commits Semânticos;
- manter branches pequenas e objetivas;
- revisar alterações antes da integração;
- documentar decisões arquiteturais quando necessário;
- manter a documentação sincronizada com a evolução do projeto.

---

# Benefícios

A estratégia adotada proporciona:

- organização do desenvolvimento;
- histórico de alterações mais claro;
- maior estabilidade da branch principal;
- facilidade para manutenção e evolução do projeto.

---

# Consequências

## Positivas

- Processo de desenvolvimento padronizado;
- Melhor rastreabilidade das alterações;
- Redução de conflitos entre branches;
- Facilidade para colaboração.

## Negativas

- Necessidade de seguir o fluxo definido;
- Maior disciplina no gerenciamento das branches.

---

# Decisões Relacionadas

- ADR-001 — Adoção de Arquitetura Modular
- ADR-007 — Padronização da Documentação Técnica