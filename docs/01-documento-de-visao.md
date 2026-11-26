# Visão da Demanda (VD) — ConectaGlobal

## Identificação e Histórico

| Campo | Informação |
|---|---|
| Nome | ConectaGlobal — Apoio à Consulta de Oportunidades Internacionais |
| Tipo | Novo sistema acadêmico conceitual |
| Produto relacionado | Portal oficial da Diretoria de Relações Internacionais (DRI): https://unifor.br/dri/inicial |
| Área solicitante | Projeto acadêmico da disciplina |
| Elaboração | Equipe do projeto |
| Validação | Não prevista; documento acadêmico elaborado por análise documental |
| Situação | Baseline acadêmica revisada |
| Versão | 2.0 — 26/11/2026 |
| Método | LAPIS — Visão da Demanda v2.1 |

| Data | Versão | Alteração |
|---|---|---|
| 26/11/2026 | 2.0 | Redefinição do escopo com base nas páginas públicas da DRI e no Manual de Boas Práticas de Internacionalização 2026. |

## 1. Objetivo
Permitir que estudantes encontrem, consultem e compreendam informações públicas sobre programas e oportunidades de internacionalização da Unifor, incluindo modalidades, critérios publicados, documentos e orientações para prosseguir pelos canais oficiais da DRI.

## 2. Contexto, Problema e Descrição Sumária

- **Situação documentada:** a DRI mantém portal próprio e divulga programas de mobilidade, dupla titulação, Buddy Program, EducationUSA, Top España e outras iniciativas. A página de apoio ao estudante apresenta perguntas frequentes, critérios e etapas do processo.
- **Oportunidade do projeto:** organizar as informações públicas em uma experiência de consulta estruturada, com filtros, detalhes, checklist informativo e links para a fonte oficial.
- **Problema não afirmado:** as fontes consultadas não comprovam que os dados estejam atualmente dispersos, que estudantes percam prazos ou que a DRI controle candidaturas manualmente. Essas afirmações não serão usadas como fatos.
- **Descrição:** catálogo informativo complementar, páginas detalhadas por programa, consulta de critérios e documentos, orientação sobre etapas e encaminhamento ao canal oficial.

## 3. Proposta de Valor e Sucesso

| Benefício | Evidência verificável | Resultado acadêmico esperado | Avaliação |
|---|---|---|---|
| Facilitar localização de programas | Catálogo com modalidades documentadas | Usuário localiza um programa por categoria e palavra-chave | Teste de tarefas |
| Tornar critérios compreensíveis | Página detalhada com critérios e fonte | Usuário identifica requisitos publicados e distingue regras gerais de edital específico | Teste de compreensão |
| Orientar próximos passos | Fluxo informativo e links oficiais | Usuário identifica que deve procurar a DRI e consultar o edital aplicável | Teste de cenário |
| Evitar informação desatualizada no protótipo | Data de consulta e link da fonte em cada conteúdo | Usuário consegue conferir a informação oficial | Inspeção de conteúdo |

## 4. Partes Interessadas

| Parte | Interesse/papel | Base documental |
|---|---|---|
| Estudantes de graduação e pós-graduação da Unifor | Consultar programas e critérios | Página DRI — Apoio ao Estudante |
| Diretoria de Relações Internacionais (DRI) | Unidade institucional responsável pela divulgação e coordenação de ações internacionais | Portal DRI e Manual 2026 |
| Setor de Apoio Discente | Atua em intercâmbio acadêmico, dupla titulação, cotutela e programas estudantis | Manual 2026 |
| Coordenação da DRI | Planejamento, organização e gerenciamento das atividades | Manual 2026 |
| Instituições de ensino parceiras | Participam de mobilidade por acordos e condições próprias | Página DRI — Convênios e Manual 2026 |
| Equipe do projeto acadêmico | Analisa fontes, define escopo e especifica o sistema | Decisão do projeto |
| Professor da disciplina | Avalia os artefatos acadêmicos | Enunciado da disciplina |

## 5. Usuários e Atores Externos

| ID | Ator | Papel |
|---|---|---|
| AT-01 | Estudante da Unifor | Pesquisa e consulta programas, critérios, documentos e orientações |
| AT-02 | Responsável editorial do ConectaGlobal (ator conceitual) | Mantém conteúdo informativo do protótipo; papel definido apenas para modelagem acadêmica |
| AT-03 | Portal oficial da DRI | Fonte externa consultada pelo usuário por links; não há integração automatizada |
| AT-04 | Navegador web | Ambiente de acesso; não é ator humano nem sistema de negócio |

Não são modelados como atores do sistema: sistema acadêmico, SSO, serviço de e-mail, coordenador de curso ou avaliador de candidatura, pois não há evidência pública suficiente de interação com o ConectaGlobal proposto.

## 6. Escopo e Entregas

### 6.1 Incluído
- Catálogo de programas e oportunidades documentados publicamente.
- Pesquisa textual e filtros por modalidade/categoria.
- Detalhes de programa com descrição, público, critérios, documentos e etapas quando publicados.
- Checklist informativo de preparação, sem upload ou envio de documentos.
- Perguntas frequentes e glossário.
- Links para páginas, editais e contatos oficiais da DRI.
- Identificação da fonte e data de consulta do conteúdo.
- Área conceitual de manutenção editorial de conteúdo do protótipo.

### 6.2 Fora do escopo
- Inscrição/candidatura oficial e envio de formulários à DRI.
- Seleção, classificação, aprovação, reprovação ou acompanhamento de candidatura.
- Cadastro de manifestações de interesse e painel operacional da DRI.
- Integração com SSO, sistema acadêmico, Pipefy, e-mail ou APIs institucionais.
- Consulta automática de matrícula, PMG, reprovações ou passaporte.
- Gestão de convênios, bolsas, pagamentos, vistos, seguros ou aproveitamento de créditos.
- Informação privada ou não publicada pela DRI.

### 6.3 Evoluções futuras
Somente mediante novas fontes e definição de escopo: recursos personalizados, notificações e integração institucional.

### 6.4 Entregas acadêmicas
Visão, stakeholders, análise documental, requisitos, regras, backlog, casos de uso, glossário e diagramas UML. A P2 acrescentará SRS, protótipo navegável e revisão de consistência.

## 7. Necessidades e Catálogo de Funcionalidades

| ID | Necessidade | Fonte | Atores |
|---|---|---|---|
| NEC-01 | Localizar programas de internacionalização | Portal DRI | AT-01 |
| NEC-02 | Entender modalidades e público de cada programa | Portal DRI | AT-01 |
| NEC-03 | Consultar critérios de participação publicados | DRI — Apoio ao Estudante e editais | AT-01 |
| NEC-04 | Identificar documentos e etapas descritos oficialmente | DRI — Apoio ao Estudante | AT-01 |
| NEC-05 | Prosseguir para o canal oficial de orientação/candidatura | Portal DRI — contatos e orientações | AT-01 |
| NEC-06 | Manter a informação do protótipo vinculada à fonte pública | Decisão de projeto DP-01 | AT-02 |

| ID | Funcionalidade | Necessidade | Atores | Prioridade | Valor | Frequência | Caso |
|---|---|---|---|---|---|---|---|
| F-01 | Consultar catálogo de programas | NEC-01 | AT-01 | Essencial | Alto | Alta | CDU-01 |
| F-02 | Pesquisar e filtrar programas | NEC-01 | AT-01 | Importante | Alto | Alta | CDU-02 |
| F-03 | Consultar detalhes de programa | NEC-02, NEC-03, NEC-04 | AT-01 | Essencial | Alto | Alta | CDU-03 |
| F-04 | Consultar critérios e documentos | NEC-03, NEC-04 | AT-01 | Essencial | Alto | Alta | CDU-03 |
| F-05 | Consultar etapas e próximos passos | NEC-04, NEC-05 | AT-01 | Essencial | Alto | Média | CDU-04 |
| F-06 | Acessar fonte e contato oficial | NEC-05, NEC-06 | AT-01 | Essencial | Alto | Média | CDU-04 |
| F-07 | Manter conteúdo informativo do protótipo | NEC-06 | AT-02 | Importante | Médio | Baixa | CDU-05 |

## 8. Visão Geral da Solução e Impactos
ConectaGlobal é um catálogo informativo complementar. O conteúdo deve reproduzir ou resumir fielmente informações públicas, mantendo referência e data de consulta. O portal oficial da DRI permanece a fonte de autoridade. O protótipo não envia dados pessoais nem executa processos institucionais.

## 9. Condições Gerais
- A informação de elegibilidade deve ser apresentada com contexto e link para o edital/programa aplicável.
- Critérios de mobilidade podem estar associados a regulamentos, programas ou editais específicos; não se deve generalizar sem fonte.
- O conteúdo público pode mudar; cada registro do protótipo deve mostrar fonte e data de consulta.
- A equipe não tem autorização presumida para usar sistemas, dados ou marcas internas além do que é publicamente disponibilizado.
- O projeto é acadêmico e não representa produto oficial da Unifor.

## 10. Riscos e Questões
| ID | Risco | Tratamento adotado |
|---|---|---|
| R-01 | Conteúdo oficial pode mudar | Exibir fonte e data de consulta; orientar conferência no portal DRI |
| R-02 | Regulamento e página-resumo podem ter escopos distintos | Priorizar o edital/regulamento aplicável e não universalizar critérios |
| R-03 | Usuário pode confundir protótipo com inscrição oficial | Avisos claros: “ambiente acadêmico; não realiza candidatura” |
| R-04 | Conteúdo não publicado não pode ser inferido | Excluir funcionalidades e regras internas sem evidência |

## 11. Documentos Relacionados
Ver `docs/02` a `docs/09`, além das fontes oficiais registradas em `docs/09-fontes-e-decisoes.md`.

## 12. Validação da Visão
Checklist de revisão interna:
- [x] Objetivo, contexto, escopo e exclusões definidos.
- [x] Necessidades ligadas a fontes públicas.
- [x] Funcionalidades ligadas às necessidades e casos de uso.
- [x] Hipóteses de integração e de processo interno removidas do escopo.
- [x] Ausência de entrevistas e validação institucional declarada.
- [x] Revisão de consistência documental realizada pela equipe do projeto (baseline acadêmica).
