# 18 — UX/UI e CRO para páginas de ofertas automotivas

**Público:** agentes de pesquisa, conteúdo, UX, UI, web e marketing. **Escopo:** landing pages de concessionárias e páginas comerciais de veículos. **Status:** síntese metodológica [DOC/PROP], sem dados de clientes, métricas internas, implementação nem validação de resultados. Não substitui o [método geral de UX](04-UX-E-DESIGN-SYSTEM.md).

## O problema a resolver
Uma LP automotiva precisa ajudar uma pessoa a compreender **qual veículo**, **qual versão/condição**, **para quem a oferta vale**, **onde comprar** e **qual ação pode tomar**. Conversão não é apenas clicar: para vendas com atendimento posterior, é relevante distinguir contato iniciado, lead aceito pelo CRM, lead qualificado, agendamento e venda.

A página pode ser de **veículo 0 km**, **seminovo**, **financiamento**, **avaliação de usado**, **venda direta** ou **agendamento**. O agente deve identificar primeiro a tarefa e as restrições; não impor um layout universal ou copiar a identidade de outro produto.

## Contrato de entrada
```text
URL(s), data de inspeção, objetivo de negócio, público/canal, tipo de oferta,
modelo/versão/ano-modelo e unidade quando conhecidos, fonte oficial da oferta,
restrições jurídicas/privacidade, identidade aprovada, acesso autorizado,
evidência disponível (texto/visual/interação/performance/analytics/CRM).
```

Quando faltar informação, marcar **PEND / não verificado** e limitar a inferência. Não completar preço, disponibilidade, juros ou dados de comprador com suposições.

## Passo a passo reproduzível
1. **Entender o anúncio e a intenção.** Qual promessa o usuário viu? A página corresponde a ela? A página atende varejo, venda direta ou outra modalidade?
2. **Mapear a tarefa.** Localizar versão, oferta, condições, especificações, unidade, prova legítima, CTA e rota de recuperação. Enumerar estados vazio/loading/erro/sucesso e comportamento mobile.
3. **Examinar hierarquia visual.** Títulos descritivos, modelo/versão, valor, chamada e condição fáceis de identificar; grid, margens, espaçamento, legibilidade, imagens coerentes e componentes consistentes. Não confundir preferência visual com falha comprovada.
4. **Verificar formulários e contato.** Labels persistentes, dados estritamente necessários, instruções, erros contextuais, confirmação real, destino correto de WhatsApp/telefone. Não chamar clique de conversa concluída.
5. **Revisar acessibilidade e performance.** Teclado, foco, contraste, reflow, alvos, movimento, carregamento do hero, layout shifts e responsividade. Distinguir medição de campo e laboratório.
6. **Conferir risco comercial/legal.** Preço à vista vs entrada, financiamentos, taxas, CET, prazo, estoque, modalidade, condições, elegibilidade e consentimento/privacidade. Submeter à revisão competente; não interpretar sozinho a legislação como parecer jurídico.
7. **Conectar funil à métrica.** Definir lead recebido e lead qualificado, ação de atendimento, proposta e venda. Usar eventos de lead conforme especificação da plataforma, não inventar integrações.
8. **Propor e priorizar.** Primeiro fatos e funcionalidades bloqueantes; depois problemas observados de usabilidade; por fim hipóteses CRO com método de validação. Definir responsável e critérios de aceite.
9. **Validar de verdade.** Testes em dispositivos/navegadores e com pessoas quando aplicável, analytics/CRM consentidos e análise de hipótese com amostra/comparabilidade adequadas. Sem acesso, concluir como proposta, não como teste.
10. **Handoff.** Guardar URL/data/versão, achados, evidência, limites, decisões, alterações realmente realizadas e próximo responsável.

## Checklist compacto para agentes
- [ ] O conteúdo do anúncio corresponde a modelo, versão e oferta da LP.
- [ ] O usuário distingue preço total, entrada, parcela e condições aplicáveis.
- [ ] Elegibilidade de venda direta/bonificação e validade de oferta são claras.
- [ ] Informações essenciais têm hierarquia, contraste, tipografia e espaçamento utilizáveis.
- [ ] CTA primário explica a consequência da ação; alternativas estão contextualizadas.
- [ ] Formulários exibem rótulos e instruções; erros e confirmação são utilizáveis.
- [ ] WhatsApp/telefone preservam contexto da oferta sem vazar dados pessoais.
- [ ] Mobile, teclado, foco, zoom, galeria e sobreposições foram de fato verificados — ou estão PEND.
- [ ] A oferta foi checada no documento comercial vigente; não há urgência falsa.
- [ ] Medição separa cliques, pedidos recebidos, qualificação, atendimento e venda.
- [ ] Nenhum resultado de conversão, inspeção de dispositivo ou integração foi inventado.

## Sistema de prioridade
- **B0**: risco factual, jurídico, privacidade ou ação principal quebrada — bloqueia aprovação até verificação/correção.
- **A1**: conflito entre anúncio e página, oferta vencida, fluxo de contato inválido, versão/unidade incorreta.
- **A2**: obstáculo observado de compreensão, acessibilidade ou hierarquia; propor correção e teste.
- **A3**: melhoria estética ou copy como hipótese, não defeito nem ganho garantido.

**Não calcular “nota de conversão” só com checklist.** Prioridade é uma hipótese operacional; resultados exigem dados.

## Esquema mínimo de um achado
```text
id; url; observado_em; viewport; etapa_funil; classe_evidencia;
descricao_observada; fonte; risco; prioridade; proposta;
excecao; teste_aceite; metrica; dependencias; status.
```

### Exemplo fictício
Uma oferta destaca “Entrada de R$ 40.000”, mas a peça hipotética omite o preço à vista e demais condições. **HIP:** leitores podem confundir entrada e preço final. **DOC:** a legislação brasileira exige clareza sobre elementos da oferta e, conforme o caso, condições de crédito. **PROP:** explicitar no contexto a natureza da quantia e acrescentar condições aprovadas pelo comercial/jurídico. **TEST:** ainda não executado. Não há marca, site, preço real ou resultado observado neste exemplo.

## Fontes verificáveis (consultadas em 20/11/2026)
- [NN/g — 10 heurísticas de usabilidade](https://www.nngroup.com/articles/ten-usability-heuristics/) e [varredura visual por títulos](https://www.nngroup.com/articles/layer-cake-pattern-scanning/).
- [NN/g — erros em formulários](https://www.nngroup.com/articles/errors-forms-design-guidelines/) e [por que placeholders não substituem labels](https://www.nngroup.com/articles/form-design-placeholders/).
- [Baymard — UX de páginas de produto](https://baymard.com/research/product-page); princípios de e-commerce transferidos **somente como hipóteses**, pois carro é compra complexa.
- [USWDS — tipografia e componentes](https://designsystem.digital.gov/components/typography/).
- [W3C — contraste](https://www.w3.org/WAI/WCAG22/Understanding/contrast-minimum), [alvos](https://www.w3.org/WAI/WCAG22/Understanding/target-size-minimum) e [labels](https://www.w3.org/WAI/WCAG22/Understanding/labels-or-instructions).
- [Google — Core Web Vitals](https://developers.google.com/search/docs/appearance/core-web-vitals?hl=pt-BR): referência p75, LCP 2,5 s, INP <200 ms e CLS <0,1.
- [Google Analytics — eventos recomendados de leads, inclusive automotivo](https://support.google.com/analytics/answer/9267735?hl=pt-BR).
- [Webmotors Autoinsights — intenção de compra 2026](https://www.webmotors.com.br/imprensa/lp/intencao-de-compra-segundo-semestre/): amostra brasileira setorial; não representa taxa de conversão de LP.
- [Cox Automotive — jornada de compra 2025, publicada em 2026](https://www.coxautoinc.com/insights/cox-automotive-car-buyer-journey-study-finds-efficiency-digital-tools-and-ai-drive-record-satisfaction/): amostra dos EUA; não extrapolar diretamente ao Brasil.
- [Lei brasileira 8.078/1990 compilada — CDC](https://www.planalto.gov.br/ccivil_03/leis/l8078compilado.htm) e [ANPD — cookies e dados pessoais](https://www.gov.br/anpd/pt-br/centrais-de-conteudo/materiais-educativos-e-publicacoes/guia_orientativo_cookies_e_protecao_de_dados_pessoais).

## Limites de aplicação
A fonte externa pode mudar. Uma LP real não foi inspecionada, um formulário não foi enviado, uma campanha não foi alterada e nenhum A/B ou medição foi conduzido ao produzir este documento. O responsável deve usar briefing atual, autorização adequada e fontes normativas vigentes antes de implementar.
