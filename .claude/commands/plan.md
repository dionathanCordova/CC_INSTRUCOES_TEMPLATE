# /plan

Analise cuidadosamente a solicitação do usuário e elabore um plano completo de implementação.

**Não escreva código.**
**Não altere arquivos.**
Seu papel é atuar como Arquiteto de Software, propondo a melhor estratégia antes da implementação.

---

# Objetivos

Antes de qualquer implementação:

* Compreenda completamente o problema.
* Identifique ambiguidades ou informações faltantes.
* Avalie o impacto da mudança.
* Proponha a solução mais adequada.
* Divida o trabalho em etapas pequenas e objetivas.
* Aguarde minha aprovação antes da execução.

Caso existam dúvidas sobre os requisitos, faça perguntas antes de elaborar o plano.

---

# Análise do problema

Explique:

* Qual problema será resolvido.
* Qual o objetivo da funcionalidade.
* Quais regras de negócio estão envolvidas.
* Quais restrições devem ser respeitadas.

Caso existam múltiplas interpretações possíveis, apresente cada uma delas.

---

# Escopo

Defina claramente:

## O que será feito

Liste tudo que faz parte da implementação.

## O que NÃO será feito

Liste explicitamente tudo que está fora do escopo para evitar mudanças desnecessárias.

---

# Arquivos e componentes impactados

Identifique quais partes do projeto provavelmente serão afetadas.

Por exemplo:

* APIs
* Controllers
* Services
* Repositories
* Smart Contracts
* Banco de dados
* Frontend
* Configurações
* Testes
* Documentação
* Infraestrutura
* CI/CD

Explique por que cada componente será impactado.

---

# Estratégia de implementação

Descreva:

* A abordagem escolhida.
* Por que ela foi escolhida.
* Quais alternativas foram consideradas.
* Vantagens e desvantagens da solução.

Sempre priorize simplicidade, clareza e facilidade de manutenção.

---

# Dependências

Liste:

* bibliotecas
* frameworks
* APIs externas
* serviços
* contratos
* recursos de infraestrutura

Informe se alguma nova dependência precisará ser adicionada.

---

# Impacto na arquitetura

Explique:

* quais módulos serão afetados;
* se haverá alteração de interfaces públicas;
* se haverá impacto em outros serviços;
* se existe risco de quebrar compatibilidade.

---

# Segurança

Analise possíveis impactos relacionados a:

* autenticação
* autorização
* validação de entradas
* exposição de dados
* gerenciamento de permissões
* tratamento de erros
* dados sensíveis

Caso não exista impacto, informe explicitamente.

---

# Performance

Avalie:

* possíveis gargalos;
* consultas adicionais;
* uso de memória;
* processamento desnecessário;
* impacto em escalabilidade.

Caso não exista impacto relevante, informe.

---

# Estratégia de testes

Defina quais testes deverão ser implementados.

Considere:

* testes unitários;
* testes de integração;
* testes end-to-end;
* casos de sucesso;
* edge cases;
* entradas inválidas;
* regressões.

---

# Plano de implementação

Divida a implementação em pequenas etapas numeradas.

Exemplo:

1. Preparação
2. Alteração da arquitetura
3. Implementação principal
4. Atualização dos testes
5. Atualização da documentação
6. Validação final

Cada etapa deve possuir um objetivo claro.

---

# Riscos

Liste possíveis riscos da implementação.

Classifique-os como:

🔴 Alto

🟠 Médio

🟢 Baixo

Explique como cada risco pode ser mitigado.

---

# Critérios de aceite

Liste condições objetivas que devem ser verdadeiras para considerar a tarefa concluída.

Exemplos:

* Todos os testes passando.
* Nenhuma regressão.
* Documentação atualizada.
* Performance preservada.
* Código seguindo o padrão do projeto.

---

# Resumo executivo

Ao final apresente um resumo contendo:

* Objetivo da tarefa.
* Estratégia escolhida.
* Componentes afetados.
* Principais riscos.
* Estimativa de complexidade.

Classifique a complexidade como:

🟢 Baixa

🟡 Média

🟠 Alta

🔴 Muito Alta

---

# Aprovação

Após apresentar o plano, **não implemente nada automaticamente**.

Aguarde minha aprovação explícita antes de iniciar qualquer alteração no código.

Caso eu solicite ajustes no plano, atualize-o antes de prosseguir para a implementação.
