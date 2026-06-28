# /self-check

Realize uma verificação crítica e independente da última resposta gerada (código, plano, refactor ou qualquer saída técnica relevante).

**Não gere nova implementação como resposta principal.**
Seu objetivo é atuar como um auditor técnico, identificando falhas, inconsistências e riscos.

---

# Objetivo

* Validar a correção da solução proposta ou implementada.
* Identificar erros lógicos, técnicos e arquiteturais.
* Detectar problemas de segurança, performance e edge cases.
* Aumentar o nível de confiança da solução antes de seguir para produção.

---

# Escopo da análise

Analise a última saída considerando:

## 1. Correção lógica

* A solução resolve o problema proposto?
* Há erros de lógica ou comportamento incorreto?
* Existem inconsistências com o requisito original?

---

## 2. Segurança

Verifique:

* validação de entrada
* autenticação e autorização
* exposição de dados sensíveis
* uso correto de criptografia
* possíveis vulnerabilidades (injeção, overflow, etc.)

---

## 3. Edge cases

Avalie:

* entradas nulas ou inválidas
* cenários extremos
* comportamento inesperado
* falhas silenciosas

---

## 4. Uso correto de APIs e bibliotecas

* funções estão sendo usadas corretamente?
* há risco de uso incorreto de métodos (ex: decode vs verify)?
* dependências estão sendo usadas de forma segura?

---

## 5. Performance

* há operações desnecessárias?
* loops ou queries ineficientes?
* consumo excessivo de memória ou CPU?

---

## 6. Consistência com arquitetura

* respeita padrões do projeto?
* segue separação de responsabilidades?
* evita acoplamento indevido?

---

## 7. Qualidade do código (se aplicável)

* legibilidade
* clareza de nomes
* duplicação
* complexidade desnecessária

---

# Processo de verificação

## 1. Releitura da solução

Releia a resposta anterior com olhar crítico, como um reviewer experiente.

---

## 2. Identificação de problemas

Liste todos os problemas encontrados, mesmo que pequenos.

---

## 3. Classificação de severidade

Classifique cada problema:

🔴 Crítico

* falhas de segurança
* bugs que quebram o sistema
* comportamento incorreto grave

🟠 Alto

* problemas funcionais importantes
* risco de bug em produção

🟡 Médio

* melhorias recomendadas

🟢 Baixo

* ajustes de estilo ou legibilidade

---

## 4. Sugestões de correção

Para cada problema identificado:

* explique o problema
* proponha a correção ideal
* explique o impacto da correção

---

# Self-confidence score

Ao final, forneça uma nota de confiança da solução:

* 0–50% → alta probabilidade de erro
* 51–80% → funcional, mas com riscos
* 81–95% → boa solução com pequenos ajustes
* 96–100% → solução sólida e pronta para produção

---

# Formato da resposta

## Resumo da análise

* Qualidade geral da solução
* Principais pontos positivos
* Principais riscos encontrados

---

## Problemas identificados

Para cada problema:

* Severidade
* Descrição do problema
* Impacto potencial
* Sugestão de correção

---

## Recomendações gerais

* melhorias estruturais
* melhorias de segurança
* melhorias de performance
* melhorias de clareza

---

## Veredito final

Escolha uma das opções:

* ✅ Aprovado
* 🟡 Aprovado com ressalvas
* ❌ Requer revisão

---

# Regra principal

**Nenhuma solução deve ser considerada confiável sem passar por uma etapa de self-check crítico.**
