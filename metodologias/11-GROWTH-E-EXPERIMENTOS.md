# 11 — Growth, experimentação e interpretação de métricas

**Objetivo:** formular experimentos que possam refutar hipóteses, proteger experiência e evitar métricas de vaidade.

## Ciclo
1. **Problema observável:** descrever fricção ou oportunidade sem inferir causa.
2. **Hipótese falsificável:** população + intervenção + efeito esperado + métrica primária + janela + condição de rejeição.
3. **Instrumentação:** evento, denominador, unidade de análise, versão, fonte e qualidade de dados. Definir antes de observar resultado.
4. **Desenho:** A/B randomizado quando viável; se observacional, registrar confundidores e vedar alegação causal forte. Plano de tamanho de amostra/poder conforme efeito mínimo útil, quando aplicável.
5. **Guardrails:** reclamações, erro, confiança, receita líquida, acessibilidade, privacidade e retenção. Não otimizar cliques destruindo valor.
6. **Execução:** preservar grupos, exposição e janela; investigar divergência na distribuição de amostras e rastreamento.
7. **Análise:** comparar resultados absolutos e relativos, incerteza, subgrupos e riscos de múltiplas comparações; não interromper teste no primeiro número favorável sem plano prévio.
8. **Decisão:** adotar, rejeitar, refinar ou repetir — inclusive se inconclusivo. Registrar aprendizado e estado.

## Vocabulário mínimo
- Conversão = eventos concluídos / população elegível segundo definição.
- Diferença em pontos percentuais ≠ uplift relativo.
- Retenção por coorte exige mesmo critério de entrada e janela.
- CAC e LTV dependem de definições contábeis e dados confiáveis.
- Tráfego/seguidores/likes são sinais possíveis, não resultado final universal.

## Cartão de experimento
ID; hipótese; público; alteração; controle; unidade; métrica primária; guardrails; janela; método de atribuição; critério de interrupção; riscos; consentimento; versão; dados; análise; resultado; conclusão; limitantes.

## Falhas comuns
Confundir relato de comunidade com demanda comprovada; extrapolar caso famoso para empresa nova; atribuir crescimento inteiro a uma campanha; comparar antes/depois ignorando sazonalidade; reportar vitória sem denominador; esconder resultado negativo; usar truques que prejudiquem confiança.

**Exemplo fictício:** trocar a primeira frase de convite para evento da biblioteca. Objetivo: aumentar inscrições válidas, não apenas cliques. Verificar que condições e público permanecem comparáveis; testar leitura e reclamações. Se nada foi executado, escrever PROPOSTA, não experimento vencedor.

[Pesquisa de evidências](01-PESQUISA-E-RASTREABILIDADE.md) · [Mercado e produto](12-PRODUTO-E-MERCADO.md).