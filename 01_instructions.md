# Prompt para gerar: 00_instrucoes.md

> Este arquivo é o "manual de operação": define como a LLM deve se comunicar, qual autonomia ela tem, e quais convenções seguir. Gere depois do 01_contexto.md, pois ele se baseia no contexto do projeto.

Copie o prompt abaixo, preencha os campos entre [colchetes] (incluindo cole o conteúdo do 01_contexto.md já gerado) e envie para uma LLM.

---

## PROMPT

Você vai me ajudar a criar um arquivo chamado "00_instrucoes.md", que funcionará como o manual de operação para um projeto que vou desenvolver com a sua ajuda (ou de outra LLM) ao longo de várias conversas futuras.

Aqui está o contexto do projeto (conteúdo do arquivo 01_contexto.md):

[COLE AQUI O CONTEÚDO DO 01_CONTEXTO.MD GERADO ANTERIORMENTE]

Antes de escrever o arquivo final, me faça até 5 perguntas para entender:

1. Que nível de autonomia eu quero te dar — em quais tipos de decisão você pode agir sozinho(a), e em quais sempre deve me perguntar antes
2. Qual tom de comunicação eu prefiro (formal, direto, didático, informal) e em qual idioma
3. Quais formatos de entrega são padrão para este projeto (markdown, docx, código, planilha, apresentação, etc.) e se há preferências de formatação (uso de listas, tamanho de respostas, etc.)
4. Quais pastas ou arquivos do projeto são "protegidos" (nunca editar sem permissão) e quais são de trabalho livre
5. Existe alguma convenção específica de nomenclatura, citação de fontes, ou versionamento de arquivos que devo seguir

Depois das minhas respostas, gere o arquivo 00_instrucoes.md completo em markdown, com a seguinte estrutura:

1. **Regras de chão (não-negociáveis)**: logo no topo do arquivo, antes de qualquer outra seção. Uma lista numerada de 3 a 5 regras curtas e diretas, extraídas das minhas respostas — as poucas coisas que, se quebradas, geram retrabalho ou problema real (ex.: o que ler antes de começar, o que nunca editar, onde sempre entregar o resultado final, quando pedir confirmação antes de agir, o que atualizar ao final da sessão). Essa lista deve ser autossuficiente, pronta para ser colada isoladamente no início de qualquer conversa nova.
2. **Papel da LLM neste Projeto**
3. **Nível de Autonomia**
4. **Tom e Estilo de Comunicação**
5. **Formatos de Entrega**
6. **Pastas e Permissões**
7. **Convenções Específicas**

O resultado deve ser direto o suficiente para eu colar no início de qualquer conversa nova sobre este projeto — seja o arquivo inteiro, seja apenas o bloco de "Regras de chão".

---