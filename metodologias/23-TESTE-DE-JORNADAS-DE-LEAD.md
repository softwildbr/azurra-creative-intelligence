# 23 — Teste de jornadas de lead e mensuração de conversão

**Quando usar** · Quando uma página depende de formulário, conversa ou retorno comercial. O objetivo é verificar a passagem de cada ação até o sistema que a recebe.

## Preparar e testar

1. Defina os destinos e seus responsáveis. Registre página, versão, dispositivo, origem simulada, canal e critérios para identificar um lead válido. Em ofertas automotivas, faça primeiro a [checagem de consistência](19-AUDITORIA-DE-CONSISTENCIA-DE-OFERTAS.md).
2. Faça a inspeção visual em mobile e desktop. Percorra os campos por toque e teclado, confira rótulos, foco, mensagens de erro, repasse do contexto da oferta e possibilidade de corrigir a entrada.
3. Combine ambiente de teste ou destino controlado com quem recebe os contatos. Use dados fictícios autorizados e identificáveis como teste. Verifique entrada inválida, falha de envio, nova tentativa, sucesso e toque duplo quando aplicável. Confira se uma falha preserva o conteúdo digitado sem gerar submissões duplicadas.
4. Para formulário, compare a confirmação exibida com a resposta da aplicação e o registro no destino. Para WhatsApp, confira destino e mensagem inicial com contexto autorizado e sem dados pessoais embutidos na URL. Verifique quando uma conversa foi de fato recebida em ambiente controlado.
5. Compare o registro de cada etapa apenas nas superfícies com acesso aprovado. Use identificadores de teste e evidências sem dados pessoais. Documente bloqueios de acesso no ponto em que surgirem.

## Etapas e evidências

| Etapa | Evidência para declarar sucesso |
|---|---|
| Clique em contato | Telemetria ou observação do acionamento |
| Formulário aceito | Resposta da aplicação para a submissão de teste |
| Conversa recebida | Mensagem efetivamente recebida no destino controlado |
| Lead registrado | Registro correspondente no destino ou CRM |
| Lead qualificado | Status registrado conforme o critério de atendimento adotado |
| Agendamento ou venda | Registro do desfecho no sistema responsável |

Para um experimento, declare hipótese, população, período, uma métrica principal, seu denominador e critérios de qualidade do lead. Registre separadamente perda entre etapas, duplicidade e casos sem acesso ao destino. Use o identificador disponível e permitido para conciliar eventos quando possível.

**Exercício fictício** · A página confirma dois envios. O CRM de teste registra apenas um. Registre dois sucessos na superfície visível e um recebimento confirmado. Reúna horário, versão e identificador para investigar a divergência antes de avaliar conversão.

[UX/CRO automotivo](18-UX-CRO-AUTOMOTIVO.md) · [Experimentação](11-GROWTH-E-EXPERIMENTOS.md) · [QA e cobertura](15-QA-E-COBERTURA.md).
