# Prompt para gerar: 08_specs.md

> Este arquivo é o contrato técnico de cada sistema do projeto: define responsabilidades, interfaces públicas, eventos emitidos, regras de comportamento e o que está fora do escopo de cada módulo. É o arquivo mais detalhado do template e deve ser gerado depois do 05_arquitetura.md — ele aprofunda cada módulo que a arquitetura apenas lista. Qualquer desvio relevante em relação a uma spec deve ser registrado em 03_decisoes.md.

Copie o prompt abaixo, preencha os campos entre [colchetes] e envie para uma LLM.

---

## PROMPT

Você vai me ajudar a criar um arquivo chamado "08_specs.md", que será o documento de especificação técnica de cada sistema de um projeto que vou desenvolver com a sua ajuda (ou de outra LLM) ao longo de várias conversas futuras.

Aqui está o contexto do projeto (conteúdo do arquivo 01_contexto.md):

[COLE AQUI O CONTEÚDO DO 01_CONTEXTO.MD]

Aqui está a arquitetura técnica do projeto (conteúdo do arquivo 05_arquitetura.md):

[COLE AQUI O CONTEÚDO DO 05_ARQUITETURA.MD]

Aqui estão as decisões já tomadas (conteúdo do arquivo 03_decisoes.md):

[COLE AQUI O CONTEÚDO DO 03_DECISOES.MD]

Informações adicionais sobre o projeto que ajudarão a escrever as specs:

- Existe algum documento de design (GDD, PRD, brief criativo)? Se sim, cole ou descreva os pontos mais relevantes aqui: [...]
- Quais são os sistemas "core" (usados em toda a aplicação) versus sistemas específicos de um contexto/módulo: [...]
- Existe alguma regra de comunicação entre sistemas (eventos, callbacks, referências diretas)? Descreva: [...]
- Quais sistemas têm comportamento extensível (ex.: classes base que serão herdadas)? Descreva o padrão: [...]
- Existem valores numéricos já definidos (timers, velocidades, pontos, preços)? Liste os que já sabe: [...]

Antes de escrever o arquivo final, me faça perguntas (pode ser mais de uma rodada) para entender:

1. Para cada sistema listado na arquitetura: qual é a responsabilidade principal e o que definitivamente NÃO é responsabilidade dele (separação de concerns)
2. Qual é a interface pública de cada sistema (métodos, funções exportadas, props) — o que outros módulos podem chamar
3. Quais eventos cada sistema emite e quais consome (se o projeto usar um sistema de eventos/EventEmitter)
4. Para sistemas que são classes base (serão estendidas): quais métodos são herdados intocados, quais devem ser sobrescritos, e quais são opcionalmente sobrescríveis
5. Quais são as regras de comportamento que não são óbvias (casos de borda, limites, comportamentos em erro)
6. Para módulos de dados estáticos: qual é o formato exato do objeto exportado

Depois das minhas respostas, gere o arquivo 08_specs.md completo em markdown com a seguinte estrutura:

1. **Como usar este arquivo** — instrução curta: antes de implementar qualquer sistema, leia a spec correspondente; a spec é o contrato do sistema; desvios relevantes vão em 03_decisoes.md
2. **Índice** — lista numerada de todos os sistemas com âncoras de link
3. **Uma seção por sistema**, contendo:
   - **Responsabilidade** — em 1-2 frases, o que este módulo faz
   - **Estado interno** (se aplicável) — variáveis que o módulo mantém, com tipo e descrição
   - **Interface pública** — métodos/funções exportados com assinatura e descrição do comportamento
   - **Eventos emitidos** (se aplicável) — nome do evento, payload e quem consome
   - **Regras** — comportamentos não óbvios, casos de borda, limites
   - **Não é responsabilidade** — lista explícita do que este módulo NÃO deve fazer (delega para quem)

Seja extremamente específico. Use exemplos de código para interfaces públicas e formatos de dados. Não invente comportamentos que não foram discutidos — marque com `[A DEFINIR]` qualquer valor ou comportamento que ainda não foi decidido, para que eu possa revisar depois. O arquivo deve ser completo o suficiente para que qualquer LLM (ou desenvolvedor novo) implemente qualquer sistema sem precisar fazer perguntas sobre o que ele deve ou não deve fazer.

---
