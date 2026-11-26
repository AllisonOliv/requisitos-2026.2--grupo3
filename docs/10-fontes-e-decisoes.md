# Fontes, Premissas e Decisões — ConectaGlobal

## 1. Fontes

| ID | Fonte | Uso |
|---|---|---|
| AD-01 | Material de Projeto de Extensão — Internacionalização, Unifor, 2026.2 | Contexto, objetivo, módulos, atores e funcionalidades sugeridas. |
| AD-02 | Propostas de Projetos de Sistemas — Internacionalização e ENADE, Unifor, 2026.2 | Fundamenta o recorte Gestão de Oportunidades Internacionais. |
| AD-03 | Repositório LAPIS | Estrutura metodológica e templates dos artefatos. |
| AD-04 | Portal público DRI/Unifor | Referência visual futura para wireframes e protótipo, sem derivar requisitos. |

## 2. Premissas e limites

- O sistema é uma proposta acadêmica de gestão da mobilidade internacional.
- O NEI permanece como ator do módulo de gestão.
- Os quatro módulos permanecem na visão do produto.
- Critérios e documentos podem variar por oportunidade.
- Autoavaliação não equivale à decisão oficial de seleção.
- Integrações não são presumidas.
- Entrevistas não foram realizadas nesta etapa e não há resultados fictícios.
- A DRI será consultada apenas como referência visual durante a criação das telas.

## 3. Decisões de modelagem

| ID | Decisão | Justificativa |
|---|---|---|
| DP-01 | Manter os módulos estudante, gestão (NEI), pós-intercâmbio e colaborativo. | Preserva a estrutura da documentação-base. |
| DP-02 | Representar NEI como ator AT-02 — Equipe do NEI. | Preserva ator organizacional expresso na proposta. |
| DP-03 | Tratar autoavaliação como indicativa. | Evita confundir apoio automatizado com decisão oficial. |
| DP-04 | Associar critérios à oportunidade correspondente. | Evita generalizar critérios de um edital. |
| DP-05 | Não presumir integração automática com sistemas institucionais. | Depende de autorização, acesso e viabilidade. |
| DP-06 | Detalhar estados e transições da candidatura na P2. | A documentação-base não define fluxo completo. |
| DP-07 | Manter módulos pós-intercâmbio e colaborativo na visão. | Preserva o escopo amplo documentado. |
| DP-08 | Usar DRI somente como referência visual para as telas. | Orientação do projeto; não define atores, requisitos ou integrações. |
| DP-09 | Usar LAPIS como padrão estrutural dos artefatos aplicáveis. | Assegura padronização metodológica e rastreabilidade. |

## 4. Referências metodológicas

- Guia LAPIS de elaboração da Visão da Demanda: `Requisitos/Elicitacao/VisaoDemanda.md`.
- Template Visão da Demanda v2.1: `Requisitos/Artefatos/Templates/template-visao-demanda.md`.
- Template de Caso de Uso: `template-cdu-caso-uso.md`.
- Template de Regra de Negócio: `template-rn-regra-negocio.md`.
- Template de Requisitos Não Funcionais: `template-requisitosNaoFuncionais.md`.
- Template de Glossário: `template-glossario.md`.

Repositório: https://github.com/marcelobezerra-dotcom/Lapis-unifor

## 5. Limites

Este conjunto de documentos não declara entrevistas, validações, aprovações institucionais ou integrações técnicas não confirmadas. A SRS deverá detalhar os requisitos e resolver as pendências identificadas, sem transformar hipóteses em fatos.
