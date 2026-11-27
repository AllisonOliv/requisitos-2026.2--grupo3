# CDU-02 — Verificar Elegibilidade Inicial

> Módulo: M01 — Módulo do Estudante · Projeto ConectaGlobal · Template de caso de uso LAPIS (16 seções).

### 1. Nome do Caso de Uso
Verificar Elegibilidade Inicial.

### 2. Objetivo
Permitir que o estudante compare suas informações com os critérios cadastrados para uma oportunidade.

### 3. Tipo
Concreto.

### 4. Atores
- **Primário:** AT-01 — Estudante.
- **Secundário:** Não se aplica.

### 5. Precondições
A oportunidade possui critérios de elegibilidade cadastrados.

### 6. Fluxo Principal
- **P1.** O estudante seleciona a opção de autoavaliação da oportunidade.
- **P2.** O sistema apresenta os critérios cadastrados.
- **P3.** O estudante informa os dados solicitados.
- **P4.** O sistema verifica o preenchimento dos campos necessários.
- **P5.** O sistema compara as informações com os critérios da oportunidade.
- **P6.** O sistema apresenta resultado indicativo e informa que a análise oficial depende do processo responsável.

### 7. Fluxos Alternativos
- **A1. Dados incompletos**
  - A1.1. O sistema identifica os campos pendentes.
  - A1.2. O estudante complementa os dados e retorna ao P4.

### 8. Fluxos de Exceção
- **E1. Critérios indisponíveis**
  - E1.1. O sistema informa que não é possível realizar a autoavaliação para aquela oportunidade.
- **E2. Erro de processamento**
  - E2.1. O sistema informa que não foi possível concluir a verificação.

### 9. Pós-condições
O resultado indicativo é apresentado; nenhuma aprovação oficial é registrada por este caso de uso.

### 10. Requisitos Não Funcionais
RNF-06, RNF-07, RNF-10, RNF-12.

### 11. Ponto de Extensão
Não se aplica.

### 12. Frequência de Utilização
Média — depende do interesse do estudante em cada oportunidade.

### 13. Interface Visual
A definir na etapa de protótipo.

### 14. Observações
Relaciona RF-04 e RN-02, RN-03 e RN-04.

### 15. Referências
NEC-02; F-03; AD-01.

### 16. Checklist de Validação
- [x] Nome iniciado por verbo no infinitivo.
- [x] Objetivo único.
- [x] Ator primário identificado.
- [x] Fluxos principal, alternativo e de exceção descritos.
- [x] Resultado indicativo diferenciado de decisão oficial.
- [ ] Critérios reais de cada edital confirmados.
