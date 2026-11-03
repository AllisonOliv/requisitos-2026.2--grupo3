# 4. Requisitos

Legenda: **[D]** base documental · **[H]** hipótese a validar · **[C]** confirmado em entrevista.
Prioridade (MoSCoW): **M** Must · **S** Should · **C** Could · **W** Won't (nesta fase).

## 4.1 Requisitos Funcionais

### Gestão de editais e bolsas (NEI/DRI)
| ID | Requisito | Prio. | Status |
|---|---|---|---|
| RF01 | O sistema deve permitir cadastrar um edital com título, tipo, destino/instituição, país, área, vagas, período de inscrição, descrição e anexos | M | D |
| RF02 | O sistema deve permitir editar, publicar, despublicar, encerrar e arquivar um edital | M | D |
| RF03 | O sistema deve permitir cadastrar uma bolsa (fonte, valor/benefício, vigência), vinculada ou não a um edital | M | D |
| RF04 | O sistema deve permitir definir, por edital, os critérios de elegibilidade (percentual concluído, média, reprovações, curso, idioma, outros) | M | D |
| RF05 | O sistema deve permitir definir a lista de documentos exigidos em cada edital | M | D |
| RF06 | O sistema deve permitir atribuir um responsável pela atualização de cada edital | S | H |
| RF07 | O sistema deve registrar o histórico de alterações de um edital | S | H |

### Consulta e acompanhamento (estudante)
| ID | Requisito | Prio. | Status |
|---|---|---|---|
| RF08 | O sistema deve listar oportunidades com busca por texto e filtros (país, área, tipo, status, prazo, curso) | M | D |
| RF09 | O sistema deve exibir o detalhe da oportunidade: requisitos, prazos, documentos e contato | M | D |
| RF10 | O sistema deve exibir um calendário/linha do tempo com os prazos das oportunidades | S | H |
| RF11 | O sistema deve permitir ao estudante verificar sua pré-elegibilidade para uma oportunidade | M | D |
| RF12 | O sistema deve permitir ao estudante registrar manifestação de interesse em uma oportunidade aberta | M | D |
| RF13 | O sistema deve permitir ao estudante cancelar sua manifestação enquanto o edital estiver aberto | S | H |
| RF14 | O sistema deve permitir ao estudante acompanhar o status de suas manifestações | M | D |
| RF15 | O sistema deve exibir um checklist de documentos e permitir marcar o que já foi reunido | S | H |
| RF16 | O sistema deve permitir salvar oportunidades como favoritas | C | H |

### Análise de manifestações (NEI/DRI)
| ID | Requisito | Prio. | Status |
|---|---|---|---|
| RF17 | O sistema deve listar as manifestações por edital com filtros por status, curso e elegibilidade | M | D |
| RF18 | O sistema deve permitir ao NEI/DRI avaliar uma manifestação, alterar seu status e registrar justificativa (obrigatória em caso de recusa ou inelegibilidade) | M | D |
| RF19 | O sistema deve permitir solicitar complementação de documentos ao estudante | S | H |
| RF20 | O sistema deve gerar relatórios (manifestações por edital, curso, destino) e permitir exportar em CSV ou PDF | S | D |

### Comunicação e acesso
| ID | Requisito | Prio. | Status |
|---|---|---|---|
| RF21 | O sistema deve notificar o estudante sobre novas oportunidades compatíveis, prazos próximos e mudanças de status | M | D |
| RF22 | O sistema deve notificar os interessados quando prazo ou requisito de um edital for alterado | S | H |
| RF23 | O sistema deve autenticar usuários com credenciais institucionais | M | H |
| RF24 | O sistema deve controlar permissões por perfil (estudante, NEI/DRI, coordenador, administrador) | M | H |
| RF25 | O sistema deve permitir ao coordenador consultar manifestações dos alunos do seu curso | C | H |
| RF26 | O sistema deve permitir informar, em cada edital, a instituição parceira e a vigência do convênio associado | S | H |

## 4.2 Requisitos Não Funcionais

| ID | Categoria | Requisito | Prio. | Status |
|---|---|---|---|---|
| RNF01 | Usabilidade | O estudante deve conseguir encontrar uma oportunidade e iniciar a manifestação em no máximo 4 passos, e concluir o fluxo completo em até 10 minutos sem treinamento prévio | M | H |
| RNF02 | Acessibilidade | A interface deve atender WCAG 2.1 nível AA | M | D |
| RNF03 | Portabilidade | O sistema deve ser responsivo (celular iOS/Android, tablet, desktop) e compatível com as duas últimas versões de Chrome, Edge, Safari e Firefox | M | D |
| RNF04 | Desempenho | Listagens e buscas devem responder em até 2 s em 95% das requisições, com até 500 usuários simultâneos; o painel do NEI/DRI deve suportar consultas sobre até 5.000 manifestações sem degradação perceptível | S | H |
| RNF05 | Disponibilidade | Disponibilidade mínima de 99% mensal, reforçada em períodos de inscrição | S | H |
| RNF06 | Segurança | Comunicação via HTTPS/TLS 1.2 ou superior; dados pessoais sensíveis (ex.: média, percentual concluído, documentos) criptografados em repouso; controle de acesso por perfil; senhas nunca armazenadas pelo sistema (SSO) | M | H |
| RNF07 | Privacidade (LGPD) | Dados pessoais devem ser tratados com base legal e consentimento explícito quando aplicável, finalidade definida, mínimo necessário, e possibilidade de solicitar exclusão, anonimização ou portabilidade | M | D |
| RNF08 | Auditoria | Ações de criação, edição e mudança de status devem ser registradas com usuário e data/hora | S | H |
| RNF09 | Interoperabilidade | O sistema deve expor/consumir dados por API REST para integrar com autenticação e sistema acadêmico | S | H |
| RNF10 | Internacionalização | A interface deve suportar, no mínimo, português e inglês (espanhol desejável) | C | D |
| RNF11 | Manutenibilidade | O sistema deve ter arquitetura modular e documentação de API | S | H |
| RNF12 | Confiabilidade | Backup diário dos dados com retenção mínima de 30 dias | S | H |
| RNF13 | Notificações | E-mails devem ser enviados em até 5 minutos após o evento gerador | C | H |

## 4.3 Rastreabilidade (resumo)
| Objetivo específico | Requisitos |
|---|---|
| OE1 — Cadastro e manutenção pelo NEI/DRI | RF01–RF07, RF24 |
| OE2 — Encontrar oportunidade, verificar elegibilidade, manifestar interesse | RF08–RF13, RF16 |
| OE3 — Acompanhamento de status | RF14, RF17–RF19, RF21–RF22 |
| OE4 — Reduzir perda de prazo e retrabalho | RF10, RF15, RF20–RF22, RF26, RNF01 |

## 4.4 Funcionalidades identificadas e deixadas fora do escopo (Won't nesta fase)

Origem: apresentação da disciplina e outras propostas do Eixo I. São registradas para mostrar que foram consideradas e para orientar releases futuras.

| Funcionalidade | Origem | Motivo de ficar fora |
|---|---|---|
| Gestão completa de convênios (cadastro, vigência, vagas) | Apresentação / escopo NEI | Foge do foco em editais e oportunidades; o sistema só referencia a instituição e a vigência (RF26) |
| Controle de concessão de bolsas (valor, beneficiário, orçamento) | Apresentação | O tema trata de divulgar e acompanhar oportunidades de bolsa; a gestão financeira exige integração com outro setor |
| Central de preparação (idioma, cultura, planejamento financeiro) e simulação de custos | Apresentação | Escopo de portal de informações (tema 4) |
| Portfólio digital do estudante | Apresentação | Valor secundário para o problema investigado |
| Aproveitamento de créditos e pós-intercâmbio (relatos, mentoria) | Apresentação / tema 1 | Fase posterior ao acompanhamento de oportunidades |
| Módulo colaborativo (Tandem, eventos, fórum) | Apresentação / tema 1 | Escopo de rede social acadêmica (tema 1) |
| Ranqueamento e resultado final da seleção | Apresentação | Exige regras de seleção ainda não conhecidas |
