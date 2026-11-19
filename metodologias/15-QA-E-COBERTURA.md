# 15 — QA verificável e matriz de cobertura

**Objetivo:** revisar o que realmente foi produzido, medir lacunas e retestar proporcionalmente a mudanças. Uma lista de 100 testes planejados não é 100 testes executados.

## Construir cobertura
Ligar cada requisito a: ID → justificativa → artefato/tela/cena → fluxo → estado → teste → evidência → resultado → responsável. Requisitos sem caso ou casos sem evidência ficam PENDENTES.

## Passes de revisão
1. **Factual:** textos, preços, datas, claims, identidade, modelo de produto e versão contra fonte aprovada.
2. **Criativo:** hierarquia, ritmo, clareza, mensagem, propósito de efeitos, leitura em contexto.
3. **Técnico:** arquivo abre; tamanho/aspecto/duração/fps/codec; dependências; editabilidade; áudio; nomes e versões.
4. **Acessibilidade e destino:** contraste, zonas seguras, legibilidade, legendas, foco e requisitos reais do canal.
5. **Direitos e distribuição:** assets/vozes/músicas/licenças, dados pessoais, consentimentos e escopo de aprovação.
6. **Regressão:** comparar master e derivados; testar novamente os pontos impactados pela alteração.
7. **Evidências:** registrar o que se abriu, observou, mediu e corrigiu. Não homologar render a partir apenas da timeline ou de um print.

## Severidade
| Estado | Exemplo | Ação |
|---|---|---|
| BLOCKER | Informação falsa, marca incorreta, direitos ausentes, arquivo quebrado | Bloquear entrega e corrigir |
| MAJOR | Texto ilegível, sobreposição, quebra de fluxo, sincronismo ruim | Corrigir e retestar |
| MINOR | Detalhe de alinhamento sem perda de função | Corrigir conforme prioridade |
| INFO | Preferência ou melhoria opcional | Registrar; não chamar de erro |
| UNKNOWN | Sem mídia/ambiente/acesso para avaliar | Solicitar evidência; não aprovar |

## Regra de reteste por mudança
- **Texto/condição comum:** todas as variantes afetadas, leitura e legal.
- **Composição local:** proporção/área segura e master relacionado.
- **Keyframe ou sincronismo:** início, pico, contato, saída, loop e trecho com som.
- **Mudança de versão de imagem:** reavaliar cues de áudio e cortes.
- **Configuração de export:** reabrir arquivo distribuído e conferir metadados relevantes.
- **Código de interface:** estados/fluxos impactados, regressão e acessibilidade.

## Matriz resumida
| ID | Req | Versão | Artefato | Caso | Esperado | Executado? | Evidência | Resultado | Reteste |
|---|---|---|---|---|---|---|---|---|---|
| EX-01 | CTA legível no mobile | v0 | mock fictício | T-01 | usuário identifica ação | não | — | PEND | após protótipo |

## Aprovação com fronteiras
Aceite de arte estática não libera automaticamente motion, mídia paga ou publicação; aprovação de um formato não cobre os demais; usuário dizer “gostei” não vale por todos os requisitos. Guardar objeto, versão, aprovador, data e escopo.

[Revisão existente](../checklists/PRONTO-PARA-APROVAR.md) · [Governança](16-GOVERNANCA-E-HANDOFF.md).