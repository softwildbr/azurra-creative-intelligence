# 20 — Especificação de agentes de produção criativa

**Quando usar** · Antes de criar ou ampliar um agente de pesquisa, criação, revisão ou atendimento. O protocolo produz uma ficha revisável e um plano de piloto.

## Especificar o trabalho

1. Descreva uma tarefa recorrente em termos de entrada, ação, entrega observável e pessoa que usa o resultado. Registre uma tarefa próxima que fica fora do papel.
2. Identifique a fonte que decide cada informação, a versão em vigor, quem autoriza exceções e como o agente registra conflitos. Se duas fontes autorizadas divergirem, preserve ambas e encaminhe a decisão.
3. Defina a saída com campos, critérios de aceite, local de entrega e evidência de conclusão. Para cada ferramenta, descreva o que ela lê, grava ou envia e como confirma o efeito.
4. Escolha a arquitetura pela necessidade demonstrada.

| Situação | Comece por |
|---|---|
| Passos fixos e verificáveis | Fluxo explícito com validação em cada transição |
| Uma tarefa varia conforme o briefing | Um agente com instruções, exemplos e ferramentas limitadas |
| Documentos mudam ou variam por projeto | Busca documental (RAG) com escopo, vigência e indicação de fonte |
| Execução com aprovações, retomada ou efeitos externos | Camada de execução (harness) com permissões, estados e confirmação no destino |
| Especialidades com saídas independentes e contratos claros | Delegação com dono por entrega e revisão da integração |
| Erro de comportamento persiste em casos de teste após corrigir instruções, fontes e ferramentas | Avaliar ajuste fino com dados autorizados e conjunto de avaliação separado |

5. Escreva instruções com exemplos de aceitação, ambiguidade real e interrupção. Especifique quando retornar um rascunho, pedir decisão, registrar bloqueio ou confirmar entrega.
6. Rode o [piloto de avaliação](21-AVALIACAO-E-CUSTO-DE-AGENTES.md) com dados fictícios. Comece com leitura antes de conceder ações que alterem sistemas, quando o fluxo permitir essa progressão.

## Operações e retomada

O agente recebe somente o escopo necessário por tarefa. Confirme autorização antes de um efeito externo. Se a confirmação de uma gravação ou de um envio falhar, consulte o destino ou o registro da operação antes de tentar novamente. Em cada handoff, identifique a tarefa, a versão, a evidência, o estado e o responsável pela próxima decisão.

**Exemplo fictício** · Um agente de revisão de anúncios recebe duas versões de um título, encontra o texto aprovado e retorna inconsistências com o trecho de origem. Se a aprovação estiver ausente, registra a lacuna e entrega a revisão dos demais itens. O piloto prevê um briefing vigente, um vencido e uma solicitação de envio fora do escopo.

[Ficha de especificação](../modelos/FICHA-DE-AGENTE-E-PILOTO.md) · [Governança e handoff](16-GOVERNANCA-E-HANDOFF.md).
