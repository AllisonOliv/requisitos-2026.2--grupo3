# Especificação de Casos de Uso — ConectaGlobal

## Convenções
Estrutura baseada no template CDU do LAPIS. Atores primários iniciam o caso de uso; atores secundários apenas fornecem ou recebem informação. Login não é pré-condição genérica.

## CDU-01 — Consultar Catálogo de Programas
- **Objetivo:** permitir que o estudante visualize programas de internacionalização disponíveis no catálogo.
- **Tipo:** concreto.
- **Ator primário:** AT-01 Estudante da Unifor.
- **Ator secundário:** não se aplica.
- **Pré-condições:** catálogo disponível.
- **Fluxo principal:**
  1. O estudante acessa a página de programas.
  2. O sistema apresenta os programas publicados, com nome, categoria e resumo.
  3. O estudante seleciona um programa.
  4. O sistema apresenta a página de detalhes do programa.
- **Alternativo A1 — Catálogo sem resultados:** no passo 2, se não houver conteúdo publicado, o sistema informa que não há programas disponíveis no catálogo.
- **Pós-condição:** programa consultado ou lista vazia apresentada.
- **Requisitos:** RF-01, RNF-01, RNF-05.

## CDU-02 — Pesquisar e Filtrar Programas
- **Objetivo:** localizar programas por palavra-chave ou categoria.
- **Tipo:** concreto.
- **Ator primário:** AT-01 Estudante da Unifor.
- **Pré-condições:** catálogo disponível.
- **Fluxo principal:**
  1. O estudante informa uma palavra-chave ou seleciona uma categoria.
  2. O sistema consulta os registros do catálogo.
  3. O sistema apresenta os resultados correspondentes.
  4. O estudante seleciona um resultado para consultar detalhes.
- **Alternativo A1 — Nenhum resultado:** no passo 3, o sistema informa que não encontrou correspondências e permite limpar os filtros.
- **Pós-condição:** resultados filtrados apresentados.
- **Requisitos:** RF-02, RF-03.

## CDU-03 — Consultar Detalhes e Critérios de um Programa
- **Objetivo:** permitir que o estudante compreenda as informações publicadas sobre um programa.
- **Tipo:** concreto.
- **Ator primário:** AT-01 Estudante da Unifor.
- **Ator secundário:** AT-03 Portal oficial da DRI, como fonte acessada por link externo.
- **Pré-condições:** programa cadastrado no catálogo.
- **Fluxo principal:**
  1. O estudante seleciona um programa.
  2. O sistema apresenta descrição, modalidade e público-alvo disponíveis.
  3. O sistema apresenta os critérios publicados para aquele programa.
  4. O sistema apresenta documentos e providências descritos pela fonte.
  5. O sistema apresenta a fonte e a data de consulta.
  6. O estudante consulta as informações.
- **Alternativo A1 — Critério não publicado:** no passo 3, o sistema informa que o critério não foi localizado na fonte e orienta consultar o edital/DRI.
- **Alternativo A2 — Documento depende do edital:** no passo 4, o sistema informa que a lista pode variar e aponta a fonte específica.
- **Pós-condição:** informações do programa apresentadas.
- **Requisitos:** RF-04, RF-05, RF-06, RF-09, RF-10; RNF-05, RNF-08.

## CDU-04 — Consultar Próximos Passos e Acessar Canal Oficial
- **Objetivo:** orientar o estudante sobre os próximos passos publicados e encaminhá-lo à DRI.
- **Tipo:** concreto.
- **Ator primário:** AT-01 Estudante da Unifor.
- **Ator secundário:** AT-03 Portal oficial da DRI.
- **Pré-condições:** programa possui orientação pública ou contato oficial associado.
- **Fluxo principal:**
  1. O estudante acessa a seção de etapas do programa.
  2. O sistema apresenta as etapas documentadas.
  3. O sistema informa quando o estudante deve procurar a DRI.
  4. O estudante seleciona o link oficial.
  5. O navegador abre a página de destino da DRI.
- **Alternativo A1 — Link indisponível:** no passo 4, o sistema informa que o endereço deve ser conferido no portal principal da DRI.
- **Pós-condição:** estudante encaminhado à fonte oficial ou orientado a acessá-la manualmente.
- **Requisitos:** RF-07, RF-08.

## CDU-05 — Manter Conteúdo Informativo do Protótipo
- **Objetivo:** manter os registros demonstrativos utilizados no protótipo acadêmico.
- **Tipo:** concreto.
- **Ator primário:** AT-02 Responsável editorial do ConectaGlobal.
- **Pré-condições:** responsável possui acesso ao ambiente de demonstração.
- **Fluxo principal:**
  1. O responsável seleciona a opção de manutenção de conteúdo.
  2. O sistema apresenta os registros existentes.
  3. O responsável cria ou seleciona um registro.
  4. O responsável informa título, resumo, categoria, conteúdo, URL da fonte e data de consulta.
  5. O sistema verifica os campos obrigatórios.
  6. O sistema salva o registro como rascunho ou publicado, conforme a opção selecionada.
- **Alternativo A1 — Campo obrigatório ausente:** no passo 5, o sistema destaca o campo e solicita correção.
- **Pós-condição:** conteúdo demonstrativo atualizado.
- **Observação:** este ator e fluxo pertencem ao protótipo acadêmico; não afirmam que a DRI adotará ou operará o sistema.
- **Requisitos:** RF-11.

## Regras aplicáveis
- RI-01 a RI-08: regras institucionais documentadas, exibidas apenas no contexto do programa a que a fonte se refere.
- RP-01 a RP-07: regras do produto em `docs/05-regras-de-negocio.md`.
