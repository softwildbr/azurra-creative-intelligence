# Growth e experimentação

**Objetivo de treino:** ajudar um agente a transformar uma oportunidade de crescimento em um teste interpretável, sem confundir alcance com adoção nem ganhar conversão às custas da confiança.

## Escolha o problema antes da tática

| Etapa | Pergunta | Exemplo de medida |
| --- | --- | --- |
| Aquisição | Estamos chegando a quem pode se beneficiar? | Visitas qualificadas por origem, não impressões brutas |
| Ativação | A pessoa chega ao primeiro resultado útil? | Proporção de visitantes elegíveis que completam a tarefa-chave |
| Retenção | Existe motivo para voltar sem insistência? | Proporção de uma coorte que repete a tarefa na janela definida |
| Indicação | Compartilhar resolve algo para quem envia e quem recebe? | Convites aceitos que chegam à primeira tarefa útil |

**Coorte** é um grupo com ponto de partida comum, como a semana do primeiro uso. Compare coortes com tempo semelhante de observação. Se o volume depende de anúncios, trate isso como canal de aquisição. Só se torna um ciclo de crescimento quando uma ação gera uma entrada que alimenta o próximo ciclo: por exemplo, alguém compartilha voluntariamente um modelo, o destinatário o usa e pode optar por compartilhar com outra pessoa.

Antes de recomendar uma tática, descreva o gargalo, a evidência, o mecanismo esperado e uma explicação alternativa. Separe alcance, atenção, ação e resultado de negócio; um não é substituto automático do outro.

## Cartão de experimento

- **Observação:** o que aconteceu, em qual grupo e período? Como sabemos?
- **Hipótese:** para [público], se [mudança única], então [ação] melhora porque [mecanismo].
- **Comparação e elegibilidade:** o que fica igual? Quem entra? Quem receberá cada versão? Evite que a mesma pessoa veja condições incompatíveis.
- **Métrica principal:** numerador, denominador, janela e diferença mínima que justificaria a mudança.
- **Métricas de proteção:** o que não pode piorar, por exemplo, reclamações, cancelamentos ou conclusão por teclado.
- **Confiabilidade:** como detectar eventos duplicados, coleta quebrada e diferença entre volumes esperados e observados de cada grupo?
- **Decisão prévia:** quando olhar, quando interromper por risco e o que conta como adotar, ajustar, repetir ou descartar.
- **Entrega:** resultado, limitações, diferenças entre grupos, próxima decisão e quem aprova.

### Nem todo teste precisa ser um A/B

Quando houver tráfego e instrumentação suficientes, distribuição aleatória ajuda a isolar o efeito. Faça primeiro uma conferência da coleta; um desbalanceamento inesperado entre grupos é sinal para investigar, não para interpretar o resultado. Evite encerrar na primeira leitura favorável. Quando houver pouco volume, um teste moderado por tarefa pode revelar atrito, mas não estima sozinho o impacto no funil. Uma comparação antes/depois pode orientar investigação, mas campanhas, sazonalidade e mudanças de público também explicam diferenças.

## Exercício: páginas de reserva de uma biblioteca fictícia

O relatório mostra muitas visitas à página das oficinas, mas não revela se as pessoas encontram horários ou concluem reservas. Primeiro, defina os eventos de visualização de horários, início e confirmação. A hipótese é que exibir horários na primeira dobra aumenta **reservas confirmadas por visitante elegível**. Use cancelamentos e pedidos de ajuda como proteção. Compare uma versão que move só os horários. Se houver poucas reservas, observe pessoas encontrando um horário no celular e registre obstáculos sem prometer melhoria percentual.

**Critério de aceite:** o agente não recomendará “dobrar anúncios” antes de saber onde a jornada trava; não chamará clique de reserva; não declarará vencedor com coleta inconsistente.

## Limites que o agente não negocia

- Nada de urgência falsa, aceite pré-marcado, descadastro dificultado, convite automático ou coleta sem finalidade clara.
- Não reúna dados pessoais só porque está tecnicamente disponível. Use o mínimo necessário no teste e defina acesso, retenção e descarte.
- Estudos de caso inspiram mecanismos, não garantem causalidade nem ganhos. Separe relato público, hipótese e medição própria.
- Use fontes e regras atualizadas antes de decidir sobre privacidade e plataformas. Este material é uma prática de produção, não orientação jurídica.

Referências públicas: [Artigo sobre desbalanceamento de amostra em experimentos](https://www.microsoft.com/en-us/research/publication/diagnosing-sample-ratio-mismatch-in-online-controlled-experiments-a-taxonomy-and-rules-of-thumb-for-practitioners/) · [OECD: práticas comerciais manipulativas](https://doi.org/10.1787/44f5e846-en).
