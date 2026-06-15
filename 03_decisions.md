# Prompt para gerar: 02_decisoes.md

> Este arquivo é o "log de decisões": registra escolhas importantes já feitas no projeto e o porquê delas, para evitar retrabalho e discussões repetidas. Diferente dos outros, este arquivo cresce com o tempo — o prompt abaixo serve para criar a estrutura inicial e já registrar as primeiras decisões.

Copie o prompt abaixo, preencha os campos entre [colchetes] (incluindo o contexto do projeto já gerado em 01_contexto.md) e envie para uma LLM.

---

## PROMPT

Você vai me ajudar a criar um arquivo chamado "02_decisoes.md", que funcionará como um log contínuo de decisões importantes tomadas ao longo de um projeto.

Aqui está o contexto do projeto (conteúdo do arquivo 01_contexto.md):

[COLE AQUI O CONTEÚDO DO 01_CONTEXTO.MD]

Decisões que já foram tomadas até agora, mesmo que informalmente:

[LISTE AQUI, EM POUCAS PALAVRAS, AS DECISÕES JÁ TOMADAS. Exemplo: "Vamos usar tom informal nas redes sociais", "Decidimos não usar a ferramenta X por causa de Y", etc. Se ainda não houver nenhuma, escreva "nenhuma ainda".]

Com base nisso, faça o seguinte:

1. Se eu já tiver listado decisões, me faça perguntas para entender o "porquê" de cada uma (qual alternativa foi descartada e o motivo)
2. Gere o arquivo 02_decisoes.md em markdown com uma tabela no formato:

| Data | Decisão | Alternativas consideradas | Motivo | Status |
|------|---------|---------------------------|--------|--------|

3. Preencha a tabela com as decisões que eu informei (use a data de hoje se eu não especificar)
4. No final do arquivo, adicione uma seção "Como usar este arquivo" com instruções curtas (em 3-4 linhas) explicando que toda nova decisão relevante deve ser adicionada como uma nova linha na tabela, sempre que eu pedir "registre essa decisão"

---