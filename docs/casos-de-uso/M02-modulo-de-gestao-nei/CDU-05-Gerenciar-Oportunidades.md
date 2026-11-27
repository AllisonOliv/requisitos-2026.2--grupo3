# CDU-05 — Gerenciar Oportunidades

> Módulo: M02 — Módulo de Gestão (NEI) · Projeto ConectaGlobal · Template de caso de uso LAPIS (16 seções).

### 1. Nome do Caso de Uso
Gerenciar Oportunidades.

### 2. Objetivo
Permitir que a equipe do NEI mantenha oportunidades e editais cadastrados e publicados.

### 3. Tipo
Concreto.

### 4. Atores
- **Primário:** AT-02 — Equipe do NEI.
- **Secundário:** Não se aplica.

### 5. Precondições
O usuário está identificado e possui permissão de gestão.

### 6. Fluxo Principal
- **P1.** A equipe do NEI acessa a gestão de oportunidades.
- **P2.** O sistema apresenta os registros existentes.
- **P3.** O usuário seleciona cadastrar ou editar uma oportunidade.
- **P4.** O usuário informa descrição, destino, modalidade, requisitos, documentos e prazo.
- **P5.** O sistema valida os campos obrigatórios.
- **P6.** O usuário solicita publicação ou salva a alteração.
- **P7.** O sistema registra a operação e apresenta o resultado.

### 7. Fluxos Alternativos
- **A1. Suspender oportunidade**
  - A1.1. O usuário seleciona uma oportunidade publicada e solicita suspensão.
  - A1.2. O sistema atualiza a situação.
- **A2. Encerrar oportunidade**
  - A2.1. O usuário solicita encerramento.
  - A2.2. O sistema registra a situação de encerrada.

### 8. Fluxos de Exceção
- **E1. Dados inválidos**
  - E1.1. O sistema indica os campos que precisam de correção.
- **E2. Usuário sem permissão**
  - E2.1. O sistema bloqueia a operação e informa a restrição.

### 9. Pós-condições
A oportunidade é criada ou atualizada conforme a operação autorizada.

### 10. Requisitos Não Funcionais
RNF-07, RNF-09, RNF-10.

### 11. Ponto de Extensão
Não se aplica.

### 12. Frequência de Utilização
Média — conforme abertura e atualização de oportunidades.

### 13. Interface Visual
A definir na etapa de protótipo.

### 14. Observações
Relaciona RF-09, RN-01, RN-08, RN-13 e RN-14.

### 15. Referências
NEC-05; F-07; EV-04 e EV-07.

### 16. Checklist de Validação
- [x] Nome iniciado por verbo no infinitivo.
- [x] Objetivo único.
- [x] Ator primário identificado.
- [x] Fluxos principal, alternativos e exceções descritos.
- [ ] Campos e estados detalhados na SRS.
