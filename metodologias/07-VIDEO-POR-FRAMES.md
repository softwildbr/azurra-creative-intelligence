# 07 — Geração de vídeo guiada por frames inicial e final

**Objetivo:** reduzir incoerência de identidade, movimento, perspectiva e geografia entre dois quadros. Este documento é um protocolo criativo; **disponibilidade, nomes, preços, créditos e suporte de modelos devem ser reconferidos na fonte oficial antes de executar**.

## Entradas
Objetivo/beat; referências autorizadas; quadro inicial e final efetivamente disponíveis; proporção; duração pretendida; ação do sujeito; movimento de câmera; elementos invariantes; geografia; iluminação; permissões de upload; custo/créditos; destino. Se não há frames reais, rotular descrições como planejadas.

## Sequência de sete gates
1. **Direitos e custo:** autorização de enviar arquivos a provedor? Licença de uso? Ferramenta e créditos confirmados? Sem isso, PLANNING_ONLY.
2. **Continuidade:** inventariar pessoa/objeto, pose, direção, cenário, escala, linha de horizonte, luz e o que deve permanecer idêntico. Comparar frames lado a lado.
3. **Viabilidade temporal:** o trajeto conecta os quadros sem teleporte? Mudança de câmera implica corte? Se houver várias ações incompatíveis, separar em cenas.
4. **Escolha de estratégia:** frame-to-video, plano único, oclusão, transição com corte, geração apenas de frame ou pós-produção convencional; justificar a opção mais simples.
5. **Prompt:** escrever assunto + ação principal + movimento de câmera + ambiente/luz + direção + invariantes + restrições observáveis. Evitar listas contraditórias de movimentos.
6. **Pré-QA:** linguagem consistente, duração factível, sentido de deslocamento explícito, objeto central preservado e ausência de elementos não autorizados.
7. **Execução e QA:** registrar versão do modelo, data, configurações, tentativa, custo, output e falhas **somente se efetivamente gerados**; inspecionar sequência e frames intermediários, não apenas começo/fim.

## Template de prompt proposto
~~~text
Shot objective: [uma ideia narrativa]
Source: [frames autorizados e suas versões]
Subject and invariants: [identidade, quantidade, proporções e itens protegidos]
Action: [um movimento principal do sujeito]
Camera: [um movimento claro ou câmera fixa]
Direction: [ex.: sujeito se desloca da direita para a esquerda na tela]
Environment and lighting: [o que deve continuar]
Temporal path: [progressão visual até o frame final]
Avoid: [duplicações, troca de ocupantes/objetos, geometria implausível]
Acceptance: [como verificar a continuidade no resultado]
~~~

## Rubrica de inspeção
Identidade/contagem; continuidade de cenário; direção correta; física e contato; sombras/reflexos; deformações; objetos atravessados; texto/logos; corte temporal; coerência de áudio quando presente; conformidade de direitos. Registrar timecode do defeito real.

**Exemplo fictício:** ônibus ilustrado atravessa uma paisagem da direita para a esquerda. Frame inicial lateral e final aéreo não constituem uma câmera única inevitável: produzir duas cenas se a transição exigir mudança de plano. Não afirmar geração sem output acessível.

[Direção de câmera](05-CINEMATOGRAFIA-E-EDICAO.md) · [QA](15-QA-E-COBERTURA.md).