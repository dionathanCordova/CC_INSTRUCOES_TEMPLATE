# Prompt para gerar: 04_status.md

> Este é o arquivo mais "vivo" do projeto: representa o estado atual e os próximos passos. Deve ser atualizado com frequência (idealmente ao final de cada sessão de trabalho relevante). O prompt abaixo cria a estrutura inicial e o primeiro snapshot de status.

Copie o prompt abaixo, preencha os campos entre [colchetes] e envie para uma LLM.

---

## PROMPT

Você vai me ajudar a criar um arquivo chamado "04_status.md", que será o "estado atual" de um projeto — o arquivo que devo colar no início de qualquer conversa nova para retomar o trabalho de onde parei.

Aqui está o contexto do projeto (conteúdo do arquivo 01_contexto.md):

[COLE AQUI O CONTEÚDO DO 01_CONTEXTO.MD]

Informações sobre o estado atual:

- O que já foi feito até agora: [...]
- O que está em andamento neste momento: [...]
- O que ainda não foi começado, mas está planejado: [...]
- Existe algum bloqueio, pendência ou dependência externa: [...]

Com base nisso, gere o arquivo 04_status.md em markdown com as seções:

1. **Última atualização**: [data de hoje]
2. **Resumo em 2-3 linhas**: visão geral rápida de onde o projeto está agora
3. **Concluído**: lista do que já foi entregue/finalizado
4. **Em andamento**: lista do que está sendo trabalhado agora, com o que falta para concluir cada item
5. **Próximos passos**: lista priorizada do que vem a seguir
6. **Bloqueios / Pendências**: o que está impedindo o progresso, se houver
7. **Notas para a próxima sessão**: qualquer informação que a LLM precisa saber para continuar o trabalho sem perder contexto

No final, adicione uma instrução curta dizendo: "Atualize este arquivo ao final de cada sessão de trabalho relevante, substituindo as seções acima pelo novo estado do projeto."

---