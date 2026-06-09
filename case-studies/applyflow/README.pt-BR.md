# Estudo de Caso — ApplyFlow

O **ApplyFlow** é um assistente local-first para organizar candidaturas, acompanhar vagas, reutilizar respostas, analisar oportunidades e apoiar a produtividade de candidatos com foco em privacidade.

Este estudo de caso documenta a visão de produto, arquitetura e decisões de engenharia por trás do ApplyFlow.

---

## Contexto do Produto

Aplicar para vagas é um processo repetitivo, difícil de acompanhar e normalmente mal organizado. Candidatos costumam usar planilhas, histórico do navegador, anotações e lembretes manuais para controlar suas candidaturas.

O ApplyFlow foi pensado para trazer estrutura, visibilidade e automação segura para esse fluxo.

---

## Problema

Candidatos enfrentam problemas como:

- Perder o controle das candidaturas enviadas
- Repetir as mesmas informações em formulários
- Não saber quais vagas priorizar
- Não ter métricas claras do funil de candidaturas
- Espalhar dados de carreira em várias ferramentas
- Correr risco de enviar candidaturas de baixa qualidade por automação cega

---

## Solução

O ApplyFlow oferece um fluxo local-first com histórico de candidaturas, banco de respostas reutilizáveis, análise de vagas, métricas e coaching opcional com IA.

O produto prioriza qualidade, controle e privacidade em vez de automação em massa.

---

## Princípios do Produto

- Dados local-first
- Privacidade por padrão
- Human-in-the-loop
- Sem envio automático cego
- Exportação/importação em JSON
- Camada de IA opcional
- Dados de carreira sob controle do usuário

---

## Arquitetura Resumida

```text
Camada de Extensão do Navegador
  ├── Interação com páginas
  ├── Armazenamento local
  ├── Sugestões assistidas de campos
  └── Fluxo de revisão pelo usuário

Pacotes TypeScript Compartilhados
  ├── Contratos de domínio
  ├── Helpers de análise de vagas
  ├── Estruturas de dados do candidato
  └── Schemas de importação/exportação

Dashboard Next.js
  ├── Funil de candidaturas
  ├── Métricas
  ├── Acompanhamento de vagas
  ├── Banco de respostas
  └── Coaching opcional com IA
```

---

## Stack Técnica

- Next.js
- React
- TypeScript
- Tailwind CSS
- Chrome Extension MV3
- Browser Local Storage
- JSON import/export
- OpenAI opcional

---

## Diferencial do Produto

O ApplyFlow não é um robô de candidatura em massa. Ele é um assistente de workflow projetado para melhorar organização, qualidade e visibilidade, mantendo o usuário no controle.

---

## Valor para Portfólio

Este case demonstra pensamento de produto aplicado a privacidade, automação responsável, extensão de navegador, produtividade e fluxos assistidos por IA.

---

## Documentos Relacionados

- [Architecture](architecture.md)
- [Privacy Decisions](privacy-decisions.md)
- [Recruiter Notes](recruiter-notes.md)

---

## Links

- Repositório do case: https://github.com/devflow-modules/applyflow-case-study
- Portfólio: https://devflowlabs.com.br
