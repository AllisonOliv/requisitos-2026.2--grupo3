# CDU-04 — Acompanhar Candidatura

> Módulo: M01 — Módulo do Estudante · Projeto ConectaGlobal · Template de caso de uso LAPIS (16 seções).

### 1. Nome do Caso de Uso
Acompanhar Candidatura.

### 2. Objetivo
Permitir que o estudante consulte situação, histórico e pendências de suas candidaturas.

### 3. Tipo
Concreto.

### 4. Atores
- **Primário:** AT-01 — Estudante.
- **Secundário:** Não se aplica.

### 5. Precondições
O estudante possui candidatura registrada.

### 6. Fluxo Principal
- **P1.** O estudante acessa a área de suas candidaturas.
- **P2.** O sistema apresenta as candidaturas vinculadas ao estudante.
- **P3.** O estudante seleciona uma candidatura.
- **P4.** O sistema apresenta situação atual, histórico, prazos e pendências disponíveis.
- **P5.** O estudante consulta os documentos e orientações associados.

### 7. Fluxos Alternativos
- **A1. Não há candidaturas registradas**
  - A1.1. O sistema informa que não existem candidaturas vinculadas ao estudante.

### 8. Fluxos de Exceção
- **E1. Candidatura não localizada**
  - E1.1. O sistema informa que o registro não está disponível e permite retornar à listagem.

### 9. Pós-condições
As informações autorizadas da candidatura são exibidas.

### 10. Requisitos Não Funcionais
RNF-07, RNF-09, RNF-11, RNF-12.

### 11. Ponto de Extensão
Não se aplica.

### 12. Frequência de Utilização
Alta durante o período de seleção.

### 13. Interface Visual
A definir na etapa de protótipo.

### 14. Observações
Relaciona RF-07, RF-08, RN-06, RN-07 e RN-15.

### 15. Referências
NEC-03, NEC-04; F-06.

### 16. Checklist de Validação
- [x] Nome iniciado por verbo no infinitivo.
- [x] Objetivo único.
- [x] Ator primário identificado.
- [x] Fluxos principal e alternativo descritos.
- [ ] Estados oficiais da candidatura confirmados.
