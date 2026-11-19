# Design System

Um guia para pessoas ensinarem seus agentes de IA a planejar, criar e revisar interfaces sem pular etapas, perder decisões aprovadas ou confundir uma imagem com uma experiência testada.

## 1. Defina o trabalho antes de desenhar

Use quatro camadas para separar consistência de repetição:

- **Método da equipe:** princípios compartilhados de pesquisa, qualidade, acessibilidade, privacidade e evidência.
- **Sistema visual adotado:** componentes, estilo e regras vigentes para aquele produto ou marca. Não transporte automaticamente a estética de um projeto para outro.
- **Ficha de projeto:** público, problema, tarefa prioritária, conteúdo, plataformas, fluxo, escopo e critérios de aceite.
- **Exceções:** registre motivo, alcance, aprovação e teste. Uma exceção de uma tela não vira regra geral.

| Etapa | O agente entrega | Só avance quando… |
| --- | --- | --- |
| Descoberta | Tarefa real, público, contexto, restrições e fontes; separa fatos de hipóteses. | O problema está claro e não depende de presumir que a solução já foi escolhida. |
| Reuso e viabilidade | Inventário de padrões existentes e riscos que podem inviabilizar o fluxo. | Está claro o que reaproveitar e o que precisa de prova antes de prometer. |
| Fluxos e estados | Caminho principal, voltar, cancelar, erros, permissões e recuperação, quando pertinentes. | Cada tarefa tem começo, desfecho e saída; a tela ideal não é o único cenário. |
| Design e aprovação | Peças numeradas e legíveis, com estados e versões identificados. | A pessoa responsável sabe o que está aprovando e o que ainda falta decidir. |
| Implementação e QA | Comparação entre referência e execução, com critérios, testes e limites. | Cada critério tem evidência ou uma pendência clara. |
| Entrega | Versão exata, alterações, testes realizados e próximos passos. | O artefato entregue foi conferido e não há aprovação implícita para publicar. |

Planeje o fluxo inteiro, mas execute em lotes revisáveis. Não corte silenciosamente requisitos aprovados para simplificar uma primeira entrega. Proposta, decisão aprovada, trabalho implementado e teste concluído são rótulos diferentes.

## 2. Use a referência visual como contrato

1. **Identifique a referência exata.** Guarde o original numa localização autorizada. No registro, identifique o arquivo e a versão, o que foi aprovado e o que ainda está em avaliação. Se o agente não puder inspecionar a referência, deve avisar e pedir o original, não usar uma aproximação sem dizer.
2. **Separe o que é fixo do que pode mudar.** Exemplo: “A estrutura, a hierarquia e o formato do painel ficam. Ajustar somente respiro e rótulos.” Ao adaptar para uma tela estreita, preserve a ordem de leitura, não necessariamente as posições absolutas. Registre a adaptação.
3. **Não amplie a aprovação.** Aprovar a forma não aprova cores, textos, ícones nem funcionamento. Uma decisão posterior substitui apenas o trecho conflitante. Preserve as versões anteriores sem misturá-las à referência atual.
4. **Mostre uma peça por imagem para avaliação de detalhes.** Numere o conjunto e associe cada número ao estado e ao formato. Acrescente “Conceito, não é captura da interface em execução” quando pertinente.
5. **Compare lado a lado.** Confira primeiro geometria, hierarquia e alinhamento. Depois revise espaçamentos, contraste, tipografia e consistência dos componentes. Relate diferenças reais, não uma impressão genérica de que “ficou parecido”.

## 3. Revise acessibilidade e funcionamento

| O que conferir | Como conferir |
| --- | --- |
| Legibilidade | Use conteúdo em português e exemplos com títulos longos. Aumente o tamanho do texto e teste largura estreita. Procure cortes e sobreposições. |
| Percepção de estado | Verifique contraste e se sucesso, erro e seleção são reconhecíveis sem depender só da cor. |
| Interação | Teste alvos de toque e, quando a plataforma permitir, ordem de foco, teclado e tecnologias assistivas. Confira se o foco está visível e se há saída do componente. |
| Movimento | Mantenha a animação quando explicar a mudança de estado; confira leitura e continuidade. Quando pertinente, teste com movimento reduzido. |
| Estados não ideais | Use dados vazios, demora, falha, cancelamento, retorno e nova tentativa. Identifique exemplos fictícios e não os apresente como dados reais. |
| Ações reais | Acione, volte e reabra quando necessário. Confira se as ações mudam o estado de verdade e se o que deve persistir continua lá. |

Não transforme tendências visuais em proibições universais. Um gradiente, um contorno ou um ícone pode ajudar; o teste é se serve à tarefa e respeita a identidade aprovada. Bloqueie a entrega se a tarefa principal quebrar, se ela induzir a uma promessa falsa ou se um requisito de acessibilidade não for atendido. Trate preferências estéticas como questões de revisão, não como defeitos comprovados.

## 4. Modelo de revisão para o agente

Copie e preencha uma ficha por fluxo:

- **Objetivo e público:** quem precisa fazer o quê e em qual contexto?
- **Referência vigente:** arquivo, versão e escopo da aprovação.
- **Mudança pedida:** o que muda e o que deve ser preservado?
- **Estado e condição de teste:** qual situação reproduzir e em que ambiente?
- **Resultado esperado e observado:** o que deveria ocorrer e o que realmente ocorreu?
- **Evidência:** conceito, captura de execução ou teste, com versão e condição identificadas.
- **Prioridade e próxima ação:** bloqueio, melhoria ou discussão editorial. Se não houve teste, marque “Não testado”.

## 5. Exercício: painel de envio para aprovação

**Cenário fictício:** o painel foi aprovado apenas quanto à forma. O pedido novo é melhorar o espaçamento e deixar claro quando o envio falhar. Mantenha a estrutura original; não altere a assinatura visual nem acrescente funções não pedidas.

1. Identifique a imagem canônica e escreva, em duas frases, o que fica e o que muda.
2. Prepare referências individuais para **formulário vazio**, **enviando**, **sucesso** e **falha com nova tentativa**. Use um título longo e confira se ele ocupa mais de uma linha sem cobrir o botão.
3. Na implementação, simule uma falha. A mensagem deve explicar o próximo passo sem depender de cor, os campos preenchidos devem permanecer e o envio deve poder ser repetido.
4. Entregue um antes/depois e uma linha de evidência por estado. Se só desenhou, entregue como conceito. Se verificou em execução, indique exatamente a versão e as condições.

**Bom critério de aceite:** “Na falha, preserva os campos, exibe a mensagem e permite tentar novamente. Testado em janela estreita com texto ampliado.” Só escreva a última frase se o teste tiver sido executado.
