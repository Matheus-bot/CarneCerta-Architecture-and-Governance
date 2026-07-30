# Git Workflow

## Objetivo

Este documento descreve o fluxo de trabalho adotado para versionamento e colaboração no ecossistema CarneCerta.

O objetivo é garantir organização, rastreabilidade e estabilidade durante o desenvolvimento dos diferentes módulos do projeto.

---

# Fluxo de Desenvolvimento

O desenvolvimento segue um fluxo baseado em branches, permitindo que novas funcionalidades, correções e documentação sejam desenvolvidas de forma isolada antes da integração ao projeto principal.

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

# Processo

## 1. Atualizar a branch principal

Antes de iniciar qualquer atividade:

- atualizar a branch local;
- sincronizar com o repositório remoto.

---

## 2. Criar uma nova branch

Cada tarefa deve ser desenvolvida em uma branch específica.

Exemplos:

```
feature/login
feature/dashboard

fix/login-validation

docs/update-readme

release/v1.0.0

hotfix/security-fix
```

---

## 3. Desenvolvimento

Durante o desenvolvimento:

- realizar commits pequenos e objetivos;
- utilizar mensagens semânticas;
- manter o código atualizado com a documentação.

---

## 4. Revisão

Antes da integração:

- revisar o código;
- executar testes;
- validar a documentação;
- confirmar que não existem conflitos.

---

## 5. Integração

Após a validação:

- integrar a branch ao ambiente correspondente;
- remover branches que não serão mais utilizadas.

---

# Commits

Utilizar Commits Semânticos.

Exemplos:

```
feat: add customer registration

fix: correct login validation

docs: update architecture documentation

refactor: improve authentication service

style: format source code

test: add unit tests

chore: update dependencies
```

---

# Pull Requests

Sempre que aplicável:

- descrever o objetivo da alteração;
- informar arquivos modificados;
- relacionar a alteração aos documentos ou ADRs relevantes;
- solicitar revisão antes da integração.

---

# Boas Práticas

- manter branches pequenas;
- evitar commits com múltiplos objetivos;
- atualizar a documentação sempre que necessário;
- manter histórico limpo e organizado;
- utilizar mensagens de commit padronizadas.

---

# Documentos Relacionados

- branch-strategy.md
- ADR-006 — Adoção do Git Workflow e Estratégia de Branches