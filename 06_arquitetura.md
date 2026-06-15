# Prompt para gerar: 06_arquitetura.md

> Este arquivo documenta a arquitetura técnica do projeto: stack escolhida, estrutura de pastas, padrões de código e decisões de arquitetura registradas. Gere depois do 01_contexto.md, pois depende do escopo e objetivos do projeto para fazer sentido.

Copie o prompt abaixo, preencha os campos entre [colchetes] (incluindo o contexto do projeto já gerado) e envie para uma LLM.

---

## PROMPT

Você vai me ajudar a criar um arquivo chamado "05_arquitetura.md", que será o documento de referência técnica de um projeto que vou desenvolver com a sua ajuda (ou de outra LLM) ao longo de várias conversas futuras.

Aqui está o contexto do projeto (conteúdo do arquivo 01_contexto.md):

[COLE AQUI O CONTEÚDO DO 01_CONTEXTO.MD]

Informações técnicas que já tenho sobre o projeto:

- Tipo de projeto (web app, jogo, API, mobile, script, etc.): [...]
- Linguagem(ns) principal(is): [...]
- Frameworks ou bibliotecas que já decidi usar (ou que são obrigatórias): [...]
- Plataforma alvo (browser, desktop, mobile, servidor, etc.): [...]
- Já existe alguma estrutura de pastas iniciada? (se sim, descreva ou cole aqui): [...]
- Existe algum padrão de nomenclatura ou convenção de código que quero seguir: [...]
- Como será feita a persistência de dados (banco, localStorage, arquivo, etc.): [...]
- Existe algum sistema de build ou deploy já definido: [...]

Antes de escrever o arquivo final, me faça perguntas (pode ser mais de uma rodada) para entender em profundidade:

1. Quais são os principais sistemas ou módulos do projeto e como eles se relacionam entre si
2. Quais são as convenções de código que devem ser seguidas (nomenclatura de arquivos, variáveis, funções, classes)
3. Existe alguma regra de isolamento ou separação de responsabilidades importante (ex.: nunca chamar X diretamente, sempre passar por Y)
4. Quais partes do projeto são "core" (reutilizadas em todo lugar) versus específicas de um contexto/módulo
5. Existe alguma decisão de arquitetura já tomada que deve ser registrada e justificada
6. Há planos de evolução técnica futura que a arquitetura atual deve antecipar (ex.: trocar banco de dados, adicionar backend, escalar para mobile)

Depois das minhas respostas, gere o arquivo 05_arquitetura.md completo em markdown, com as seguintes seções:

1. **Visão Geral Técnica**: tabela com stack, rendering/runtime, persistência, plataforma alvo, sistema de build
2. **Estrutura de Pastas**: árvore de diretórios comentada, explicando o papel de cada pasta e arquivo relevante
3. **Padrões de Código**: regras de nomenclatura, convenções de herança/extensão, regras de isolamento (o que nunca deve ser feito diretamente e por quê)
4. **Decisões de Arquitetura Registradas**: lista das principais decisões técnicas tomadas, cada uma com justificativa e referência ao 03_decisoes.md quando aplicável

Seja específico e use exatamente as informações que eu te dei. Não invente tecnologias, nomes de arquivos ou padrões que não foram mencionados. O arquivo deve ser completo o suficiente para que qualquer LLM (ou desenvolvedor novo no projeto) entenda como o projeto está estruturado e quais regras seguir, sem precisar perguntar o básico.

---
