# Análise Documental e Elicitação — ConectaGlobal

## Histórico de versões

| Data | Versão | Descrição | Autor |
|---|---|---|---|
| 26/11/2026 | 1.1 | Consolidação das fontes, evidências, roteiros e limitações sem fabricar resultados. | Equipe do projeto |
| 26/11/2026 | 1.2 | Recuperação dos achados documentais específicos (convênios, dados de contexto e critérios de elegibilidade) que constavam da versão anterior do documento, com identificação explícita da fonte e do limite de cada achado. | Equipe do projeto |

## 1. Objetivo

Registrar as fontes consultadas, evidências documentais, técnicas de elicitação previstas e questões ainda não confirmadas para a proposta ConectaGlobal.

## 2. Fontes analisadas

| ID | Fonte | Contribuição |
|---|---|---|
| AD-01 | Material de Projeto de Extensão — Internacionalização, Unifor, 2026.2 | Contexto, objetivo, módulos, públicos e funcionalidades propostas. |
| AD-02 | Propostas de Projetos de Sistemas — Internacionalização e ENADE, Unifor, 2026.2 | Recorte Gestão de Oportunidades Internacionais, editais, bolsas, requisitos, prazos, documentos e manifestações de interesse. |
| AD-03 | Repositório LAPIS | Método e templates para Visão da Demanda, casos de uso, regras, RNF e glossário. |
| AD-04 | Portal público da DRI | Referência visual futura para organização das telas; não é fonte de requisitos. |

## 3. Evidências documentais

| ID | Evidência | Fonte |
|---|---|---|
| EV-01 | A proposta busca apoiar a gestão da mobilidade acadêmica internacional. | AD-01 |
| EV-02 | O módulo do estudante prevê portal de oportunidades com filtros por país, área e duração. | AD-01 |
| EV-03 | O módulo do estudante prevê autoavaliação e preparação em idiomas, cultura e planejamento financeiro. | AD-01 |
| EV-04 | O módulo de gestão (NEI) prevê gestão de convênios, painel de candidaturas, notificações, bolsas e relatórios. | AD-01 |
| EV-05 | O módulo pós-intercâmbio prevê relatos, informações de aproveitamento de créditos e rede de ex-participantes para mentoria. | AD-01 |
| EV-06 | O módulo colaborativo prevê Tandem, eventos, workshops, palestras e fórum de dúvidas. | AD-01 |
| EV-07 | A proposta Gestão de Oportunidades Internacionais contempla cadastro e divulgação de editais, bolsas, requisitos, prazos, documentos e acompanhamento de manifestações de interesse. | AD-02 |
| EV-08 | A documentação-base identifica como beneficiados diretos os estudantes de graduação elegíveis, a equipe do NEI e os alunos estrangeiros recebidos; e como beneficiados indiretos os coordenadores de curso, os professores envolvidos em cooperações internacionais e futuros candidatos. | AD-01 |
| EV-09 | O material da disciplina informa que a Unifor oferece acesso a mais de 140 instituições em 30 países. | AD-01 |
| EV-10 | O material da disciplina apresenta dados da pesquisa Selo Belta indicando que 28,6% dos estudantes pretendiam viajar em 2024 e 21% planejavam intercâmbio em 2025 ou depois. | AD-01 |
| EV-11 | O material da disciplina menciona, como requisitos de elegibilidade, matrícula ativa, percentual do curso concluído entre 30% e 70%, média igual ou superior a 7,0 e ausência de reprovações. | AD-01 |
| EV-12 | O documento de propostas indica como questões a investigar os critérios de elegibilidade, os responsáveis pela atualização das informações e a integração com processos institucionais. | AD-02 |
| EV-13 | O material da disciplina propõe validação automática dos critérios de elegibilidade no sistema e um painel de candidaturas com análise automatizada. | AD-01 |
| EV-14 | O material da disciplina prevê, na central de preparação, recursos linguísticos e certificação, além de ferramentas de estimativa de custos e busca por bolsas disponíveis. | AD-01 |
| EV-15 | O material da disciplina prevê o portfólio digital acompanhado de acompanhamento em tempo real. | AD-01 |
| EV-16 | O material da disciplina lista como entregáveis o Documento de Visão, os requisitos elicitados, a especificação SRS no padrão IEEE 830, diagramas UML de Casos de Uso, Classes, Sequência, Atividades e Estados, protótipos de interface e apresentação final em pitch para banca com representantes do NEI. | AD-01 |
| EV-17 | O documento de propostas orienta selecionar uma das seis propostas e afirma que a definição do produto mínimo e dos limites do sistema integra a própria atividade de análise, não se exigindo implementar todas as funcionalidades sugeridas. | AD-02 |

### 3.1 Limite de interpretação de cada achado

| Evidência | O que a evidência sustenta | O que a evidência não sustenta |
|---|---|---|
| EV-09 | Existência de uma rede de convênios ampla o suficiente para justificar catálogo e filtros por país e instituição. | Quantidade, vigência ou distribuição atual dos convênios, que não foram verificadas em fonte institucional. |
| EV-10 | Interesse declarado de estudantes por mobilidade, usado apenas como contexto de demanda. | Que informações estejam dispersas, que prazos sejam perdidos ou que exista dificuldade operacional específica na Unifor. |
| EV-11 | Que existem critérios de elegibilidade objetivos e parametrizáveis, o que fundamenta RN-02, RN-03 e a autoavaliação (CDU-02). | Que esses valores sejam universais, vigentes ou aplicáveis a todas as modalidades: o material não informa a abrangência. Permanece em PQ-01/H-02. |
| EV-12 | Que as próprias fontes reconhecem lacunas sobre critérios, responsabilidades e integração. | Qualquer definição desses pontos, que seguem como questões abertas. |
| EV-13 | Que a documentação-base esperava automatizar a verificação de elegibilidade e apoiar a análise das candidaturas. | Que essa automação seja decisão oficial de seleção. O projeto decidiu tratar a autoavaliação como indicativa (DP-03, RN-04) e manter fora de escopo a decisão exclusivamente algorítmica; esta é uma divergência deliberada em relação a AD-01, registrada como decisão. |
| EV-16 | Que o escopo de modelagem previsto na documentação-base é mais amplo do que o conjunto entregue até aqui. | Que os diagramas ausentes sejam dispensáveis: Classes, Sequência e Estados constam de AD-01 e não foram elaborados. |
| EV-17 | Que delimitar o escopo é parte avaliada do trabalho. | Que o recorte adotado esteja validado: a manutenção dos quatro módulos de AD-01 sobre o recorte do Tema 3 de AD-02 é decisão da equipe (DP-01, DP-07).

## 4. Técnicas de elicitação e situação

| Técnica | Público/fonte | Objetivo | Situação |
|---|---|---|---|
| Análise documental | AD-01 e AD-02 | Identificar contexto, escopo e funcionalidades | Executada |
| Entrevista semiestruturada | Equipe responsável pelo processo | Confirmar regras, atualização e acompanhamento | Não realizada nesta etapa |
| Entrevista | Estudantes | Compreender busca e avaliação de oportunidades | Não realizada nesta etapa |
| Entrevista | Ex-intercambistas | Identificar dificuldades e necessidades pós-mobilidade | Não realizada nesta etapa |
| Entrevista | Coordenadores | Confirmar participação acadêmica | Não realizada nesta etapa |
| Questionário | Estudantes | Identificar padrões e necessidades | Planejado, não aplicado |
| Prototipação/teste | Usuários potenciais | Avaliar compreensão e navegação | Planejado para P2 |

Conforme orientação informada para a etapa, entrevistas não foram exigidas agora. Os roteiros são instrumentos preparados, não resultados de pesquisa.

## 5. Limites da evidência

- Não há transcrições nem resultados de entrevistas.
- Não houve observação direta do processo institucional.
- Não foi confirmado um edital real com todas as regras aplicáveis; os valores de EV-11 são tratados como exemplo de parametrização, não como regra institucional vigente.
- Não há confirmação de integração com sistema acadêmico, SSO ou outros sistemas.
- Dados contextuais presentes nos materiais não comprovam, por si só, dificuldades operacionais específicas.
- O Núcleo de Estratégias Internacionais (NEI) é nomeado em AD-01, que o indica como área responsável e como participante da banca final. AD-02 não menciona o NEI: cita equipe de internacionalização no Tema 1 e serviços da DRI no Tema 4. A presença do NEI como ator sustenta-se, portanto, em AD-01.
- A DRI é referência visual futura, não fonte para definição de atores, regras ou requisitos do produto.

## 6. Hipóteses e questões a validar

| ID | Hipótese/questão | Como validar | Situação |
|---|---|---|---|
| H-01 | Informações de oportunidades podem estar distribuídas em canais distintos. | Levantamento com responsáveis e canais oficiais. | Aberta |
| H-02 | Critérios de elegibilidade podem variar por edital. | Analisar editais reais. | Aberta |
| H-03 | A equipe necessita acompanhar manifestações em etapas/status. | Confirmar processo com NEI. | Aberta |
| H-04 | Coordenadores podem participar de etapas acadêmicas. | Confirmar responsabilidades e permissões. | Aberta |
| H-05 | Dados acadêmicos poderiam ser consultados por integração. | Avaliação com TI e responsáveis; sem presumir integração. | Aberta |
| H-06 | Estudantes podem preferir acesso mobile. | Teste de protótipo/questionário futuro. | Aberta |
| H-07 | Relatórios gerenciais precisam de indicadores específicos. | Levantar necessidades com responsáveis. | Aberta |

## 7. Roteiros preparados (não aplicados)

### 7.1 Equipe do NEI
1. Como uma oportunidade é recebida, cadastrada, revisada e publicada?
2. Quais informações são obrigatórias em cada edital?
3. Quem atualiza prazos, documentos e critérios?
4. Os critérios variam por edital, curso ou instituição?
5. Como o estudante demonstra interesse atualmente?
6. Quais etapas/status são utilizados para acompanhar candidaturas?
7. Como são solicitados documentos complementares?
8. Quais relatórios e indicadores são necessários?
9. Quais sistemas participam do processo e quais integrações seriam autorizadas?
10. Quais restrições de privacidade e acesso precisam ser consideradas?

### 7.2 Estudante
1. Onde procuraria oportunidades internacionais?
2. Quais informações precisa conhecer antes de demonstrar interesse?
3. Como gostaria de entender os critérios de elegibilidade?
4. Quais documentos e prazos são mais difíceis de acompanhar?
5. Como gostaria de acompanhar o andamento?
6. Quais avisos seriam úteis?
7. Quais recursos de preparação seriam mais relevantes?

### 7.3 Ex-intercambista
1. Como encontrou a oportunidade?
2. Quais etapas foram mais difíceis?
3. Quais informações gostaria de ter encontrado centralizadas?
4. Que orientações compartilharia com futuros participantes?

### 7.4 Coordenador de curso
1. Em quais etapas participa?
2. Quais informações acadêmicas precisa consultar?
3. Existem critérios específicos por curso?
4. Quais restrições de acesso devem ser respeitadas?

## 8. Registro de resultados

**Nenhuma entrevista ou questionário foi realizado/registrado nesta versão.** Esta seção só deverá ser preenchida após coleta real, sem atribuir respostas fictícias a participantes.

| Data | Técnica | Perfil | Resultado/achado | Requisitos afetados |
|---|---|---|---|---|
| A realizar | A definir | A definir | Sem resultados coletados | A definir |

## 9. Rastreabilidade inicial

| Evidência | Necessidade | Funcionalidades |
|---|---|---|
| EV-02, EV-07 | NEC-01 | F-01, F-02 |
| EV-03 | NEC-02, NEC-06 | F-03, F-04 |
| EV-04, EV-07 | NEC-05 | F-07, F-08, F-09, F-10, F-11, F-15 |
| EV-05 | NEC-07 | F-12 |
| EV-06 | NEC-07 | F-13 |
| EV-04 | NEC-08 | F-11 |
| EV-07 | NEC-03, NEC-04 | F-05, F-06, F-10 |
| EV-09 | NEC-01, NEC-05 | F-01, F-08 |
| EV-11 | NEC-02 | F-03 |
| EV-12 | NEC-05 | F-07, F-09 |
| EV-05 | NEC-07 | F-16 |
| EV-03, EV-07 | NEC-03 | F-18 |
| EV-06 | NEC-09 | F-17, F-19 |
