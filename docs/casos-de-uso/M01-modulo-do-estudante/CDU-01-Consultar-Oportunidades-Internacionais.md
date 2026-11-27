# CDU-01 — Consultar Oportunidades Internacionais

> Módulo: M01 — Módulo do Estudante · Projeto ConectaGlobal · Template de caso de uso LAPIS (16 seções).

### 1. Nome do Caso de Uso
Consultar Oportunidades Internacionais.

### 2. Objetivo
Permitir que o estudante localize oportunidades internacionais e consulte suas informações.

### 3. Tipo
Concreto.

### 4. Atores
- **Primário:** AT-01 — Estudante.
- **Secundário:** Não se aplica.

### 5. Precondições
Existem oportunidades publicadas no sistema.

### 6. Fluxo Principal
- **P1.** O estudante acessa a área de oportunidades.
- **P2.** O sistema apresenta as oportunidades publicadas.
- **P3.** O estudante informa filtros ou seleciona uma oportunidade.
- **P4.** O sistema aplica os filtros, quando informados.
- **P5.** O sistema apresenta os resultados correspondentes.
- **P6.** O estudante seleciona uma oportunidade.
- **P7.** O sistema apresenta destino, modalidade, descrição, requisitos, prazo, benefícios e documentos cadastrados.

### 7. Fluxos Alternativos
- **A1. Nenhum filtro informado**
  - A1.1. O sistema mantém a listagem geral de oportunidades publicadas.
- **A2. Nenhum resultado encontrado**
  - A2.1. O sistema informa que não há oportunidades correspondentes aos filtros.

### 8. Fluxos de Exceção
- **E1. Falha ao carregar oportunidades**
  - E1.1. O sistema informa que não foi possível carregar os dados.
  - E1.2. O sistema permite tentar novamente.

### 9. Pós-condições
As informações da oportunidade são apresentadas ao estudante.

### 10. Requisitos Não Funcionais
RNF-01, RNF-03, RNF-12, RNF-13, RNF-15.

### 11. Ponto de Extensão
Não se aplica.

### 12. Frequência de Utilização
Alta — consulta de oportunidades é atividade central do módulo do estudante.

### 13. Interface Visual
A definir na etapa de wireframes/protótipo.

### 14. Observações
Relaciona RF-01, RF-02 e RF-03; RN-01 a RN-03.

### 15. Referências
NEC-01; F-01; F-02; AD-01; AD-02.

### 16. Checklist de Validação
- [x] Nome iniciado por verbo no infinitivo.
- [x] Objetivo único e claro.
- [x] Ator primário identificado.
- [x] Fluxo principal e alternativas descritos.
- [ ] Mensagens e critérios de aceitação detalhados na SRS.
- [ ] Interface visual vinculada ao protótipo.
