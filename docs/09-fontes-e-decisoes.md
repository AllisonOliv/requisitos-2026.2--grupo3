# Fontes, premissas e decisões — ConectaGlobal

## 1. Fontes

| ID | Fonte | Uso |
|---|---|---|
| FON-01 | Material de Projeto de Extensão — Internacionalização, Unifor, 2026.2 | Fonte principal de contexto, objetivo, módulos, atores e funcionalidades sugeridas. |
| FON-02 | Propostas de Projetos de Sistemas — Internacionalização e ENADE, Unifor, 2026.2 | Fundamenta o recorte Gestão de Oportunidades Internacionais. |
| FON-03 | Repositório LAPIS | Referência metodológica para estruturar visão, requisitos, regras e casos de uso. |

## 2. Premissas de projeto
- O sistema é uma proposta acadêmica de gestão da mobilidade internacional.
- O NEI permanece como ator do módulo de gestão, conforme documentação-base.
- Estudantes são usuários centrais do módulo de oportunidades e candidaturas.
- Critérios variam por edital e oportunidade.
- Autoavaliação não equivale à decisão oficial de seleção.
- Recursos pós-intercâmbio e colaborativos fazem parte da visão ampla apresentada no material-base; sua priorização de implementação será decidida na P2.

## 3. Decisões de modelagem
| ID | Decisão | Justificativa |
|---|---|---|
| DP-01 | Manter quatro módulos: estudante, gestão (NEI), pós-intercâmbio e colaborativo. | Preserva a estrutura do material-base. |
| DP-02 | Representar NEI como ator “Equipe do NEI”. | Preserva o ator organizacional expresso na proposta. |
| DP-03 | Tratar autoavaliação como indicativa. | Evita confundir apoio automatizado com decisão oficial. |
| DP-04 | Configurar requisitos por oportunidade. | Critérios e documentos podem variar por edital. |
| DP-05 | Não presumir integrações automáticas. | Integrações dependem de autorização, acesso e viabilidade. |
| DP-06 | Detalhar estados da candidatura na P2. | A documentação-base não define o fluxo completo de status. |
| DP-07 | Manter módulos colaborativo e pós-intercâmbio na visão, priorizando o núcleo de gestão na primeira entrega funcional. | Preserva a visão e permite planejamento incremental. |
| DP-08 | Consultar a DRI somente como referência visual durante a elaboração das telas. | Orientação expressa para a etapa de wireframes/protótipo; não define atores, requisitos ou integrações. |

## 4. Limites
Este documento não declara entrevistas, validações, aprovações institucionais ou integrações técnicas que não tenham sido confirmadas. Funcionalidades detalhadas nesta revisão são uma especificação acadêmica derivada do escopo proposto e deverão ser refinadas na SRS da P2.
