# CDU-16 — Manter Portfólio Digital

> Módulo: M01 — Módulo do Estudante · Projeto ConectaGlobal · Template de caso de uso LAPIS (16 seções).

### 1. Nome do Caso de Uso
Manter Portfólio Digital.

### 2. Objetivo
Permitir que o estudante registre e mantenha dados e documentos próprios que possam ser reaproveitados em suas candidaturas.

### 3. Tipo
Concreto.

### 4. Atores
- **Primário:** AT-01 — Estudante.
- **Secundário:** Não se aplica.

### 5. Precondições
O estudante está identificado no sistema (CDU-15).

### 6. Fluxo Principal
- **P1.** O estudante acessa seu portfólio.
- **P2.** O sistema apresenta os dados e documentos já registrados.
- **P3.** O estudante inclui, atualiza ou remove um dado ou documento.
- **P4.** O sistema verifica os campos necessários e o formato do arquivo.
- **P5.** O sistema registra a alteração.
- **P6.** O sistema apresenta o portfólio atualizado.

### 7. Fluxos Alternativos
- **A1. Vincular item do portfólio a uma candidatura**
  - A1.1. O estudante seleciona itens do portfólio ao registrar uma candidatura.
  - A1.2. O sistema associa os itens selecionados à candidatura, mantendo o item no portfólio.
- **A2. Documento com pendência**
  - A2.1. O sistema indica que o documento não atende ao formato ou ao tamanho aceito.
  - A2.2. O estudante substitui o arquivo e retorna ao P4.

### 8. Fluxos de Exceção
- **E1. Falha ao armazenar o documento**
  - E1.1. O sistema informa que não foi possível concluir o registro e mantém o estado anterior.
- **E2. Remoção de documento vinculado a candidatura em análise**
  - E2.1. O sistema informa que o documento está vinculado a uma candidatura e não permite a remoção da cópia vinculada.

### 9. Pós-condições
O portfólio reflete as alterações confirmadas; os documentos já vinculados a candidaturas permanecem preservados.

### 10. Requisitos Não Funcionais
RNF-05, RNF-07, RNF-10, RNF-11, RNF-14.

### 11. Ponto de Extensão
Fornece itens reaproveitáveis ao CDU-03 — Registrar Candidatura.

### 12. Frequência de Utilização
Média.

### 13. Interface Visual
A definir na etapa de wireframes/protótipo.

### 14. Observações
Relaciona RF-22; RN-15. O portfólio reúne informações declaradas pelo próprio estudante e não constitui registro acadêmico oficial. Os tipos de documento aceitos e a política de retenção serão definidos na P2, em conjunto com RNF-10 e RNF-11.

### 15. Referências
NEC-03; F-18; EV-03; EV-07.

### 16. Checklist de Validação
- [x] Nome iniciado por verbo no infinitivo.
- [x] Objetivo único e claro.
- [x] Ator primário identificado.
- [x] Fluxo principal, alternativas e exceções descritos.
- [ ] Tipos de documento, limites e retenção definidos na SRS.
- [ ] Interface visual vinculada ao protótipo.
