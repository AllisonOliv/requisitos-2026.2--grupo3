# CDU-07 — Analisar Candidaturas

> Módulo: M02 — Módulo de Gestão (NEI) · Projeto ConectaGlobal · Template de caso de uso LAPIS (16 seções).

### 1. Nome do Caso de Uso
Analisar Candidaturas.

### 2. Objetivo
Permitir que a equipe do NEI consulte candidaturas e registre o andamento da análise.

### 3. Tipo
Concreto.

### 4. Atores
- **Primário:** AT-02 — Equipe do NEI.
- **Secundário:** AT-03 — Coordenador de curso, quando sua participação for aplicável e autorizada.

### 5. Precondições
Existem candidaturas registradas e o usuário possui permissão de consulta.

### 6. Fluxo Principal
- **P1.** A equipe do NEI acessa o painel de candidaturas.
- **P2.** O sistema apresenta candidaturas conforme as permissões do usuário.
- **P3.** O usuário seleciona uma candidatura.
- **P4.** O sistema apresenta dados e documentos autorizados.
- **P5.** O usuário registra observação ou atualiza a situação conforme as opções disponíveis.
- **P6.** O sistema registra responsável, data/hora e situação resultante.
- **P7.** O sistema confirma a atualização.

### 7. Fluxos Alternativos
- **A1. Documentação pendente**
  - A1.1. O usuário registra a pendência.
  - A1.2. O sistema associa a pendência à candidatura para consulta pelo estudante.

### 8. Fluxos de Exceção
- **E1. Acesso não autorizado**
  - E1.1. O sistema bloqueia a consulta ou alteração.
- **E2. Transição de situação inválida**
  - E2.1. O sistema não realiza a alteração e informa a inconsistência.

### 9. Pós-condições
A candidatura permanece consultável com o histórico atualizado, quando houver alteração.

### 10. Requisitos Não Funcionais
RNF-07, RNF-09, RNF-11.

### 11. Ponto de Extensão
Não se aplica.

### 12. Frequência de Utilização
Alta durante períodos de seleção.

### 13. Interface Visual
A definir na etapa de protótipo.

### 14. Observações
As situações e transições oficiais permanecem pendentes de confirmação. Relaciona RF-11, RF-12, RN-07, RN-10 e RN-15.

### 15. Referências
NEC-04, NEC-05; F-09; EV-04.

### 16. Checklist de Validação
- [x] Nome iniciado por verbo no infinitivo.
- [x] Objetivo único.
- [x] Atores identificados.
- [x] Fluxos principal, alternativo e exceções descritos.
- [ ] Estados/transições confirmados com o processo responsável.
