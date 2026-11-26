# Documento de Visão — ConectaGlobal

**Projeto:** ConectaGlobal — Sistema de Gestão de Oportunidades Internacionais  
**Disciplina:** Requisitos e Modelagem de Sistemas — Unifor, 2026.2  
**Versão:** 3.0 — 26/11/2026  
**Situação:** Base revisada da P1 para evolução à P2

## 1. Objetivo
Definir a visão de um sistema acadêmico autoral que centraliza oportunidades internacionais e apoia o estudante desde a consulta de uma oportunidade até o acompanhamento de sua manifestação de interesse ou candidatura. O sistema também oferece recursos para que usuários responsáveis cadastrem oportunidades, configurem critérios e acompanhem as solicitações recebidas.

## 2. Contexto, problema e descrição sumária
Oportunidades internacionais podem envolver diferentes modalidades, instituições de destino, critérios de elegibilidade, prazos e documentos. Quando essas informações ficam dispersas, o interessado pode ter dificuldade para localizar oportunidades compatíveis, compreender requisitos e acompanhar os passos de sua candidatura.

O ConectaGlobal propõe um ambiente único para organizar essas informações e apoiar o fluxo de interesse/candidatura. O problema é tratado como motivação de projeto, não como diagnóstico institucional validado por entrevistas.

## 3. Proposta de valor e sucesso
**Proposta de valor:** facilitar a descoberta e a gestão de oportunidades internacionais, oferecendo informações estruturadas e acompanhamento transparente das solicitações.

Indicadores propostos para avaliação do protótipo:
- estudante consegue localizar oportunidades por filtros;
- estudante consegue consultar requisitos, prazos e documentos;
- estudante consegue registrar interesse/candidatura e consultar seu andamento;
- gestor consegue cadastrar, atualizar e publicar oportunidades;
- gestor consegue consultar solicitações e atualizar seus estados;
- informações essenciais são apresentadas de forma clara e consistente.

## 4. Partes interessadas
| ID | Parte interessada | Interesse |
|---|---|---|
| ST-01 | Estudantes | Encontrar oportunidades, compreender requisitos e acompanhar solicitações. |
| ST-02 | Equipe gestora de oportunidades | Cadastrar oportunidades, manter dados atualizados e acompanhar solicitações. |
| ST-03 | Coordenações/avaliadores designados no contexto do projeto | Analisar solicitações e registrar decisões ou mudanças de situação. |
| ST-04 | Administração do sistema | Gerenciar usuários, perfis e parâmetros gerais. |
| ST-05 | Equipe de desenvolvimento | Construir e manter a solução acadêmica. |
| ST-06 | Docente da disciplina | Avaliar os artefatos e a evolução do projeto. |

Os papéis acima são papéis conceituais do sistema. Não afirmam que uma unidade institucional específica execute oficialmente essas atividades.

## 5. Usuários e atores externos
| ID | Ator | Descrição |
|---|---|---|
| AT-01 | Estudante | Consulta oportunidades, verifica requisitos, registra interesse/candidatura e acompanha solicitações próprias. |
| AT-02 | Gestor de oportunidades | Cadastra, edita, publica, encerra oportunidades e acompanha solicitações. |
| AT-03 | Avaliador | Consulta solicitações atribuídas e registra análise ou atualização de situação. |
| AT-04 | Administrador do sistema | Gerencia contas, perfis e parâmetros de acesso. |

## 6. Escopo e entregas previstas
### 6.1 Dentro do escopo
- cadastro, edição, publicação e encerramento de oportunidades;
- consulta, pesquisa e filtragem de oportunidades;
- visualização de detalhes, prazos, critérios e documentos exigidos;
- apresentação de critérios de elegibilidade e indicação informativa de compatibilidade;
- manifestação de interesse ou envio de candidatura pelo estudante;
- registro e consulta de documentos associados à candidatura;
- acompanhamento do status da solicitação;
- análise de solicitações e atualização de status por usuários autorizados;
- notificações sobre eventos relevantes do fluxo;
- painéis e relatórios básicos de oportunidades e solicitações;
- gerenciamento de usuários e perfis de acesso.

### 6.2 Fora do escopo nesta etapa
- integração obrigatória com sistemas acadêmicos ou institucionais;
- autenticação por SSO institucional;
- comunicação automática com sistemas de instituições parceiras;
- decisão automatizada de seleção ou garantia de aprovação por instituição de destino;
- emissão de vistos, passagens, seguros, pagamentos ou gestão financeira;
- substituição de processos oficiais de instituições ou setores existentes;
- validação institucional do fluxo proposto.

## 7. Necessidades e catálogo de funcionalidades
| ID | Necessidade | Funcionalidades relacionadas |
|---|---|---|
| NEC-01 | Localizar oportunidades relevantes | F-01, F-02 |
| NEC-02 | Compreender condições e requisitos | F-03, F-04 |
| NEC-03 | Registrar interesse/candidatura | F-05, F-06 |
| NEC-04 | Acompanhar o andamento | F-07, F-08 |
| NEC-05 | Manter oportunidades organizadas | F-09, F-10 |
| NEC-06 | Analisar solicitações recebidas | F-11 |
| NEC-07 | Acompanhar indicadores da operação | F-12 |
| NEC-08 | Controlar acesso e perfis | F-13 |

### Catálogo
- **F-01 — Consultar oportunidades:** listar oportunidades disponíveis.
- **F-02 — Pesquisar e filtrar oportunidades:** localizar por modalidade, destino, área, prazo e situação.
- **F-03 — Consultar detalhes:** exibir descrição, instituição/destino, período, prazos e condições.
- **F-04 — Consultar requisitos e documentos:** apresentar critérios e lista de documentos exigidos.
- **F-05 — Manifestar interesse/candidatar-se:** registrar uma solicitação vinculada à oportunidade.
- **F-06 — Gerenciar documentos da solicitação:** anexar, consultar e substituir documentos permitidos.
- **F-07 — Acompanhar solicitação:** consultar situação e histórico da candidatura.
- **F-08 — Receber notificações:** informar eventos e mudanças relevantes.
- **F-09 — Cadastrar oportunidade:** registrar dados de uma nova oportunidade.
- **F-10 — Manter/publicar oportunidade:** editar, publicar, suspender ou encerrar uma oportunidade.
- **F-11 — Analisar solicitações:** consultar dados recebidos e atualizar a situação.
- **F-12 — Gerar relatórios:** apresentar quantitativos e estados das oportunidades e solicitações.
- **F-13 — Gerenciar usuários e perfis:** administrar contas e permissões.

## 8. Visão geral da solução e impactos
A solução é concebida como aplicação web, acessível por navegador. Seus módulos lógicos incluem autenticação e autorização, gestão de oportunidades, consulta e elegibilidade, gestão de candidaturas, documentos, notificações e relatórios.

O impacto esperado é organizar o fluxo informacional e permitir rastreabilidade básica das solicitações. A solução não substitui a avaliação humana nem garante que uma candidatura seja aceita por uma instituição de destino.

## 9. Condições gerais
- As funcionalidades descritas são decisões de projeto acadêmico.
- Critérios específicos de cada oportunidade devem ser cadastrados e associados à oportunidade correspondente.
- A indicação de elegibilidade é informativa e depende dos dados e critérios cadastrados.
- A análise final de uma candidatura cabe ao papel autorizado definido no fluxo do sistema.
- Dados pessoais e documentos devem ter acesso restrito conforme perfil e finalidade.
- O protótipo da disciplina poderá simular partes do fluxo sem implementar integrações externas.

## 10. Riscos e questões em aberto
| Risco/questão | Tratamento previsto |
|---|---|
| Critérios variam entre oportunidades | Associar critérios à oportunidade, evitando regra universal. |
| Informações podem ficar desatualizadas | Permitir manutenção e registrar data de atualização. |
| Usuário interpretar elegibilidade como aprovação | Exibir aviso de que a indicação não garante seleção. |
| Exposição indevida de documentos | Restringir acesso por usuário e perfil. |
| Escopo extenso para o protótipo | Priorizar fluxo principal de consulta, candidatura e gestão. |
| Notificações e relatórios excederem o tempo disponível | Implementar inicialmente versão simplificada ou simulação no protótipo. |

## 11. Documentos relacionados
- Requisitos funcionais e não funcionais — `04-requisitos.md`.
- Regras de negócio — `05-regras-de-negocio.md`.
- Backlog — `06-backlog.md`.
- Casos de uso — `07-casos-de-uso.md`.
- Diagramas UML — `../uml/diagramas.puml`.
- Análise documental e referências — `03-analise-documental.md` e `09-fontes-e-decisoes.md`.

## 12. Validação da visão
Esta versão representa a definição acadêmica da equipe para orientar a P2. Não houve validação institucional nem entrevistas com usuários. A revisão de consistência será realizada internamente entre visão, requisitos, casos de uso, diagramas e protótipo.
