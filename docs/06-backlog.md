# 6. Backlog Priorizado

Prioridade MoSCoW. Estimativa em pontos de história (escala relativa: 1, 2, 3, 5, 8).

| # | Épico | História de usuário | Prio. | Pts | Critérios de aceite (resumo) | Reqs |
|---|---|---|---|---|---|---|
| 1 | Autenticação | Como usuário, quero entrar com minha conta institucional para acessar o sistema conforme meu perfil | M | 5 | Login via SSO; perfil identificado; acesso negado a áreas não permitidas | RF23, RF24 |
| 2 | Gestão de editais | Como NEI/DRI, quero cadastrar um edital com datas, requisitos e documentos para divulgá-lo aos alunos | M | 8 | Campos obrigatórios validados; edital salvo como rascunho; não publica se incompleto | RF01, RF05, RN10 |
| 3 | Gestão de editais | Como NEI/DRI, quero definir critérios de elegibilidade por edital para que a verificação seja automática | M | 8 | Critérios configuráveis (percentual, média, reprovações, curso); salvos no edital | RF04 |
| 4 | Gestão de editais | Como NEI/DRI, quero publicar, editar e encerrar editais para manter a informação atual | M | 5 | Status muda corretamente; edital encerrado não aceita manifestação | RF02, RN01, RN03 |
| 5 | Busca | Como estudante, quero buscar e filtrar oportunidades para achar as que me interessam | M | 5 | Filtros por país, área, tipo, prazo; resultado em até 2 s | RF08 |
| 6 | Busca | Como estudante, quero ver o detalhe da oportunidade para entender requisitos, prazos e documentos | M | 3 | Tela exibe todas as informações do edital | RF09 |
| 7 | Elegibilidade | Como estudante, quero verificar se sou elegível para saber se vale a pena me inscrever | M | 8 | Mostra resultado e motivo; deixa claro que não garante aprovação | RF11, RN05, RN07 |
| 8 | Manifestação | Como estudante, quero manifestar interesse em um edital aberto | M | 5 | Uma manifestação ativa por edital; só com inscrição aberta | RF12, RN02, RN04 |
| 9 | Manifestação | Como estudante, quero acompanhar o status das minhas manifestações | M | 5 | Lista com status atual e histórico | RF14, RN14 |
| 10 | Análise | Como NEI/DRI, quero listar e filtrar manifestações por edital para analisá-las | M | 5 | Filtros por status, curso, elegibilidade | RF17 |
| 11 | Análise | Como NEI/DRI, quero alterar o status de uma manifestação e registrar observações | M | 3 | Mudança registrada com autor e data; aluno é notificado | RF18, RF21 |
| 12 | Notificações | Como estudante, quero receber alertas de prazo e de mudança de status para não perder oportunidades | M | 5 | Notificação por e-mail nos prazos configurados | RF21, RN18 |
| 13 | Bolsas | Como NEI/DRI, quero cadastrar bolsas e vinculá-las a editais | S | 5 | Bolsa com fonte, benefício, vigência; vínculo opcional | RF03 |
| 14 | Documentos | Como estudante, quero um checklist de documentos para me organizar | S | 3 | Itens do edital; marcar/desmarcar | RF15 |
| 15 | Prazos | Como estudante, quero um calendário de prazos | S | 3 | Visão mensal/lista com prazos | RF10 |
| 16 | Análise | Como NEI/DRI, quero pedir complementação de documentos ao aluno | S | 3 | Status de pendência; aluno notificado | RF19 |
| 17 | Relatórios | Como NEI/DRI, quero relatórios e exportação CSV para prestar contas | S | 5 | Manifestações por edital, curso e destino | RF20 |
| 18 | Governança | Como NEI/DRI, quero designar um responsável por edital e ver o histórico de alterações | S | 5 | Responsável registrado; log de edições | RF06, RF07, RNF08 |
| 19 | Manifestação | Como estudante, quero cancelar uma manifestação | S | 2 | Só com edital aberto | RF13, RN15 |
| 20 | Notificações | Como interessado, quero ser avisado de alterações de prazo/requisito | S | 3 | Notifica quem manifestou interesse | RF22, RN11 |
| 21 | Favoritos | Como estudante, quero favoritar oportunidades | C | 2 | Lista de favoritos | RF16 |
| 22 | Coordenação | Como coordenador, quero ver as manifestações dos alunos do meu curso | C | 3 | Filtra por curso do coordenador | RF25, RN13 |
| 23 | i18n | Como estudante estrangeiro, quero usar o sistema em inglês/espanhol | C | 5 | Troca de idioma na interface | RNF10 |
| 24 | Seleção | Ranqueamento e resultado final da seleção | W | — | Fora do escopo desta fase | — |
| 25 | Convênios / pós-intercâmbio | Gestão de convênios, aproveitamento de créditos, rede de ex-alunos | W | — | Pertencem a outros temas | — |

## Sugestão de sprints
- **Sprint 2:** itens 1–6 (base e catálogo)
- **Sprint 3:** itens 7–12 (elegibilidade, manifestação, notificações)
- **Sprint 4:** itens 13–20 (Should)
