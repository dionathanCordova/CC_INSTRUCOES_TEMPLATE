# Guia de Uso — Template de Arquivos Essenciais para Projetos com LLM

Este kit contém 5 arquivos. Cada um traz, em vez do conteúdo final, um **prompt pronto** para você preencher e enviar a uma LLM (Claude ou outra). A LLM vai te fazer perguntas de contexto e, ao final, gerar o conteúdo definitivo daquele arquivo.

## Ordem recomendada de geração

1. **01_contexto.md** — comece por aqui. É a base de tudo: define o que é o projeto, objetivo e restrições.
2. **00_instrucoes.md** — com o contexto pronto, defina como você quer ser atendido (autonomia, tom, formatos).
3. **03_glossario.md** — termos e nomenclaturas que vão se repetir no projeto.
4. **02_decisoes.md** — registre as decisões já tomadas até aqui (mesmo que poucas).
5. **04_status.md** — o "estado atual" do projeto. Este é o único que você deve **atualizar com frequência** (a cada sessão de trabalho relevante).

## Como usar no dia a dia

- No início de qualquer conversa nova sobre o projeto, cole o conteúdo de `00_instrucoes.md`, `01_contexto.md` e `04_status.md` (os 3 mais importantes para retomar o contexto).
- Sempre que uma decisão importante for tomada, peça para registrar em `02_decisoes.md`.
- Ao final de uma sessão de trabalho, peça para atualizar `04_status.md` com o que foi feito e os próximos passos.

## Sobre as pastas físicas

Junto com esses 5 arquivos, crie estas pastas (vazias por enquanto):

```
templates/   ← modelos protegidos, nunca editar
entradas/    ← material bruto, pesquisas, referências
trabalho/    ← rascunhos e versões em andamento
saidas/      ← entregas finalizadas
arquivo/     ← histórico encerrado
```

Pronto. Bora gerar o conteúdo real?