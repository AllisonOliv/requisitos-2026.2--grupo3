# CDU-14 — Gerenciar Usuários e Permissões

> Módulo: M05 — Acesso e Administração · Projeto ConectaGlobal · Template de caso de uso LAPIS (16 seções).

### 1. Nome do Caso de Uso
Gerenciar Usuários e Permissões.

### 2. Objetivo
Permitir que o administrador mantenha usuários, perfis e permissões do sistema.

### 3. Tipo
Concreto.

### 4. Atores
- **Primário:** AT-07 — Administrador do sistema.
- **Secundário:** Não se aplica.

### 5. Precondições
Administrador identificado e autorizado.

### 6. Fluxo Principal
- **P1.** O administrador acessa a área de usuários.
- **P2.** O sistema apresenta os registros disponíveis.
- **P3.** O administrador seleciona um usuário ou solicita novo cadastro.
- **P4.** O administrador define ou atualiza o perfil e as permissões.
- **P5.** O sistema valida a operação.
- **P6.** O sistema registra a alteração e apresenta confirmação.

### 7. Fluxos Alternativos
- **A1. Consultar usuário**
  - A1.1. O administrador seleciona um usuário.
  - A1.2. O sistema apresenta dados permitidos.

### 8. Fluxos de Exceção
- **E1. Permissão insuficiente**
  - E1.1. O sistema bloqueia a operação.
- **E2. Dados inválidos**
  - E2.1. O sistema informa os campos a corrigir.

### 9. Pós-condições
Usuário ou permissões atualizados conforme autorização.

### 10. Requisitos Não Funcionais
RNF-07, RNF-08, RNF-09, RNF-11.

### 11. Ponto de Extensão
Não se aplica.

### 12. Frequência de Utilização
Baixa.

### 13. Interface Visual
A definir na etapa de protótipo.

### 14. Observações
Relaciona RF-19 e RN-13, RN-14.

### 15. Referências
F-15; RNF-07.

### 16. Checklist de Validação
- [x] Objetivo, ator e fluxo identificados.
- [ ] Matriz definitiva de perfis e permissões definida.
