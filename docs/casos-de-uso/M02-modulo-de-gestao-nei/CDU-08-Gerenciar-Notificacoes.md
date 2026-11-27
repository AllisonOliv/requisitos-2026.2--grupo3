# CDU-08 — Gerenciar Notificações

> Módulo: M02 — Módulo de Gestão (NEI) · Projeto ConectaGlobal · Template de caso de uso LAPIS (16 seções).

### 1. Nome do Caso de Uso
Gerenciar Notificações.

### 2. Objetivo
Permitir que o sistema disponibilize avisos relacionados a prazos, pendências e mudanças de situação.

### 3. Tipo
Concreto.

### 4. Atores
- **Primário:** AT-02 — Equipe do NEI, para configuração/gestão de eventos quando autorizada.
- **Secundário:** AT-01 — Estudante, como destinatário das notificações.

### 5. Precondições
Existem eventos relevantes configurados para gerar notificação.

### 6. Fluxo Principal
- **P1.** Ocorre um evento configurado, como prazo próximo, pendência ou mudança de situação.
- **P2.** O sistema identifica os usuários relacionados ao evento.
- **P3.** O sistema prepara a notificação com as informações permitidas.
- **P4.** O sistema disponibiliza a notificação ao destinatário.
- **P5.** O destinatário consulta o aviso.

### 7. Fluxos Alternativos
- **A1. Destinatário sem notificação pendente**
  - A1.1. O sistema apresenta a área de notificações sem novos avisos.

### 8. Fluxos de Exceção
- **E1. Falha na geração**
  - E1.1. O sistema registra a falha para tratamento, sem indicar envio concluído.

### 9. Pós-condições
A notificação fica disponível quando gerada com sucesso.

### 10. Requisitos Não Funcionais
RNF-07, RNF-09, RNF-11.

### 11. Ponto de Extensão
Não se aplica.

### 12. Frequência de Utilização
Média; depende dos eventos cadastrados.

### 13. Interface Visual
A definir na etapa de protótipo.

### 14. Observações
Canais e prazos de envio precisam ser definidos na P2. Relaciona RF-13 e RN-17.

### 15. Referências
NEC-04; F-10.

### 16. Checklist de Validação
- [x] Objetivo e atores identificados.
- [x] Fluxo principal e exceção descritos.
- [ ] Canais e tempos definidos.
