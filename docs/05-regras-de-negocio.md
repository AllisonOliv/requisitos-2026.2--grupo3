# Especificação de Regras de Negócio — ConectaGlobal

## 1. Objetivo

Registrar políticas e restrições que orientam o comportamento do ConectaGlobal. As regras são propostas de especificação derivadas do material didático e da modelagem inicial. A maioria depende de validação com o setor responsável.

## 2. Convenções

- **RN-xx:** identificador estável da regra.
- **[D]:** regra ou referência derivada de material documental.
- **[H]:** hipótese pendente de validação.
- **[P]:** proposta de regra para revisão.
- **Origem:** necessidade, requisito ou questão relacionada.

## 3. Regras de negócio

| ID | Nome da regra | Descrição | Origem | Situação |
|---|---|---|---|---|
| RN-01 | O sistema exibe oportunidades publicadas | O catálogo destinado aos estudantes deve apresentar apenas oportunidades com estado publicado e dentro das condições de visibilidade definidas. | RF02, RF08 | [P] |
| RN-02 | O estudante manifesta interesse dentro do período permitido | O estudante somente pode registrar manifestação enquanto a oportunidade aceitar manifestações. | RF12 | [P] |
| RN-03 | O sistema encerra oportunidades após o prazo | Ao atingir o prazo final configurado, a oportunidade deixa de aceitar novas manifestações. O encerramento automático depende de confirmação do processo. | RF02, RF12 | [H] |
| RN-04 | O estudante mantém uma manifestação ativa por oportunidade | Deve existir no máximo uma manifestação ativa do mesmo estudante para a mesma oportunidade. | RF12 | [P] |
| RN-05 | A oportunidade define seus próprios critérios | Os critérios de elegibilidade devem ser configurados para cada oportunidade, permitindo variações. | RF04, RF11 | [H] |
| RN-06 | A pré-elegibilidade considera os critérios configurados | A verificação preliminar deve comparar os dados disponíveis do estudante com os critérios cadastrados para a oportunidade. | RF04, RF11 | [P] |
| RN-07 | A pré-elegibilidade não representa aprovação | Resultado positivo na pré-elegibilidade não garante seleção, aprovação ou concessão de bolsa. | RF11, RF18 | [P] |
| RN-08 | O estudante consulta oportunidades mesmo sem ser elegível | A indicação de não elegibilidade não deve, por si só, ocultar a oportunidade; o estudante deve poder consultar os critérios e a justificativa, salvo restrição específica. | RF09, RF11 | [P] |
| RN-09 | Apenas perfis autorizados mantêm oportunidades | Cadastro, edição, publicação, encerramento e arquivamento devem ser restritos a perfis autorizados. | RF02, RF24 | [P] |
| RN-10 | A publicação exige informações mínimas | Antes de publicar, o sistema deve exigir os campos obrigatórios definidos pela área responsável, incluindo título, período, critérios e documentos quando aplicáveis. | RF01, RF04, RF05 | [H] |
| RN-11 | Alterações relevantes são registradas e comunicadas | Mudanças em prazo ou critérios de oportunidade publicada devem gerar histórico e, quando aplicável, aviso aos estudantes com manifestação ativa. | RF07, RF22 | [P] |
| RN-12 | Dados acadêmicos têm fonte oficial | Quando houver integração, dados acadêmicos utilizados na pré-elegibilidade devem vir de fonte institucional autorizada; a solução não deve tratá-los como fonte oficial se forem autodeclarados. | RF11, RNF09 | [H] |
| RN-13 | Cada perfil acessa apenas informações autorizadas | O estudante consulta suas próprias manifestações; a equipe responsável acessa as manifestações necessárias ao processo; acesso de coordenação depende de autorização e escopo definidos. | RF17, RF24, RF25 | [P] |
| RN-14 | A manifestação segue estados definidos | A manifestação deve possuir estados controlados. Proposta inicial: Registrada, Em análise, Pendência de documentos, Aprovada para próxima fase, Não elegível, Cancelada e Encerrada. Transições devem ser validadas com o setor. | RF14, RF18, RF19 | [H] |
| RN-15 | O estudante cancela manifestação conforme prazo permitido | O cancelamento pelo estudante deve ser permitido apenas nos estados e períodos definidos pela oportunidade e pelo processo institucional. | RF13 | [H] |
| RN-16 | O sistema trata dados pessoais para finalidade definida | Dados pessoais devem ser coletados e utilizados apenas para finalidades informadas e autorizadas, com acesso restrito e tratamento conforme LGPD e políticas institucionais. | RNF07 | [D]/[P] |
| RN-17 | O sistema arquiva oportunidades encerradas | Oportunidades encerradas devem permanecer consultáveis em histórico quando isso for permitido pela política de retenção. | RF02 | [P] |
| RN-18 | O sistema envia lembretes conforme configuração | Lembretes de prazo devem seguir antecedência, público e canal definidos pela área responsável. Os prazos de 7 e 1 dia são propostas a validar, não regras confirmadas. | RF21 | [H] |
| RN-19 | A equipe justifica decisões negativas | Alterações para estados de não elegibilidade ou rejeição devem registrar justificativa quando exigido pelo processo. | RF18 | [H] |
| RN-20 | A validade de acordo pode restringir oportunidade | Se a instituição determinar que a vigência do acordo é condição para disponibilizar uma oportunidade, o sistema deve impedir nova manifestação quando o acordo não estiver válido. Aplicabilidade ainda não confirmada. | RF26 | [H] |

## 4. Estados propostos para manifestação

O seguinte ciclo é uma proposta de modelagem, não um fluxo institucional confirmado:

`Registrada → Em análise → Pendência de documentos → Em análise → Aprovada para próxima fase / Não elegível / Cancelada / Encerrada`

Regras para validar:
- Quais estados existem realmente?
- Quem pode realizar cada transição?
- Uma manifestação pode retornar de “Pendência de documentos” para “Em análise”?
- “Aprovada para próxima fase” representa aprovação final ou apenas avanço?
- Em quais estados o estudante pode cancelar?
- Quais transições exigem justificativa e notificação?

## 5. Regras de acesso e auditoria

Como proposta de controle:
- Registrar inclusão, alteração, publicação, retirada de publicação, encerramento e mudança de situação.
- Para cada evento, registrar usuário responsável, ação, data/hora e objeto afetado.
- Não permitir que um estudante consulte manifestações de outro estudante.
- Restringir operações administrativas aos perfis autorizados.
- Definir retenção dos registros conforme política institucional.

A definição final de perfis, retenção e dados de auditoria depende da instituição.

## 6. Questões pendentes

1. Confirmar quais informações são obrigatórias para publicar um edital.
2. Confirmar os estados e transições reais de manifestação.
3. Confirmar os prazos de lembrete e os canais permitidos.
4. Confirmar se a pré-elegibilidade usa dados oficiais integrados ou dados informados pelo estudante.
5. Confirmar se a validade de convênio é condição de elegibilidade ou se fica fora do escopo.
6. Confirmar regras de retenção e exclusão de dados.

## 7. Histórico

| Versão | Data | Alteração |
|---|---|---|
| 1.0 | 26/11/2026 | Reorganização das 20 regras conforme orientação LAPIS; nomes em formato sujeito + verbo + objeto; hipóteses preservadas. |
