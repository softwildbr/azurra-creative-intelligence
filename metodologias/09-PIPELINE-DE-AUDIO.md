# 09 — Pipeline de áudio: Premiere, Audition e After Effects

**Padrão operacional proposto:** Premiere é a central de montagem e exportação; After Effects anima e pode usar áudio-guia; Audition entra quando reparos ou mixagem multitrack justificam a ida e volta. Em projetos complexos pode ser necessário outro ambiente de pós especializada. Não é exclusividade de software.

## Roteador R0–R3
| Rota | Condição | Saída |
|---|---|---|
| R0 — Premiere | Poucas camadas, voz/trilha/SFX simples, picture em revisão | Mix e vídeo final no Premiere |
| R1 — Audition Clip | Ruído, clique, hum, reparo pontual | Áudio derivado tratado, reintegrado ao Premiere |
| R2 — Audition Multitrack | Foley, ambientes, buses, automação, múltiplas stems | Sessão, premix, mix/stems e conform |
| R3 — Pós especializada | ADR extenso, multicanal, cinema, intercâmbio complexo | Escopo e turnover técnico para equipe apropriada |

## Procedimento
1. **Intake:** confirmar picture_version, duração, FPS racional, canais, sample rate, material original, roteiro/locução, destino, licenças e specs. Não inferir da extensão ou nome do arquivo.
2. **Spotting:** construir mapa de cenas, DX/VO, BG/AMB, FOLEY, SPOT/HARD FX, DESIGN, MX e silêncio; definir prioridade e ponto de escuta.
3. **Pré-montagem:** música-guia e cues temporários sincronizados ao corte; evitar round-trip de mix complexa enquanto imagem mudar intensamente.
4. **Tratamento:** original preservado; processamento por problema comprovado. Não usar nuvem, plugins pagos ou IA que consuma créditos sem aprovação.
5. **Sessão:** pistas e buses coerentes; rotas ao master sem duplicar ganho; nomes consistentes; FX editáveis e material dry disponível quando útil.
6. **Mix:** começar pela inteligibilidade de voz quando houver, depois música/ambiente/efeitos. Checar mascaramento, transientes, dinâmica, espacialidade e continuidade.
7. **Conform:** se mudou picture, registrar antes/depois e revisar cues afetados por corte, mudança temporal ou deslocamento; não assumir que stems continuam sincronizadas.
8. **Entrega:** exportar e reabrir mix, stems e master; conferir valores conforme norma do destino, canais, ausência de clipping, versão e integridade.

## Conferir o arquivo exportado

- **Voz encoberta** · Ouça a sequência nas passagens com música e efeitos. Isole as camadas para localizar mascaramento e reavalie a fala com a mixagem completa depois do ajuste.
- **Efeito fora do tempo** · Compare o transiente com o quadro de contato no master de vídeo. Se o corte mudou, revise primeiro a versão e a posição do cue.
- **Som inconsistente entre planos** · Ouça as emendas em sequência. Revise o nível do ambiente, a perspectiva, as caudas e as transições onde o espaço muda.
- **Mix e stems** · Reabra os arquivos produzidos e compare versão, início, duração e canais. Onde o contrato pedir recomposição, verifique a soma nas condições descritas no turnover e registre diferenças esperadas decorrentes do processamento do master.

## Condições de bloqueio
Sem direitos de música/voz/SFX, impedir publicação. Sem vídeo e áudio reais, entregar apenas planejamento. Sem medidor, não declarar LUFS/dBTP testados. Sem prova de preview, não declarar sync perfeito.

## Exemplo fictício
Anúncio de 20 segundos com fala, trilha e três SFX: começar em R0. Se houver restauração de uma fala ruim, usar R1 para aquele clipe. Se o projeto passar a ter cenas com ambientes, passos e camadas articuladas, avaliar R2. O número de segundos não é regra fixa.

[Spotting](08-SPOTTING-E-SOUND-DESIGN.md) · [Ficha audiovisual](../modelos/FICHA-AUDIOVISUAL-E-SPOTTING.md).
