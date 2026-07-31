# Monitoring

## Objetivo

Este documento define as diretrizes de monitoramento adotadas pelo ecossistema CarneCerta.

O objetivo é acompanhar a disponibilidade, desempenho, integridade e funcionamento das aplicações, permitindo identificar e corrigir problemas de forma rápida e eficiente.

---

# Objetivos do Monitoramento

O monitoramento busca:

- garantir a disponibilidade das aplicações;
- identificar falhas rapidamente;
- acompanhar o desempenho dos serviços;
- apoiar a manutenção preventiva;
- fornecer informações para melhoria contínua.

---

# O que Deve ser Monitorado

Sempre que possível, deverão ser monitorados:

- disponibilidade da aplicação;
- tempo de resposta;
- utilização de recursos;
- registros de erro (logs);
- integrações entre módulos;
- funcionamento das APIs.

---

# Logs

Os sistemas deverão registrar eventos relevantes para facilitar a identificação de problemas.

Exemplos:

- erros da aplicação;
- falhas de autenticação;
- exceções não tratadas;
- falhas de integração;
- eventos críticos do sistema.

Os logs não devem expor informações sensíveis dos usuários.

---

# Indicadores

Alguns indicadores recomendados incluem:

- disponibilidade da aplicação;
- tempo médio de resposta;
- quantidade de erros;
- tempo médio para recuperação (MTTR);
- frequência de falhas.

---

# Alertas

Sempre que possível, o sistema deverá gerar alertas para situações como:

- indisponibilidade da aplicação;
- aumento significativo de erros;
- falhas em integrações;
- degradação de desempenho.

---

# Monitoramento da Acessibilidade

Considerando o compromisso do CarneCerta com a inclusão, recomenda-se acompanhar periodicamente o funcionamento dos recursos de acessibilidade.

Exemplos:

- navegação por teclado;
- contraste das interfaces;
- compatibilidade com leitores de tela;
- funcionamento do recurso de tradução para Libras;
- disponibilidade dos recursos de acessibilidade após novas versões.

---

# Melhoria Contínua

As informações obtidas por meio do monitoramento deverão apoiar:

- identificação de gargalos;
- planejamento de melhorias;
- evolução da arquitetura;
- aumento da confiabilidade das aplicações.

---

# Documentos Relacionados

- security.md
- testing.md
- ci-cd.md
- deployment.md
- accessibility.md