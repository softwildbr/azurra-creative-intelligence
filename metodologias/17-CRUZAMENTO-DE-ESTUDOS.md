# 17 — Cruzar pesquisas e gerar insights operacionais

**Finalidade:** criar descobertas testáveis a partir de fontes de áreas diferentes, sem inventar vínculo causal. Recomendado para planejamento de campanha, UX, produto, audiovisual e treinamento de agentes.

## Método de cruzamento
1. **Pergunta de decisão:** ex.: como melhorar compreensão de um anúncio audiovisual de serviço?
2. **Selecionar eixos:** atenção/psicologia, composição/UX, narrativa, câmera/edição, som/voz, contexto de canal e métrica. Não usar todo o acervo indiscriminadamente.
3. **Extrair cartões de evidência:** ID, afirmação, fonte, data/escopo, tipo, força, limitação e aplicabilidade.
4. **Montar matriz:** linhas = problema de produção; colunas = eixos. Anotar convergências, contradições e ausências.
5. **Propor mecanismo:** “pode ocorrer porque...”, qual intervenção é de baixo risco e o que refutaria a interpretação.
6. **Priorizar:** impacto plausível, confiança na evidência, custo, risco/direitos e reversibilidade. Pontuação é heurística, não resultado empírico.
7. **Criar procedimento:** uma ação observável, entrada, responsável, teste e saída. Regras vagas como “mais cinematográfico” não são metodologia.
8. **Comparar com alternativa simples:** se um corte ou texto resolver, não adicionar IA, motion, plugins e camadas por reflexo.
9. **Registrar decisão:** hipótese aprovada para testar, implementada com QA ou descartada, sem confundir estados.

## Matriz de análise exemplificativa
| Fricção | Evidência por área | Hipótese transferível | Teste |
|---|---|---|---|
| Público não identifica oferta | UX: hierarquia; direção de arte: foco; edição: tempo de permanência | CTA/benefício pode precisar de hierarquia melhor | leitura sem contexto e inspeção em celular |
| Vídeo parece ruidoso | Som: mascaramento; roteiro: excesso de informação; motion: efeitos simultâneos | Reduzir densidade pode melhorar compreensão | comparar montagem com/sem camada |
| Cena gerada perde coerência | Câmera: continuidade; vídeo por frames: invariantes; QA: estado de origem | Dividir em dois planos pode reduzir contradições | comparar artefatos reais, se autorizados |
| Engajamento alto, uso baixo | Growth: proxy; produto: proposta de valor; UI: tarefa | Canal pode trazer audiência pouco aderente | métricas por coorte e entrevistas/piloto |

## Formato do insight
**Problema** / **observação comprovada** / **mecanismo candidato** / **contraexplicações** / **ação proposta** / **condições de uso** / **efeitos adversos** / **teste mínimo** / **evidência necessária** / **status**.

## Gates de integridade
- Não promover correlação a causalidade.
- Não reaproveitar identidade de cliente ou produto em outra marca.
- Não tornar regra geral uma preferência local.
- Não afirmar que algoritmo, público ou voz reagirão de determinado modo sem teste.
- Não executar teste real quando o usuário o dispensou ou não autorizou; propor apenas protocolo documental quando aplicável.

**Exemplo fictício:** uma biblioteca tem vídeo social que o público não compreende. Cruzamento de hierarquia, corte e carga cognitiva sugere apresentar serviço antes de efeitos. O insight é hipótese, não prova de conversão.

[Pesquisa](01-PESQUISA-E-RASTREABILIDADE.md) · [Síntese](02-SINTESE-PARA-AGENTES.md) · [QA](15-QA-E-COBERTURA.md).