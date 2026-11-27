# Especificação de Requisitos Funcionais — ConectaGlobal

## Histórico de versões

| Data | Versão | Descrição | Autor |
|---|---|---|---|
| 26/11/2026 | 1.1 | Padronização dos requisitos e rastreabilidade com necessidades, casos de uso e regras. | Equipe do projeto |
| 26/11/2026 | 1.2 | Inclusão de RF-21 a RF-24, cobrindo acesso identificado, portfólio digital, aproveitamento de créditos e moderação de conteúdo — capacidades previstas no escopo da Visão da Demanda ou exigidas por regras de negócio, mas sem requisito correspondente. | Equipe do projeto |

## 1. Requisitos funcionais

| ID | Requisito | Prioridade | Necessidade | Caso de uso |
|---|---|---|---|---|
| RF-01 | O sistema deve permitir ao estudante consultar oportunidades internacionais publicadas. | Essencial | NEC-01 | CDU-01 |
| RF-02 | O sistema deve permitir filtrar oportunidades por país, área, duração, modalidade e prazo. | Essencial | NEC-01 | CDU-01 |
| RF-03 | O sistema deve apresentar detalhes da oportunidade, incluindo requisitos, prazos, benefícios e documentos. | Essencial | NEC-01 | CDU-01 |
| RF-04 | O sistema deve permitir ao estudante realizar autoavaliação inicial de elegibilidade conforme critérios cadastrados para a oportunidade. | Importante | NEC-02 | CDU-02 |
| RF-05 | O sistema deve disponibilizar recursos de preparação sobre idiomas, cultura e planejamento financeiro. | Importante | NEC-06 | CDU-10 |
| RF-06 | O sistema deve permitir ao estudante registrar manifestação de interesse ou candidatura a uma oportunidade. | Essencial | NEC-03 | CDU-03 |
| RF-07 | O sistema deve permitir ao estudante organizar e consultar documentos e pendências da candidatura. | Essencial | NEC-03, NEC-04 | CDU-04 |
| RF-08 | O sistema deve apresentar ao estudante o status e o histórico de sua candidatura. | Essencial | NEC-04 | CDU-04 |
| RF-09 | O sistema deve permitir à equipe do NEI cadastrar, editar, publicar, suspender e encerrar oportunidades e editais. | Essencial | NEC-05 | CDU-05 |
| RF-10 | O sistema deve permitir à equipe do NEI cadastrar e manter instituições parceiras, convênios e bolsas. | Importante | NEC-05 | CDU-06 |
| RF-11 | O sistema deve permitir à equipe do NEI consultar candidaturas recebidas. | Essencial | NEC-05 | CDU-07 |
| RF-12 | O sistema deve permitir à equipe do NEI registrar observações e atualizar o status da candidatura. | Essencial | NEC-04, NEC-05 | CDU-07 |
| RF-13 | O sistema deve emitir notificações sobre prazos, pendências e mudanças de status. | Importante | NEC-04 | CDU-08 |
| RF-14 | O sistema deve permitir o registro e a consulta de relatos de experiência de mobilidade. | Desejável | NEC-07 | CDU-11 |
| RF-15 | O sistema deve permitir a participação em atividades de mentoria entre estudantes e ex-intercambistas. | Desejável | NEC-07 | CDU-11 |
| RF-16 | O sistema deve disponibilizar espaço Tandem para troca de idiomas entre participantes. | Desejável | NEC-07 | CDU-12 |
| RF-17 | O sistema deve permitir divulgar e consultar eventos, workshops, palestras e fórum de dúvidas. | Desejável | NEC-07 | CDU-12 |
| RF-18 | O sistema deve gerar relatórios gerenciais sobre candidaturas, perfis de interesse e destinos procurados. | Importante | NEC-08 | CDU-09 |
| RF-19 | O sistema deve permitir ao administrador gerenciar usuários, perfis e permissões. | Essencial | NEC-05 | CDU-14 |
| RF-20 | O sistema deve permitir ao estudante estrangeiro recebido consultar informações e recursos de integração. | Importante | NEC-07 | CDU-13 |
| RF-21 | O sistema deve permitir que o usuário acesse o sistema de forma identificada, com perfil associado às funcionalidades autorizadas. | Essencial | NEC-09 | CDU-15 |
| RF-22 | O sistema deve permitir ao estudante manter um portfólio digital com dados acadêmicos e documentos reutilizáveis entre candidaturas. | Importante | NEC-03 | CDU-16 |
| RF-23 | O sistema deve permitir o registro e a consulta de informações relacionadas ao aproveitamento de créditos da mobilidade realizada. | Importante | NEC-07 | CDU-17 |
| RF-24 | O sistema deve permitir a um perfil autorizado analisar, aprovar, recusar ou remover conteúdo colaborativo publicado por participantes. | Importante | NEC-09 | CDU-18 |

## 2. Regras de especificação

- A autoavaliação é indicativa e não representa decisão oficial de seleção.
- Os critérios e documentos devem estar vinculados à oportunidade correspondente.
- Os estados e transições da candidatura precisam ser detalhados na SRS, sem inventar um fluxo institucional confirmado.
- Não se presume integração com sistemas acadêmicos ou SSO.
- O ator AT-02 (Equipe do NEI) permanece responsável pelas funcionalidades de gestão descritas.
- RF-21 é pré-condição dos requisitos que dependem de perfil (RF-04, RF-06 a RF-12, RF-18, RF-19, RF-22 a RF-24); o método de autenticação permanece A definir (RNF-08) e não se presume SSO institucional.
- RF-22 não cria um repositório acadêmico oficial: o portfólio reúne informações fornecidas pelo próprio estudante.
- RF-23 registra informação declarada e acompanhada no processo; não executa nem substitui a análise acadêmica de aproveitamento, conforme RN-20.
- RF-24 existe para dar execução a RN-12, que exige moderação; o perfil responsável pela moderação está definido em RN-18.
- As prioridades seguem a escala da Visão da Demanda (Essencial, Importante, Desejável) e correspondem às prioridades do backlog conforme a tabela de equivalência do documento 07.
