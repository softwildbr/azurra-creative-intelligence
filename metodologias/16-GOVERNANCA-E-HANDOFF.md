# 16 — Governança, estados e memória de produção para agentes

**Objetivo:** preservar continuidade entre agentes sem supor que outro agente viu o histórico de conversa. O repositório deve explicar **estado real, decisões, evidências, riscos e próxima ação**.

## Preflight obrigatório
1. Ler pedido, briefing vigente, README, regras de agentes, status, histórico de mudanças e decisões pertinentes.
2. Identificar o arquivo canônico, versão atual e autorização — diferenciar branch, protótipo, render, aprovado e publicado.
3. Verificar se há outra tarefa/alteração em andamento antes de sobrescrever arquivos. Usar commits atômicos quando possível e não forçar atualização sem necessidade.
4. Consultar métodos específicos e fontes atuais antes de alterar produto/UX/criação de maneira substancial.
5. Formular execução pequena, teste correspondente e critério de conclusão.

## Máquina de estados comum
**PESQUISA → HIPÓTESE → PLANO → PROVA/PILOTO → PRODUÇÃO → QA REAL → APROVAÇÃO → ENTREGA/PUBLICAÇÃO.** O processo pode ter iterações, mas uma etapa documental não se transforma em execução por descrição.

| Registro | Exigência mínima |
|---|---|
| Decisão | objeto, alternativas, motivo, responsável, data, versão e limitações |
| Alteração | arquivos, comportamento antes/depois, dependência e motivo |
| Teste | ambiente, ação, saída, resultado e evidência concreta |
| Aprovação | quem, o quê, versão, canal e escopo |
| Entrega | destino, artefato, hash/versão se aplicável e confirmação |
| Handoff | pendências, riscos, próximo passo e condição de aceite |

## Memória resistente a links quebrados
Guardar no documento contexto, problema, decisão, método, resultado e limite. Links servem para conferir, não como único lugar da instrução. Teste: se todos os links forem ocultados, outro agente ainda sabe o que ocorreu e o que falta? Links privados nunca devem constar da versão pública.

## Rotina de revisão de mudanças
- Se o arquivo não existe, não afirmar que foi criado.
- Se ferramenta não foi executada, escrever NOT_EXECUTED.
- Se QA falhou, continuar PEND e registrar correção/reteste.
- Se uma nova versão substitui recomendação anterior, criar registro de mudança, não apagar histórico silenciosamente.
- Se fonte recente contradiz guia antigo, expor conflito e validar o escopo antes de promover regra.

## Handoff obrigatório em cada entrega
Objetivo → fontes e versões → decisões e status → arquivos modificados → verificação efetuada → verificação não efetuada → bloqueios → autorização pendente → próxima ação mínima.

**Exemplo fictício:** outro agente recebeu apenas um PDF de preview de um hotsite. Registro correto: “prévia gerada; código, clique do botão e responsividade não verificados; aguarda fonte editável”. Não escrever “site pronto”.

[Modelo de handoff](../modelos/HANDOFF-AGENTE-VERIFICAVEL.md) · [Direitos](14-DIREITOS-E-PUBLICACAO.md).