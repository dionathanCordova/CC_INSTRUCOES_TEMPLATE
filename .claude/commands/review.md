# /review

Revise todas as alterações realizadas na sessão atual ou no conjunto de arquivos modificados.

**Não faça alterações no código.**
Seu papel é apenas analisar e fornecer feedback.

## Objetivos

Realize uma revisão completa considerando:

### 1. Correção

* Há bugs ou comportamentos incorretos?
* Existem edge cases não tratados?
* Há possíveis regressões?

### 2. Arquitetura

* A solução segue a arquitetura do projeto?
* Há violação de responsabilidades?
* Existe alto acoplamento?
* A solução poderia ser mais simples?

### 3. Clean Code

Avalie:

* nomes
* organização
* legibilidade
* duplicação
* complexidade
* funções muito grandes
* classes muito grandes
* responsabilidade única

### 4. Performance

Procure por:

* consultas desnecessárias
* loops ineficientes
* processamento redundante
* consumo excessivo de memória
* oportunidades de otimização

### 5. Segurança

Verifique:

* validações ausentes
* autenticação
* autorização
* exposição de dados
* tratamento de entradas
* possíveis vulnerabilidades

### 6. Testes

Avalie:

* cobertura suficiente
* casos de sucesso
* edge cases
* casos inválidos
* testes ausentes

### 7. Manutenibilidade

Analise:

* facilidade para futuras alterações
* escalabilidade da solução
* facilidade de leitura
* facilidade de manutenção

---

## Classifique cada problema

Utilize uma das categorias:

🔴 Crítico
Problema que pode gerar falhas, perda de dados, vulnerabilidades ou comportamento incorreto.

🟠 Alto
Problema importante que deve ser corrigido antes do merge.

🟡 Médio
Melhoria recomendada.

🟢 Baixo
Pequenos ajustes de qualidade ou estilo.

---

## Formato da resposta

### Resumo

* Qualidade geral da implementação
* Principais pontos positivos
* Principais riscos encontrados

### Problemas encontrados

Para cada problema informe:

* Severidade
* Arquivo
* Linha (quando possível)
* Explicação
* Sugestão de correção

### Melhorias sugeridas

Liste melhorias que aumentariam:

* legibilidade
* performance
* segurança
* simplicidade
* arquitetura

### Veredito final

Escolha apenas uma opção:

* ✅ Aprovado
* 🟡 Aprovado com ressalvas
* ❌ Requer alterações antes do merge

Não faça alterações automaticamente. Aguarde minha aprovação caso eu solicite que alguma sugestão seja implementada.
