# Coding Standards

## Objetivo

Este documento define os padrões de código adotados pelo ecossistema CarneCerta.

Seu objetivo é promover consistência, legibilidade, manutenibilidade e qualidade do código em todos os módulos do projeto.

---

# Princípios

Todo código desenvolvido para o CarneCerta deve seguir os seguintes princípios:

- simplicidade;
- legibilidade;
- reutilização;
- baixo acoplamento;
- alta coesão;
- responsabilidade única;
- documentação quando necessária.

---

# Convenções de Nomenclatura

## Arquivos

Utilizar nomes descritivos e consistentes.

Exemplos:

```
customer-service.ts
product-controller.java
sales-report.sql
```

---

## Variáveis

Utilizar nomes claros e significativos.

Exemplo:

```
totalRevenue
customerName
saleDate
```

Evitar abreviações desnecessárias.

---

## Funções e Métodos

Devem representar claramente a ação executada.

Exemplos:

```
calculateTotal()
findCustomerById()
generateSalesReport()
```

---

## Classes

Utilizar substantivos no padrão PascalCase.

Exemplos:

```
CustomerService
SalesRepository
ProductController
```

---

# Organização do Código

Sempre que possível:

- separar responsabilidades;
- evitar duplicação;
- criar componentes reutilizáveis;
- manter arquivos pequenos;
- agrupar funcionalidades relacionadas.

---

# Comentários

Comentários devem explicar decisões importantes e não repetir o que o código já demonstra.

Priorizar código autoexplicativo.

---

# Tratamento de Erros

Sempre que possível:

- tratar exceções adequadamente;
- registrar erros relevantes;
- evitar falhas silenciosas;
- retornar mensagens claras ao usuário.

---

# Qualidade

Antes de enviar alterações para o repositório, verificar:

- funcionamento da funcionalidade;
- remoção de código morto;
- remoção de comentários temporários;
- padronização da formatação;
- atualização da documentação quando necessário.

---

# Acessibilidade

Durante o desenvolvimento das interfaces, considerar:

- HTML semântico;
- contraste adequado;
- navegação por teclado;
- textos alternativos para imagens;
- compatibilidade com leitores de tela;
- suporte aos recursos de acessibilidade definidos para o projeto.

---

# Referências

- ADR-005 — Accessibility by Design
- ADR-006 — Git Workflow
- ADR-007 — Padronização da Documentação Técnica