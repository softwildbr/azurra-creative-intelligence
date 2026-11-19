# 04 — UX, UI e design system orientados a estados

**Aplicação:** websites, landing pages, dashboards, apps, onboarding, extensões e experiências interativas. Não adotar uma solução de outro produto como identidade aprovada.

## Sequência
1. **Descoberta da tarefa:** usuário, objetivo, ambiente, fricção, critérios de sucesso e restrições. Não começar pela estética.
2. **Arquitetura de informação:** fluxos, ações principais e secundárias; entradas, erros, vazios, carregamentos, permissões e recuperação.
3. **Contrato de estados:** para cada componente, mapear default, hover/foco (quando aplicável), pressionado, desabilitado, carregando, erro, sucesso e vazio.
4. **Sistema de componentes:** tokens de espaço, tipografia, cor, ícones, bordas e motion; anotar origem, versão e possibilidade de extensão.
5. **Protótipo e implementação:** preservar hierarquia e textos críticos entre wireframe, design e produto funcional. Separar protótipo de código executado.
6. **Validação:** testar tarefa completa no dispositivo-alvo, com zoom, teclado, acessibilidade e interrupções plausíveis.
7. **Cobertura:** ligar requisito → tela → componente → estado → teste → resultado.

## Grade mínima de avaliação
| Critério | Pergunta de QA |
|---|---|
| Utilidade | A função resolve a necessidade observada? |
| Clareza | Nome de ação, texto e próximo passo compreensíveis? |
| Localização | Idioma, unidades, formatação e direção coerentes? |
| Acessibilidade | Foco, rótulos, contraste, zoom e tecnologia assistiva? |
| Robustez | Erro/sem internet/permissão negada/voltar funcionam? |
| Consistência | Tokens e componentes coerentes sem impedir contexto? |
| Performance | Tempo de resposta e feedback testados no ambiente real? |
| Segurança | Dados, permissões e tratamento de conteúdo externo restritos? |

## Design system ≠ galeria de telas
Regras precisam dizer **quando aplicar**, **qual componente usar**, **variações**, **exceções**, **contraexemplos** e **o que testar**. Guardar fonte oficial aprovada. Captura de screenshot não prova clique funcional; UI bonita não prova requisito concluído.

## Instrução para agente
Entregar: mapa de tarefas, árvore de navegação, inventário de estados, especificação de tokens quando conhecidos, telas propostas, testes e lacunas. Usar estados PEND quando não houver implementação/acesso. Não inventar compatibilidade de navegador/dispositivo.

**Exemplo fictício:** formulário de inscrição de uma biblioteca. Estados obrigatórios: vazio, preenchimento parcial, erro campo, envio em progresso, falha de rede e confirmação; testar recuperação sem perda de texto. A tela inicial sozinha não valida o fluxo.

[Design system introdutório](../modulos/design-system/design-system.md) · [QA de cobertura](15-QA-E-COBERTURA.md).