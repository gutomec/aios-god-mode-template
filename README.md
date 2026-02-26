<h1 align="center">
  ⚡ create-aios-god-mode
</h1>

<p align="center">
  <strong>Monte um sistema completo de desenvolvimento orquestrado por IA em segundos.</strong><br>
  <sub>10 agentes de IA. 22 skills. 3 servidores MCP. Um único comando.</sub>
</p>

<p align="center">
  <a href="https://www.npmjs.com/package/create-aios-god-mode"><img src="https://img.shields.io/npm/v/create-aios-god-mode?style=flat-square&color=cb3837&label=npm" alt="npm version"></a>
  <a href="https://www.npmjs.com/package/create-aios-god-mode"><img src="https://img.shields.io/npm/dm/create-aios-god-mode?style=flat-square&color=blue" alt="npm downloads"></a>
  <a href="https://github.com/gutomec/create-aios-god-mode/blob/main/LICENSE"><img src="https://img.shields.io/npm/l/create-aios-god-mode?style=flat-square&color=green" alt="license"></a>
  <img src="https://img.shields.io/node/v/create-aios-god-mode?style=flat-square&color=339933" alt="node version">
</p>

<p align="center">
  <a href="#-início-rápido">Início Rápido</a> ·
  <a href="#-veja-em-ação">Exemplos</a> ·
  <a href="#-o-que-você-recebe">O Que Você Recebe</a> ·
  <a href="#-funcionalidades">Funcionalidades</a> ·
  <a href="#-comandos">Comandos</a> ·
  <a href="#-agentes-de-ia">Agentes</a> ·
  <a href="#-skills-do-ecossistema">Skills</a>
</p>

<br>

<p align="center">
  <sub>
    Baseado no <a href="https://github.com/SynkraAI/aios-core"><strong>Synkra AIOS</strong></a> por <a href="https://github.com/Pedrovaleriolopez"><strong>Pedro Valério</strong></a> · Construído sobre o <a href="https://docs.anthropic.com/en/docs/claude-code"><strong>Claude Code</strong></a> da <a href="https://www.anthropic.com">Anthropic</a>
  </sub>
</p>

---

### 🏆 Créditos e Agradecimentos

> **Este projeto é construído sobre o [Synkra AIOS](https://github.com/SynkraAI/aios-core)**, o framework open-source de orquestração de agentes de IA para desenvolvimento full-stack criado por **[Pedro Valério](https://github.com/Pedrovaleriolopez)** e mantido pela organização **[SynkraAI](https://github.com/SynkraAI)** (1.850+ stars no GitHub). Sem o trabalho do Pedro e da comunidade Synkra, este projeto não existiria.

Este projeto existe graças ao trabalho incrível de diversas comunidades e criadores open-source:

| Projeto | Autor / Organização | Contribuição |
|---------|---------------------|--------------|
| [**Synkra AIOS**](https://github.com/SynkraAI/aios-core) | [**Pedro Valério**](https://github.com/Pedrovaleriolopez) / [SynkraAI](https://github.com/SynkraAI) | Framework core — toda a arquitetura de agentes, constitution, workflows, tasks, templates e o sistema de squads que este CLI instala e configura |
| [squads.sh](https://squads.sh) | [gutomec](https://github.com/gutomec) | Plataforma de gerenciamento de squads para projetos AIOS |
| [Claude Code](https://docs.anthropic.com/en/docs/claude-code) | [Anthropic](https://www.anthropic.com) | Motor de IA que torna tudo possível — agentes, skills e MCP rodam sobre o Claude Code |
| [Skills CLI](https://github.com/anthropics/skills) | [Anthropic](https://github.com/anthropics) | Skills oficiais: `frontend-design`, `pdf`, `docx`, `xlsx`, `pptx` |
| [Vercel Agent Skills](https://github.com/vercel-labs/agent-skills) | [Vercel](https://github.com/vercel-labs) | Skills: `web-design-guidelines`, `vercel-react-best-practices`, `vercel-composition-patterns` |
| [wshobson/agents](https://github.com/wshobson/agents) | [wshobson](https://github.com/wshobson) | Skills: `stripe-integration`, `api-design-principles`, `architecture-patterns`, `nodejs-backend-patterns`, `error-handling-patterns`, `github-actions-templates`, `deployment-pipeline-design`, `prompt-engineering-patterns` |
| [Marketing Skills](https://github.com/coreyhaines31/marketingskills) | [coreyhaines31](https://github.com/coreyhaines31) | Skills: `seo-audit`, `programmatic-seo`, `schema-markup` |
| [Inference Skills](https://github.com/inference-sh/skills) | [inference-sh](https://github.com/inference-sh) | Skills: `ai-video-generation`, `ai-image-generation` |
| [UI/UX Pro Max](https://github.com/nextlevelbuilder/ui-ux-pro-max-skill) | [nextlevelbuilder](https://github.com/nextlevelbuilder) | Skill: `ui-ux-pro-max` |
| [Clean Code Skill](https://github.com/ratacat/claude-skills) | [ratacat](https://github.com/ratacat) | Skill: `clean-code` |
| [nano-banana-pro](https://www.npmjs.com/package/@rafarafarafa/nano-banana-pro-mcp) | [rafarafarafa](https://github.com/rafarafarafa) | Servidor MCP para geração de imagens com Gemini |
| [Context7](https://github.com/upstash/context7-mcp) | [Upstash](https://github.com/upstash) | Servidor MCP para documentação de bibliotecas ao vivo |
| [21st.dev Magic](https://github.com/21st-dev/magic) | [21st.dev](https://github.com/21st-dev) | Servidor MCP para busca e geração de componentes UI |
| [Get Shit Done](https://www.npmjs.com/package/get-shit-done-cc) | [get-shit-done](https://github.com/get-shit-done) | Framework GSD para gestão de projetos com Claude Code |
| [cc-deploy](https://github.com/saadnvd1/cc-deploy) | [saadnvd1](https://github.com/saadnvd1) | Deploy em VPS via Claude Code |

> [!NOTE]
> `create-aios-god-mode` é um **instalador e orquestrador** — ele baixa, configura e integra os projetos listados acima. Todo o crédito pelo framework Synkra AIOS pertence a [Pedro Valério](https://github.com/Pedrovaleriolopez) e à organização [SynkraAI](https://github.com/SynkraAI). O crédito pelas skills, MCPs e ferramentas pertence aos respectivos autores. Se você é autor de algum projeto listado e deseja ajustes na atribuição, [abra uma issue](https://github.com/gutomec/create-aios-god-mode/issues).

---

```bash
npx create-aios-god-mode meu-projeto
```

> [!TIP]
> Use `--yes` para pular todos os prompts e aceitar os padrões: `npx create-aios-god-mode meu-projeto --yes`

---

## 🎯 O Que Você Recebe

<table>
<tr>
<td align="center" width="33%">
<h3>🤖 10 Agentes de IA</h3>
<sub>Dev, QA, Architect, PM, PO, SM, Analyst, Data Engineer, UX Designer, DevOps — cada um com persona única e comandos exclusivos</sub>
</td>
<td align="center" width="33%">
<h3>🧩 22 Skills</h3>
<sub>Design frontend, SEO, clean code, Stripe, CI/CD, geração de imagens/vídeos com IA, processamento de documentos e mais</sub>
</td>
<td align="center" width="33%">
<h3>🔌 3 Servidores MCP</h3>
<sub>nano-banana-pro (imagens IA), Context7 (docs ao vivo), 21st.dev (componentes UI) — pré-configurados e prontos</sub>
</td>
</tr>
<tr>
<td align="center" width="33%">
<h3>👥 4 Squads</h3>
<sub>AFS (dev de framework), NSC (criador de squads), BrandCraft (design de marca), Ultimate LP (landing pages)</sub>
</td>
<td align="center" width="33%">
<h3>📖 Dev Orientado a Stories</h3>
<sub>Ciclo completo: criar → validar → implementar → QA gate. Toda feature começa com uma story</sub>
</td>
<td align="center" width="33%">
<h3>🛡️ Proteção do Framework</h3>
<sub>Modelo de 4 camadas (L1–L4) com deny rules. Arquivos core do framework são imutáveis por design</sub>
</td>
</tr>
</table>

---

## 🚀 Início Rápido

**1.** Crie seu projeto

```bash
npx create-aios-god-mode meu-projeto
```

**2.** Entre no diretório

```bash
cd meu-projeto
```

**3.** Ative o God Mode

```bash
claude
# depois digite: /aios-god-mode
```

> [!IMPORTANT]
> O [Claude Code](https://docs.anthropic.com/en/docs/claude-code) precisa estar instalado para usar o sistema de agentes AIOS. Instale com `npm install -g @anthropic-ai/claude-code`.

---

## 🎬 Veja em Ação

> **Um prompt. Sistema completo. Zero trabalho manual.**
>
> Os exemplos abaixo mostram prompts do God Mode que produzem sistemas completos — landing page + painel admin + backend + imagens geradas por IA — tudo orquestrado por agentes AIOS. De briefings detalhados a instruções simples, os resultados são igualmente impressionantes.

<details>
<summary><strong>🏥 Exemplo Real: Clínica Médica Premium — Landing Page High-Ticket + Sistema Admin</strong></summary>

<br>

Copie este prompt no Claude Code após ativar `/aios-god-mode`:

---

### 🏥 CLÍNICA PREMIUM HIGH-TICKET MODE

Ative `aios-god-mode`.

Você irá **conceber, posicionar e implementar** uma landing page e sistema completo para uma clínica de nutrologia com posicionamento premium.

O objetivo NÃO é vender um plano de R$347.

O objetivo é vender:

> 🔥 Um programa médico exclusivo de transformação metabólica contínua
> (O valor é R$347/mês, mas a percepção deve ser de algo que valeria R$1.500+)

---

#### 🎯 POSICIONAMENTO ESTRATÉGICO

Antes de executar qualquer código:

**1️⃣ Defina o posicionamento**

A clínica não vende emagrecimento.
Ela vende:

* Longevidade
* Performance
* Controle metabólico
* Supervisão médica contínua
* Segurança clínica
* Método estruturado

Evite linguagem popular.
Use linguagem médica sofisticada e acessível.

---

**2️⃣ Defina o Avatar Premium**

Público-alvo:

* Homens e mulheres 30–55+
* Empresários
* Profissionais liberais
* Pessoas com rotina intensa
* Que já tentaram dietas
* Que valorizam acompanhamento médico real

Eles não querem "dieta".
Eles querem:

* Controle
* Segurança
* Acompanhamento
* Método científico
* Resultado previsível

---

#### 🧠 ESTRUTURA DA LANDING (HIGH-TICKET)

**HERO SECTION**

* Headline forte e elegante
* Subheadline médica e técnica
* CTA discreto e sofisticado
* Imagem premium estilo editorial médico

Exemplo de direção (não copie literalmente):

> "Supervisão Médica Contínua Para Transformação Metabólica Sustentável."

---

**SEÇÃO 1 — AUTORIDADE**

* Apresentação da equipe médica
* Formação, CRM, Especializações
* Método exclusivo

Tom: Confiança silenciosa. Sem exagero. Sem hype.

---

**SEÇÃO 2 — O MÉTODO**

Explicar o método como um protocolo estruturado:

* Avaliação metabólica
* Estratégia personalizada
* Monitoramento contínuo
* Ajustes clínicos
* Acompanhamento da equipe

Nomeie o método. Ex: *Protocolo de Regulação Metabólica Contínua™*

---

**SEÇÃO 3 — DIFERENCIAL**

Comparar implicitamente com dietas genéricas, apps, influenciadores, programas sem médico.
Sem atacar diretamente.

---

**SEÇÃO 4 — PROVA SOCIAL PREMIUM**

* Depoimentos elegantes
* Fotos discretas
* Histórias realistas
* Transformações sem exagero visual

Nada apelativo.

---

**SEÇÃO 5 — INVESTIMENTO**

Apresente como:

> Programa de Acompanhamento Médico Contínuo
> Investimento mensal: R$347

Ancoragem psicológica antes: consultas avulsas, nutricionistas, personal, exames, tempo perdido.

---

#### 📸 IMAGENS (nano banana pro)

Gerar imagens no padrão:

* Fotografia médica editorial
* Luz natural, ambiente clean
* Consultório sofisticado
* Expressões confiantes
* Pacientes reais (não fitness influencer)

Estilo: Tons neutros, branco, bege, azul clínico. Sem exagero de saturação. Sem aparência artificial.

---

#### 💾 BACKEND

**Banco SQLite:**

| Tabela | Campos |
|--------|--------|
| `leads` | id, nome, email, telefone, data_cadastro, origem, status, observacoes |
| `users` (admin) | id, nome, email, senha_hash, role, data_criacao |

---

#### 🔐 AUTENTICAÇÃO

* Login seguro com senha hash
* Proteção de rotas
* Sessão autenticada
* Logout

---

#### 📊 PAINEL ADMIN PREMIUM

Design limpo estilo SaaS médico.

**Dashboard:** Total de leads, leads por período, gráfico de crescimento, conversões, origem de tráfego.

**Tabela de leads:** Ordenação, filtro, busca, paginação + botão **Exportar para Excel (.xlsx)**.

---

#### 🎨 ESTILO VISUAL

* Minimalista, espaçamento generoso
* Tipografia elegante
* Animações sutis, transições suaves
* UX fluida

Referência mental: SaaS médico americano, clínica de luxo, estética discreta.

---

#### ⚙️ EXECUÇÃO

1. Planeje estrategicamente tudo
2. Defina arquitetura
3. Estruture código
4. Implemente frontend + backend
5. Gere imagens
6. Organize estrutura de pastas
7. Entregue pronto para deploy

Execute tudo usando `aios-god-mode`.

Nível exigido:

> Clínica de alto padrão.
> Produto que transmite confiança médica absoluta.
> Conversão elegante, não agressiva.

---

<br>

**O que o AIOS faz com esse prompt:**

| Agente | Ação |
|--------|------|
| `@architect` | Projeta a arquitetura full-stack (Next.js + SQLite + Auth) |
| `@ux-design-expert` | Cria spec de UI premium com estética editorial médica |
| `@dev` | Implementa landing page, painel admin e API backend |
| `@data-engineer` | Projeta schema SQLite com índices adequados |
| `@qa` | Valida qualidade, segurança e responsividade |
| `nano-banana-pro` | Gera fotografia médica editorial via MCP |
| `@devops` | Faz push para o GitHub quando pronto |

</details>

<br>

> [!TIP]
> **Você não precisa de um prompt detalhado para ter resultados impressionantes.** O exemplo abaixo é muito mais simples — e o God Mode entrega um sistema completo e pronto para produção com a mesma qualidade.

<details>
<summary><strong>⚡ Exemplo Rápido: Mesmo Projeto, Prompt Simples — Resultados Igualmente Impressionantes</strong></summary>

<br>

Este prompt mais curto alcança o mesmo escopo — landing page, backend, painel admin, fotos com IA, gestão de leads — com instruções mínimas. O God Mode preenche as lacunas usando suas skills e expertise de agentes integrados:

---

Ative sua skill aios-god-mode.

Utilize AIOS para criar uma landing page de alta conversão para um sistema de acompanhamento médico de uma clínica de nutrologia. A equipe médica deve estar disponível para acompanhamento contínuo de atendimentos relacionados à nutrologia, como emagrecimento e reeducação alimentar.

O plano de assinatura mensal custa R$347.

Gere fotografias utilizando nano banana pro com qualidade de fotógrafo profissional, transmitindo credibilidade, profissionalismo e padrão premium.

Implemente um sistema completo com backend que:

- Salve os leads em um banco de dados SQLite.
- Possua painel de administração com autenticação via SQLite.
- Permita que usuários cadastrados analisem estatísticas dos leads coletados.
- Exiba uma tabela com os leads cadastrados.
- Tenha um botão para exportação dos leads em formato Excel (.xlsx).

Para o planejamento do projeto, utilize suas melhores skills estratégicas. Após concluir o planejamento, execute toda a implementação utilizando a skill aios-god-mode.

---

<br>

**Mesmo resultado, menos esforço.** Os agentes do God Mode lidam autonomamente com tudo:

| O Que Você Escreveu | O Que o AIOS Faz |
|---------------------|-------------------|
| "landing page de alta conversão" | `@ux-design-expert` projeta layout otimizado para conversão, `@dev` implementa |
| "fotografias com nano banana pro" | Gera fotografia médica profissional via MCP |
| "leads em SQLite" | `@data-engineer` projeta o schema, `@dev` implementa a API CRUD |
| "painel de administração com autenticação" | Sistema completo de auth + dashboard admin com estatísticas |
| "exportação em Excel" | Exportação `.xlsx` usando a skill `xlsx` |
| "melhores skills estratégicas" | `@architect` planeja a arquitetura, `@pm` define requisitos |

> **A diferença?** O prompt detalhado dá controle preciso sobre posicionamento, tom de copy e direção visual. O prompt simples deixa o AIOS tomar essas decisões por você. Ambos entregam resultados prontos para produção.

</details>

---

## ✨ Funcionalidades

- **⚡ God Mode** — Orquestração completa com 10 personas de IA especializadas, cada uma com comandos dedicados
- **🤖 Sistema de Agentes** — Ative agentes com `@nome-do-agente`, execute comandos com `*comando`. Protocolo de handoff integrado preserva contexto entre trocas
- **📖 Desenvolvimento Orientado a Stories** — Todo trabalho flui por stories: `@sm *draft` → `@po *validate` → `@dev *develop` → `@qa *gate`
- **👥 Sistema de Squads** — Squads multi-agente pré-configurados para workflows de domínios específicos (dev de framework, design de marca, landing pages)
- **🧩 Ecossistema de Skills** — 22 skills da comunidade instaladas automaticamente: frontend, backend, SEO, pagamentos, documentos, geração com IA
- **🔌 Integração MCP** — 3 servidores MCP pré-configurados em `.mcp.json` para geração de imagens com IA, documentação ao vivo e componentes UI
- **🛡️ Proteção do Framework** — Modelo de 4 camadas com deny rules determinísticas em `settings.json`. Arquivos L1/L2 são imutáveis
- **🔄 QA Loop** — Ciclo automatizado de revisão-correção: `@qa review → veredito → @dev corrige → re-review` (máx. 5 iterações)
- **📋 Spec Pipeline** — Transforma requisitos informais em specs executáveis com seleção de fases baseada em complexidade (3-6 fases)
- **🔍 Brownfield Discovery** — Avaliação de débito técnico em 10 fases para codebases existentes com coleta de dados multi-agente

---

## 📦 Fluxo de Instalação

O instalador executa um **pipeline automatizado de 10 etapas**:

| Etapa | Descrição |
|:-----:|-----------|
| 1 | 🔍 **Validar ambiente** — Verifica versão do Node.js, nome do projeto, diretório e rede |
| 2 | 🏗️ **Inicializar framework AIOS** — Baixa e estrutura `.aios-core/` com constitution, tasks e workflows |
| 3 | ⚡ **Instalar God Mode** — Baixa personas de agentes, skills e rules do [aios-god-mode-template](https://github.com/gutomec/aios-god-mode-template) |
| 4 | 👥 **Instalar squads** — Baixa e configura os pacotes de squads selecionados |
| 5 | 🔌 **Configurar servidores MCP** — Configura `nano-banana-pro`, `context7`, `21st-dev` em `.mcp.json` |
| 6 | 🧩 **Instalar skills do ecossistema** — 22 skills de repos da comunidade via `npx skills add` |
| 7 | 🚀 **Instalar framework GSD** — [Get Shit Done](https://www.npmjs.com/package/get-shit-done-cc) para gestão de projetos |
| 8 | 📦 **Instalar dependências** — Executa `npm install` dentro de `.aios-core/` |
| 9 | 🗃️ **Inicializar git** — `git init` com commit inicial |
| 10 | ✅ **Pronto** — Projeto preparado para desenvolvimento orientado por agentes |

---

## 🛠️ Comandos

### `init` (padrão)

Cria um novo projeto AIOS do zero.

```bash
npx create-aios-god-mode meu-projeto
npx create-aios-god-mode meu-projeto --yes    # Aceitar todos os padrões
```

### `update`

Atualiza um projeto existente para a versão mais recente do template.

```bash
cd meu-projeto
npx create-aios-god-mode update
```

### `doctor`

Executa verificações de saúde em uma instalação AIOS existente.

```bash
cd meu-projeto
npx create-aios-god-mode doctor
```

### `add-squad`

Adiciona uma nova configuração de squad ao projeto.

```bash
cd meu-projeto
npx create-aios-god-mode add-squad backend
```

---

<details>
<summary><h2>🤖 Agentes de IA</h2></summary>

Todos os agentes são ativados com `@nome-do-agente` e suportam comandos via prefixo `*`.

| Agente | Persona | Função | Comandos Principais |
|--------|---------|--------|---------------------|
| `@dev` | **Dex** | Desenvolvedor Full Stack | `*develop`, `*build-autonomous`, `*run-tests`, `*self-critique` |
| `@qa` | **Quinn** | Arquiteto de Testes | `*review`, `*gate`, `*security-check`, `*test-design` |
| `@architect` | **Aria** | Arquiteto Técnico | `*design-system`, `*tech-selection`, `*api-design` |
| `@pm` | **Morgan** | Product Manager | `*create-prd`, `*create-epic`, `*execute-epic`, `*write-spec` |
| `@po` | **Pax** | Product Owner | `*validate-story-draft`, `*close-story`, `*backlog-review` |
| `@sm` | **River** | Scrum Master | `*draft`, `*story-checklist` |
| `@analyst` | **Atlas** | Analista de Negócios | `*research`, `*feasibility-study`, `*user-research` |
| `@data-engineer` | **Dara** | Especialista em Banco de Dados | Design DDL, políticas RLS, migrações, otimização de queries |
| `@ux-design-expert` | **Uma** | Designer UX/UI | Specs frontend, jornadas de usuário, design systems |
| `@devops` | **Gage** | Gerente de Repositório | `*push`, `*create-pr`, `*release`, `*add-mcp` |
| `@aios-master` | **Orion** | Orquestrador do Framework | `*create`, `*modify`, `*run-workflow`, `*correct-course` |

**Comandos universais** (disponíveis em todos os agentes): `*help`, `*guide`, `*session-info`, `*yolo`, `*exit`

</details>

---

<details>
<summary><h2>🧩 Skills do Ecossistema</h2></summary>

22 skills instaladas automaticamente, organizadas por categoria:

#### Design & Frontend

| Skill | Fonte |
|-------|-------|
| `ui-ux-pro-max` | nextlevelbuilder/ui-ux-pro-max-skill |
| `frontend-design` | anthropics/skills |
| `web-design-guidelines` | vercel-labs/agent-skills |
| `vercel-react-best-practices` | vercel-labs/agent-skills |
| `vercel-composition-patterns` | vercel-labs/agent-skills |

#### SEO & Marketing

| Skill | Fonte |
|-------|-------|
| `seo-audit` | coreyhaines31/marketingskills |
| `programmatic-seo` | coreyhaines31/marketingskills |
| `schema-markup` | coreyhaines31/marketingskills |

#### CI/CD & Deploy

| Skill | Fonte |
|-------|-------|
| `github-actions-templates` | wshobson/agents |
| `deployment-pipeline-design` | wshobson/agents |

#### Pagamentos

| Skill | Fonte |
|-------|-------|
| `stripe-integration` | wshobson/agents |

#### Backend & Clean Code

| Skill | Fonte |
|-------|-------|
| `nodejs-backend-patterns` | wshobson/agents |
| `api-design-principles` | wshobson/agents |
| `architecture-patterns` | wshobson/agents |
| `error-handling-patterns` | wshobson/agents |
| `clean-code` | ratacat/claude-skills |

#### Engenharia de Prompts

| Skill | Fonte |
|-------|-------|
| `prompt-engineering-patterns` | wshobson/agents |

#### Geração de Mídia com IA

| Skill | Fonte |
|-------|-------|
| `ai-video-generation` | inference-sh/skills |
| `ai-image-generation` | inference-sh/skills |

#### Processamento de Documentos

| Skill | Fonte |
|-------|-------|
| `pdf` | anthropics/skills |
| `docx` | anthropics/skills |
| `xlsx` | anthropics/skills |
| `pptx` | anthropics/skills |

</details>

---

## 🔌 Servidores MCP

Pré-configurados em `.mcp.json` e prontos para uso:

| Servidor | Pacote | Propósito |
|----------|--------|-----------|
| **nano-banana-pro** | `@rafarafarafa/nano-banana-pro-mcp` | Geração de imagens com IA via Gemini |
| **context7** | `@upstash/context7-mcp` | Consulta de documentação de bibliotecas ao vivo |
| **21st-dev** | `@21st-dev/magic` | Busca e geração de componentes UI |

> [!NOTE]
> O `nano-banana-pro` requer a variável de ambiente `GEMINI_API_KEY`. Adicione-a ao seu arquivo `.env`.

---

## 📁 Estrutura do Projeto

```
meu-projeto/
├── .claude/
│   ├── settings.json              # Permissões do Claude Code + deny rules
│   ├── rules/                     # Regras de workflow, exemplos de tools, autoridade de agentes
│   ├── skills/                    # God Mode + 22 skills do ecossistema
│   └── CLAUDE.md                  # Instruções do projeto para o Claude
├── .aios-core/
│   ├── constitution.md            # Princípios do framework (imutável)
│   ├── core/                      # Módulos core do framework
│   ├── development/
│   │   ├── tasks/                 # Definições de tasks executáveis
│   │   ├── templates/             # Templates de documentos e código
│   │   ├── checklists/            # Checklists de validação
│   │   └── workflows/             # Workflows multi-etapa
│   └── data/                      # Registro de tools, dados de configuração
├── .mcp.json                      # Configuração dos servidores MCP
├── docs/
│   ├── stories/                   # Stories de desenvolvimento
│   ├── prd/                       # Documentos de requisitos do produto
│   └── architecture/              # Documentação de arquitetura do sistema
├── squads/                        # Configurações de squads
├── packages/                      # Pacotes do projeto
├── tests/                         # Suítes de teste
├── package.json
└── README.md
```

---

## 👥 Squads

Disponíveis durante a configuração interativa (ou todos selecionados com `--yes`):

| Squad | Descrição | Padrão |
|-------|-----------|:------:|
| **AFS** — AIOS Forge Squad | Desenvolvimento e contribuição ao framework | ✅ |
| **NSC** — Nirvana Squad Creator | Criação e gerenciamento de novos squads | ✅ |
| **BrandCraft** | Identidade de marca e design system | — |
| **Ultimate LP** | Criação de landing pages com workflow multi-agente | — |

---

## ⚙️ Opções e Configuração

| Opção | Descrição |
|-------|-----------|
| `--yes` | Aceitar todos os padrões sem prompts interativos |

### Prompts Interativos

Ao executar sem `--yes`, o instalador pergunta:

| Prompt | Opções | Padrão |
|--------|--------|--------|
| **Nome do projeto** | Qualquer nome válido em kebab-case | — |
| **Tipo de projeto** | `Greenfield` / `Brownfield` | Greenfield |
| **Idioma** | `Português (PT-BR)` / `English` | PT-BR |
| **Squads** | Seleção múltipla dos squads disponíveis | AFS + NSC |

---

<details>
<summary><h2>🔄 Workflows</h2></summary>

### Story Development Cycle (SDC) — Principal

O workflow principal de desenvolvimento, usado para toda implementação de stories:

```
@sm *draft → @po *validate → @dev *develop → @qa *gate → @devops *push
```

| Fase | Agente | Tarefa |
|------|--------|--------|
| Criar | `@sm` | Rascunho da story a partir de epic/PRD |
| Validar | `@po` | Checklist de 10 pontos → GO / NO-GO |
| Implementar | `@dev` | Código, testes, autocrítica |
| QA Gate | `@qa` | 7 verificações de qualidade → PASS / FAIL |

### QA Loop — Revisão Iterativa

Ciclo automatizado de revisão-correção após o QA gate inicial:

```
@qa review → veredito → @dev corrige → re-review (máx. 5 iterações)
```

### Spec Pipeline — Pré-Implementação

Transforma requisitos informais em especificações executáveis:

| Complexidade | Fases | Fluxo |
|--------------|-------|-------|
| Simples (≤8) | 3 | coletar → spec → crítica |
| Padrão (9-15) | 6 | coletar → avaliar → pesquisar → spec → crítica → planejar |
| Complexo (≥16) | 6+ | Todas as fases + ciclo de revisão |

### Brownfield Discovery — Avaliação de Legado

Avaliação de débito técnico em 10 fases para codebases existentes com coleta de dados (arquitetura, banco de dados, frontend), revisão multi-agente e geração de relatório executivo.

</details>

---

## 📋 Requisitos

| Requisito | Versão | Obrigatório |
|-----------|--------|:-----------:|
| **Node.js** | ≥ 18.0.0 | ✅ |
| **Git** | Qualquer recente | ✅ |
| **GitHub CLI** (`gh`) | Qualquer recente | Recomendado |
| **Claude Code** | Mais recente | ✅ |

---

## 🔗 Links Relacionados

- [Synkra AIOS](https://github.com/SynkraAI/aios-core) — O framework de Sistema Orquestrado por IA, por [Pedro Valério](https://github.com/Pedrovaleriolopez)
- [squads.sh](https://squads.sh) — Gerenciamento de squads para projetos AIOS
- [aios-god-mode-template](https://github.com/gutomec/aios-god-mode-template) — O template que este CLI utiliza
- [Get Shit Done](https://www.npmjs.com/package/get-shit-done-cc) — Framework de gestão de projetos

---

## 📄 Licença

[MIT](LICENSE) © [gutomec](https://github.com/gutomec)
