# CC_INSTRUCOES_TEMPLATE

Repositório de boas práticas e templates para desenvolvimento com IA/LLM. Serve como documentação viva de como trabalhar corretamente com modelos de linguagem em projetos reais.

---

## Filosofia central

A IA deve se comportar como um desenvolvedor experiente: **primeiro pensa, depois executa**.

O erro mais comum ao trabalhar com LLMs é pedir implementação direta sem planejamento. O fluxo correto é:

```
Nova tarefa
    ↓
/plan  ← LLM atua como Arquiteto de Software
    ↓
Revisar e aprovar o plano
    ↓
Ajustar se necessário
    ↓
/implement  ← LLM executa o plano aprovado, sem inventar
    ↓
/review  ← LLM analisa o que foi feito, sem alterar
    ↓
Corrigir se necessário
    ↓
Commit
```

Equipes que ignoram esse fluxo acumulam retrabalho porque a LLM toma decisões arquiteturais durante a implementação, sem contexto suficiente.

---

## Estrutura do repositório

```
CC_INSTRUCOES_TEMPLATE/
├── README.md                 ← este arquivo
├── use_guide.md              ← como usar o kit de templates
│
├── 01_instructions.md        ← prompt para gerar: 00_instrucoes.md
├── 02_context.md             ← prompt para gerar: 01_contexto.md
├── 03_decisions.md           ← prompt para gerar: 02_decisoes.md
├── 04_glossary.md            ← prompt para gerar: 03_glossario.md
├── 05_status.md              ← prompt para gerar: 04_status.md
├── 06_arquitetura.md         ← prompt para gerar: 05_arquitetura.md
├── 07_progresso_tecnico.md   ← prompt para gerar: 07_progresso_tecnico.md
├── 08_specs.md               ← prompt para gerar: 08_specs.md
├── 09_testes.md              ← prompt para gerar: 09_testes.md
│
└── .claude/
    └── commands/
        ├── plan.md           ← slash command /plan
        ├── implement.md      ← slash command /implement
        └── review.md         ← slash command /review
```

---

## Os dois pilares

### 1. Arquivos de contexto (01–09)

Cada arquivo numerado é um **prompt pronto** para você enviar à LLM e gerar a documentação real do seu projeto. Não são documentos finais — são geradores de documentos.

### 2. Slash commands (.claude/commands/)

São instruções de comportamento que governam como a LLM deve agir em cada fase do trabalho. Salvos em `.claude/commands/`, são ativados via `/plan`, `/implement`, `/review`.

---

## Os arquivos de contexto

### Ordem de geração recomendada

```
02_context.md   →  gera 01_contexto.md      (base de tudo: o que é, para quem, restrições)
01_instructions.md → gera 00_instrucoes.md  (como a LLM deve se comportar)
04_glossary.md  →  gera 03_glossario.md     (termos e nomenclaturas do projeto)
03_decisions.md →  gera 02_decisoes.md      (decisões já tomadas e o porquê)
05_status.md    →  gera 04_status.md        (estado atual — atualizar a cada sessão)
06_arquitetura.md → gera 05_arquitetura.md  (stack, estrutura de pastas, padrões)
07_progresso_tecnico.md → gera 07_progresso_tecnico.md (saúde técnica, bugs, dívida)
08_specs.md     →  gera 08_specs.md         (contratos de cada sistema/módulo)
09_testes.md    →  gera 09_testes.md        (filosofia, stack e padrões de teste)
```

### O que cada arquivo gera

| Arquivo | Gera | Propósito |
|---------|------|-----------|
| `02_context.md` | `01_contexto.md` | Briefing permanente: o que é o projeto, objetivo, restrições, stakeholders |
| `01_instructions.md` | `00_instrucoes.md` | Manual de operação: autonomia da LLM, tom, formatos, pastas protegidas |
| `04_glossary.md` | `03_glossario.md` | Termos padronizados — evita inconsistência de nomenclatura |
| `03_decisions.md` | `02_decisoes.md` | Log de decisões com alternativas descartadas e justificativas |
| `05_status.md` | `04_status.md` | Estado atual do projeto — o mais atualizado dos arquivos |
| `06_arquitetura.md` | `05_arquitetura.md` | Estrutura técnica, stack, padrões de código, decisões de arquitetura |
| `07_progresso_tecnico.md` | `07_progresso_tecnico.md` | Status por módulo, dívida técnica, bugs ativos e corrigidos |
| `08_specs.md` | `08_specs.md` | Contrato de cada sistema: responsabilidade, interface pública, regras |
| `09_testes.md` | `09_testes.md` | Filosofia de testes, stack, estrutura de pastas, exemplos reais |

---

## Os slash commands

### `/plan` — Arquiteto de Software

Ativa antes de qualquer implementação. A LLM analisa o problema sem tocar em código.

O que o `/plan` produz:
- Análise do problema e regras de negócio envolvidas
- Escopo: o que será feito e o que **não** será feito
- Arquivos e componentes impactados
- Estratégia de implementação com alternativas consideradas
- Análise de segurança e performance
- Estratégia de testes
- Plano numerado em etapas pequenas
- Classificação de riscos (🔴 Alto / 🟠 Médio / 🟢 Baixo)
- Critérios de aceite objetivos

**Regra:** a LLM não implementa nada até receber aprovação explícita.

---

### `/implement` — Executor do plano

Ativa após aprovação do `/plan`. A LLM executa o plano aprovado sem inventar soluções.

Regras do `/implement`:
- Implementar apenas o que foi descrito no plano
- Não "melhorar" a solução durante a execução
- Não mudar bibliotecas, padrões arquiteturais ou APIs não incluídas no plano
- Se algo estiver faltando ou ambíguo, parar e pedir esclarecimento
- Ao final: atualizar testes e validar todos os critérios de aceite

**Regra de ouro:** o plano é a verdade absoluta. A implementação não reinterpreta — executa.

---

### `/review` — Revisor

Ativa após a implementação. A LLM analisa as alterações sem fazer mudanças.

O que o `/review` avalia:
- **Correção:** bugs, edge cases, regressões
- **Arquitetura:** violações de responsabilidade, acoplamento alto
- **Clean Code:** nomes, legibilidade, duplicação, complexidade
- **Performance:** consultas desnecessárias, loops ineficientes
- **Segurança:** validações ausentes, exposição de dados
- **Testes:** cobertura, casos válidos e inválidos
- **Manutenibilidade:** facilidade de alteração futura

Classificação de problemas:
- 🔴 Crítico — falhas, vulnerabilidades, dados incorretos
- 🟠 Alto — deve corrigir antes do merge
- 🟡 Médio — melhoria recomendada
- 🟢 Baixo — ajuste de qualidade ou estilo

Veredito: ✅ Aprovado / 🟡 Aprovado com ressalvas / ❌ Requer alterações

---

## Como usar no dia a dia

### Início de uma nova sessão

Cole no chat (nessa ordem):
1. `00_instrucoes.md` — como a LLM deve se comportar
2. `01_contexto.md` — o que é o projeto
3. `04_status.md` — onde o projeto está agora

Esses três arquivos são suficientes para a LLM retomar o trabalho sem perder contexto.

### Durante o trabalho

- Nova decisão importante → peça para registrar em `02_decisoes.md`
- Novo código escrito → peça para atualizar `07_progresso_tecnico.md`
- Ao final da sessão → peça para atualizar `04_status.md`

### Estrutura de pastas recomendada para o projeto real

```
templates/   ← modelos protegidos, nunca editar diretamente
entradas/    ← material bruto, pesquisas, referências
trabalho/    ← rascunhos e versões em andamento
saidas/      ← entregas finalizadas
arquivo/     ← histórico encerrado
```

---

## Por que esse sistema funciona

### Problema: LLMs sem contexto tomam decisões ruins

Quando você pede implementação direta, a LLM preenche lacunas com suposições. Sem saber o porquê das decisões arquiteturais, sem conhecer restrições do projeto, ela inventa.

### Solução: contexto persistente + fases separadas

| Fase | Arquivo | Resultado |
|------|---------|-----------|
| Entender | `01_contexto.md` + `04_status.md` | LLM sabe onde está |
| Planejar | `/plan` | LLM pensa antes de agir |
| Executar | `/implement` | LLM age dentro do que foi aprovado |
| Verificar | `/review` | LLM audita sem conflito de interesse |

### As três separações fundamentais

1. **Pensar ≠ Executar** — nunca peça implementação sem plano aprovado
2. **Executar ≠ Revisar** — o código deve ser revisado depois de escrito, não durante
3. **Sessão atual ≠ Próxima sessão** — documentar o estado ao final de cada sessão garante continuidade

---

## Boas práticas essenciais

**Contexto:**
- Sempre inicie a sessão colando os 3 arquivos principais
- Mantenha `04_status.md` atualizado — é sua memória entre sessões
- Use `02_decisoes.md` para registrar o **porquê** das decisões, não só o quê

**Planejamento:**
- Nunca pule o `/plan` para tarefas com impacto em arquitetura
- Revise o plano antes de aprovar — a LLM pode ter lacunas
- Defina critérios de aceite claros no plano

**Implementação:**
- Se a LLM sugerir mudanças fora do escopo durante o `/implement`, rejeite e peça para registrar como próximo passo
- Mantenha `07_progresso_tecnico.md` atualizado a cada sessão com código

**Revisão:**
- Execute `/review` antes de qualquer commit em feature crítica
- Trate problemas 🔴 e 🟠 como bloqueadores

---

## Adicionando ao seu projeto

Copie os arquivos que fazem sentido para o seu contexto:

```bash
# Mínimo para qualquer projeto com LLM
cp 02_context.md    seu-projeto/01_contexto.md
cp 01_instructions.md  seu-projeto/00_instrucoes.md
cp 05_status.md     seu-projeto/04_status.md

# Para projetos de software
cp 06_arquitetura.md   seu-projeto/05_arquitetura.md
cp 03_decisions.md     seu-projeto/02_decisoes.md

# Slash commands (Claude Code)
mkdir -p seu-projeto/.claude/commands/
cp .claude/commands/plan.md      seu-projeto/.claude/commands/
cp .claude/commands/implement.md seu-projeto/.claude/commands/
cp .claude/commands/review.md    seu-projeto/.claude/commands/
```

Depois use cada arquivo como prompt para gerar o conteúdo real com a LLM, seguindo a ordem recomendada em `use_guide.md`.
