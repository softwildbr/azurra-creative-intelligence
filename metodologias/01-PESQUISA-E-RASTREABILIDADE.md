# 01 — Pesquisa rigorosa, evidências e rastreabilidade

**Objetivo:** transformar uma pergunta vaga em uma decisão sustentada por documentação verificável. Indicado para novas ferramentas, tendências, benchmarking, áreas técnicas e avaliação de hipóteses.

## Contrato de entrada
Pergunta principal; decisão que a pesquisa vai informar; público/cenário; período e região; fontes autorizadas; exclusões; limites de tempo/acesso; formato da entrega. Registre o que já se sabe e o que precisa ser confirmado. Se a questão se alterar durante a busca, versionar a pergunta.

## Protocolo
1. **Decompor:** uma pergunta central, 3–7 subperguntas que possam ser respondidas ou explicitamente permanecer sem resposta.
2. **Planejar a busca:** termos principais, sinônimos em português/inglês, documentação oficial, literatura técnica e comunidade. Anotar data, buscas tentadas e cobertura. Pesquisa exploratória NÃO é revisão sistemática.
3. **Priorizar fontes conforme a afirmação:** especificação de software exige fabricante e versão; regra jurídica exige norma atual e jurisdição; experiência de uso pode exigir observação direta; Reddit/fóruns sinalizam problemas e divergências, não frequência populacional.
4. **Extrair unidade por unidade:** afirmação; trecho/paráfrase; URL e autor; data; contexto; tipo DOC/OBS/COM; condições; limites; possível conflito.
5. **Triangular:** conferir fonte primária, descrição independente e contraexemplo quando material. Se divergem, registrar ambas; não escolher a mais conveniente.
6. **Separar quatro camadas:** fato documental; inferência analítica; hipótese de aplicação; proposta de execução. Não permitir que uma hipótese vire fato por repetição.
7. **Traduzir em ação:** entrada, procedimento, saída, custo/risco, condição para aceitar/rejeitar e evidência a coletar. Não terminar apenas com lista de links.
8. **Revisar e atualizar:** conteúdo regulatório, versão de produto e preços envelhecem. Registrar data de verificação e sinal de rechecagem.

## Força da evidência — matriz de uso
| Tipo | Serve para | Não autoriza concluir |
|---|---|---|
| Manual/API/fabricante | Funcionalidade declarada, limites e compatibilidade documentada | Que funcionou no equipamento do projeto |
| Artigo acadêmico | Questão, método, resultados no escopo estudado | Causalidade além do desenho ou transferência direta |
| Reportagem/caso de fornecedor | Contexto e alegações atribuídas | Resultados independentemente auditados |
| Comunidade/Reddit | Descobrir fricções, vocabulário e hipóteses | Tamanho de mercado, taxa de ocorrência e representatividade |
| Teste do próprio projeto | Comportamento observado sob condições registradas | Generalização para todo público/versão |

## Ficha da evidência
ID | pergunta | alegação | tipo | fonte/URL | autor | publicado/em consulta | versão/região | evidência extraída | interpretação | conflito | grau de confiança justificado | uso recomendado | direito de reprodução.

## Gates
- **G1 Cobertura:** foram buscadas fontes contraditórias e primárias?
- **G2 Proveniência:** cada fato material tem fonte e contexto verificáveis?
- **G3 Transferência:** o método pode falhar em outra audiência, ferramenta ou país?
- **G4 Implementação:** existe autorização e ambiente para teste? Se não, saída = PLANO DOCUMENTAL.
- **G5 Publicação:** só síntese própria, sem reproduzir artigo, PDF, print ou áudio protegido sem direito.

**Exemplo fictício:** um fórum diz que vídeos curtos convertem mais. Resultado responsável: registrar o relato [COM], propor duas aberturas [HIP], definir métrica por público e canal [PROP]. Não afirmar conversão superior [TEST] sem experimento real.

[Modelo de ficha](../modelos/FICHA-PESQUISA-OPERACIONAL.md) · [Síntese](02-SINTESE-PARA-AGENTES.md).