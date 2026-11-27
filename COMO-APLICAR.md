# Como aplicar este refino no repositório

Este pacote contém o conteúdo **completo e final** de `docs/`, `uml/` e `README.md`.

## Caminho recomendado

1. Clone o repositório (ou use seu clone atualizado):

   ```bash
   git clone https://github.com/AllisonOliv/requisitos-2026.2--grupo3
   cd requisitos-2026.2--grupo3
   git checkout -b refino-lapis
   ```

2. **Apague** as pastas antigas e o README:

   ```bash
   rm -rf docs uml README.md
   ```

   Isso remove, entre outros, os 11 arquivos duplicados que não eram referenciados pelo README
   (`01-documento-de-visao.md`, `02-stakeholders.md`, `03-analise-documental.md`, `03-entrevistas.md`,
   `04-requisitos.md`, `05-regras-de-negocio.md`, `06-backlog.md`, `07-casos-de-uso.md`,
   `08-glossario.md`, `09-fontes-e-decisoes.md` e o arquivo com o nome corrompido
   `03-analise-documental-e-elicita├º├úo.md`). O histórico do git preserva todos eles.

3. Extraia o conteúdo deste pacote na raiz do repositório.

4. Confira e faça o commit:

   ```bash
   git add -A
   git status
   git commit -m "Refino LAPIS: evidencias validadas, requisitos completados e UML grafico"
   git push -u origin refino-lapis
   ```

   Abrir um Pull Request facilita a revisão pelo grupo antes de ir para a `main`.

## O que mudou

| Mudança | Onde |
|---|---|
| Remoção de 11 arquivos duplicados ou órfãos | `docs/` |
| Nome de arquivo com acento corrigido | `docs/03-analise-documental-e-elicitacao.md` |
| Evidências EV-09 a EV-17 recuperadas e validadas contra o PDF e o Word originais | `docs/03-...` |
| Limite de interpretação declarado para cada evidência | `docs/03-...` |
| RF-21 a RF-24 (acesso, portfólio, aproveitamento de créditos, moderação) | `docs/04-...` |
| RNF-27 a RNF-29 (sessão e internacionalização) | `docs/05-...` |
| RN-18 a RN-20 (responsável pela moderação, identificação, limite do registro de créditos) | `docs/06-...` |
| Prioridades do backlog alinhadas com os RF, mais US-19 a US-22 | `docs/07-...` |
| CDU-15 a CDU-18 especificados no template de 16 seções | `docs/casos-de-uso/` |
| Casos de uso separados por módulo, no padrão do exemplo SINAIZ do LAPIS | `docs/casos-de-uso/` |
| NEC-09 e F-16 a F-19 no catálogo da Visão | `docs/01-...` |
| Diagramas de casos de uso, componentes e implantação em versão gráfica | `uml/*.svg`, `uml/png/` |
| IDs do UML alinhados com os CDU (antes eram UC01–UC14, fora de ordem) | `uml/diagramas.puml` |
| Fluxos de atividade corrigidos: autoavaliação não bloqueia candidatura (RN-04) e relato passa por moderação (RN-12) | `uml/atividade-*.svg` |

## Ainda em aberto

- SRS no padrão IEEE 830 (entregável 1 do P2).
- Wireframes e protótipo navegável (entregável 3 do P2, 1,0 ponto; e 0,5 na demonstração do pitch).
- Issues e milestones da disciplina no GitHub — use o script `criar-issues.sh`.
- Confirmar que o usuário **marcelobezerra-dotcom** é colaborador do repositório.
- Diagramas de Classes, Sequência e Estados, previstos nos entregáveis do PDF do projeto de extensão.
