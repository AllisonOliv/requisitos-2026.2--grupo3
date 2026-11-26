# Especificação de Casos de Uso — ConectaGlobal (LAPIS)

## Histórico de versões

| Data | Versão | Descrição | Autor |
|---|---|---|---|
| 26/11/2026 | 1.1 | Casos de uso reorganizados conforme template LAPIS, com rastreabilidade e fluxos estruturados. | Equipe do projeto |

> Os casos abaixo representam especificação inicial. A SRS da P2 deverá completar mensagens, exceções, estados, regras específicas e critérios de aceitação. O fluxo é proposta de modelagem, não declaração de processo institucional validado.

## CDU-01 — Consultar Oportunidades Internacionais

### 1. Nome do Caso de Uso
Consultar Oportunidades Internacionais.

### 2. Objetivo
Permitir que o estudante localize oportunidades internacionais e consulte suas informações.

### 3. Tipo
Concreto.

### 4. Atores
- **Primário:** AT-01 — Estudante.
- **Secundário:** Não se aplica.

### 5. Precondições
Existem oportunidades publicadas no sistema.

### 6. Fluxo Principal
- **P1.** O estudante acessa a área de oportunidades.
- **P2.** O sistema apresenta as oportunidades publicadas.
- **P3.** O estudante informa filtros ou seleciona uma oportunidade.
- **P4.** O sistema aplica os filtros, quando informados.
- **P5.** O sistema apresenta os resultados correspondentes.
- **P6.** O estudante seleciona uma oportunidade.
- **P7.** O sistema apresenta destino, modalidade, descrição, requisitos, prazo, benefícios e documentos cadastrados.

### 7. Fluxos Alternativos
- **A1. Nenhum filtro informado**
  - A1.1. O sistema mantém a listagem geral de oportunidades publicadas.
- **A2. Nenhum resultado encontrado**
  - A2.1. O sistema informa que não há oportunidades correspondentes aos filtros.

### 8. Fluxos de Exceção
- **E1. Falha ao carregar oportunidades**
  - E1.1. O sistema informa que não foi possível carregar os dados.
  - E1.2. O sistema permite tentar novamente.

### 9. Pós-condições
As informações da oportunidade são apresentadas ao estudante.

### 10. Requisitos Não Funcionais
RNF-01, RNF-03, RNF-12, RNF-13, RNF-15.

### 11. Ponto de Extensão
Não se aplica.

### 12. Frequência de Utilização
Alta — consulta de oportunidades é atividade central do módulo do estudante.

### 13. Interface Visual
A definir na etapa de wireframes/protótipo.

### 14. Observações
Relaciona RF-01, RF-02 e RF-03; RN-01 a RN-03.

### 15. Referências
NEC-01; F-01; F-02; AD-01; AD-02.

### 16. Checklist de Validação
- [x] Nome iniciado por verbo no infinitivo.
- [x] Objetivo único e claro.
- [x] Ator primário identificado.
- [x] Fluxo principal e alternativas descritos.
- [ ] Mensagens e critérios de aceitação detalhados na SRS.
- [ ] Interface visual vinculada ao protótipo.

---

## CDU-02 — Verificar Elegibilidade Inicial

### 1. Nome do Caso de Uso
Verificar Elegibilidade Inicial.

### 2. Objetivo
Permitir que o estudante compare suas informações com os critérios cadastrados para uma oportunidade.

### 3. Tipo
Concreto.

### 4. Atores
- **Primário:** AT-01 — Estudante.
- **Secundário:** Não se aplica.

### 5. Precondições
A oportunidade possui critérios de elegibilidade cadastrados.

### 6. Fluxo Principal
- **P1.** O estudante seleciona a opção de autoavaliação da oportunidade.
- **P2.** O sistema apresenta os critérios cadastrados.
- **P3.** O estudante informa os dados solicitados.
- **P4.** O sistema verifica o preenchimento dos campos necessários.
- **P5.** O sistema compara as informações com os critérios da oportunidade.
- **P6.** O sistema apresenta resultado indicativo e informa que a análise oficial depende do processo responsável.

### 7. Fluxos Alternativos
- **A1. Dados incompletos**
  - A1.1. O sistema identifica os campos pendentes.
  - A1.2. O estudante complementa os dados e retorna ao P4.

### 8. Fluxos de Exceção
- **E1. Critérios indisponíveis**
  - E1.1. O sistema informa que não é possível realizar a autoavaliação para aquela oportunidade.
- **E2. Erro de processamento**
  - E2.1. O sistema informa que não foi possível concluir a verificação.

### 9. Pós-condições
O resultado indicativo é apresentado; nenhuma aprovação oficial é registrada por este caso de uso.

### 10. Requisitos Não Funcionais
RNF-06, RNF-07, RNF-10, RNF-12.

### 11. Ponto de Extensão
Não se aplica.

### 12. Frequência de Utilização
Média — depende do interesse do estudante em cada oportunidade.

### 13. Interface Visual
A definir na etapa de protótipo.

### 14. Observações
Relaciona RF-04 e RN-02, RN-03 e RN-04.

### 15. Referências
NEC-02; F-03; AD-01.

### 16. Checklist de Validação
- [x] Nome iniciado por verbo no infinitivo.
- [x] Objetivo único.
- [x] Ator primário identificado.
- [x] Fluxos principal, alternativo e de exceção descritos.
- [x] Resultado indicativo diferenciado de decisão oficial.
- [ ] Critérios reais de cada edital confirmados.

---

## CDU-03 — Registrar Candidatura

### 1. Nome do Caso de Uso
Registrar Candidatura.

### 2. Objetivo
Permitir que o estudante registre manifestação de interesse ou candidatura a uma oportunidade.

### 3. Tipo
Concreto.

### 4. Atores
- **Primário:** AT-01 — Estudante.
- **Secundário:** Não se aplica.

### 5. Precondições
O estudante está identificado no sistema e a oportunidade está publicada e dentro do prazo configurado.

### 6. Fluxo Principal
- **P1.** O estudante seleciona a oportunidade.
- **P2.** O sistema apresenta condições e documentos exigidos.
- **P3.** O estudante informa os dados solicitados e confirma a manifestação.
- **P4.** O sistema valida os campos obrigatórios.
- **P5.** O sistema verifica o prazo da oportunidade.
- **P6.** O sistema registra a candidatura vinculada ao estudante e à oportunidade.
- **P7.** O sistema apresenta confirmação e situação inicial do registro.

### 7. Fluxos Alternativos
- **A1. Dados obrigatórios ausentes**
  - A1.1. O sistema destaca os campos pendentes.
  - A1.2. O estudante complementa os dados e retorna ao P4.

### 8. Fluxos de Exceção
- **E1. Prazo encerrado**
  - E1.1. O sistema impede o envio e informa o encerramento do prazo.
- **E2. Oportunidade indisponível**
  - E2.1. O sistema informa que a oportunidade não aceita novas candidaturas.
- **E3. Falha no registro**
  - E3.1. O sistema informa que o registro não foi concluído e não apresenta confirmação de sucesso.

### 9. Pós-condições
A candidatura fica registrada e vinculada ao estudante e à oportunidade.

### 10. Requisitos Não Funcionais
RNF-05, RNF-07, RNF-09, RNF-10.

### 11. Ponto de Extensão
CDU-04 — Acompanhar Candidatura, após o registro.

### 12. Frequência de Utilização
Média — varia conforme a abertura de oportunidades.

### 13. Interface Visual
A definir na etapa de protótipo.

### 14. Observações
Relaciona RF-06 e RN-05, RN-06 e RN-09.

### 15. Referências
NEC-03; F-05; AD-02.

### 16. Checklist de Validação
- [x] Nome iniciado por verbo no infinitivo.
- [x] Objetivo único.
- [x] Ator primário identificado.
- [x] Fluxos principal, alternativo e de exceção descritos.
- [ ] Estados e dados obrigatórios detalhados na SRS.

---

## CDU-04 — Acompanhar Candidatura

### 1. Nome do Caso de Uso
Acompanhar Candidatura.

### 2. Objetivo
Permitir que o estudante consulte situação, histórico e pendências de suas candidaturas.

### 3. Tipo
Concreto.

### 4. Atores
- **Primário:** AT-01 — Estudante.
- **Secundário:** Não se aplica.

### 5. Precondições
O estudante possui candidatura registrada.

### 6. Fluxo Principal
- **P1.** O estudante acessa a área de suas candidaturas.
- **P2.** O sistema apresenta as candidaturas vinculadas ao estudante.
- **P3.** O estudante seleciona uma candidatura.
- **P4.** O sistema apresenta situação atual, histórico, prazos e pendências disponíveis.
- **P5.** O estudante consulta os documentos e orientações associados.

### 7. Fluxos Alternativos
- **A1. Não há candidaturas registradas**
  - A1.1. O sistema informa que não existem candidaturas vinculadas ao estudante.

### 8. Fluxos de Exceção
- **E1. Candidatura não localizada**
  - E1.1. O sistema informa que o registro não está disponível e permite retornar à listagem.

### 9. Pós-condições
As informações autorizadas da candidatura são exibidas.

### 10. Requisitos Não Funcionais
RNF-07, RNF-09, RNF-11, RNF-12.

### 11. Ponto de Extensão
Não se aplica.

### 12. Frequência de Utilização
Alta durante o período de seleção.

### 13. Interface Visual
A definir na etapa de protótipo.

### 14. Observações
Relaciona RF-07, RF-08, RN-06, RN-07 e RN-15.

### 15. Referências
NEC-03, NEC-04; F-06.

### 16. Checklist de Validação
- [x] Nome iniciado por verbo no infinitivo.
- [x] Objetivo único.
- [x] Ator primário identificado.
- [x] Fluxos principal e alternativo descritos.
- [ ] Estados oficiais da candidatura confirmados.

---

## CDU-05 — Gerenciar Oportunidades

### 1. Nome do Caso de Uso
Gerenciar Oportunidades.

### 2. Objetivo
Permitir que a equipe do NEI mantenha oportunidades e editais cadastrados e publicados.

### 3. Tipo
Concreto.

### 4. Atores
- **Primário:** AT-02 — Equipe do NEI.
- **Secundário:** Não se aplica.

### 5. Precondições
O usuário está identificado e possui permissão de gestão.

### 6. Fluxo Principal
- **P1.** A equipe do NEI acessa a gestão de oportunidades.
- **P2.** O sistema apresenta os registros existentes.
- **P3.** O usuário seleciona cadastrar ou editar uma oportunidade.
- **P4.** O usuário informa descrição, destino, modalidade, requisitos, documentos e prazo.
- **P5.** O sistema valida os campos obrigatórios.
- **P6.** O usuário solicita publicação ou salva a alteração.
- **P7.** O sistema registra a operação e apresenta o resultado.

### 7. Fluxos Alternativos
- **A1. Suspender oportunidade**
  - A1.1. O usuário seleciona uma oportunidade publicada e solicita suspensão.
  - A1.2. O sistema atualiza a situação.
- **A2. Encerrar oportunidade**
  - A2.1. O usuário solicita encerramento.
  - A2.2. O sistema registra a situação de encerrada.

### 8. Fluxos de Exceção
- **E1. Dados inválidos**
  - E1.1. O sistema indica os campos que precisam de correção.
- **E2. Usuário sem permissão**
  - E2.1. O sistema bloqueia a operação e informa a restrição.

### 9. Pós-condições
A oportunidade é criada ou atualizada conforme a operação autorizada.

### 10. Requisitos Não Funcionais
RNF-07, RNF-09, RNF-10.

### 11. Ponto de Extensão
Não se aplica.

### 12. Frequência de Utilização
Média — conforme abertura e atualização de oportunidades.

### 13. Interface Visual
A definir na etapa de protótipo.

### 14. Observações
Relaciona RF-09, RN-01, RN-08, RN-13 e RN-14.

### 15. Referências
NEC-05; F-07; EV-04 e EV-07.

### 16. Checklist de Validação
- [x] Nome iniciado por verbo no infinitivo.
- [x] Objetivo único.
- [x] Ator primário identificado.
- [x] Fluxos principal, alternativos e exceções descritos.
- [ ] Campos e estados detalhados na SRS.

---

## CDU-06 — Gerenciar Convênios e Bolsas

### 1. Nome do Caso de Uso
Gerenciar Convênios e Bolsas.

### 2. Objetivo
Permitir que a equipe do NEI mantenha informações de instituições parceiras, convênios e bolsas.

### 3. Tipo
Concreto.

### 4. Atores
- **Primário:** AT-02 — Equipe do NEI.
- **Secundário:** Não se aplica.

### 5. Precondições
Usuário identificado e autorizado.

### 6. Fluxo Principal
- **P1.** A equipe do NEI acessa a área de gestão.
- **P2.** O sistema apresenta instituições, convênios e bolsas cadastrados.
- **P3.** O usuário seleciona um registro ou solicita novo cadastro.
- **P4.** O usuário informa ou altera os dados.
- **P5.** O sistema valida os campos.
- **P6.** O sistema salva o registro e apresenta confirmação.

### 7. Fluxos Alternativos
- **A1. Consultar registro**
  - A1.1. O usuário seleciona um registro.
  - A1.2. O sistema apresenta os dados disponíveis.

### 8. Fluxos de Exceção
- **E1. Dados inválidos**
  - E1.1. O sistema informa os campos a corrigir.
- **E2. Usuário sem permissão**
  - E2.1. O sistema bloqueia a alteração.

### 9. Pós-condições
O registro é consultado ou atualizado.

### 10. Requisitos Não Funcionais
RNF-07, RNF-09.

### 11. Ponto de Extensão
Não se aplica.

### 12. Frequência de Utilização
Média.

### 13. Interface Visual
A definir na etapa de protótipo.

### 14. Observações
Relaciona RF-10, RN-08 e RN-14.

### 15. Referências
NEC-05; F-08; EV-04.

### 16. Checklist de Validação
- [x] Nome iniciado por verbo no infinitivo.
- [x] Objetivo único.
- [x] Ator primário identificado.
- [x] Fluxos principal, alternativo e exceções descritos.
- [ ] Campos específicos confirmados.

---

## CDU-07 — Analisar Candidaturas

### 1. Nome do Caso de Uso
Analisar Candidaturas.

### 2. Objetivo
Permitir que a equipe do NEI consulte candidaturas e registre o andamento da análise.

### 3. Tipo
Concreto.

### 4. Atores
- **Primário:** AT-02 — Equipe do NEI.
- **Secundário:** AT-03 — Coordenador de curso, quando sua participação for aplicável e autorizada.

### 5. Precondições
Existem candidaturas registradas e o usuário possui permissão de consulta.

### 6. Fluxo Principal
- **P1.** A equipe do NEI acessa o painel de candidaturas.
- **P2.** O sistema apresenta candidaturas conforme as permissões do usuário.
- **P3.** O usuário seleciona uma candidatura.
- **P4.** O sistema apresenta dados e documentos autorizados.
- **P5.** O usuário registra observação ou atualiza a situação conforme as opções disponíveis.
- **P6.** O sistema registra responsável, data/hora e situação resultante.
- **P7.** O sistema confirma a atualização.

### 7. Fluxos Alternativos
- **A1. Documentação pendente**
  - A1.1. O usuário registra a pendência.
  - A1.2. O sistema associa a pendência à candidatura para consulta pelo estudante.

### 8. Fluxos de Exceção
- **E1. Acesso não autorizado**
  - E1.1. O sistema bloqueia a consulta ou alteração.
- **E2. Transição de situação inválida**
  - E2.1. O sistema não realiza a alteração e informa a inconsistência.

### 9. Pós-condições
A candidatura permanece consultável com o histórico atualizado, quando houver alteração.

### 10. Requisitos Não Funcionais
RNF-07, RNF-09, RNF-11.

### 11. Ponto de Extensão
Não se aplica.

### 12. Frequência de Utilização
Alta durante períodos de seleção.

### 13. Interface Visual
A definir na etapa de protótipo.

### 14. Observações
As situações e transições oficiais permanecem pendentes de confirmação. Relaciona RF-11, RF-12, RN-07, RN-10 e RN-15.

### 15. Referências
NEC-04, NEC-05; F-09; EV-04.

### 16. Checklist de Validação
- [x] Nome iniciado por verbo no infinitivo.
- [x] Objetivo único.
- [x] Atores identificados.
- [x] Fluxos principal, alternativo e exceções descritos.
- [ ] Estados/transições confirmados com o processo responsável.

---

## CDU-08 — Gerenciar Notificações

### 1. Nome do Caso de Uso
Gerenciar Notificações.

### 2. Objetivo
Permitir que o sistema disponibilize avisos relacionados a prazos, pendências e mudanças de situação.

### 3. Tipo
Concreto.

### 4. Atores
- **Primário:** AT-02 — Equipe do NEI, para configuração/gestão de eventos quando autorizada.
- **Secundário:** AT-01 — Estudante, como destinatário das notificações.

### 5. Precondições
Existem eventos relevantes configurados para gerar notificação.

### 6. Fluxo Principal
- **P1.** Ocorre um evento configurado, como prazo próximo, pendência ou mudança de situação.
- **P2.** O sistema identifica os usuários relacionados ao evento.
- **P3.** O sistema prepara a notificação com as informações permitidas.
- **P4.** O sistema disponibiliza a notificação ao destinatário.
- **P5.** O destinatário consulta o aviso.

### 7. Fluxos Alternativos
- **A1. Destinatário sem notificação pendente**
  - A1.1. O sistema apresenta a área de notificações sem novos avisos.

### 8. Fluxos de Exceção
- **E1. Falha na geração**
  - E1.1. O sistema registra a falha para tratamento, sem indicar envio concluído.

### 9. Pós-condições
A notificação fica disponível quando gerada com sucesso.

### 10. Requisitos Não Funcionais
RNF-07, RNF-09, RNF-11.

### 11. Ponto de Extensão
Não se aplica.

### 12. Frequência de Utilização
Média; depende dos eventos cadastrados.

### 13. Interface Visual
A definir na etapa de protótipo.

### 14. Observações
Canais e prazos de envio precisam ser definidos na P2. Relaciona RF-13 e RN-17.

### 15. Referências
NEC-04; F-10.

### 16. Checklist de Validação
- [x] Objetivo e atores identificados.
- [x] Fluxo principal e exceção descritos.
- [ ] Canais e tempos definidos.

---

## CDU-09 — Consultar Relatórios Gerenciais

### 1. Nome do Caso de Uso
Consultar Relatórios Gerenciais.

### 2. Objetivo
Permitir que a equipe do NEI consulte informações consolidadas sobre candidaturas, perfis e destinos procurados.

### 3. Tipo
Concreto.

### 4. Atores
- **Primário:** AT-02 — Equipe do NEI.
- **Secundário:** Não se aplica.

### 5. Precondições
Existem dados registrados e o usuário possui permissão para consultar relatórios.

### 6. Fluxo Principal
- **P1.** O usuário acessa a área de relatórios.
- **P2.** O sistema apresenta filtros disponíveis.
- **P3.** O usuário seleciona período, destino ou oportunidade, conforme filtros existentes.
- **P4.** O sistema consolida os dados autorizados.
- **P5.** O sistema apresenta o relatório.

### 7. Fluxos Alternativos
- **A1. Sem filtros**
  - A1.1. O sistema apresenta o conjunto padrão de informações permitido.

### 8. Fluxos de Exceção
- **E1. Sem dados para os filtros**
  - E1.1. O sistema informa que não foram encontrados dados.
- **E2. Acesso não autorizado**
  - E2.1. O sistema bloqueia a consulta.

### 9. Pós-condições
Relatório consultado sem alteração dos dados de origem.

### 10. Requisitos Não Funcionais
RNF-01, RNF-07, RNF-11.

### 11. Ponto de Extensão
Não se aplica.

### 12. Frequência de Utilização
Média.

### 13. Interface Visual
A definir na etapa de protótipo.

### 14. Observações
Indicadores e filtros precisam de confirmação com responsáveis. Relaciona RF-18 e RN-16.

### 15. Referências
NEC-08; F-11; EV-04.

### 16. Checklist de Validação
- [x] Objetivo, ator e fluxos identificados.
- [ ] Indicadores gerenciais definidos.

---

## CDU-10 — Consultar Recursos de Preparação

### 1. Nome do Caso de Uso
Consultar Recursos de Preparação.

### 2. Objetivo
Permitir que o estudante consulte conteúdos de preparação linguística, cultural e financeira.

### 3. Tipo
Concreto.

### 4. Atores
- **Primário:** AT-01 — Estudante.
- **Secundário:** Não se aplica.

### 5. Precondições
Existem conteúdos disponíveis.

### 6. Fluxo Principal
- **P1.** O estudante acessa a central de preparação.
- **P2.** O sistema apresenta as categorias de conteúdo.
- **P3.** O estudante seleciona uma categoria.
- **P4.** O sistema apresenta os materiais disponíveis.
- **P5.** O estudante seleciona um material.
- **P6.** O sistema apresenta o conteúdo.

### 7. Fluxos Alternativos
- **A1. Categoria sem conteúdo**
  - A1.1. O sistema informa que não há materiais disponíveis na categoria.

### 8. Fluxos de Exceção
- **E1. Conteúdo indisponível**
  - E1.1. O sistema informa que não foi possível carregar o material.

### 9. Pós-condições
Conteúdo consultado.

### 10. Requisitos Não Funcionais
RNF-03, RNF-12, RNF-13, RNF-15.

### 11. Ponto de Extensão
Não se aplica.

### 12. Frequência de Utilização
Média.

### 13. Interface Visual
A definir na etapa de protótipo.

### 14. Observações
Relaciona RF-05.

### 15. Referências
NEC-06; F-04; EV-03.

### 16. Checklist de Validação
- [x] Objetivo, ator e fluxo identificados.
- [ ] Conteúdos e responsáveis editoriais definidos.

---

## CDU-11 — Compartilhar Relatos e Participar de Mentoria

### 1. Nome do Caso de Uso
Compartilhar Relatos e Participar de Mentoria.

### 2. Objetivo
Permitir que ex-intercambistas compartilhem experiências e apoiem estudantes interessados em mobilidade.

### 3. Tipo
Concreto.

### 4. Atores
- **Primário:** AT-06 — Ex-intercambista.
- **Secundário:** AT-01 — Estudante.

### 5. Precondições
Usuário identificado e recurso disponível.

### 6. Fluxo Principal
- **P1.** O ex-intercambista acessa a área de experiências.
- **P2.** O sistema apresenta opções de relato e mentoria.
- **P3.** O ex-intercambista seleciona compartilhar relato.
- **P4.** O sistema apresenta o formulário.
- **P5.** O ex-intercambista preenche e envia o relato.
- **P6.** O sistema encaminha o conteúdo para moderação.
- **P7.** Após aprovação, o sistema disponibiliza o relato conforme permissões.

### 7. Fluxos Alternativos
- **A1. Consultar mentores**
  - A1.1. O estudante consulta perfis disponíveis.
  - A1.2. O sistema apresenta informações permitidas para contato/solicitação.

### 8. Fluxos de Exceção
- **E1. Conteúdo não aprovado**
  - E1.1. O sistema mantém o conteúdo indisponível ao público e registra a situação.

### 9. Pós-condições
Relato encaminhado à moderação ou disponibilizado após aprovação; solicitação de mentoria registrada conforme fluxo definido.

### 10. Requisitos Não Funcionais
RNF-07, RNF-11, RNF-12, RNF-13.

### 11. Ponto de Extensão
Não se aplica.

### 12. Frequência de Utilização
Baixa a média.

### 13. Interface Visual
A definir na etapa de protótipo.

### 14. Observações
Regras de moderação e privacidade precisam ser detalhadas. Relaciona RF-14 e RF-15, RN-12.

### 15. Referências
NEC-07; F-12; EV-05.

### 16. Checklist de Validação
- [x] Objetivo, atores e fluxo identificados.
- [ ] Regras de moderação e mentoria definidas.

---

## CDU-12 — Participar de Atividades Colaborativas

### 1. Nome do Caso de Uso
Participar de Atividades Colaborativas.

### 2. Objetivo
Permitir que participantes consultem e participem de atividades Tandem, eventos e fórum.

### 3. Tipo
Concreto.

### 4. Atores
- **Primário:** AT-01 — Estudante.
- **Secundários:** AT-04 — Professor; AT-05 — Estudante estrangeiro recebido; AT-06 — Ex-intercambista, conforme atividade.

### 5. Precondições
A atividade ou espaço colaborativo está disponível.

### 6. Fluxo Principal
- **P1.** O participante acessa a área colaborativa.
- **P2.** O sistema apresenta as opções de Tandem, eventos e fórum.
- **P3.** O participante seleciona uma opção.
- **P4.** O sistema apresenta os conteúdos ou atividades disponíveis.
- **P5.** O participante seleciona a atividade ou tópico.
- **P6.** O sistema apresenta detalhes e permite participação conforme regras aplicáveis.

### 7. Fluxos Alternativos
- **A1. Consultar evento**
  - A1.1. O participante seleciona evento.
  - A1.2. O sistema apresenta data, descrição e informações disponíveis.
- **A2. Consultar tópico do fórum**
  - A2.1. O participante seleciona tópico.
  - A2.2. O sistema apresenta conteúdo e interações permitidas.

### 8. Fluxos de Exceção
- **E1. Conteúdo indisponível**
  - E1.1. O sistema informa que o conteúdo não está disponível.
- **E2. Interação não autorizada**
  - E2.1. O sistema bloqueia a ação e informa a restrição.

### 9. Pós-condições
Atividade ou conteúdo consultado; participação registrada quando aplicável.

### 10. Requisitos Não Funcionais
RNF-07, RNF-11, RNF-12, RNF-13.

### 11. Ponto de Extensão
Não se aplica.

### 12. Frequência de Utilização
Média, conforme calendário e participação.

### 13. Interface Visual
A definir na etapa de protótipo.

### 14. Observações
Relaciona RF-16 e RF-17; regras de moderação e convivência a detalhar.

### 15. Referências
NEC-07; F-13; EV-06.

### 16. Checklist de Validação
- [x] Objetivo, atores e fluxos identificados.
- [ ] Regras de participação e moderação definidas.

---

## CDU-13 — Consultar Recursos de Integração

### 1. Nome do Caso de Uso
Consultar Recursos de Integração.

### 2. Objetivo
Permitir que o estudante estrangeiro recebido consulte orientações e atividades de integração.

### 3. Tipo
Concreto.

### 4. Atores
- **Primário:** AT-05 — Estudante estrangeiro recebido.
- **Secundário:** Não se aplica.

### 5. Precondições
Existem informações de integração disponíveis.

### 6. Fluxo Principal
- **P1.** O estudante estrangeiro acessa a área de integração.
- **P2.** O sistema apresenta orientações e atividades disponíveis.
- **P3.** O estudante seleciona um conteúdo.
- **P4.** O sistema apresenta as informações correspondentes.

### 7. Fluxos Alternativos
- **A1. Sem conteúdo disponível**
  - A1.1. O sistema informa que não há conteúdo publicado no momento.

### 8. Fluxos de Exceção
- **E1. Falha ao carregar conteúdo**
  - E1.1. O sistema informa a indisponibilidade temporária.

### 9. Pós-condições
Informações de integração consultadas.

### 10. Requisitos Não Funcionais
RNF-03, RNF-12, RNF-13, RNF-15.

### 11. Ponto de Extensão
Não se aplica.

### 12. Frequência de Utilização
Média, especialmente no período de chegada.

### 13. Interface Visual
A definir na etapa de protótipo.

### 14. Observações
Relaciona RF-20.

### 15. Referências
NEC-07; F-14; EV-06.

### 16. Checklist de Validação
- [x] Objetivo, ator e fluxo identificados.
- [ ] Conteúdos e responsáveis definidos.

---

## CDU-14 — Gerenciar Usuários e Permissões

### 1. Nome do Caso de Uso
Gerenciar Usuários e Permissões.

### 2. Objetivo
Permitir que o administrador mantenha usuários, perfis e permissões do sistema.

### 3. Tipo
Concreto.

### 4. Atores
- **Primário:** AT-07 — Administrador do sistema.
- **Secundário:** Não se aplica.

### 5. Precondições
Administrador identificado e autorizado.

### 6. Fluxo Principal
- **P1.** O administrador acessa a área de usuários.
- **P2.** O sistema apresenta os registros disponíveis.
- **P3.** O administrador seleciona um usuário ou solicita novo cadastro.
- **P4.** O administrador define ou atualiza o perfil e as permissões.
- **P5.** O sistema valida a operação.
- **P6.** O sistema registra a alteração e apresenta confirmação.

### 7. Fluxos Alternativos
- **A1. Consultar usuário**
  - A1.1. O administrador seleciona um usuário.
  - A1.2. O sistema apresenta dados permitidos.

### 8. Fluxos de Exceção
- **E1. Permissão insuficiente**
  - E1.1. O sistema bloqueia a operação.
- **E2. Dados inválidos**
  - E2.1. O sistema informa os campos a corrigir.

### 9. Pós-condições
Usuário ou permissões atualizados conforme autorização.

### 10. Requisitos Não Funcionais
RNF-07, RNF-08, RNF-09, RNF-11.

### 11. Ponto de Extensão
Não se aplica.

### 12. Frequência de Utilização
Baixa.

### 13. Interface Visual
A definir na etapa de protótipo.

### 14. Observações
Relaciona RF-19 e RN-13, RN-14.

### 15. Referências
F-15; RNF-07.

### 16. Checklist de Validação
- [x] Objetivo, ator e fluxo identificados.
- [ ] Matriz definitiva de perfis e permissões definida.
