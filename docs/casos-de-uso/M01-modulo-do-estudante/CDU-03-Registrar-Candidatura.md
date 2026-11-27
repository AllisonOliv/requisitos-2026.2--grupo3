# CDU-03 — Registrar Candidatura

> Módulo: M01 — Módulo do Estudante · Projeto ConectaGlobal · Template de caso de uso LAPIS (16 seções).

### 1. Nome do Caso de Uso
Registrar Candidatura.

### 2. Objetivo
Permitir que o estudante registre manifestação de interesse ou candidatura a uma oportunidade.

### 3. Tipo
Concreto.

### 4. Atores
- **Primário:** AT-01 — Estudante.
- **Secundário:** Não se aplica.

### 5. Precondições
O estudante está identificado no sistema e a oportunidade está publicada e dentro do prazo configurado.

### 6. Fluxo Principal
- **P1.** O estudante seleciona a oportunidade.
- **P2.** O sistema apresenta condições e documentos exigidos.
- **P3.** O estudante informa os dados solicitados e confirma a manifestação.
- **P4.** O sistema valida os campos obrigatórios.
- **P5.** O sistema verifica o prazo da oportunidade.
- **P6.** O sistema registra a candidatura vinculada ao estudante e à oportunidade.
- **P7.** O sistema apresenta confirmação e situação inicial do registro.

### 7. Fluxos Alternativos
- **A1. Dados obrigatórios ausentes**
  - A1.1. O sistema destaca os campos pendentes.
  - A1.2. O estudante complementa os dados e retorna ao P4.

### 8. Fluxos de Exceção
- **E1. Prazo encerrado**
  - E1.1. O sistema impede o envio e informa o encerramento do prazo.
- **E2. Oportunidade indisponível**
  - E2.1. O sistema informa que a oportunidade não aceita novas candidaturas.
- **E3. Falha no registro**
  - E3.1. O sistema informa que o registro não foi concluído e não apresenta confirmação de sucesso.

### 9. Pós-condições
A candidatura fica registrada e vinculada ao estudante e à oportunidade.

### 10. Requisitos Não Funcionais
RNF-05, RNF-07, RNF-09, RNF-10.

### 11. Ponto de Extensão
CDU-04 — Acompanhar Candidatura, após o registro.

### 12. Frequência de Utilização
Média — varia conforme a abertura de oportunidades.

### 13. Interface Visual
A definir na etapa de protótipo.

### 14. Observações
Relaciona RF-06 e RN-05, RN-06 e RN-09.

### 15. Referências
NEC-03; F-05; AD-02.

### 16. Checklist de Validação
- [x] Nome iniciado por verbo no infinitivo.
- [x] Objetivo único.
- [x] Ator primário identificado.
- [x] Fluxos principal, alternativo e de exceção descritos.
- [ ] Estados e dados obrigatórios detalhados na SRS.
