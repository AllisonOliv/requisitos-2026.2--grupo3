# Documento de Visão — ConectaGlobal

**Projeto:** ConectaGlobal — Sistema de Gestão de Oportunidades Internacionais  
**Disciplina:** Requisitos e Modelagem de Sistemas — Unifor, 2026.2  
**Versão:** 2.1 — revisão para continuidade à P2

## 1. Objetivo
Especificar uma solução web/mobile para apoiar a gestão da mobilidade acadêmica internacional, tornando mais acessível e organizado o ciclo de oportunidades, preparação, candidatura, acompanhamento e atividades pós-intercâmbio.

## 2. Contexto, problema e descrição sumária
A documentação-base descreve a necessidade de centralizar e tornar mais transparente o processo de mobilidade acadêmica internacional. Estudantes precisam localizar oportunidades, compreender critérios, preparar documentos e acompanhar candidaturas. A equipe do NEI precisa apoiar a gestão de oportunidades, convênios, bolsas e candidaturas.

O ConectaGlobal é proposto como ambiente integrado para esses processos. Esta visão representa uma proposta acadêmica; não afirma que os fluxos internos descritos já estejam implantados na instituição.

## 3. Proposta de valor e sucesso
- Centralizar oportunidades, editais, bolsas, destinos e requisitos.
- Facilitar a autoavaliação inicial de elegibilidade.
- Organizar documentos e preparação do candidato.
- Permitir acompanhamento do andamento da candidatura.
- Apoiar o NEI na gestão de oportunidades, convênios, candidaturas e relatórios.
- Incentivar integração, troca de experiências e apoio entre estudantes.

Indicadores propostos: oportunidades cadastradas e atualizadas; candidaturas acompanhadas; pendências documentais identificadas; utilização dos recursos de preparação; participação em atividades colaborativas.

## 4. Partes interessadas
- Estudantes interessados em mobilidade internacional.
- Equipe do Núcleo de Estratégias Internacionais (NEI).
- Coordenadores de curso.
- Professores envolvidos em cooperação internacional.
- Estudantes estrangeiros recebidos pela Unifor.
- Ex-participantes de mobilidade.
- Equipe acadêmica responsável pela especificação do projeto.
- Docente da disciplina.

## 5. Usuários e atores externos
- **Estudante:** consulta oportunidades, verifica requisitos, prepara candidatura e acompanha seu processo.
- **Equipe do NEI:** gerencia oportunidades, convênios, bolsas, candidaturas, comunicações e relatórios.
- **Coordenador de curso:** acompanha estudantes vinculados ao curso e apoia aspectos acadêmicos da mobilidade.
- **Professor:** participa de ações de cooperação, orientação e atividades internacionais, conforme permissões definidas.
- **Estudante estrangeiro recebido:** acessa informações e recursos de integração destinados a incoming students.
- **Ex-intercambista:** compartilha relatos e pode atuar em mentoria.
- **Administrador do sistema:** mantém contas, perfis e parâmetros técnicos da solução.

## 6. Escopo e entregas previstas

### 6.1 Módulo do estudante
- Portal unificado de oportunidades, com filtros por país, área e duração.
- Autoavaliação inicial de elegibilidade.
- Central de preparação com recursos sobre idiomas, cultura e planejamento financeiro.
- Portfólio digital e acompanhamento da candidatura.
- Consulta de documentos e pendências.

### 6.2 Módulo de gestão (NEI)
- Gestão de convênios e instituições parceiras.
- Cadastro e divulgação de editais, oportunidades e bolsas.
- Painel de candidaturas e apoio à análise.
- Gestão de notificações.
- Relatórios sobre perfil dos candidatos e destinos procurados.

### 6.3 Módulo pós-intercâmbio
- Relatos de experiência.
- Rede de ex-participantes e mentoria.
- Registro de informações relacionadas ao aproveitamento de créditos, sem presumir integração automática com sistema acadêmico.

### 6.4 Módulo colaborativo
- Tandem para troca de idiomas.
- Agenda de eventos, workshops e palestras.
- Fórum de dúvidas e orientações sobre processos.

### 6.5 Fora do escopo confirmado nesta etapa
- Integrações automáticas com sistemas institucionais, bases acadêmicas ou plataformas de terceiros.
- Decisões oficiais de seleção ou concessão de bolsas tomadas exclusivamente por algoritmo.
- Processamento financeiro, emissão de vistos ou contratação de seguros.
- Operação institucional real: o produto é especificado academicamente.

## 7. Necessidades e catálogo inicial de funcionalidades
- **NEC-01:** localizar oportunidades internacionais adequadas ao perfil e interesse do estudante.
- **NEC-02:** compreender critérios, prazos e documentos necessários.
- **NEC-03:** organizar preparação e candidatura.
- **NEC-04:** acompanhar o andamento e as pendências da candidatura.
- **NEC-05:** permitir ao NEI administrar oportunidades, convênios, bolsas e candidaturas.
- **NEC-06:** apoiar preparação linguística, cultural e financeira.
- **NEC-07:** promover troca de experiências, mentoria e integração.
- **NEC-08:** oferecer visão gerencial por relatórios.

## 8. Visão geral da solução e impactos
A solução é organizada em módulos integrados, com perfis de acesso distintos. A arquitetura lógica deverá separar interface, serviços de negócio e persistência. A especificação detalhada de tecnologia, integrações e políticas de segurança será consolidada na P2.

## 9. Condições gerais
- Requisitos de elegibilidade devem ser configuráveis por oportunidade, pois podem variar conforme edital.
- A autoavaliação é indicativa e não substitui análise responsável.
- Dados pessoais e documentos de candidatura devem receber proteção compatível com a LGPD.
- O NEI é mantido como ator conforme a documentação-base.
- A DRI não é ator, stakeholder nem integração nesta modelagem.

## 10. Riscos e questões em aberto
- Critérios e documentos variam entre oportunidades.
- Necessidade de definir níveis de acesso e responsáveis por cada etapa.
- Necessidade de detalhar estados e transições das candidaturas.
- Integrações futuras dependem de autorização, acesso e análise de viabilidade.
- Recursos colaborativos exigem regras de moderação e privacidade.

## 11. Documentos relacionados
- Material de projeto de extensão — Internacionalização, Unifor, 2026.2.
- Propostas de Projetos de Sistemas — Internacionalização e ENADE, Unifor, 2026.2.
- Artefatos LAPIS usados como referência metodológica.

## 12. Situação da visão
Documento-base revisado para manter a proposta de Gestão de Oportunidades Internacionais. A equipe deverá detalhar e priorizar os requisitos na SRS da P2. Não se declara validação institucional ou entrevista não realizada.
