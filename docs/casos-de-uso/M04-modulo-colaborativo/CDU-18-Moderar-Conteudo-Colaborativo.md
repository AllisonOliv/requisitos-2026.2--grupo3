# CDU-18 — Moderar Conteúdo Colaborativo

> Módulo: M04 — Módulo Colaborativo · Projeto ConectaGlobal · Template de caso de uso LAPIS (16 seções).

### 1. Nome do Caso de Uso
Moderar Conteúdo Colaborativo.

### 2. Objetivo
Permitir que perfil autorizado analise o conteúdo submetido pelos participantes e decida sobre sua disponibilização.

### 3. Tipo
Concreto.

### 4. Atores
- **Primário:** AT-02 — Equipe do NEI ou perfil por ela autorizado.
- **Secundário:** AT-01, AT-05, AT-06 — autores do conteúdo submetido.

### 5. Precondições
Existe conteúdo submetido aguardando análise.

### 6. Fluxo Principal
- **P1.** O moderador acessa a fila de conteúdo pendente.
- **P2.** O sistema apresenta os itens submetidos, com autor e data de submissão.
- **P3.** O moderador seleciona um item e consulta seu conteúdo.
- **P4.** O moderador aprova, recusa ou solicita ajuste do item.
- **P5.** O sistema registra a decisão, o responsável e a data/hora.
- **P6.** O sistema disponibiliza o conteúdo aprovado e mantém indisponível o conteúdo recusado.
- **P7.** O sistema notifica o autor sobre a decisão.

### 7. Fluxos Alternativos
- **A1. Remoção de conteúdo já publicado**
  - A1.1. O moderador seleciona conteúdo publicado e registra sua remoção com a justificativa.
  - A1.2. O sistema retira o conteúdo da visualização e mantém o registro da remoção.
- **A2. Denúncia de conteúdo por participante**
  - A2.1. Um participante sinaliza conteúdo publicado.
  - A2.2. O sistema inclui o item na fila de análise e o fluxo segue em P3.

### 8. Fluxos de Exceção
- **E1. Item já analisado por outro moderador**
  - E1.1. O sistema informa que o item já possui decisão registrada e apresenta a decisão vigente.
- **E2. Falha ao registrar a decisão**
  - E2.1. O sistema informa que não foi possível concluir a operação e mantém o item pendente.

### 9. Pós-condições
O item possui decisão registrada e situação de publicação correspondente; o histórico da moderação é preservado.

### 10. Requisitos Não Funcionais
RNF-07, RNF-09, RNF-11, RNF-14, RNF-22.

### 11. Ponto de Extensão
Condiciona a publicação em CDU-11 — Compartilhar Relatos e Participar de Mentoria — e em CDU-12 — Participar de Atividades Colaborativas.

### 12. Frequência de Utilização
Média — proporcional ao volume de conteúdo submetido.

### 13. Interface Visual
A definir na etapa de wireframes/protótipo.

### 14. Observações
Relaciona RF-24; RN-12, RN-18. Este caso de uso existe porque RN-12 exige moderação sem designar responsável nem função. Os critérios de recusa e o prazo máximo de análise permanecem a definir na P2 (PQ-07).

### 15. Referências
NEC-09; F-19; EV-06; RNF-22.

### 16. Checklist de Validação
- [x] Nome iniciado por verbo no infinitivo.
- [x] Objetivo único e claro.
- [x] Ator primário identificado.
- [x] Fluxo principal, alternativas e exceções descritos.
- [ ] Critérios de recusa e prazo de análise definidos na SRS.
- [ ] Interface visual vinculada ao protótipo.
