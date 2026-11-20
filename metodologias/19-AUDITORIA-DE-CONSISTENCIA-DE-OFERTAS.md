# 19 — Auditoria de consistência comercial e jornada de conversão

**Aplicação:** landing pages de ofertas, campanhas, e-commerce de compras complexas, concessionárias e serviços com condições comerciais. **Status:** método público generalizado, com exemplos fictícios; sem dados internos, testes executados, métricas de clientes ou sites modificados. Complementa [18 — UX/UI e CRO automotivo](18-UX-CRO-AUTOMOTIVO.md) e [04 — UX/design system](04-UX-E-DESIGN-SYSTEM.md).

## Por que precisa de um módulo separado?
Uma página pode ter hierarquia impecável e ser ruim para o usuário porque **o produto da chamada não é o mesmo do contrato**, ou porque o formulário destina o lead à loja errada. Um agente que olha somente o layout pode ignorar erro material e sugerir trocar a cor do botão. Este módulo impõe um **gate factual/comercial** antes de otimização estética.

## Regra de ouro
Não corrigir por inferência uma divergência entre fontes. O agente **encontra** dois valores, classifica o risco, identifica a fonte oficial e encaminha aos responsáveis. O valor final deve vir de documento vigente aprovado, não da resposta do modelo.

## Contrato mínimo de entrada
`page_url, reviewed_at, offer_id_or_unknown, product_model, version, model_year, payment_modality, eligible_audience, region_or_unit, approved_ad_or_unknown, terms_source_or_unknown, access_level, device_evidence`.

## Sequência operacional
1. **Mapear a entidade comercial:** modelo/variante/ano, prazo, região, modalidade, público elegível, preço à vista, entrada, parcela, taxas/encargos e bônus como campos **separados**.
2. **Construir matriz de correspondência:** anúncio, catálogo, hero da LP, detalhes, tabela técnica, regulamento, CTA, WhatsApp/formulário, CRM. Se não houver acesso ao CRM, marcar PEND.
3. **Detectar conflitos:** nome, versão, ano-modelo, motor/equipamentos, período/estoque, tipo de preço, taxa/CET e destino da ação.
4. **Classificar evidência:** OBS-T se houve leitura documental; OBS visual só quando houve screenshot/inspeção de tela; TEST somente se ação executada; HIP para hipótese de melhoria.
5. **Bloquear correção indevida:** exigir responsável comercial/jurídico/produto para master comercial; design e desenvolvimento aplicam alteração apenas após decisão.
6. **Auditar experiência:** clareza hierárquica, informação material acessível, formulário proporcional à etapa, estados de erro/sucesso, acessibilidade e dispositivos.
7. **Mapear funil:** evento de clique ≠ pedido confirmado ≠ contato atendido ≠ lead qualificado ≠ venda. Sem dados de CRM, otimizar como hipótese, nunca afirmar conversão.
8. **Priorizar e registrar:** riscos factuais antes de hipóteses estéticas, critérios de aceite, versão e evidência de implementação.

## Ficha de conflito
`id; url; data; campo; fonte_a; valor_a; fonte_b; valor_b; gravidade_candidata; fonte_mestra_a_confirmar; responsavel; proposta_sem_valor_inventado; teste_aceite; status`.

### Exercício fictício A — divergência entre resumo e tabela
Uma ficha imaginária de SUV descreve rodas de 18", enquanto a tabela interna indica 17". **OBS** apenas se ambas as seções foram abertas; caso contrário **HIP**. Não escolher um valor. **PROP:** consultar SKU/ano-modelo oficial, corrigir em todos os módulos e fazer QA em produção. Não transformar a divergência em acusação de fraude.

### Exercício fictício B — promessa de financiamento
Um anúncio imaginário de carro apresenta “taxa 0%” e, em termos, tarifas/encargos podem compor o custo total. **DOC**: no Brasil, a legislação exige informações de crédito e CET conforme modalidade. **PROP**: comercial/jurídico conferir clareza da oferta, diferenças entre juros nominais e CET, financiador, valor total, condições e validade. Não deduzir ilegalidade só pela expressão publicitária.

### Exercício fictício C — formulário extenso
Uma etapa inicial de consulta solicita nome, telefone, CPF, renda, banco e documentação. **HIP:** coleta pode ser desproporcional para pergunta simples, mas justificável numa etapa de análise de crédito. **PROP:** mapear finalidade, minimizar dados e apresentar progressivamente conforme a jornada, sem retirar campos essenciais ou prometer aprovação financeira.

## UI e acessibilidade: avaliação real, não opinião
- Inspecionar desktop e mobile em tamanhos relevantes ao público, com **320 CSS px para reflow** quando pertinente.
- Validar foco, contraste, rótulos de formulário, teclado, sticky CTA, overlays e informações da oferta.
- Um print não prova que o botão envia, nem que o design é WCAG conforme todas as regras.
- Tokens tipográficos, margens e cards devem seguir marca vigente e ser ajustados ao conteúdo; não impor valores universais.

## Checklist de treinamento do agente
- [ ] Detectou conflitos sem escolher dado comercial por suposição.
- [ ] Separou o que foi lido no site do que foi testado.
- [ ] Registrou URL/data/versão e responsáveis.
- [ ] Identificou diferença entre preço total, entrada, parcela, juros e CET.
- [ ] Considerou modalidade e elegibilidade sem copiar condição de outro público.
- [ ] Examinou formulário e WhatsApp pelo estágio e finalidade do contato.
- [ ] Priorizou conformidade/fato/fluxo acima de preferências de composição.
- [ ] Não prometeu crescimento de conversão sem experimento.
- [ ] Documentou perguntas em aberto, gate de aceite e handoff.

## Fontes públicas
- [CDC brasileiro compilado](https://www.planalto.gov.br/ccivil_03/leis/l8078compilado.htm), arts. 30–31, 52 e 54-B/C.
- [Nielsen Norman Group — formulário EAS](https://www.nngroup.com/articles/eas-framework-simplify-forms/) e [progressive disclosure](https://www.nngroup.com/articles/progressive-disclosure/).
- [USWDS — Forms](https://designsystem.digital.gov/components/form/).
- [W3C WCAG 2.2 — reflow](https://www.w3.org/WAI/WCAG22/Understanding/reflow) e [focus visible](https://www.w3.org/WAI/WCAG22/Understanding/focus-visible).
- [GA4 — eventos de lead](https://developers.google.com/analytics/devguides/collection/ga4/reference/events?hl=pt-BR).

**Limites:** pesquisa documental, não consultoria jurídica. Não armazenar dados pessoais ou exemplos de campanhas confidenciais no repositório público. Uma recomendação só vira teste/resultado quando os registros reais comprovam isso.
