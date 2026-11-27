# ConectaGlobal — Sistema de Gestão de Oportunidades Internacionais

Projeto acadêmico da disciplina **Requisitos e Modelagem de Sistemas** — Universidade de Fortaleza, 2026.2.

Proposta de sistema web/mobile para apoiar a gestão da mobilidade acadêmica internacional, alinhada às diretrizes do Núcleo de Estratégias Internacionais (NEI) da Unifor. Tema escolhido: **Gestão de Oportunidades Internacionais** (Tema 3 do documento de propostas).

---

## Artefatos de requisitos

| # | Artefato | Arquivo |
|---|---|---|
| 01 | Visão da Demanda — template LAPIS v2.1 | [docs/01-visao-da-demanda.md](docs/01-visao-da-demanda.md) |
| 02 | Partes interessadas e atores | [docs/02-partes-interessadas-e-atores.md](docs/02-partes-interessadas-e-atores.md) |
| 03 | Análise documental e elicitação | [docs/03-analise-documental-e-elicitacao.md](docs/03-analise-documental-e-elicitacao.md) |
| 04 | Requisitos funcionais | [docs/04-requisitos-funcionais.md](docs/04-requisitos-funcionais.md) |
| 05 | Requisitos não funcionais | [docs/05-requisitos-nao-funcionais.md](docs/05-requisitos-nao-funcionais.md) |
| 06 | Regras de negócio | [docs/06-regras-de-negocio.md](docs/06-regras-de-negocio.md) |
| 07 | Backlog priorizado | [docs/07-backlog.md](docs/07-backlog.md) |
| 08 | Casos de uso — índice e especificações por módulo | [docs/08-casos-de-uso.md](docs/08-casos-de-uso.md) · [docs/casos-de-uso/](docs/casos-de-uso/README.md) |
| 09 | Glossário | [docs/09-glossario.md](docs/09-glossario.md) |
| 10 | Fontes, premissas e decisões | [docs/10-fontes-e-decisoes.md](docs/10-fontes-e-decisoes.md) |
| — | Diagramas UML | [uml/diagramas.md](uml/diagramas.md) |

## Diagramas UML

Todos em SVG (visualização direta no GitHub), PNG (`uml/png/`, para slides) e PlantUML (fonte editável).

| Diagrama | Abrir |
|---|---|
| Casos de uso | [uml/casos-de-uso.svg](uml/casos-de-uso.svg) |
| Componentes | [uml/componentes.svg](uml/componentes.svg) |
| Implantação | [uml/implantacao.svg](uml/implantacao.svg) |
| Atividades — candidatura, gestão NEI e pós-intercâmbio | [uml/diagramas.md](uml/diagramas.md) |

Os identificadores dos diagramas são os mesmos dos casos de uso (CDU-01 a CDU-18), permitindo rastrear cada elemento até o requisito funcional e a regra de negócio correspondentes.

---

## Rastreabilidade

A cadeia de rastreabilidade do projeto liga, em ambos os sentidos:

```
Evidência documental (EV)  →  Necessidade (NEC)  →  Funcionalidade (F)
        →  Requisito funcional (RF)  →  Caso de uso (CDU)  →  Diagrama UML
                     ↘  Regra de negócio (RN)  ↘  Requisito não funcional (RNF)
                                    ↘  História de usuário (US)
```

As matrizes estão em [docs/03-analise-documental-e-elicitacao.md](docs/03-analise-documental-e-elicitacao.md) (seção 9) e nas colunas de referência de cada artefato.

---

## Padrão metodológico

Os artefatos seguem o processo e os templates do repositório LAPIS: <https://github.com/marcelobezerra-dotcom/Lapis-unifor>

A Visão da Demanda segue as 12 seções do template LAPIS v2.1. Casos de uso, regras de negócio, requisitos não funcionais e glossário seguem as estruturas correspondentes. Os casos de uso são organizados por módulo, como no exemplo SINAIZ do repositório LAPIS. Backlog e UML são artefatos complementares e mantêm rastreabilidade com os requisitos.

## Escopo

A proposta mantém os quatro módulos identificados na documentação-base:

1. **Estudante** — oportunidades, elegibilidade, preparação, portfólio, candidatura e acompanhamento;
2. **Gestão (NEI)** — convênios, bolsas, editais, análise de candidaturas, notificações e relatórios;
3. **Pós-intercâmbio** — relatos, mentoria e aproveitamento de créditos;
4. **Colaborativo** — Tandem, eventos, fórum, integração de estudantes recebidos e moderação.

O núcleo do recorte escolhido (Tema 3) corresponde ao cadastro e divulgação de editais, bolsas, requisitos, prazos e documentação, com acompanhamento das manifestações de interesse. Os módulos pós-intercâmbio e colaborativo são preservados por constarem do escopo do projeto de extensão.

O NEI permanece como ator. A DRI não é ator, parte interessada, integração nem fonte de requisitos do produto: será consultada somente como referência visual quando forem elaboradas as telas.

## Critério de confiabilidade

O documento de propostas afirma que as descrições "não constituem requisitos validados nem pressupõem que os sistemas propostos já existam". Em consonância:

- Conteúdo da documentação-base é identificado como fonte, com o limite de cada evidência registrado.
- Detalhamentos necessários à modelagem são identificados como decisões acadêmicas de especificação.
- Informações não confirmadas permanecem como hipótese, pendência ou "A definir".
- Não são declaradas entrevistas, validações institucionais, aprovações ou integrações não realizadas.

Conforme orientação informada para a etapa, entrevistas com stakeholders não foram exigidas; os roteiros estão preparados e registrados, sem resultados fictícios.

---

## Estado das entregas

| Sprint | Entrega | Situação |
|---|---|---|
| M1 — Elicitação e UML | Visão, stakeholders, elicitação, requisitos, regras, backlog e UML (casos de uso, componentes, implantação) | Entregue |
| M2 — Especificação e Protótipo | SRS (IEEE 830), revisão de consistência UML × requisitos, wireframes e protótipo navegável | Em andamento |
| M3 — Pitch | Slides e apresentação final | Em andamento |

## Equipe

Allison de Oliveira Girão · Maria Rafaele Gomes de Araújo
