# Requisitos — ConectaGlobal

## 1. Convenções
- **RF:** requisito funcional.
- **RNF:** requisito não funcional.
- Prioridade: **Alta**, **Média** ou **Baixa**.
- Os requisitos são decisões de projeto acadêmico e serão detalhados na SRS da P2.

## 2. Requisitos funcionais
| ID | Requisito | Prioridade | Caso de uso |
|---|---|---|---|
| RF-01 | O sistema deve permitir consultar a lista de oportunidades publicadas e disponíveis. | Alta | UC-01 |
| RF-02 | O sistema deve permitir pesquisar e filtrar oportunidades por modalidade, destino, área, prazo e situação. | Alta | UC-02 |
| RF-03 | O sistema deve exibir os detalhes de uma oportunidade, incluindo descrição, destino, período, prazos e situação. | Alta | UC-03 |
| RF-04 | O sistema deve exibir os critérios de elegibilidade e os documentos exigidos para cada oportunidade. | Alta | UC-04 |
| RF-05 | O sistema deve permitir que o estudante registre uma manifestação de interesse/candidatura em oportunidade publicada e dentro do prazo. | Alta | UC-05 |
| RF-06 | O sistema deve permitir anexar, consultar e substituir documentos de uma candidatura, respeitando as permissões e o prazo. | Alta | UC-06 |
| RF-07 | O sistema deve permitir ao estudante consultar o status e o histórico de sua candidatura. | Alta | UC-07 |
| RF-08 | O sistema deve registrar notificações sobre confirmação de envio e mudanças relevantes no status da candidatura. | Média | UC-08 |
| RF-09 | O sistema deve permitir ao gestor cadastrar uma oportunidade com descrição, modalidade, destino, período, prazo, critérios e documentos. | Alta | UC-09 |
| RF-10 | O sistema deve permitir ao gestor editar, publicar, suspender e encerrar oportunidades. | Alta | UC-10 |
| RF-11 | O sistema deve permitir ao avaliador consultar candidaturas e registrar análise e atualização de status. | Alta | UC-11 |
| RF-12 | O sistema deve disponibilizar relatórios básicos de oportunidades e candidaturas por período e situação. | Média | UC-12 |
| RF-13 | O sistema deve permitir ao administrador cadastrar, ativar, desativar e atribuir perfis a usuários. | Média | UC-13 |

## 3. Requisitos não funcionais
| ID | Requisito | Prioridade |
|---|---|---|
| RNF-01 | A interface deve utilizar linguagem clara e consistente em português. | Alta |
| RNF-02 | A interface deve ser responsiva para uso em computadores, tablets e celulares. | Alta |
| RNF-03 | A navegação deve manter padrões consistentes de menus, formulários, mensagens e ações. | Alta |
| RNF-04 | O sistema deve restringir o acesso a funções e dados conforme o perfil do usuário. | Alta |
| RNF-05 | A comunicação com o sistema deve utilizar conexão protegida (HTTPS) quando implantado em ambiente real. | Alta |
| RNF-06 | Senhas não devem ser armazenadas em texto puro; devem utilizar mecanismo seguro de hash quando houver autenticação própria. | Alta |
| RNF-07 | O sistema deve validar campos obrigatórios, formatos e limites antes de salvar dados. | Alta |
| RNF-08 | O sistema deve apresentar mensagens de erro compreensíveis, sem expor detalhes técnicos ou dados sensíveis. | Média |
| RNF-09 | Documentos e dados pessoais devem ser acessíveis somente a usuários autorizados. | Alta |
| RNF-10 | As principais páginas de consulta devem apresentar conteúdo em tempo de resposta adequado ao uso interativo, com meta de até 3 segundos em condições normais de teste. | Média |
| RNF-11 | O sistema deve registrar operações relevantes de gestão e alteração de status para permitir rastreabilidade. | Média |
| RNF-12 | A interface deve observar boas práticas de acessibilidade, incluindo contraste, identificação de campos e navegação por teclado. | Média |

## 4. Rastreabilidade resumida
| Necessidade | Requisitos |
|---|---|
| NEC-01 — Localizar oportunidades | RF-01, RF-02 |
| NEC-02 — Compreender condições | RF-03, RF-04 |
| NEC-03 — Registrar candidatura | RF-05, RF-06 |
| NEC-04 — Acompanhar andamento | RF-07, RF-08 |
| NEC-05 — Manter oportunidades | RF-09, RF-10 |
| NEC-06 — Analisar solicitações | RF-11 |
| NEC-07 — Consultar indicadores | RF-12 |
| NEC-08 — Controlar acesso | RF-13, RNF-04, RNF-09 |

## 5. Observações para a SRS
Na P2, cada requisito deverá receber descrição detalhada, entradas, saídas, regras aplicáveis, condições de aceitação e prioridade confirmada. A equipe deverá decidir no protótipo quais operações serão funcionais e quais serão simuladas, sem alterar silenciosamente o escopo documentado.
