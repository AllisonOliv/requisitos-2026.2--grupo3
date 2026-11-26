# Regras de Negócio — ConectaGlobal

As regras abaixo são decisões de projeto para o funcionamento proposto do ConectaGlobal. Não devem ser interpretadas como normas oficiais de uma instituição.

## 1. Regras gerais
| ID | Regra | Origem |
|---|---|---|
| RN-01 | Toda oportunidade deve possuir título, descrição, modalidade, destino ou abrangência, prazo e situação antes de ser publicada. | Decisão de projeto |
| RN-02 | Uma oportunidade em rascunho não aparece na consulta pública dos estudantes. | Decisão de projeto |
| RN-03 | Somente usuários com perfil de gestor podem cadastrar, editar, publicar, suspender ou encerrar oportunidades. | Decisão de projeto |
| RN-04 | Cada oportunidade pode possuir critérios de elegibilidade e documentos específicos. | Decisão de projeto |
| RN-05 | O sistema não deve aplicar um único conjunto de critérios a todas as oportunidades. | Decisão de projeto |
| RN-06 | O estudante só pode registrar candidatura para oportunidade publicada e dentro do prazo de inscrição. | Decisão de projeto |
| RN-07 | O estudante pode consultar e alterar apenas suas próprias candidaturas, respeitadas as permissões e o estado do processo. | Decisão de projeto |
| RN-08 | Uma candidatura deve estar vinculada a exatamente um estudante e a uma oportunidade. | Decisão de projeto |
| RN-09 | O sistema deve impedir o envio de uma segunda candidatura ativa do mesmo estudante para a mesma oportunidade, salvo se a candidatura anterior tiver sido cancelada conforme regra definida. | Decisão de projeto |
| RN-10 | A indicação de compatibilidade com critérios é informativa e não representa aprovação, classificação ou garantia de seleção. | Decisão de projeto |
| RN-11 | Somente avaliadores ou gestores autorizados podem atualizar o status de uma candidatura após o envio. | Decisão de projeto |
| RN-12 | Toda mudança de status deve registrar o novo estado, a data e o usuário responsável. | Decisão de projeto |
| RN-13 | Documentos de candidatura devem ser acessíveis somente ao estudante titular e aos perfis autorizados para análise/gestão. | Decisão de projeto |
| RN-14 | O encerramento de uma oportunidade impede novas candidaturas, mas preserva o histórico das candidaturas já registradas. | Decisão de projeto |
| RN-15 | Notificações devem ser geradas para eventos relevantes, como confirmação de candidatura e alteração de status. | Decisão de projeto |
| RN-16 | Relatórios devem apresentar dados agregados e respeitar as permissões do usuário solicitante. | Decisão de projeto |

## 2. Fluxo de status proposto
Estados iniciais sugeridos:
1. **Rascunho:** oportunidade ainda não publicada.
2. **Publicada:** disponível para consulta e candidatura dentro do prazo.
3. **Suspensa:** temporariamente indisponível para novas candidaturas.
4. **Encerrada:** prazo/processo encerrado.

Status de candidatura propostos:
1. **Enviada**
2. **Em análise**
3. **Pendente de documentação**
4. **Aprovada**
5. **Não aprovada**
6. **Cancelada**

A transição entre estados deve ser controlada por permissões e registrada no histórico. Na P2, a equipe deverá especificar quais transições são permitidas.

## 3. Regras contextuais
Materiais de referência sobre internacionalização apresentam critérios que podem variar conforme modalidade, oportunidade e instituição de destino. Por esse motivo, tais critérios não são fixados como regra global do ConectaGlobal: devem ser cadastrados no contexto da oportunidade correspondente.
