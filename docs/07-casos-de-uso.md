# Especificação de Casos de Uso — ConectaGlobal

## 1. Convenções LAPIS

Os casos de uso seguem a estrutura do template LAPIS: nome iniciado por verbo no infinitivo, objetivo único, atores primários e secundários, precondições, fluxo principal, fluxos alternativos, exceções, pós-condições, RNFs específicos, frequência, interface, observações e referências.

Os fluxos abaixo são uma primeira especificação acadêmica [P]. Devem ser revisados com usuários e responsáveis pelo processo. Os estados e permissões ainda hipotéticos estão identificados.

## CDU-01 — Manter oportunidade

**Objetivo:** permitir que um operador autorizado cadastre e mantenha uma oportunidade internacional.

**Tipo:** Concreto.

**Atores primários:** AT-02 — Operador NEI/DRI.

**Atores secundários:** AT-07 — Serviço de mensagens (quando houver aviso).

**Precondições:**
- O operador está autenticado.
- O operador possui permissão de manutenção.

**Fluxo principal**
- **P1.** O operador seleciona a opção de cadastrar oportunidade.
- **P2.** O sistema apresenta o formulário de oportunidade.
- **P3.** O operador informa título, descrição, instituição, modalidade e período.
- **P4.** O operador informa critérios de elegibilidade e documentos requeridos.
- **P5.** O operador salva o cadastro.
- **P6.** O sistema valida os campos obrigatórios conforme RN-10.
- **P7.** O sistema registra a oportunidade como rascunho.
- **P8.** O sistema registra o autor e a data da operação conforme RN-07.
- **P9.** O sistema confirma o cadastro ao operador.

**Fluxos alternativos**
- **A1.** Salvar como rascunho com dados incompletos.
  - **A1.1.** No passo P4, o operador escolhe salvar sem publicar.
  - **A1.2.** O sistema armazena os dados disponíveis como rascunho.
  - **A1.3.** O sistema retorna ao passo P9.
- **A2.** Publicar oportunidade.
  - **A2.1.** No passo P7, o operador solicita a publicação.
  - **A2.2.** O sistema verifica os campos obrigatórios e critérios de publicação conforme RN-10.
  - **A2.3.** Se as condições forem atendidas, o sistema altera o estado para publicado e apresenta confirmação.
  - **A2.4.** O caso de uso é encerrado.

**Fluxos de exceção**
- **E1.** Dados obrigatórios ausentes.
  - **E1.1.** No passo P6, o sistema identifica campos obrigatórios não preenchidos.
  - **E1.2.** O sistema apresenta os campos que precisam de correção.
- **E2.** Usuário sem permissão.
  - **E2.1.** Nos passos P1 ou P5, o sistema identifica ausência de autorização.
  - **E2.2.** O sistema informa que a operação não está autorizada.

**Pós-condições:** oportunidade criada ou atualizada; estado e histórico registrados.

**RNFs específicos:** RNF06, RNF07, RNF08.

**Frequência:** média, estimativa inicial.

**Interface visual:** formulário de oportunidade e tela de detalhes; protótipo a elaborar.

**Regras relacionadas:** RN-07, RN-09, RN-10, RN-11.

**Referências:** RF01, RF01.1, RF02, RF04, RF05, RF06, RF07, RF26; F-01; NEC-05.

---

## CDU-02 — Consultar oportunidades

**Objetivo:** permitir que o estudante localize e consulte oportunidades internacionais disponíveis.

**Tipo:** Concreto.

**Atores primários:** AT-01 — Estudante de graduação.

**Atores secundários:** Não se aplica.

**Precondições:** Não se aplica para consulta pública; autenticação poderá ser exigida para funções personalizadas, a definir.

**Fluxo principal**
- **P1.** O estudante acessa o catálogo de oportunidades.
- **P2.** O sistema apresenta oportunidades visíveis conforme RN-01.
- **P3.** O estudante informa termo de busca ou seleciona filtros.
- **P4.** O sistema aplica os critérios de pesquisa.
- **P5.** O sistema apresenta os resultados encontrados.
- **P6.** O estudante seleciona uma oportunidade.
- **P7.** O sistema apresenta detalhes, instituição, período, critérios e documentos disponíveis.

**Fluxos alternativos**
- **A1.** Nenhum resultado encontrado.
  - **A1.1.** No passo P4, o sistema não encontra oportunidade correspondente.
  - **A1.2.** O sistema informa que não há resultados e permite alterar filtros.
  - **A1.3.** Retorna ao passo P3.
- **A2.** Consultar oportunidade encerrada.
  - **A2.1.** No passo P6, o estudante seleciona uma oportunidade encerrada disponível no histórico.
  - **A2.2.** O sistema apresenta os detalhes e informa que não aceita novas manifestações.

**Fluxos de exceção**
- **E1.** Falha ao carregar catálogo.
  - **E1.1.** No passo P2 ou P5, o sistema não consegue recuperar os dados.
  - **E1.2.** O sistema informa indisponibilidade temporária.

**Pós-condições:** nenhuma alteração de dados é realizada.

**RNFs específicos:** RNF01, RNF02, RNF03, RNF04.

**Frequência:** alta, estimativa inicial.

**Interface visual:** catálogo, filtros e página de detalhes; protótipo a elaborar.

**Regras relacionadas:** RN-01, RN-08, RN-17.

**Referências:** RF08, RF09, RF10; F-02, F-03; NEC-01, NEC-02.

---

## CDU-03 — Verificar pré-elegibilidade

**Objetivo:** apresentar ao estudante uma indicação preliminar de atendimento aos critérios configurados para uma oportunidade.

**Tipo:** Concreto.

**Atores primários:** AT-01 — Estudante de graduação.

**Atores secundários:** AT-05 — Sistema acadêmico, somente se integração autorizada.

**Precondições:** estudante consultou uma oportunidade com critérios cadastrados.

**Fluxo principal**
- **P1.** O estudante seleciona a opção de verificar pré-elegibilidade.
- **P2.** O sistema identifica os critérios configurados para a oportunidade.
- **P3.** O sistema obtém os dados necessários de fonte autorizada ou solicita informações ao estudante, conforme a integração disponível.
- **P4.** O sistema compara os dados com os critérios da oportunidade conforme RN-05 e RN-06.
- **P5.** O sistema apresenta o resultado preliminar e os critérios atendidos ou não atendidos.
- **P6.** O sistema informa que a pré-elegibilidade não representa aprovação, conforme RN-07.

**Fluxos alternativos**
- **A1.** Dados insuficientes.
  - **A1.1.** No passo P3, o sistema identifica dados ausentes.
  - **A1.2.** O sistema solicita as informações necessárias ou informa que não foi possível concluir a verificação.
  - **A1.3.** O estudante complementa os dados e o fluxo retorna ao passo P4.
- **A2.** O estudante não atende a um ou mais critérios.
  - **A2.1.** No passo P5, o sistema identifica critérios não atendidos.
  - **A2.2.** O sistema apresenta os critérios correspondentes e mantém a oportunidade consultável conforme RN-08.

**Fluxos de exceção**
- **E1.** Fonte acadêmica indisponível.
  - **E1.1.** No passo P3, a consulta externa falha.
  - **E1.2.** O sistema informa que a verificação não pôde ser concluída.

**Pós-condições:** resultado preliminar apresentado; nenhuma aprovação ou seleção é registrada.

**RNFs específicos:** RNF06, RNF07, RNF09.

**Frequência:** média, estimativa inicial.

**Interface visual:** resumo de critérios e resultado de pré-elegibilidade; protótipo a elaborar.

**Regras relacionadas:** RN-05, RN-06, RN-07, RN-08, RN-12.

**Referências:** RF04, RF11; F-05; NEC-03.

---

## CDU-04 — Registrar manifestação de interesse

**Objetivo:** permitir que o estudante registre interesse em uma oportunidade dentro do período permitido.

**Tipo:** Concreto.

**Atores primários:** AT-01 — Estudante de graduação.

**Atores secundários:** Não se aplica.

**Precondições:** estudante está autenticado; oportunidade está publicada e aceita manifestações.

**Fluxo principal**
- **P1.** O estudante acessa os detalhes da oportunidade.
- **P2.** O estudante seleciona a opção de manifestar interesse.
- **P3.** O sistema verifica o prazo e a situação da oportunidade conforme RN-02.
- **P4.** O sistema verifica se já existe manifestação ativa para o estudante e a oportunidade conforme RN-04.
- **P5.** O sistema apresenta os dados e condições da manifestação.
- **P6.** O estudante confirma o registro.
- **P7.** O sistema registra a manifestação com situação inicial.
- **P8.** O sistema confirma o registro ao estudante.

**Fluxos alternativos**
- **A1.** Manifestação já existente.
  - **A1.1.** No passo P4, o sistema identifica manifestação ativa.
  - **A1.2.** O sistema informa que já existe manifestação e apresenta acesso ao acompanhamento.
  - **A1.3.** O caso de uso é encerrado.
- **A2.** O estudante desiste antes da confirmação.
  - **A2.1.** No passo P5, o estudante cancela a operação.
  - **A2.2.** O sistema não registra a manifestação.
  - **A2.3.** O caso de uso é encerrado.

**Fluxos de exceção**
- **E1.** Prazo encerrado.
  - **E1.1.** No passo P3, o sistema identifica que a oportunidade não aceita novas manifestações.
  - **E1.2.** O sistema informa o encerramento do prazo.
- **E2.** Falha ao salvar.
  - **E2.1.** No passo P7, o sistema não consegue persistir a manifestação.
  - **E2.2.** O sistema informa que o registro não foi concluído.

**Pós-condições:** manifestação registrada ou operação encerrada sem registro.

**RNFs específicos:** RNF06, RNF07, RNF08.

**Frequência:** média, estimativa inicial; pode variar conforme abertura de editais.

**Interface visual:** resumo da oportunidade, confirmação e comprovante de manifestação; protótipo a elaborar.

**Regras relacionadas:** RN-02, RN-04, RN-07, RN-16.

**Referências:** RF12; F-06; NEC-04.

---

## CDU-05 — Acompanhar manifestação

**Objetivo:** permitir que o estudante consulte a situação de suas manifestações de interesse.

**Tipo:** Concreto.

**Atores primários:** AT-01 — Estudante de graduação.

**Atores secundários:** Não se aplica.

**Precondições:** estudante autenticado.

**Fluxo principal**
- **P1.** O estudante acessa a área de minhas manifestações.
- **P2.** O sistema recupera as manifestações vinculadas ao estudante conforme RN-13.
- **P3.** O sistema apresenta a lista de manifestações e suas situações.
- **P4.** O estudante seleciona uma manifestação.
- **P5.** O sistema apresenta os detalhes, a situação atual e as pendências registradas.

**Fluxos alternativos**
- **A1.** Nenhuma manifestação cadastrada.
  - **A1.1.** No passo P2, o sistema não encontra manifestações.
  - **A1.2.** O sistema informa que não há manifestações registradas.

**Fluxos de exceção**
- **E1.** Acesso não autorizado.
  - **E1.1.** Nos passos P2 ou P4, o sistema identifica tentativa de consultar manifestação de outro usuário.
  - **E1.2.** O sistema bloqueia a consulta e apresenta mensagem de acesso não autorizado.

**Pós-condições:** informações consultadas sem alteração de estado.

**RNFs específicos:** RNF01, RNF02, RNF06, RNF07.

**Frequência:** alta, estimativa inicial.

**Interface visual:** lista de manifestações e detalhe de situação; protótipo a elaborar.

**Regras relacionadas:** RN-13, RN-14, RN-16.

**Referências:** RF14, RF15; F-07, F-10; NEC-04.

---

## CDU-06 — Analisar manifestação

**Objetivo:** permitir que o operador autorizado analise uma manifestação e atualize sua situação.

**Tipo:** Concreto.

**Atores primários:** AT-02 — Operador NEI/DRI.

**Atores secundários:** AT-01 — Estudante de graduação; AT-07 — Serviço de mensagens.

**Precondições:** operador autenticado e autorizado; manifestação existente.

**Fluxo principal**
- **P1.** O operador acessa a lista de manifestações.
- **P2.** O sistema apresenta manifestações conforme as permissões do operador.
- **P3.** O operador seleciona uma manifestação.
- **P4.** O sistema apresenta os dados necessários à análise.
- **P5.** O operador seleciona uma nova situação permitida.
- **P6.** O operador registra justificativa ou orientação, quando exigida.
- **P7.** O sistema valida a transição conforme RN-14 e RN-19.
- **P8.** O sistema registra a alteração, o responsável e a data conforme RN-07.
- **P9.** O sistema disponibiliza a situação atualizada para consulta do estudante.
- **P10.** O sistema aciona notificação, se a regra e o canal estiverem configurados.

**Fluxos alternativos**
- **A1.** Solicitar complementação documental.
  - **A1.1.** No passo P5, o operador seleciona a situação de pendência.
  - **A1.2.** O operador descreve os documentos ou informações necessários.
  - **A1.3.** O sistema registra a pendência e disponibiliza a informação ao estudante.
  - **A1.4.** O caso de uso é encerrado.
- **A2.** Manter situação atual.
  - **A2.1.** No passo P5, o operador decide não alterar a situação.
  - **A2.2.** O sistema não modifica o registro e encerra o caso de uso.

**Fluxos de exceção**
- **E1.** Transição não permitida.
  - **E1.1.** No passo P7, o sistema identifica transição inválida.
  - **E1.2.** O sistema informa que a situação não pode ser alterada dessa forma.
- **E2.** Justificativa obrigatória ausente.
  - **E2.1.** No passo P7, o sistema identifica ausência de justificativa exigida.
  - **E2.2.** O sistema solicita o preenchimento.

**Pós-condições:** situação atualizada e histórico registrado, ou registro mantido sem alteração.

**RNFs específicos:** RNF06, RNF07, RNF08.

**Frequência:** média, estimativa inicial.

**Interface visual:** fila de análise e formulário de atualização; protótipo a elaborar.

**Regras relacionadas:** RN-07, RN-13, RN-14, RN-19.

**Referências:** RF17, RF18, RF19; F-08, F-09; NEC-06.

---

## CDU-07 — Consultar documentos requeridos

**Objetivo:** permitir que o estudante consulte os documentos exigidos para uma oportunidade e acompanhe sua situação quando o checklist estiver habilitado.

**Tipo:** Concreto.

**Atores primários:** AT-01 — Estudante de graduação.

**Atores secundários:** AT-02 — Operador NEI/DRI.

**Precondições:** oportunidade possui documentos cadastrados.

**Fluxo principal**
- **P1.** O estudante acessa os detalhes da oportunidade ou de sua manifestação.
- **P2.** O sistema apresenta a lista de documentos exigidos.
- **P3.** O estudante seleciona um documento para consultar instruções.
- **P4.** O sistema apresenta descrição, formato e instruções disponíveis.
- **P5.** Quando o checklist estiver habilitado, o sistema apresenta a situação de cada documento.

**Fluxos alternativos**
- **A1.** Documento não exigido para aquela oportunidade.
  - **A1.1.** No passo P2, o sistema identifica que não há documentos cadastrados.
  - **A1.2.** O sistema informa que não há documentos listados.

**Fluxos de exceção**
- **E1.** Documento indisponível.
  - **E1.1.** No passo P4, o sistema não consegue recuperar o arquivo ou instrução.
  - **E1.2.** O sistema informa indisponibilidade do conteúdo.

**Pós-condições:** documentos consultados; nenhuma alteração obrigatória realizada.

**RNFs específicos:** RNF02, RNF06, RNF07.

**Frequência:** média.

**Interface visual:** lista/checklist de documentos; protótipo a elaborar.

**Regras relacionadas:** RN-10, RN-16.

**Referências:** RF05, RF15; F-03, F-10; NEC-02, NEC-04.

---

## CDU-08 — Enviar notificação

**Objetivo:** encaminhar aviso a um usuário quando ocorrer evento configurado e autorizado.

**Tipo:** Abstrato (iniciado pelo sistema).

**Atores primários:** AT-07 — Serviço de mensagens, acionado pelo sistema.

**Atores secundários:** AT-01 — Estudante; AT-02 — Operador.

**Precondições:** evento notificável configurado; destinatário e canal válidos.

**Fluxo principal**
- **P1.** O sistema identifica um evento que exige notificação conforme configuração aprovada.
- **P2.** O sistema identifica os destinatários autorizados.
- **P3.** O sistema prepara a mensagem com informações necessárias.
- **P4.** O sistema encaminha a mensagem ao serviço de mensagens.
- **P5.** O serviço de mensagens informa o resultado do envio.
- **P6.** O sistema registra o resultado da tentativa.

**Fluxos alternativos**
- **A1.** Evento sem destinatário elegível.
  - **A1.1.** No passo P2, o sistema não identifica destinatários.
  - **A1.2.** O sistema registra que nenhuma notificação foi necessária e encerra o caso de uso.

**Fluxos de exceção**
- **E1.** Serviço indisponível.
  - **E1.1.** No passo P4, o serviço não recebe a mensagem.
  - **E1.2.** O sistema registra falha para tratamento conforme política de retentativa a definir.

**Pós-condições:** envio registrado como concluído ou falho.

**RNFs específicos:** RNF06, RNF07, RNF13.

**Frequência:** variável, conforme eventos e prazos.

**Interface visual:** não se aplica; processo executado em segundo plano.

**Regras relacionadas:** RN-11, RN-18.

**Referências:** RF21, RF22; F-11; NEC-07.

---

## CDU-09 — Consultar painel e relatórios

**Objetivo:** permitir que o operador autorizado consulte indicadores básicos de oportunidades e manifestações.

**Tipo:** Concreto.

**Atores primários:** AT-02 — Operador NEI/DRI.

**Atores secundários:** AT-03 — Coordenador de curso, se autorizado.

**Precondições:** usuário autenticado e autorizado.

**Fluxo principal**
- **P1.** O operador acessa o painel gerencial.
- **P2.** O sistema apresenta indicadores disponíveis conforme permissão.
- **P3.** O operador seleciona filtros de período, oportunidade ou situação.
- **P4.** O sistema aplica os filtros.
- **P5.** O sistema apresenta os resultados agregados.
- **P6.** O operador solicita exportação, se disponível.
- **P7.** O sistema gera arquivo no formato habilitado.

**Fluxos alternativos**
- **A1.** Sem dados para o filtro.
  - **A1.1.** No passo P4, o sistema não encontra registros.
  - **A1.2.** O sistema apresenta resultado vazio.

**Fluxos de exceção**
- **E1.** Exportação não autorizada.
  - **E1.1.** No passo P6, o sistema identifica ausência de permissão.
  - **E1.2.** O sistema informa que a operação não está autorizada.

**Pós-condições:** dados consultados ou relatório gerado sem alteração dos registros de origem.

**RNFs específicos:** RNF04, RNF06, RNF07.

**Frequência:** baixa, estimativa inicial.

**Interface visual:** painel, filtros e relatório; protótipo a elaborar.

**Regras relacionadas:** RN-13, RN-16.

**Referências:** RF20, RF25; F-12, F-14; NEC-08.

---

## CDU-10 — Autenticar e controlar acesso

**Objetivo:** permitir acesso de usuários identificados às funcionalidades autorizadas.

**Tipo:** Concreto.

**Atores primários:** AT-01, AT-02, AT-03 ou AT-04, conforme perfil.

**Atores secundários:** AT-06 — Provedor SSO institucional, se integração aprovada.

**Precondições:** usuário possui meio de autenticação válido.

**Fluxo principal**
- **P1.** O usuário solicita acesso a uma funcionalidade restrita.
- **P2.** O sistema verifica se existe sessão autenticada.
- **P3.** Se não houver sessão, o sistema solicita autenticação.
- **P4.** O usuário informa suas credenciais no mecanismo institucional disponível.
- **P5.** O provedor de autenticação valida a identidade, quando SSO estiver integrado.
- **P6.** O sistema recebe a identidade e identifica o perfil autorizado.
- **P7.** O sistema permite acesso às funcionalidades correspondentes ao perfil.

**Fluxos alternativos**
- **A1.** Sessão já autenticada.
  - **A1.1.** No passo P2, o sistema identifica sessão válida.
  - **A1.2.** O sistema segue para o passo P6.
- **A2.** Usuário autenticado sem permissão para a função solicitada.
  - **A2.1.** No passo P6, o sistema identifica perfil sem autorização.
  - **A2.2.** O sistema informa que a função não está disponível para aquele perfil.

**Fluxos de exceção**
- **E1.** Falha de autenticação.
  - **E1.1.** No passo P5, a autenticação não é validada.
  - **E1.2.** O sistema informa que não foi possível autenticar o usuário.
- **E2.** Provedor indisponível.
  - **E2.1.** No passo P5, o serviço externo não responde.
  - **E2.2.** O sistema informa indisponibilidade temporária.

**Pós-condições:** sessão autenticada com perfil aplicado ou acesso negado.

**RNFs específicos:** RNF06, RNF07.

**Frequência:** alta.

**Interface visual:** tela de acesso e mensagens de autorização; solução de autenticação a definir com TI.

**Regras relacionadas:** RN-09, RN-13, RN-16.

**Referências:** RF23, RF24; F-13.

---

## 2. Pendências de validação dos casos de uso

- Confirmar atores e permissões reais.
- Confirmar estados e transições das manifestações.
- Confirmar se a consulta de pré-elegibilidade utiliza integração ou autodeclaração.
- Confirmar exigências documentais e necessidade de upload.
- Confirmar se relatórios e consulta por curso fazem parte do processo.
- Elaborar diagramas de atividades UML por fluxo quando solicitados na etapa correspondente.
- Elaborar protótipos de interface para os casos de uso prioritários.

## 3. Histórico

| Versão | Data | Alteração |
|---|---|---|
| 1.0 | 26/11/2026 | Primeira especificação dos principais casos de uso com estrutura LAPIS; fluxos marcados como propostas a validar. |
