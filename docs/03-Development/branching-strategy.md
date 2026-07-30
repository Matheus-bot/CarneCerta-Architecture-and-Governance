# Branching Strategy

## Objetivo

Este documento define a estratégia de branches adotada no ecossistema CarneCerta.

Seu objetivo é organizar o desenvolvimento, facilitar a colaboração entre desenvolvedores e garantir a estabilidade dos projetos durante sua evolução.

---

# Branches Principais

## main

A branch `main` representa a versão estável do projeto.

Características:

- contém apenas código validado;
- representa versões prontas para uso;
- recebe alterações somente após revisão e aprovação.

---

## develop

A branch `develop` concentra o desenvolvimento das próximas versões.

Características:

- integração de novas funcionalidades;
- base para testes antes da publicação;
- utilizada como origem para novas branches de desenvolvimento.

---

# Branches de Apoio

## feature/*

Utilizada para o desenvolvimento de novas funcionalidades.

Exemplos:

```
feature/login

feature/dashboard

feature/accessibility
```

Após a conclusão, a branch deve ser integrada à `develop`.

---

## fix/*

Utilizada para correção de defeitos identificados durante o desenvolvimento.

Exemplos:

```
fix/login-validation

fix/product-filter
```

---

## docs/*

Utilizada para alterações na documentação.

Exemplos:

```
docs/update-readme

docs/architecture-review
```

---

## release/*

Utilizada para preparar uma nova versão do projeto.

Exemplo:

```
release/v1.0.0
```

Durante essa etapa são realizados:

- testes finais;
- ajustes de documentação;
- correções menores.

---

## hotfix/*

Utilizada para corrigir problemas críticos encontrados após uma versão publicada.

Exemplo:

```
hotfix/security-patch
```

Após a correção, a alteração deve ser integrada às branches correspondentes.

---

# Fluxo de Branches

```text
main
 ▲
 │
release/*
 ▲
 │
develop
 ▲
 │
feature/*
fix/*
docs/*
```

---

# Boas Práticas

- criar uma branch para cada atividade;
- utilizar nomes descritivos;
- manter branches pequenas e objetivas;
- remover branches concluídas;
- evitar desenvolvimento diretamente na `main`.

---

# Convenções de Nome

| Tipo | Exemplo |
|------|----------|
| feature | feature/customer-registration |
| fix | fix/login-error |
| docs | docs/update-roadmap |
| release | release/v1.0.0 |
| hotfix | hotfix/security-fix |

---

# Documentos Relacionados

- git-workflow.md
- coding-standards.md
- ADR-006 — Adoção do Git Workflow e Estratégia de Branches