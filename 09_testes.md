# Prompt para gerar: 09_testes.md

> Este arquivo define a filosofia, stack, estrutura, convenções e padrões de teste do projeto. É o guardião da qualidade do código — garante que qualquer implementação feita (por humano ou LLM) possa ser verificada antes e depois. Gere depois do 05_arquitetura.md e 08_specs.md, pois a estrutura de testes espelha diretamente os sistemas definidos na arquitetura e os contratos definidos nas specs.

Copie o prompt abaixo, preencha os campos entre [colchetes] e envie para uma LLM.

---

## PROMPT

Você vai me ajudar a criar um arquivo chamado "09_testes.md", que definirá a filosofia, stack, estrutura de pastas, convenções e padrões de teste de um projeto que vou desenvolver com a sua ajuda (ou de outra LLM) ao longo de várias conversas futuras.

Aqui está o contexto do projeto (conteúdo do arquivo 01_contexto.md):

[COLE AQUI O CONTEÚDO DO 01_CONTEXTO.MD]

Aqui está a arquitetura técnica do projeto (conteúdo do arquivo 05_arquitetura.md):

[COLE AQUI O CONTEÚDO DO 05_ARQUITETURA.MD]

Aqui estão as specs de cada sistema (conteúdo do arquivo 08_specs.md):

[COLE AQUI O CONTEÚDO DO 08_SPECS.MD]

Informações sobre testes que já sei:

- Quero seguir TDD? (sim / não / parcialmente — descreva): [...]
- Ferramentas de teste que já decidi usar (ou que estão disponíveis no projeto): [...]
- Existe alguma camada do projeto que é difícil ou impossível de testar unitariamente (ex.: cenas de UI, contexto de framework)? Descreva: [...]
- Existe algum requisito de cobertura mínima? (ex.: 80% de cobertura, 100% das funções públicas de core): [...]
- Existe algum fluxo end-to-end crítico que precisa ser testado no browser/runtime real?: [...]

Antes de escrever o arquivo final, me faça perguntas (pode ser mais de uma rodada) para entender:

1. Qual é a sequência obrigatória de passos para implementar qualquer sistema (ex.: escrever testes → implementar → refatorar)
2. Quais sistemas do projeto são testáveis unitariamente (sem dependência de framework/runtime) e quais precisam de testes de integração ou E2E
3. Para cada camada de teste (unitário, integração, E2E): qual ferramenta será usada e qual é o escopo de cada uma
4. Quais helpers de mock serão necessários (substitutos de localStorage, grid de jogo, objetos de estado padrão, etc.) e o que cada um precisa suportar
5. Quais são as convenções de nomenclatura de arquivos, describes e its
6. Quais são as regras de cobertura por camada do projeto
7. Existe alguma integração entre o runtime do projeto e o framework de testes E2E que precisa ser planejada (ex.: expor interface de controle de estado via `window.__X` para o Playwright conseguir manipular o estado interno)

Depois das minhas respostas, gere o arquivo 09_testes.md completo em markdown com as seguintes seções:

1. **Filosofia** — abordagem de testes do projeto (TDD ou não, princípios, sequência obrigatória de implementação em bloco de código ou lista numerada)
2. **Stack de Testes** — tabela com camada, ferramenta e escopo de cada uma
3. **Estrutura de Pastas** — árvore de diretórios da pasta `tests/` espelhando os sistemas da arquitetura, com comentários explicando o que cada subpasta contém
4. **Convenções de Nomenclatura** — regras para nomes de arquivo, describes, its e qualquer outra convenção relevante
5. **Regras de Cobertura** — tabela com camada do projeto e cobertura mínima obrigatória
6. **Padrão de Teste Unitário** — exemplo de código real baseado em um dos sistemas do projeto (não genérico), comentado onde necessário
7. **Padrão de Teste de Integração** — exemplo de código real com dois sistemas do projeto interagindo
8. **Padrão de Teste E2E** — exemplo de código real de um fluxo crítico, incluindo qualquer nota sobre integração com o runtime do projeto
9. **Helpers de Teste** — descrição de cada helper de mock necessário e o que ele suporta
10. **Comandos** — bloco de código com os comandos para rodar cada camada de testes (unitários, watch, cobertura, E2E, E2E com UI)
11. **Regra de Ouro** — em destaque (blockquote), a regra inegociável sobre quando um commit/implementação é válido e o que fazer quando um teste precisa mudar

Nos exemplos de código, use os nomes reais dos sistemas, arquivos e constantes do projeto — não use placeholders genéricos como `MyClass` ou `myFunction`. Marque com `[A DEFINIR]` qualquer detalhe que ainda não foi decidido.

---
