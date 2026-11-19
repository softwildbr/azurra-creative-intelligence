# 02 — Converter estudos em instruções executáveis para agentes

Uma biblioteca útil para IA precisa responder **quando**, **como**, **com quais insumos**, **que evidência prova o resultado** e **quando parar**. Resumos de pesquisa, isoladamente, não constituem instrução de produção.

## Conversão em sete passos
1. **Inventariar:** título, versão, autor/fonte, escopo, status e dependências. Distinguir resultado de pesquisa, regra aprovada e experimento não realizado.
2. **Extrair mecanismos:** o que foi observado, qual princípio pode explicar e em que condições ele não vale.
3. **Resolver duplicatas:** agrupar orientações equivalentes, marcar conflitos e escolher uma fonte canônica por conceito sem apagar divergências.
4. **Escrever a decisão:** problema detectável → opções viáveis → critério de escolha → comportamento esperado.
5. **Criar runbook:** papel do agente; entradas mínimas; sequência numerada; bloqueios; testes; saída; exemplo fictício; registro para o próximo agente.
6. **Amarrar ao artefato:** mapa pergunta→evidência→decisão→arquivo→teste→aprovação. Não chamar um link ou prompt de produto entregue.
7. **Revisar manutenção:** gatilho para nova pesquisa (versão, política, caso adverso, métrica nova), responsável, data e changelog.

## Estrutura canônica de um playbook
- **Propósito e limites:** qual tipo de solicitação resolve; que resultado não garante.
- **Entradas:** objetivo, projeto, fonte oficial, mídia, destino, direitos, ambiente, aprovação.
- **Roteador:** selecione técnica A/B/C com condições observáveis e alternativa simples.
- **Passos:** verbo de ação, artefato intermediário, gate e erro comum por etapa.
- **QA verificável:** inspeção real, método de comparação, falhas graves, reteste.
- **Saída:** documento, arquivo, versão e evidências, ou plano com bloqueios.
- **Handoff:** decisão tomada, resultado, o que NÃO foi testado, próxima ação.

## Níveis de maturidade
| Nível | Pode afirmar | Não pode afirmar |
|---|---|---|
| L0 referência | Fonte catalogada | Método aplicável |
| L1 síntese | Princípio com limites | Execução funcional |
| L2 runbook | Procedimento reproduzível proposto | Teste realizado |
| L3 piloto | Resultado sob condições registradas | Validação geral |
| L4 homologado | Aceite formal para escopo e versão | Validade para todos os clientes |

## Contrato de saída recomendado
~~~yaml
module: pesquisa
objective: ""
decision: ""
sources: []
observations: []
hypotheses: []
recommended_procedure: []
blocking_dependencies: []
actual_artifacts: []
tests_executed: []
tests_not_executed: []
approval: pending
next_action: ""
~~~

## Antipadrões
- Copiar 100 páginas e deixar o agente sem rota de consulta.
- Tratar especialista, criador de conteúdo ou fórum como regra universal.
- Confundir padrão visual com identidade de cliente.
- Converter preferência do revisor em aceite global.
- Publicar casos reais ou links restritos como exemplo didático.
- Relatar QA sem abrir a saída renderizada.

**Exemplo fictício:** pesquisa sobre tipografia revela uma recomendação de contraste. O runbook diz verificar texto crítico em tela pequena, comparar com especificação real e registrar resultado; não impõe um tamanho universal por ser popular na web.