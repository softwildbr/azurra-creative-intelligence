# 06 — Motion, Graph Editor, cinemagraph e loops

**Propósito:** criar movimento legível, deliberado e reproduzível, com curvas e fechamentos de ciclo verificáveis. Primeiro escolher o comportamento; depois os controles do software.

## Roteador
| Caso | Rota inicial | Controle principal |
|---|---|---|
| Elemento entrando/saindo | Position/Opacity/Scale com keyframes | Timing e spacing |
| Impacto ou pouso | Acelerar para o contato e amortecer se apropriado | Speed Graph e overshoot real |
| Movimento em trajetória | Path + temporal/spatial interpolation | Geometria e velocidade separadas |
| Movimento contínuo | Ciclo com início/fim coerentes | Continuidade C0 e velocidade C1 |
| Cinemagraph | Região móvel isolada e maior parte estática | Máscara, backfill, loop e limites |
| Ilustração com partes | Separação de camadas e pivôs | Não rasgar traço, evitar deformação |

## Procedimento
1. **Intenção:** definir o que o movimento comunica (entrada, importância, surpresa, continuidade, calma).
2. **Asset:** confirmar fonte, camadas, área móvel (ROI), áreas intocáveis, oclusões, formato, fps e direitos.
3. **Diagnóstico:** identificar propriedade (posição, valor, rotação, forma), keys, velocidade, trajetórias e pivôs. Uma curva visualmente suave pode gerar aceleração indesejada.
4. **Plano:** marcar começo, antecipação, aceleração, pico, desaceleração, hold e saída; usar primeiro a solução com menos keys.
5. **Execução controlada:** alterar cópia do master; comparar Value Graph e Speed Graph conforme propriedade; verificar influência e velocidade efetivas, não copiar percentuais sem contexto.
6. **Loop:** escolher período e domínio. Verificar correspondência visual do último para o primeiro (C0) e continuidade de direção/velocidade (C1) quando requerida. Um corte brusco pode ser intencional, mas deve ser justificado.
7. **Revisão:** assistir em velocidade de exibição, no formato-alvo, com 3–5 repetições quando houver loop; conferir overlays, máscaras, variação de cor, marca e legibilidade.
8. **Entregar:** versão editável, render real, fps/duração/codec e registro dos testes efetivamente realizados.

## Armadilhas
- Ease in/ease out aplicado a todas as propriedades sem considerar finalidade.
- Uma posição espacial aparentemente correta com velocidade indesejada em ponto de controle.
- Confundir rotação local com deslocamento de câmera.
- Esconder emendas com blur exagerado ou múltiplos efeitos.
- Gerar movimento de uma fotografia e chamar de footage de evento real.
- Animar a marca, condição ou texto legal além do uso autorizado.

## Exemplo fictício
Ilustração de janela de biblioteca: só a cortina oscila. Estático = parede, placa, texto e janela. ROI = tecido; pivô superior. Opção A: Puppet Pin discreto; B: deformação de shape. Aprovada a direção, criar 1 ciclo, testar bordas de máscara e emenda temporal; se não houver AE/arquivo, entregar apenas plano e não afirmar render.

[Filmagem e edição](05-CINEMATOGRAFIA-E-EDICAO.md) · [QA](15-QA-E-COBERTURA.md).