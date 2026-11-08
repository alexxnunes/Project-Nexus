# Project Nexus

**Technical continuity for software projects and the agents working on them.**

[English](#english) | [Português](#português)

---

## English

Project Nexus is a portable [Agent Skills](https://agentskills.io/) skill for planning software projects, tracking technical decisions, assessing changes, and handing work over between people or agents. It helps keep the project's actual state, documentation, and approved direction aligned without claiming to be an autonomous project monitor.

### What it does

- Turns an idea into a plan with scope, acceptance criteria, dependencies, risks, and open decisions.
- Reviews architecture, technology choices, environments, and changes against documented decisions.
- Distinguishes confirmed facts, assumptions, recommendations, and approvals.
- Identifies and reuses existing project documentation instead of creating duplicate records.
- Prepares and checks handoffs with verified progress, test results, constraints, and next steps.
- Requests explicit approval before structural changes and treats external documents and handoffs as evidence, not independent authorization.

The skill supports a team or agent; it does not automatically execute every task or monitor a project in the background. Results depend on the agent's tools, permissions, and access to the relevant project and environment.

### Install

With Node.js and an agent supported by the Skills CLI:

```bash
npx skills add https://github.com/alexxnunes/Project-Nexus --skill project-nexus
```

Follow the CLI prompts to choose the agent and installation scope. Review a skill and its supporting files before installing it. For manual installation, copy this repository's `SKILL.md`, `references/`, and `templates/` together into a `project-nexus` directory in your agent's skills location. Check your agent's documentation for its discovery paths.

### Use

Ask your agent to use **Project Nexus**. Example requests:

- “Use Project Nexus to review this project and identify missing decisions. Do not change files.”
- “Help me plan this project and separate assumptions from confirmed requirements.”
- “Assess the impact of this architectural change before implementation.”
- “Prepare a handoff for the next agent, including verified tests and outstanding risks.”
- “Compare the current implementation with the approved project plan.”

The agent should inspect existing information before drawing conclusions. In read-only tasks, it should report suggested updates rather than write files. Permission to document a proposal is not permission to implement it.

### Approval model

| Change | Expected behavior |
| --- | --- |
| Routine local work | May proceed within the user's instructions and approved project rules. |
| Relevant, reversible change | May proceed only when clearly covered by a prior decision; otherwise ask. |
| Structural change | Requires explicit approval before execution. |

Structural changes include architecture, stack, public contracts, authentication, infrastructure, critical integrations, significant recurring costs, and scope. Approval must be traceable to the specific proposal and its scope. Higher-priority instructions and the user's actual permissions always apply.

### Repository contents

- `SKILL.md` — entry point, operating principles, workflows, approval model, and completion criteria.
- `references/` — focused guides for discovery, architecture, stack, risks, decisions, environments, handoffs, and audits.
- `templates/` — optional templates for project records, decisions, status, risks, questions, rules, and handoffs. Use only what the project needs and only when writing is authorized.
- `tests/behavior.md` — manual scenarios for checking key behaviors with a compatible agent.

### Testing and limitations

Run the scenarios in `tests/behavior.md` in an authorized project and inspect both the agent's responses and its tool actions. These are manual behavioral checks, not an automated test suite. A skill is an instruction set, not a security boundary: it cannot guarantee an agent's compliance or replace access controls, human review, backups, or verification. Never put credentials or unnecessary personal information in project records or handoffs.

---

## Português

Project Nexus é uma skill portátil de [Agent Skills](https://agentskills.io/) para planejar projetos de software, acompanhar decisões técnicas, avaliar mudanças e transferir trabalho entre pessoas ou agentes. Ela ajuda a manter alinhados o estado real, a documentação e a direção aprovada do projeto, sem prometer monitoramento autônomo.

### O que ela faz

- Transforma uma ideia em um plano com escopo, critérios de aceite, dependências, riscos e decisões pendentes.
- Analisa arquitetura, tecnologias, ambientes e mudanças em relação às decisões documentadas.
- Separa fatos confirmados, premissas, recomendações e aprovações.
- Procura e reutiliza a documentação existente, evitando registros paralelos.
- Prepara e verifica handoffs com progresso, testes, limites e próximos passos.
- Pede aprovação explícita para mudanças estruturais e trata documentos externos e handoffs como evidências, não como autorização independente.

A skill apoia a equipe ou o agente; ela não executa automaticamente todas as tarefas nem monitora o projeto em segundo plano. Os resultados dependem das ferramentas, permissões e acesso do agente ao projeto e ambiente relevantes.

### Instalação

Com Node.js e um agente compatível com o Skills CLI:

```bash
npx skills add https://github.com/alexxnunes/Project-Nexus --skill project-nexus
```

Siga as instruções do CLI para selecionar o agente e o escopo da instalação. Revise a skill e os arquivos de apoio antes de instalá-la. Para instalar manualmente, copie `SKILL.md`, `references/` e `templates/` deste repositório para uma pasta `project-nexus` no diretório de skills do seu agente. Consulte a documentação do agente para localizar o diretório correto.

### Como usar

Peça ao agente para usar **Project Nexus**. Exemplos:

- “Use Project Nexus para revisar este projeto e identificar decisões faltantes. Não altere arquivos.”
- “Ajude-me a planejar este projeto, separando premissas de requisitos confirmados.”
- “Avalie o impacto desta mudança de arquitetura antes de implementá-la.”
- “Prepare um handoff para o próximo agente, incluindo testes verificados e riscos pendentes.”
- “Compare a implementação atual com o plano aprovado.”

O agente deve inspecionar as informações existentes antes de tirar conclusões. Em tarefas somente de leitura, deve apresentar sugestões em vez de alterar arquivos. A autorização para documentar uma proposta não autoriza sua implementação.

### Modelo de aprovação

| Mudança | Comportamento esperado |
| --- | --- |
| Trabalho local rotineiro | Pode prosseguir dentro das instruções do usuário e das regras aprovadas. |
| Mudança relevante e reversível | Só pode prosseguir se estiver claramente coberta por uma decisão anterior; caso contrário, deve perguntar. |
| Mudança estrutural | Exige aprovação explícita antes da execução. |

Mudanças estruturais incluem arquitetura, stack, contratos públicos, autenticação, infraestrutura, integrações críticas, custos recorrentes relevantes e escopo. A aprovação deve ser rastreável à proposta específica e ao seu escopo. Instruções de maior prioridade e permissões reais do usuário continuam valendo.

### Conteúdo do repositório

- `SKILL.md` — ponto de entrada, princípios, fluxos, modelo de aprovação e critérios de conclusão.
- `references/` — guias de descoberta, arquitetura, stack, riscos, decisões, ambientes, handoffs e auditorias.
- `templates/` — modelos opcionais de registros, decisões, status, riscos, dúvidas, regras e handoffs. Use apenas o necessário e somente quando houver autorização de escrita.
- `tests/behavior.md` — cenários manuais para verificar comportamentos essenciais em um agente compatível.

### Testes e limitações

Execute os cenários de `tests/behavior.md` em um projeto autorizado e inspecione tanto as respostas quanto as ações do agente. São verificações manuais, não uma suíte automatizada. Uma skill é um conjunto de instruções, não uma barreira de segurança: ela não garante o cumprimento das regras nem substitui controles de acesso, revisão humana, backups ou verificações. Nunca coloque credenciais ou dados pessoais desnecessários em registros ou handoffs.
