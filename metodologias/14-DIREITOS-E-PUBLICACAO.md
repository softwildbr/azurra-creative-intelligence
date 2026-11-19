# 14 — Direitos, confidencialidade e publicação responsável

**Regra:** acesso para ler não implica licença para redistribuir. Um repositório privado aberto ao agente não autoriza migrar arquivos inteiros, vídeos, PSDs, imagens, fontes, músicas, código ou registros de pessoas para um espaço público.

## Gates para qualquer publicação
1. **Escopo:** usuário autorizou publicar o quê, onde e em qual visibilidade? Projeto, pesquisa ou documentação?
2. **Titularidade:** material é original da equipe, licenciado, de cliente ou de terceiro? Há autorização documentada para republicação?
3. **Confidencialidade:** contém estratégia, tarefas, métricas, preços, contatos, conversas, orçamento, geolocalização privada, API keys, credenciais ou URLs restritas?
4. **Dependência de plataforma:** termos de uso, direitos de modelo/voz, canais de distribuição e exigências de atribuição precisam ser verificados na data do uso.
5. **Minimização:** substituir casos reais por exemplos fictícios; abstrair princípios; remover nomes, IDs de tarefa, screenshots, dados internos e assets não necessários.
6. **Checagem factual:** nenhuma aprovação, teste, performance, disponibilidade ou licença presumidos.
7. **Revisão final:** inspecionar texto, frontmatter, nomes de arquivos, referências, links e histórico de alterações. **Não escrever segredo em commit e apagar depois**: Git preserva histórico.
8. **Evidência:** registrar origem e autorização em ambiente privado apropriado, sem publicar documento comprobatório confidencial.

## Matriz de decisão
| Conteúdo candidato | Ação |
|---|---|
| Princípio geral formulado de maneira própria | Publicável após checagem factual |
| Checklist operacional original sem cliente | Publicável após revisão |
| Link para manual público de fornecedor | Referenciar com data, sem reproduzir integralmente |
| Print do ClickUp, diálogo ou briefing real | Manter restrito |
| Arte/vídeo/música/logo de terceiro | Não copiar sem direito verificado |
| Dados financeiros, estratégicos ou pessoais | Manter restrito; usar caso fictício |
| Código de repositório privado | Exige escopo, titularidade e auditoria separados |
| Texto que revela endpoint/chave/permissão | Bloquear, retirar e rever risco |

## Risco de reidentificação
Trocar nome próprio por Empresa X pode ser insuficiente se datas, valores, lugares e eventos permitirem reconhecer uma pessoa ou cliente. Generalizar também os detalhes singulares. Não usar prints de campanhas privadas como material de treinamento público.

**Exemplo:** uma revisão confidencial aponta problema de legibilidade em um banner. Publicar “teste a maior e a menor proporção” e um cenário fictício é aceitável como princípio; publicar captura, nome de cliente e link da tarefa não é.

**Nota:** este guia oferece controle editorial de publicação, não parecer jurídico nem licença de conteúdo. Regras de privacidade, autor e marca dependem da jurisdição e do caso.