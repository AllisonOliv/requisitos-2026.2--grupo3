# Casos de uso — ConectaGlobal

## CDU-01 — Consultar oportunidades internacionais
- **Ator primário:** Estudante.
- **Objetivo:** localizar oportunidades de mobilidade disponíveis.
- **Pré-condições:** existem oportunidades cadastradas e publicadas.
- **Fluxo principal:**
  1. Estudante acessa a área de oportunidades.
  2. Sistema apresenta oportunidades publicadas.
  3. Estudante seleciona uma oportunidade.
  4. Sistema apresenta detalhes, destino, modalidade e prazo.
- **Alternativas:** se não houver oportunidades, sistema informa ausência de resultados.
- **Pós-condição:** oportunidade consultada.
- **Requisitos:** RF-01, RF-02, RF-03.

## CDU-02 — Verificar elegibilidade inicial
- **Ator primário:** Estudante.
- **Objetivo:** comparar informações do estudante com critérios de uma oportunidade.
- **Pré-condições:** oportunidade possui critérios cadastrados.
- **Fluxo principal:**
  1. Estudante seleciona a autoavaliação.
  2. Sistema apresenta os critérios aplicáveis.
  3. Estudante informa os dados solicitados.
  4. Sistema compara os dados com os critérios.
  5. Sistema apresenta resultado indicativo e ressalva de análise.
- **Alternativas:** dados incompletos; sistema solicita complementação.
- **Pós-condição:** resultado indicativo apresentado.
- **Requisitos:** RF-04.

## CDU-03 — Registrar candidatura
- **Ator primário:** Estudante.
- **Objetivo:** registrar interesse ou candidatura em uma oportunidade.
- **Pré-condições:** oportunidade publicada e dentro do prazo; estudante autenticado.
- **Fluxo principal:**
  1. Estudante seleciona a oportunidade.
  2. Sistema apresenta condições e documentos exigidos.
  3. Estudante confirma interesse e preenche os dados solicitados.
  4. Sistema valida campos obrigatórios.
  5. Sistema registra a candidatura.
  6. Sistema confirma o registro e apresenta o status inicial.
- **Alternativas:** prazo encerrado; dados obrigatórios ausentes; sistema informa o impedimento.
- **Pós-condição:** candidatura registrada.
- **Requisitos:** RF-06, RF-07.

## CDU-04 — Acompanhar candidatura
- **Ator primário:** Estudante.
- **Objetivo:** consultar status, histórico e pendências.
- **Pré-condições:** estudante possui candidatura registrada.
- **Fluxo principal:**
  1. Estudante acessa suas candidaturas.
  2. Sistema lista candidaturas vinculadas.
  3. Estudante seleciona uma candidatura.
  4. Sistema apresenta status, histórico, prazos e pendências.
- **Pós-condição:** informações de acompanhamento exibidas.
- **Requisitos:** RF-07, RF-08, RF-13.

## CDU-05 — Gerenciar oportunidades
- **Ator primário:** Equipe do NEI.
- **Objetivo:** manter oportunidades e editais disponíveis no sistema.
- **Pré-condições:** usuário do NEI autenticado e autorizado.
- **Fluxo principal:**
  1. Usuário acessa a gestão de oportunidades.
  2. Sistema apresenta registros existentes.
  3. Usuário cadastra ou seleciona uma oportunidade.
  4. Usuário informa descrição, destino, modalidade, requisitos e prazo.
  5. Sistema valida os dados.
  6. Usuário publica, atualiza, suspende ou encerra a oportunidade.
  7. Sistema registra a operação.
- **Alternativas:** dados inválidos; sistema informa os campos a corrigir.
- **Pós-condição:** oportunidade atualizada conforme ação.
- **Requisitos:** RF-09.

## CDU-06 — Gerenciar convênios e bolsas
- **Ator primário:** Equipe do NEI.
- **Objetivo:** manter instituições parceiras, convênios e bolsas.
- **Pré-condições:** usuário autorizado.
- **Fluxo principal:**
  1. Usuário acessa a área de gestão.
  2. Sistema apresenta registros.
  3. Usuário cadastra ou seleciona instituição, convênio ou bolsa.
  4. Usuário informa ou altera dados.
  5. Sistema valida e salva as informações.
- **Pós-condição:** registro atualizado.
- **Requisitos:** RF-10.

## CDU-07 — Analisar candidatura
- **Ator primário:** Equipe do NEI.
- **Ator secundário:** Coordenador de curso, quando aplicável.
- **Objetivo:** consultar dados e registrar andamento da análise.
- **Pré-condições:** candidatura registrada.
- **Fluxo principal:**
  1. Usuário do NEI acessa o painel de candidaturas.
  2. Sistema apresenta candidaturas conforme permissões.
  3. Usuário seleciona uma candidatura.
  4. Sistema apresenta dados e documentos disponíveis.
  5. Usuário registra observação e atualiza o status.
  6. Sistema registra responsável, data e novo status.
- **Alternativas:** documentação pendente; usuário registra pendência para o estudante.
- **Pós-condição:** análise e status atualizados.
- **Requisitos:** RF-11, RF-12, RF-13.

## CDU-08 — Consultar relatórios gerenciais
- **Ator primário:** Equipe do NEI.
- **Objetivo:** obter visão consolidada de candidaturas e destinos.
- **Pré-condições:** existem dados registrados e usuário possui permissão.
- **Fluxo principal:**
  1. Usuário acessa relatórios.
  2. Sistema apresenta filtros disponíveis.
  3. Usuário seleciona período, destino ou oportunidade.
  4. Sistema consolida os dados.
  5. Sistema apresenta o relatório.
- **Pós-condição:** relatório consultado.
- **Requisitos:** RF-18.

## CDU-09 — Compartilhar relato de experiência
- **Ator primário:** Ex-intercambista.
- **Objetivo:** registrar experiência para consulta por outros participantes.
- **Pré-condições:** usuário autenticado.
- **Fluxo principal:** usuário preenche relato; sistema valida e encaminha para moderação; após aprovação, o relato fica disponível.
- **Requisitos:** RF-14.

## CDU-10 — Participar de atividades colaborativas
- **Atores primários:** Estudante, estudante estrangeiro recebido e ex-intercambista.
- **Objetivo:** participar de atividades de integração, Tandem, eventos e fórum.
- **Fluxo principal:** participante consulta atividade ou tópico; seleciona opção; sistema apresenta detalhes e permite participação conforme regras.
- **Requisitos:** RF-15, RF-16, RF-17, RF-20.

## CDU-11 — Gerenciar usuários e permissões
- **Ator primário:** Administrador do sistema.
- **Objetivo:** manter usuários, perfis e permissões.
- **Pré-condições:** administrador autenticado.
- **Fluxo principal:** administrador consulta usuários; cria ou atualiza perfil; define permissões; sistema valida e registra alteração.
- **Requisitos:** RF-19.

## CDU-12 — Consultar recursos de preparação
- **Ator primário:** Estudante.
- **Objetivo:** acessar materiais de idioma, cultura e planejamento financeiro.
- **Fluxo principal:** estudante acessa central de preparação; sistema apresenta categorias; estudante seleciona conteúdo; sistema exibe material.
- **Requisitos:** RF-05.
