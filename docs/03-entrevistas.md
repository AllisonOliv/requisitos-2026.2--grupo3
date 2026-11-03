# 3. Roteiro e Resultados de Entrevistas

> **Status (03/11/2026):** o professor Marcelo informou que as entrevistas **não precisam ser realizadas por enquanto**. Os roteiros abaixo seguem prontos para quando forem liberadas. A análise documental (3.2) foi executada com o material já disponível da disciplina. Nenhuma resposta ou achado de entrevista foi inventado — a seção 3.9 (registro de resultados) continua vazia até a coleta real acontecer, e os requisitos hoje marcados **[H]** serão confirmados, ajustados ou descartados quando isso ocorrer.

## 3.1 Técnicas de elicitação planejadas

| Técnica | Público | Objetivo | Situação |
|---|---|---|---|
| Entrevista com o professor (orientador) | Prof. Marcelo | Validar o recorte do projeto e o formato esperado das entregas | Dispensada por ora |
| Entrevista semiestruturada | Equipe NEI/DRI | Entender processo atual, regras de elegibilidade e rotina de atualização | Dispensada por ora |
| Entrevista individual | Estudante interessado em intercâmbio | Entender como busca informações e avalia sua elegibilidade | Dispensada por ora |
| Entrevista individual | Estudante que já voltou de intercâmbio (ex-intercambista) | Entender dificuldades reais já vividas no processo | Dispensada por ora |
| Entrevista curta | Coordenador de curso | Critérios acadêmicos e acompanhamento | Dispensada por ora |
| Questionário online | Estudantes em geral | Validar hipóteses em maior escala | Pendente |
| Análise documental | Material da disciplina (apresentação e documento de propostas) | Extrair regras e campos existentes | **Executada — ver 3.2** |
| Prototipação (próximas sprints) | NEI/DRI e alunos | Validar telas | Próxima sprint |

## 3.2 Análise documental (executada)

**Fontes:** apresentação "Projeto de Extensão — Internacionalização" (disciplina Requisitos e Modelagem de Sistemas) e documento "Propostas de Projetos de Sistemas — Internacionalização e ENADE" (semestre 2026.2). Um edital real do NEI/DRI ainda **não** foi obtido — ver limitação ao final desta seção.

**Achados [D]:**
- A Unifor mantém convênios com mais de 140 instituições em 30 países (apresentação da disciplina).
- Pesquisa Selo Belta citada na apresentação: 28,6% dos estudantes pretendiam viajar em 2024; 21% planejavam intercâmbio a partir de 2025. Indica demanda, mas não mede diretamente o problema de dispersão de informação investigado aqui.
- Critério de elegibilidade citado no slide "Requisitos de Elegibilidade" da apresentação: matrícula ativa, 30%–70% do curso concluído, média ≥ 7,0, sem reprovações. Usado como base de RN06 e RF04 — ainda **[H]**, pois o material não esclarece se é um critério institucional único ou varia por edital/instituição parceira.
- O documento de propostas descreve o escopo inicial do Tema 3 como "cadastro e divulgação de editais, oportunidades de bolsas, requisitos, prazos, documentação necessária e acompanhamento de manifestações de interesse" — usado diretamente para delimitar o MVP do Documento de Visão (seção 1.5).
- O mesmo documento já aponta, como questões a investigar, exatamente os pontos que viraram premissas e riscos do projeto: "critérios de elegibilidade, responsáveis pela atualização e integração com processos institucionais" (ver P2/P3 e RS3 no Documento de Visão).

**Limitação assumida [H]:** os campos reais de um edital de mobilidade (layout, linguagem, campos obrigatórios) ainda não foram extraídos de um documento primário do NEI/DRI — RF01 e RF05 seguem baseados no material da disciplina, não em um edital real. Tratar como hipótese até acesso a um exemplo concreto.

## 3.3 Roteiro 00 — Professor (orientador da disciplina)
*~20 min. Objetivo: validar o recorte do projeto antes de aprofundar o levantamento.*

**Recorte do projeto**
1. Escolhemos o tema 3 (Gestão de Oportunidades Internacionais). O recorte em editais, bolsas, prazos, documentos e manifestação de interesse está dentro do esperado?
2. O senhor recomenda restringir ou ampliar algo? Os módulos de pós-intercâmbio e colaborativo do PPT devem ficar de fora desta fase?

**Acesso ao NEI/DRI e aos estudantes**
3. É possível indicar um contato no NEI/DRI para agendar a entrevista, ou devemos buscar por conta própria?
4. Há restrições de acesso a dados de estudantes ou editais (LGPD, sigilo) que devemos observar?

**Entregas e avaliação**
5. O formato do Documento de Visão, requisitos e diagramas atende ao esperado? Há modelo institucional a seguir?
6. Qual critério o senhor recomenda priorizar nesta fase?
7. Existe uma data limite para a conclusão das entrevistas com o NEI/DRI e os estudantes?
8. O NEI/DRI é o mesmo setor? (O PPT usa "NEI" e o material de propostas usa "DRI".)

## 3.4 Roteiro 01 — Equipe do NEI/DRI
*~40 min, semiestruturada.*

**Abertura**
1. Como funciona hoje, passo a passo, a divulgação de um edital ou bolsa de mobilidade?
2. Quantas manifestações de interesse ou candidaturas vocês recebem, em média, por edital?

**Processo atual e canais**
3. Quais canais são usados (site, e-mail, redes sociais, murais, WhatsApp)? Qual deles gera mais dúvidas?
4. Que informações todo edital precisa conter? Existe um modelo padrão?
5. Quem atualiza as informações e com que frequência?

**Elegibilidade**
6. Quais critérios de elegibilidade existem? Variam por edital, curso ou destino?
7. Como a elegibilidade é verificada hoje? Quem faz e com que fonte de dados?
8. Há critérios de idioma? Como são comprovados?

**Manifestação de interesse e acompanhamento**
9. Como o estudante demonstra interesse hoje (formulário, e-mail, atendimento)?
10. Como vocês acompanham cada candidatura e informam o status ao aluno?
11. Como as bolsas divulgadas são controladas (valor, vigência, fonte)?

**Relatórios, integrações e restrições**
12. Que relatório ou indicador falta hoje e seria útil (destinos mais procurados, taxa de aprovação por curso)?
13. Quais sistemas institucionais já são usados (acadêmico, protocolo, e-mail)? Seria possível integrar?
14. Há restrições de proteção de dados ou política institucional que devemos conhecer?

**Fechamento**
15. O que seria indispensável nesse sistema? O que seria "bom ter"?
16. Se pudessem resolver um único problema do processo atual, qual seria?
17. Há mais alguém da equipe que devemos entrevistar?

## 3.5 Roteiro 02 — Estudante interessado em intercâmbio
*~25 min, individual.*
1. Você já considerou fazer intercâmbio pela Unifor? O que te motivou ou te afastou?
2. Onde você buscaria (ou buscou) informações sobre prazos, requisitos e documentos?
3. Já perdeu algum prazo ou desistiu por falta de informação? Conte como foi.
4. Você saberia dizer hoje se é elegível? Como descobriria?
5. Que dúvidas você imagina que teria durante a candidatura?
6. Como gostaria de acompanhar o andamento depois de manifestar interesse?
7. Prefere usar celular ou computador? Quer ser avisado por e-mail, push ou WhatsApp?
8. O que tornaria esse processo mais simples?

## 3.6 Roteiro 03 — Ex-intercambista
*~25 min, individual.*
1. Como foi, em geral, seu processo de candidatura e preparação?
2. Quais etapas foram mais difíceis de acompanhar ou entender?
3. Como descobriu os requisitos e documentos? Faltou alguma informação importante?
4. Como foi acompanhar o resultado da sua candidatura?
5. Que informação você gostaria de ter tido antes e não teve?
6. Você recomendaria o processo a um colega hoje? Por quê?

## 3.7 Roteiro 04 — Coordenador de curso
1. Como você é informado sobre alunos do curso em mobilidade?
2. Existem critérios acadêmicos próprios do curso para liberar um aluno?
3. Que informações gostaria de acompanhar no sistema?
4. Quais prazos do calendário acadêmico impactam a mobilidade?

## 3.8 Mini-questionário (online, ~3 min)
1. Curso e semestre
2. Você já pensou em fazer intercâmbio? (sim / não / já fiz)
3. Onde procura informações sobre oportunidades? (site Unifor, e-mail, Instagram, colegas, NEI/DRI presencial, outro)
4. Já perdeu prazo ou desistiu por falta de informação? (sim / não)
5. Qual a maior dificuldade? (achar editais / entender requisitos / saber se sou elegível / reunir documentos / acompanhar status / outra)
6. Qual funcionalidade seria mais útil? (alerta de prazo / filtro por destino / verificação de elegibilidade / checklist de documentos / acompanhamento de status)
7. Como prefere ser avisado? (e-mail / push / WhatsApp)
8. Usaria mais no celular ou no computador?

## 3.9 Registro de resultados (preencher após a coleta)

### Entrevista 1
- **Entrevistado / papel:** _______
- **Data / duração / formato:** _______
- **Principais achados:** _______
- **Requisitos novos ou alterados:** _______
- **Hipóteses confirmadas / refutadas:** _______

*(copiar o bloco para cada entrevista)*

### Questionário
- **Nº de respostas:** _____
- **Resumo por pergunta:** _____
- **Impacto no backlog:** _____

## 3.10 Hipóteses a validar

| ID | Hipótese | Origem | Pergunta que valida | Status |
|---|---|---|---|---|
| H1 | Informações sobre editais estão dispersas em vários canais | Análise do problema | NEI 3; Aluno 2; Quest. 3 | Pendente |
| H2 | Estudantes perdem prazos por falta de alertas | Hipótese da equipe | Aluno 3; Quest. 4 | Pendente |
| H3 | Critérios de elegibilidade variam por edital | Material da disciplina | NEI 6 | Pendente |
| H4 | Elegibilidade padrão: 30–70% concluído, média ≥ 7,0, sem reprovações | Apresentação da disciplina | NEI 6–7 | Pendente |
| H5 | O acompanhamento das manifestações é manual | Hipótese da equipe | NEI 9–10 | Pendente |
| H6 | É possível integrar com o sistema acadêmico | Hipótese da equipe | NEI 13 | Pendente |
| H7 | Estudantes preferem acessar pelo celular | Hipótese da equipe | Aluno 7; Quest. 8 | Pendente |
| H8 | O estudante tem dúvida sobre a própria elegibilidade antes de se inscrever | Análise do problema | Aluno 4; Ex-interc. 3 | Pendente |
| H9 | Falta retorno claro do status após manifestar interesse | Análise do problema | Aluno 6; Ex-interc. 4; NEI 10 | Pendente |
| H10 | Faltam relatórios consolidados (destinos, aprovação por curso) | Análise do problema | NEI 12 | Pendente |
