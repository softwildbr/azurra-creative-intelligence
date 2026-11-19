# 08 — Análise visual, spotting e sound design de cena

**Regra central:** a presença visual de um objeto não prova que ele produz um som audível. A IA pode **propor** efeitos; para declarar som realmente existente, precisa escutar mídia acessível.

## Contrato
Vídeo/versão autorizada; FPS real e timebase; duração; áudio original; objetivo; perspectiva do ouvinte; ambiente; direitos; catálogo disponível; prioridade de fala; formato de entrega e exigências acústicas. Sem mídia, não criar timecodes observados.

## Operação por passes
1. **Decupagem:** identificar limites de planos, movimentos de câmera e espaço acústico persistente.
2. **Inventário visual:** registrar fontes em cena, ações, superfícies, contatos, distâncias, entradas/saídas e possíveis fontes fora de quadro.
3. **Classificação de evidência:** OBSERVADO_VISUALMENTE; OUVIDO_NO_ORIGINAL; INFERIDO_ACUSTICAMENTE; ESCOLHA_CRIATIVA.
4. **Causalidade:** fonte + ação + material + perspectiva + distância + ambiente; avaliar se um som faria sentido, seria mascarado ou deveria ser silêncio.
5. **Prioridade:** HERO (atenção), SUPPORT (ação), BED (ambiente), OPTIONAL, SILENCE. Não preencher todos os espaços compulsoriamente.
6. **Spotting:** indicar ID, in/out real, frame de contato/impacto, transiente, cauda, cena, espaço e intenção. Descrever sincronismo em timebase correta.
7. **Busca em biblioteca autorizada:** consultas em inglês quando ajudarem — source + action + material + perspective + distance + location. Catalogar candidato, licença e escopo.
8. **Pré-escuta:** só registrar como selecionado quando arquivo foi realmente acessado e ouvido; conferir artefatos, tonalidade, dinâmica, perspectiva e licenciamento.
9. **Montagem e revisão:** ambiente base antes de multiplicar pontuais; ouvir em sequência com e sem fala; ajustar panorama, oclusão, EQ e caudas pela escuta, não só pela caixa delimitadora.
10. **Handoff:** spotting sheet, fontes/licenças, escolhas, arquivo real ou status de planejamento e testes pendentes.

## Campos da ficha de cue
~~~yaml
cue_id: FX-001
picture_version: null
shot_id: null
visual_event: ""
visual_evidence: unverified
sound_hypothesis: ""
audibility: optional
listener_perspective: ""
timecode: null
search_terms: []
asset_candidate: null
license_verified: false
audition_verified: false
placement_verified: false
mix_qa: not_tested
~~~

## Erros a evitar
- Inventar um helicóptero no áudio só porque há um objeto distante semelhante na imagem.
- Transformar silêncio expressivo em ruído.
- Confundir efeito de impacto com som de início da ação.
- Preencher URL de banco de sons sem acesso ou licença comprovada.
- Declarar mixagem final a partir de uma planilha de cues.
- Fixar LUFS/true peak sem especificação da plataforma ou do cliente.

**Exemplo fictício:** cena de leitura em biblioteca. Fundo discreto é uma possibilidade [PROP]; passos só onde há movimentação causal; virada de página não é obrigatória; silêncio pode ser o centro da intenção.

[Planilha de spotting](../modelos/FICHA-AUDIOVISUAL-E-SPOTTING.md) · [Pipeline](09-PIPELINE-DE-AUDIO.md).