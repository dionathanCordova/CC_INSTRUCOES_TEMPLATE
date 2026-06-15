# Prompt para gerar: 07_progresso_tecnico.md

> Este arquivo é o mapa de saúde técnica do projeto: rastreia o status de implementação de cada sistema/módulo, registra dívida técnica, bugs ativos e histórico de correções. É diferente do 04_status.md (que é operacional/gerencial) — este é 100% focado em código. Gere depois do 05_arquitetura.md, pois a lista de sistemas vem diretamente da estrutura de pastas e módulos definidos lá.

Copie o prompt abaixo, preencha os campos entre [colchetes] e envie para uma LLM.

---

## PROMPT

Você vai me ajudar a criar um arquivo chamado "07_progresso_tecnico.md", que será o mapa técnico de implementação de um projeto que vou desenvolver com a sua ajuda (ou de outra LLM) ao longo de várias conversas futuras.

Aqui está o contexto do projeto (conteúdo do arquivo 01_contexto.md):

[COLE AQUI O CONTEÚDO DO 01_CONTEXTO.MD]

Aqui está a arquitetura técnica do projeto (conteúdo do arquivo 05_arquitetura.md):

[COLE AQUI O CONTEÚDO DO 05_ARQUITETURA.MD]

Estado atual da implementação:

- Já existe algum código escrito? (se sim, descreva quais sistemas ou arquivos já existem): [...]
- Existe algum bug ativo já identificado? (se sim, descreva): [...]
- Existe alguma dívida técnica já conhecida? (ex.: solução provisória, atalho tomado, refatoração pendente): [...]

Com base na arquitetura fornecida, faça o seguinte:

1. **Extraia todos os sistemas e módulos** listados na estrutura de pastas do 05_arquitetura.md e monte a tabela de status com uma linha por sistema, no formato:

| Sistema | Arquivo(s) | Status | Observações |
|---------|-----------|--------|-------------|

2. **Preencha o status inicial** de cada sistema com base no que eu informei sobre o estado atual. Para sistemas não mencionados, use ⬜ Não iniciado.

3. **Use a seguinte legenda de status** (inclua no arquivo):

| Ícone | Significado |
|-------|-------------|
| ⬜ Não iniciado | Nenhum código criado ainda |
| 🟡 Em andamento | Implementação parcial, não funcional ainda |
| 🔵 Funcional (parcial) | Funciona, mas incompleto ou com limitações conhecidas |
| ✅ Completo | Implementado, testado e sem pendências conhecidas |
| 🔴 Com bug | Implementado mas com bug ativo (detalhar na seção de Bugs Ativos) |

4. Gere o arquivo 07_progresso_tecnico.md completo em markdown com as seções:

- **Última atualização**: [data de hoje]
- **Status por Sistema**: tabela completa extraída da arquitetura
- **Legenda de Status**: tabela da legenda acima
- **Dívida Técnica**: lista de dívidas conhecidas (ou "Nenhuma registrada ainda")
- **Bugs Ativos**: lista de bugs ativos com descrição (ou "Nenhum registrado ainda")
- **Histórico de Bugs Corrigidos**: lista de bugs resolvidos (ou "Nenhum registrado ainda")
- **Como usar este arquivo**: instrução curta dizendo que este arquivo deve ser consultado antes de implementar qualquer sistema (para evitar retrabalho), e atualizado ao final de cada sessão em que código foi criado ou modificado — atualizando status, registrando dívida técnica e movendo bugs resolvidos para o histórico.

---
