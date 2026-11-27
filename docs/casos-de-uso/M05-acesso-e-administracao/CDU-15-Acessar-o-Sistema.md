# CDU-15 — Acessar o Sistema

> Módulo: M05 — Acesso e Administração · Projeto ConectaGlobal · Template de caso de uso LAPIS (16 seções).

### 1. Nome do Caso de Uso
Acessar o Sistema.

### 2. Objetivo
Permitir que o usuário se identifique no sistema e passe a operar as funcionalidades autorizadas ao seu perfil.

### 3. Tipo
Concreto.

### 4. Atores
- **Primário:** AT-01, AT-02, AT-03, AT-04, AT-05, AT-06, AT-07 — qualquer usuário cadastrado.
- **Secundário:** Não se aplica.

### 5. Precondições
O usuário possui cadastro ativo com perfil associado.

### 6. Fluxo Principal
- **P1.** O usuário acessa a tela de identificação.
- **P2.** O usuário informa suas credenciais.
- **P3.** O sistema verifica o preenchimento dos campos necessários.
- **P4.** O sistema valida as credenciais informadas.
- **P5.** O sistema identifica o perfil do usuário.
- **P6.** O sistema apresenta apenas as funcionalidades autorizadas ao perfil.

### 7. Fluxos Alternativos
- **A1. Campos não preenchidos**
  - A1.1. O sistema identifica os campos pendentes.
  - A1.2. O usuário complementa os dados e retorna ao P4.
- **A2. Usuário com mais de um perfil**
  - A2.1. O sistema apresenta os perfis disponíveis.
  - A2.2. O usuário seleciona o perfil de trabalho e o fluxo segue em P6.
- **A3. Encerramento de sessão**
  - A3.1. O usuário solicita o logout ou a sessão expira por inatividade.
  - A3.2. O sistema encerra a sessão e exige nova identificação.

### 8. Fluxos de Exceção
- **E1. Credenciais inválidas**
  - E1.1. O sistema informa que não foi possível concluir o acesso, sem revelar qual informação está incorreta.
  - E1.2. O sistema permite nova tentativa, conforme política de tentativas a definir na P2.
- **E2. Cadastro inativo ou sem perfil**
  - E2.1. O sistema informa que o acesso não está disponível e orienta procurar o responsável.
- **E3. Falha no serviço de autenticação**
  - E3.1. O sistema informa a indisponibilidade e não concede acesso.

### 9. Pós-condições
A sessão identificada é estabelecida e as funções do perfil ficam disponíveis; ou nenhum acesso é concedido.

### 10. Requisitos Não Funcionais
RNF-07, RNF-08, RNF-09, RNF-14, RNF-27.

### 11. Ponto de Extensão
Não se aplica. Os demais casos de uso que exigem perfil pressupõem este caso concluído.

### 12. Frequência de Utilização
Alta — precede o uso de qualquer função restrita.

### 13. Interface Visual
A definir na etapa de wireframes/protótipo.

### 14. Observações
Relaciona RF-21; RN-13, RN-19. O método de autenticação permanece A definir e não se presume SSO institucional. A possibilidade de consultar o catálogo de oportunidades sem identificação é questão aberta (PQ-09).

### 15. Referências
NEC-09; F-17; RNF-08; RNF-27.

### 16. Checklist de Validação
- [x] Nome iniciado por verbo no infinitivo.
- [x] Objetivo único e claro.
- [x] Ator primário identificado.
- [x] Fluxo principal, alternativas e exceções descritos.
- [ ] Método de autenticação e política de tentativas definidos na SRS.
- [ ] Interface visual vinculada ao protótipo.
