# CDU-09 — Consultar Relatórios Gerenciais

> Módulo: M02 — Módulo de Gestão (NEI) · Projeto ConectaGlobal · Template de caso de uso LAPIS (16 seções).

### 1. Nome do Caso de Uso
Consultar Relatórios Gerenciais.

### 2. Objetivo
Permitir que a equipe do NEI consulte informações consolidadas sobre candidaturas, perfis e destinos procurados.

### 3. Tipo
Concreto.

### 4. Atores
- **Primário:** AT-02 — Equipe do NEI.
- **Secundário:** Não se aplica.

### 5. Precondições
Existem dados registrados e o usuário possui permissão para consultar relatórios.

### 6. Fluxo Principal
- **P1.** O usuário acessa a área de relatórios.
- **P2.** O sistema apresenta filtros disponíveis.
- **P3.** O usuário seleciona período, destino ou oportunidade, conforme filtros existentes.
- **P4.** O sistema consolida os dados autorizados.
- **P5.** O sistema apresenta o relatório.

### 7. Fluxos Alternativos
- **A1. Sem filtros**
  - A1.1. O sistema apresenta o conjunto padrão de informações permitido.

### 8. Fluxos de Exceção
- **E1. Sem dados para os filtros**
  - E1.1. O sistema informa que não foram encontrados dados.
- **E2. Acesso não autorizado**
  - E2.1. O sistema bloqueia a consulta.

### 9. Pós-condições
Relatório consultado sem alteração dos dados de origem.

### 10. Requisitos Não Funcionais
RNF-01, RNF-07, RNF-11.

### 11. Ponto de Extensão
Não se aplica.

### 12. Frequência de Utilização
Média.

### 13. Interface Visual
A definir na etapa de protótipo.

### 14. Observações
Indicadores e filtros precisam de confirmação com responsáveis. Relaciona RF-18 e RN-16.

### 15. Referências
NEC-08; F-11; EV-04.

### 16. Checklist de Validação
- [x] Objetivo, ator e fluxos identificados.
- [ ] Indicadores gerenciais definidos.
