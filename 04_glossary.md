# Prompt para gerar: 03_glossario.md

> Este arquivo padroniza termos, nomes próprios, abreviações e definições específicas do projeto, para que a LLM (e qualquer pessoa da equipe) use sempre a mesma nomenclatura.

Copie o prompt abaixo, preencha os campos entre [colchetes] e envie para uma LLM.

---

## PROMPT

Você vai me ajudar a criar um arquivo chamado "03_glossario.md", que será o glossário oficial de termos de um projeto.

Aqui está o contexto do projeto (conteúdo do arquivo 01_contexto.md):

[COLE AQUI O CONTEÚDO DO 01_CONTEXTO.MD]

Termos que eu já sei que precisam de definição/padronização (nomes de produtos, marcas, abreviações, jargões internos, nomes de pessoas/cargos relevantes):

[LISTE AQUI OS TERMOS, UM POR LINHA, COM UMA BREVE EXPLICAÇÃO SE TIVER. Se não tiver nenhum ainda, escreva "nenhum ainda, me ajude a identificar quais seriam necessários".]

Com base nisso:

1. Se eu não tiver listado termos, analise o contexto do projeto e sugira de 5 a 10 termos que provavelmente precisarão de padronização, e me pergunte as definições corretas de cada um
2. Gere o arquivo 03_glossario.md em markdown com uma tabela no formato:

| Termo | Definição / Forma correta | Não usar | Observações |
|-------|---------------------------|----------|-------------|

3. Preencha a tabela com os termos e definições fornecidos
4. No final, adicione uma seção curta "Como usar este arquivo" explicando que, ao escrever qualquer conteúdo para o projeto, este glossário deve ser consultado para manter consistência, e que novos termos devem ser adicionados conforme surgirem

---