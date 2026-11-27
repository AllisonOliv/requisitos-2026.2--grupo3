# CDU-06 — Gerenciar Convênios e Bolsas

> Módulo: M02 — Módulo de Gestão (NEI) · Projeto ConectaGlobal · Template de caso de uso LAPIS (16 seções).

### 1. Nome do Caso de Uso
Gerenciar Convênios e Bolsas.

### 2. Objetivo
Permitir que a equipe do NEI mantenha informações de instituições parceiras, convênios e bolsas.

### 3. Tipo
Concreto.

### 4. Atores
- **Primário:** AT-02 — Equipe do NEI.
- **Secundário:** Não se aplica.

### 5. Precondições
Usuário identificado e autorizado.

### 6. Fluxo Principal
- **P1.** A equipe do NEI acessa a área de gestão.
- **P2.** O sistema apresenta instituições, convênios e bolsas cadastrados.
- **P3.** O usuário seleciona um registro ou solicita novo cadastro.
- **P4.** O usuário informa ou altera os dados.
- **P5.** O sistema valida os campos.
- **P6.** O sistema salva o registro e apresenta confirmação.

### 7. Fluxos Alternativos
- **A1. Consultar registro**
  - A1.1. O usuário seleciona um registro.
  - A1.2. O sistema apresenta os dados disponíveis.

### 8. Fluxos de Exceção
- **E1. Dados inválidos**
  - E1.1. O sistema informa os campos a corrigir.
- **E2. Usuário sem permissão**
  - E2.1. O sistema bloqueia a alteração.

### 9. Pós-condições
O registro é consultado ou atualizado.

### 10. Requisitos Não Funcionais
RNF-07, RNF-09.

### 11. Ponto de Extensão
Não se aplica.

### 12. Frequência de Utilização
Média.

### 13. Interface Visual
A definir na etapa de protótipo.

### 14. Observações
Relaciona RF-10, RN-08 e RN-14.

### 15. Referências
NEC-05; F-08; EV-04.

### 16. Checklist de Validação
- [x] Nome iniciado por verbo no infinitivo.
- [x] Objetivo único.
- [x] Ator primário identificado.
- [x] Fluxos principal, alternativo e exceções descritos.
- [ ] Campos específicos confirmados.
