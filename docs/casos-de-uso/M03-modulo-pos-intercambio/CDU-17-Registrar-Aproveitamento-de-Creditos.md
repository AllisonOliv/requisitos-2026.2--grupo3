# CDU-17 — Registrar Aproveitamento de Créditos

> Módulo: M03 — Módulo Pós-intercâmbio · Projeto ConectaGlobal · Template de caso de uso LAPIS (16 seções).

### 1. Nome do Caso de Uso
Registrar Aproveitamento de Créditos.

### 2. Objetivo
Permitir o registro e a consulta das informações de aproveitamento de créditos referentes a uma mobilidade realizada.

### 3. Tipo
Concreto.

### 4. Atores
- **Primário:** AT-01 — Estudante.
- **Secundário:** AT-02 — Equipe do NEI; AT-03 — Coordenador de curso, conforme permissões a definir.

### 5. Precondições
Existe mobilidade concluída registrada para o estudante.

### 6. Fluxo Principal
- **P1.** O estudante acessa a área de pós-intercâmbio da mobilidade concluída.
- **P2.** O sistema apresenta a situação registrada do aproveitamento, quando houver.
- **P3.** O estudante informa as disciplinas cursadas e anexa os comprovantes solicitados.
- **P4.** O sistema verifica os campos necessários.
- **P5.** O sistema registra a solicitação com situação inicial e data/hora.
- **P6.** O sistema informa que a decisão sobre o aproveitamento é da instância acadêmica responsável.

### 7. Fluxos Alternativos
- **A1. Consulta da situação**
  - A1.1. O estudante consulta a situação e o histórico do registro, sem alterá-lo.
- **A2. Atualização da situação por perfil autorizado**
  - A2.1. O perfil autorizado registra a situação informada pela instância acadêmica e a data correspondente.
  - A2.2. O sistema registra o responsável, a data/hora e a situação resultante.

### 8. Fluxos de Exceção
- **E1. Documentação incompleta**
  - E1.1. O sistema indica as pendências e mantém o registro como pendente.
- **E2. Falha ao registrar**
  - E2.1. O sistema informa que não foi possível concluir o registro e preserva o estado anterior.

### 9. Pós-condições
O registro de aproveitamento fica disponível para consulta, com histórico de situações; nenhuma decisão acadêmica é produzida pelo sistema.

### 10. Requisitos Não Funcionais
RNF-05, RNF-07, RNF-09, RNF-10, RNF-14.

### 11. Ponto de Extensão
Não se aplica.

### 12. Frequência de Utilização
Baixa — ocorre ao término de uma mobilidade.

### 13. Interface Visual
A definir na etapa de wireframes/protótipo.

### 14. Observações
Relaciona RF-23; RN-20. Item previsto na seção 6.1 da Visão da Demanda. Não se presume integração com o sistema acadêmico: as situações são registradas manualmente por perfil autorizado enquanto não houver integração autorizada (PQ-05).

### 15. Referências
NEC-07; F-16; EV-05.

### 16. Checklist de Validação
- [x] Nome iniciado por verbo no infinitivo.
- [x] Objetivo único e claro.
- [x] Ator primário identificado.
- [x] Fluxo principal, alternativas e exceções descritos.
- [ ] Situações, responsáveis e prazos confirmados com as instâncias acadêmicas.
- [ ] Interface visual vinculada ao protótipo.
