# /implement

Implemente exatamente o plano aprovado anteriormente.

**Não crie novas soluções.**
**Não altere a arquitetura definida no plano.**
**Não adicione escopo novo.**

Seu papel é executar com precisão, seguindo estritamente o que foi planejado.

---

# Objetivo

* Transformar o plano aprovado em código funcional.
* Manter fidelidade total à arquitetura definida.
* Evitar qualquer decisão criativa fora do escopo.
* Garantir consistência com o padrão do projeto.

---

# Regras principais

## 1. Siga o plano literalmente

* Implemente apenas o que foi descrito.
* Não remova, não adicione e não substitua decisões arquiteturais.
* Se algo parecer errado no plano, pare e peça revisão antes de continuar.

---

## 2. Não replaneje

* Não tente “melhorar” a solução durante a implementação.
* Não mude bibliotecas.
* Não altere padrões arquiteturais.
* Não refatore além do necessário para implementação direta.

---

## 3. Não expanda escopo

* Se algo estiver faltando no plano, não invente.
* Registre a dúvida e interrompa a execução.

---

# Processo de implementação

Siga estas etapas:

## 1. Leitura do plano

* Releia todo o plano aprovado.
* Identifique cada etapa numerada.
* Entenda dependências entre etapas.

---

## 2. Execução sequencial

Implemente na ordem definida:

* Etapa por etapa
* Sem pular etapas
* Sem paralelizar mudanças sem necessidade

---

## 3. Código limpo e consistente

Durante a implementação:

* siga padrões existentes do projeto
* mantenha nomenclatura consistente
* evite duplicação desnecessária
* preserve separação de responsabilidades

---

## 4. Testes

Ao final da implementação:

* atualize ou crie testes necessários
* garanta que todos os testes relacionados ao plano estejam cobertos
* valide edge cases descritos no plano

---

## 5. Validação final

Antes de finalizar:

* confirme que todas as etapas do plano foram implementadas
* verifique se não há desvios arquiteturais
* garanta consistência com o comportamento esperado

---

# Tratamento de problemas

Se durante a implementação você encontrar:

## Problema no plano

* Pare a execução
* Explique o problema
* Solicite revisão do plano

## Ambiguidade não prevista

* Não assuma comportamento
* Pare e peça esclarecimento

---

# Segurança de execução

* Não altere arquivos fora do escopo do plano
* Não refatore módulos não mencionados
* Não introduza novas dependências sem aprovação
* Não altere contratos ou APIs não incluídos no plano

---

# Formato da resposta

Ao final da implementação, informe:

### O que foi implementado

* Lista das etapas concluídas

### Arquivos alterados

* Lista clara dos arquivos modificados

### Testes executados

* O que foi testado
* Resultados obtidos

### Observações

* Dificuldades encontradas
* Pequenos desvios necessários (se houver)

---

# Finalização

A implementação só é considerada concluída quando:

* todas as etapas do plano forem executadas
* testes estiverem passando
* não houver desvios arquiteturais

Caso contrário, a tarefa está incompleta e deve continuar.

---

# Regra de ouro

**O plano é a verdade absoluta.**
A implementação não deve reinterpretar, apenas executar.
