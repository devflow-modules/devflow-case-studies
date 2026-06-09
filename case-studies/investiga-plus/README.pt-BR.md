# Estudo de Caso — Investiga+

O **Investiga+** é uma plataforma SaaS para inteligência de CNPJ, consulta de dados empresariais, autenticação segura, cache de buscas, histórico por usuário e análise em dashboard.

Este estudo de caso documenta a visão de produto, arquitetura e decisões técnicas por trás do Investiga+ dentro do ecossistema DevFlow Labs.

---

## Contexto do Produto

Empresas brasileiras frequentemente precisam consultar e validar dados de CNPJ para processos comerciais, administrativos, operacionais e de prospecção.

O Investiga+ foi criado para centralizar esse fluxo em uma experiência SaaS com autenticação segura, histórico de buscas, estratégia de cache e arquitetura fullstack modular.

---

## Problema

Dores resolvidas pelo produto:

- Consultas repetitivas de CNPJ em ferramentas desconectadas
- Falta de histórico de buscas
- Chamadas repetidas para APIs externas
- Necessidade de acesso seguro por usuário
- Falta de dashboard limpo para visualizar dados empresariais
- Dificuldade de evoluir o fluxo sem backend modular

---

## Solução

O Investiga+ oferece uma interface SaaS em que usuários autenticados podem consultar CNPJs, visualizar dados empresariais, armazenar histórico e reutilizar resultados em cache quando disponíveis.

O sistema foi pensado como produto real, não apenas como demonstração técnica.

---

## Funcionalidades Principais

- Autenticação JWT com Cookies HttpOnly
- Consulta de CNPJ via integração com API externa
- Estratégia de cache local para buscas repetidas
- Histórico de buscas por usuário
- Dashboard responsivo
- Área de perfil e uso
- Backend modular
- Testes automatizados com Jest
- Prisma ORM com PostgreSQL/SQLite
- Estrutura pronta para CI/CD

---

## Arquitetura Resumida

```text
Frontend Next.js
  ├── Landing page
  ├── Login e autenticação
  ├── Dashboard
  ├── Busca de CNPJ
  ├── Histórico de buscas
  └── Área de perfil

Backend Node.js + Express
  ├── Módulo de autenticação
  ├── Módulo de consulta CNPJ
  ├── Módulo de histórico
  ├── Middlewares de validação
  ├── Tratamento de erros
  └── Camada de integração externa

Banco de Dados
  ├── Prisma ORM
  ├── Usuários
  ├── Histórico de buscas
  └── Empresas em cache
```

---

## Stack Técnica

- Next.js
- React
- Chakra UI
- Framer Motion
- Node.js
- Express.js
- Prisma ORM
- PostgreSQL
- SQLite para desenvolvimento local
- JWT
- Cookies HttpOnly
- Jest
- Docker
- GitHub Actions

---

## Valor para Portfólio

Este case demonstra capacidade de transformar uma operação de negócio repetitiva em um produto SaaS com autenticação, persistência, histórico, integrações, cache e uma base escalável.

---

## Documentos Relacionados

- [Architecture](architecture.md)
- [Security Decisions](security-decisions.md)
- [Product Roadmap](product-roadmap.md)
- [Business Context](business-context.md)
- [Recruiter Notes](recruiter-notes.md)

---

## Links

- Repositório: https://github.com/devflow-modules/investiga-mais
- Produção: https://investigamais.com
- Portfólio: https://devflowlabs.com.br
