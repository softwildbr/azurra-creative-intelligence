# 21 — Avaliação, seleção de modelos e economia de tokens

**Quando usar** · Para decidir se um agente, modelo ou instrução pode assumir uma tarefa de produção e qual configuração compensa manter.

## Medir antes de trocar

1. Defina uma configuração de referência com versão de modelo, instruções, fontes, ferramentas e permissões. Declare entregáveis, verificações obrigatórias e tempo aceitável por classe de tarefa.
2. Monte um corpus pequeno e versionado com entradas autorizadas. Inclua casos comuns, fonte vencida, conflito, ferramenta indisponível, evidência ausente e efeito externo solicitado sem autorização. Separe exemplos usados para ajustar o agente dos casos reservados para comparação.
3. Rode as configurações nas mesmas entradas. Use verificações determinísticas para campos, referências e recibos quando possível. Use revisão humana para julgamento editorial, legibilidade e justificativa. Se houver avaliador automático para questões editoriais, confira divergências em amostra humana.
4. Registre sucesso e falha por caso com evidência. Meça tarefas aceitas sobre as iniciadas, tempo até aceite e custo total por tarefa aceita. O custo deve incluir tentativas, chamadas a ferramentas cobradas e revisão quando mensurável. Com zero aceites, reporte custo total e zero aceites, deixando a razão como indefinida.
5. Aplique bloqueios antes de comparar médias. Vazamento, publicação indevida, duplicação de gravação e falso relato de conclusão impedem promoção enquanto persistirem. Reexecute os casos afetados após a correção e mantenha uma configuração anterior recuperável.

## Reduzir custo com qualidade

| Sinal observado | Mudança para testar | Evidência para decidir |
|---|---|---|
| Muita leitura irrelevante | Carregar índice e buscar trechos autorizados por necessidade | Tokens de entrada e aceitação dos casos com fonte |
| Instruções repetidas com pouca variação | Testar prefixo estável e cache, quando suportados | Uso efetivo de cache, custo e tempo medidos |
| Classificação e extração bem delimitadas | Comparar modelo com menor custo para essa classe | Erros por classe, custo por aceite e escalonamentos |
| Muitas tentativas ou reanálises | Melhorar o contrato, validar entrada e limitar novas tentativas | Tempo, custo total e falhas recuperadas |
| Casos ambíguos passam com falsa segurança | Escalar para configuração mais capaz ou revisão humana | Precisão nos casos críticos e qualidade do encaminhamento |

Preserve a instrução vigente, a autorização e as evidências mínimas ao reduzir contexto. Compare preço de tabela com consumo observado e registre a base da cobrança. Sob assinatura ou quota, acompanhe uso disponível, espera e volume aceito. Se o custo financeiro por tarefa estiver indisponível, reporte essa lacuna junto de tokens e tempo observáveis.

**Exemplo fictício** · Em um lote de dez análises, uma configuração entrega oito pareceres aceitos e duas devoluções. O custo total das dez execuções, incluindo novas tentativas, é dividido por oito. Uma média menor só favorece a troca se as falhas críticas estiverem resolvidas e os critérios editoriais forem atendidos.

[Especificação de agentes](20-ESPECIFICACAO-DE-AGENTES.md) · [Ficha de agente e piloto](../modelos/FICHA-DE-AGENTE-E-PILOTO.md).
