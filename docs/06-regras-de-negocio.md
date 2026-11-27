# Regras de Negócio — ConectaGlobal

## Histórico de versões

| Data | Versão | Descrição | Autor |
|---|---|---|---|
| 26/11/2026 | 1.1 | Padronização das regras conforme template LAPIS e inclusão de origem/rastreabilidade. | Equipe do projeto |
| 26/11/2026 | 1.2 | Inclusão de RN-18 a RN-20, atribuindo responsável pela moderação exigida por RN-12, condicionando operações à identificação do usuário e delimitando o registro de aproveitamento de créditos. | Equipe do projeto |

As regras são identificadas como RN-XX para manter compatibilidade com os requisitos existentes. O título segue o padrão sujeito + verbo + objeto. Regras que dependem de política institucional ainda não confirmada são decisões propostas para a modelagem acadêmica.

## 1. Regras de negócio

### RN-01 — Oportunidade possui dados essenciais
**Descrição:** Toda oportunidade cadastrada deve possuir identificação, descrição, modalidade, destino, prazo e responsável pela atualização antes de ser publicada.

**Origem:** decisão de modelagem derivada de EV-07.  
**Relacionados:** RF-09, CDU-05.

### RN-02 — Critérios pertencem à oportunidade
**Descrição:** Os critérios de elegibilidade devem estar associados à oportunidade correspondente, evitando aplicar automaticamente critérios de um edital a outro.

**Origem:** EV-03 e necessidade de parametrização; abrangência exata a confirmar.  
**Relacionados:** RF-04, CDU-02.

### RN-03 — Requisitos variam conforme edital
**Descrição:** Requisitos acadêmicos, linguísticos e documentais podem variar conforme edital ou instituição parceira; a configuração deve refletir as condições da oportunidade cadastrada.

**Origem:** documentação-base e ponto a confirmar por análise de editais reais.  
**Relacionados:** RF-03, RF-04, RF-09.

### RN-04 — Autoavaliação não substitui análise
**Descrição:** O resultado da autoavaliação deve ser apresentado como indicativo e não pode ser interpretado como aprovação, seleção ou concessão de bolsa.

**Origem:** decisão de modelagem para distinguir apoio automatizado de decisão responsável.  
**Relacionados:** RF-04, CDU-02.

### RN-05 — Candidatura referencia oportunidade publicada
**Descrição:** Toda manifestação de interesse/candidatura deve estar vinculada a uma oportunidade cadastrada e publicada.

**Origem:** decisão de modelagem.  
**Relacionados:** RF-06, CDU-03.

### RN-06 — Candidato recebe indicação de documentos
**Descrição:** Para cada candidatura, o sistema deve apresentar os documentos exigidos para a oportunidade correspondente.

**Origem:** EV-07.  
**Relacionados:** RF-03, RF-07, CDU-04.

### RN-07 — Candidatura mantém histórico
**Descrição:** A candidatura deve manter sua situação atual e o histórico de alterações realizadas.

**Origem:** decisão de modelagem para viabilizar acompanhamento.  
**Relacionados:** RF-08, RF-12, CDU-04, CDU-07.

### RN-08 — Gestão de oportunidade é restrita
**Descrição:** Somente a equipe do NEI ou perfil autorizado pode criar, editar, publicar, suspender ou encerrar oportunidades.

**Origem:** EV-04 e decisão de controle de acesso.  
**Relacionados:** RF-09, RNF-07, CDU-05.

### RN-09 — Candidatura respeita prazo
**Descrição:** O sistema deve impedir o envio de candidatura após o prazo cadastrado, exceto quando uma exceção estiver explicitamente configurada por usuário autorizado.

**Origem:** decisão de modelagem baseada na existência de prazos em EV-07; exceções precisam ser confirmadas.  
**Relacionados:** RF-06, CDU-03.

### RN-10 — Atualização de status identifica responsável
**Descrição:** Toda alteração de status deve registrar a data/hora, o responsável e a situação resultante.

**Origem:** decisão de modelagem.  
**Relacionados:** RF-12, RNF-09, CDU-07.

### RN-11 — Indicação não garante admissão externa
**Descrição:** A aprovação interna ou indicação do candidato não garante aceitação pela instituição de destino quando existir etapa externa de admissão.

**Origem:** decisão de modelagem para explicitar limite do sistema.  
**Relacionados:** RF-08, CDU-07.

### RN-12 — Conteúdo colaborativo respeita moderação
**Descrição:** Relatos e interações colaborativas devem seguir regras de privacidade e moderação antes de sua disponibilização, conforme política a detalhar.

**Origem:** decisão de modelagem.  
**Relacionados:** RF-14 a RF-17.

### RN-13 — Usuário acessa funções autorizadas
**Descrição:** Cada usuário pode acessar somente as funcionalidades permitidas ao seu perfil.

**Origem:** requisito de segurança.  
**Relacionados:** RF-19, RNF-07.

### RN-14 — Alteração administrativa exige autorização
**Descrição:** Apenas usuários autorizados podem criar ou alterar convênios, oportunidades, bolsas e parâmetros de elegibilidade.

**Origem:** EV-04 e decisão de controle de acesso.  
**Relacionados:** RF-09, RF-10, RF-19.

### RN-15 — Documentos têm acesso restrito
**Descrição:** Dados e documentos de candidatura devem ser acessíveis somente ao próprio candidato e a usuários autorizados, conforme permissões definidas.

**Origem:** requisito de privacidade e segurança.  
**Relacionados:** RF-07, RNF-07, RNF-11.

### RN-16 — Relatórios preservam privacidade
**Descrição:** Relatórios devem respeitar permissões e evitar exposição de dados pessoais que não sejam necessários à finalidade gerencial.

**Origem:** requisito de privacidade.  
**Relacionados:** RF-18, RNF-10, RNF-11.

### RN-17 — Notificação decorre de evento relevante
**Descrição:** Notificações devem ser geradas a partir de eventos relevantes configurados, como prazo próximo, pendência ou mudança de status.

**Origem:** EV-04 e decisão de modelagem.  
**Relacionados:** RF-13, CDU-08.

### RN-18 — Perfil autorizado responde pela moderação
**Descrição:** A análise do conteúdo colaborativo submetido por participantes — relatos, mensagens de fórum e demais publicações — é atribuída à equipe do NEI ou a perfil autorizado por ela, que pode aprovar, recusar ou remover a publicação. Enquanto não houver decisão registrada, o conteúdo permanece indisponível aos demais usuários.

**Origem:** decisão de modelagem necessária para dar execução a RN-12, que exige moderação sem indicar responsável.  
**Relacionados:** RN-12, RF-14, RF-24, CDU-11, CDU-18.

### RN-19 — Operação sobre dados pessoais exige identificação
**Descrição:** Operações que criem, consultem ou alterem dados pessoais, documentos ou candidaturas somente podem ser executadas por usuário identificado pelo sistema, com perfil associado. A consulta ao catálogo público de oportunidades pode ser disponibilizada sem identificação, conforme decisão a confirmar na P2.

**Origem:** decisão de modelagem derivada dos requisitos de confidencialidade e autenticidade.  
**Relacionados:** RF-21, RN-13, RN-15, RNF-07, RNF-08, RNF-27, CDU-15.

### RN-20 — Registro de créditos não substitui análise acadêmica
**Descrição:** As informações de aproveitamento de créditos registradas no sistema são informativas e de acompanhamento. A decisão sobre aproveitamento permanece com as instâncias acadêmicas responsáveis, e o sistema não a calcula nem a formaliza.

**Origem:** decisão de modelagem, na mesma lógica de RN-04 e RN-11, para explicitar o limite do sistema.  
**Relacionados:** RF-23, CDU-17.

## 2. Checklist de validação LAPIS

- [x] Identificadores únicos e padronizados.
- [x] Títulos no formato sujeito + verbo + objeto.
- [x] Cada regra descreve uma condição principal.
- [x] Origem e artefatos relacionados registrados.
- [x] Toda regra que exige uma ação tem requisito funcional e responsável correspondentes.
- [ ] Regras institucionais confirmadas com o setor responsável.
- [ ] Estados, exceções e prazos detalhados na SRS.
- [ ] Revisão por partes interessadas realizada.
