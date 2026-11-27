# Especificação de Requisitos Não Funcionais — ConectaGlobal

## Histórico de versões

| Data | Versão | Descrição | Autor |
|---|---|---|---|
| 26/11/2026 | 1.1 | Reorganização pelas categorias do template LAPIS; métricas não confirmadas marcadas como pendentes. | Equipe do projeto |
| 26/11/2026 | 1.2 | Recuperação do requisito de internacionalização (idioma da interface), que existia na versão anterior e não havia sido transposto, e inclusão do requisito de gestão de sessão associado a RF-21. | Equipe do projeto |

Os requisitos abaixo seguem a organização do template LAPIS. Quando não há meta técnica definida nos documentos-base, o critério permanece como **A definir na P2**, em vez de receber um número inventado.

## 1. Requisitos de Produto

### 1.1 Eficiência de desempenho

| ID | Categoria | Requisito e critério de verificação |
|---|---|---|
| RNF-01 | Comportamento temporal | Consultas de oportunidades e candidaturas devem apresentar retorno em tempo adequado ao uso. Limite numérico: A definir na P2 após definição do ambiente e carga esperada. |
| RNF-02 | Capacidade | A solução deve suportar o volume de usuários, oportunidades e candidaturas previsto para o escopo acadêmico. Limites: A definir. |

### 1.2 Flexibilidade (portabilidade)

| ID | Categoria | Requisito e critério de verificação |
|---|---|---|
| RNF-03 | Adaptabilidade | A interface deve se adaptar a navegadores modernos em desktop e dispositivos móveis; verificar por testes em larguras de tela distintas. |
| RNF-04 | Escalabilidade | A organização modular deve permitir evolução de módulos sem exigir reescrita integral da solução; verificar pela separação das responsabilidades. |

### 1.3 Confiabilidade

| ID | Categoria | Requisito e critério de verificação |
|---|---|---|
| RNF-05 | Integridade/recuperabilidade | Operações de cadastro e atualização devem preservar consistência dos registros; cenários de falha e recuperação serão especificados na P2. |
| RNF-06 | Disponibilidade | A disponibilidade esperada deverá ser definida conforme ambiente de implantação; meta percentual: A definir. |

### 1.4 Segurança

| ID | Categoria | Requisito e critério de verificação |
|---|---|---|
| RNF-07 | Confidencialidade | Dados de candidatura e documentos devem ser acessíveis apenas ao próprio candidato e a perfis autorizados; verificar por testes de autorização. |
| RNF-08 | Autenticidade | A solução deve identificar usuários antes de permitir operações restritas; método de autenticação: A definir. |
| RNF-27 | Gestão de sessão | A sessão do usuário autenticado deve ser encerrada por inatividade e no logout explícito, impedindo reuso do acesso; tempo de expiração: A definir na P2. Relacionado a RF-21. |
| RNF-09 | Auditabilidade | Alterações relevantes em oportunidades e status de candidaturas devem registrar usuário responsável, data/hora e operação; verificar histórico. |

### 1.5 Privacidade

| ID | Categoria | Requisito e critério de verificação |
|---|---|---|
| RNF-10 | Finalidade e necessidade | A solução deve solicitar e tratar apenas dados necessários às funcionalidades previstas; campos e finalidades devem ser documentados na SRS. |
| RNF-11 | Tratamento | O acesso, armazenamento, retenção e eventual compartilhamento de dados pessoais devem observar a LGPD e política a definir; verificar matriz de dados e permissões. |

### 1.6 Capacidade de interação (UX, usabilidade e acessibilidade)

| ID | Categoria | Requisito e critério de verificação |
|---|---|---|
| RNF-12 | Facilidade de aprendizado | A interface deve apresentar rótulos claros e navegação consistente; verificar por roteiro de teste com usuários. |
| RNF-13 | Inclusividade | A interface deve considerar WCAG 2.2 nível AA como referência de acessibilidade; verificar contraste, navegação por teclado, textos alternativos e estrutura semântica. |
| RNF-14 | Operabilidade | As funções principais devem estar organizadas por perfil e módulo, com mensagens claras de sucesso, erro e pendência; verificar nos fluxos do protótipo. |
| RNF-15 | Responsividade | As telas devem manter legibilidade e operação em desktop e dispositivos móveis; verificar em resoluções representativas. |

### 1.7 Manutenibilidade

| ID | Categoria | Requisito e critério de verificação |
|---|---|---|
| RNF-16 | Modularidade | A solução deve separar responsabilidades de oportunidades, candidaturas, gestão, conteúdos e colaboração; verificar arquitetura lógica. |
| RNF-17 | Testabilidade | Requisitos funcionais devem possuir critérios de aceitação e cenários de teste rastreáveis; verificar matriz de rastreabilidade. |

### 1.8 Compatibilidade

| ID | Categoria | Requisito e critério de verificação |
|---|---|---|
| RNF-18 | Interoperabilidade | Nenhuma integração externa está confirmada nesta versão. Qualquer integração futura deverá definir autorização, contrato, dados e tratamento de falhas antes de ser especificada. |

### 1.8.1 Internacionalização

| ID | Categoria | Requisito e critério de verificação |
|---|---|---|
| RNF-28 | Internacionalização | A interface e os conteúdos informativos devem ser preparados para disponibilização em mais de um idioma, no mínimo português e inglês, sem exigir reescrita das telas; verificar pela externalização dos rótulos e pela existência de um mecanismo de seleção de idioma. |
| RNF-29 | Localização de dados | Datas, prazos e valores monetários devem ser apresentados em formato compatível com o idioma selecionado; verificar nas telas de oportunidades e candidaturas. |

> Justificativa: AT-05 (estudante estrangeiro recebido) é ator da solução e CDU-13 destina-se a incoming students. Uma interface exclusivamente em português tornaria esse caso de uso inoperante na prática. Requisito já previsto na versão anterior deste documento e aqui recuperado.

### 1.9 Segurança operacional

Não se aplica ao escopo acadêmico atual: o sistema não controla equipamentos físicos nem processos operacionais de risco. Reavaliar se o escopo mudar.

### 1.10 Adequação funcional

| ID | Categoria | Requisito e critério de verificação |
|---|---|---|
| RNF-19 | Completude funcional | As funções implementadas deverão corresponder aos requisitos aprovados e aos casos de uso relacionados; verificar matriz de rastreabilidade. |
| RNF-20 | Corretude funcional | Resultados de filtros, validações e atualizações devem corresponder aos dados e regras cadastrados; verificar por testes funcionais. |

## 2. Requisitos Externos

| ID | Categoria | Requisito |
|---|---|---|
| RNF-21 | Legislativo | O tratamento de dados pessoais deve observar a Lei Geral de Proteção de Dados Pessoais (LGPD), conforme aplicabilidade ao sistema e sua operação. |
| RNF-22 | Ético | Relatos, fórum, mentoria e interações devem respeitar privacidade, respeito entre participantes e regras de moderação a especificar. |
| RNF-23 | Regulatório | Outras exigências institucionais ou regulatórias aplicáveis devem ser levantadas com os responsáveis; atualmente A definir. |

## 3. Requisitos Organizacionais

| ID | Categoria | Requisito |
|---|---|---|
| RNF-24 | Desenvolvimento | Os artefatos de requisitos devem manter versionamento e rastreabilidade no repositório do projeto. |
| RNF-25 | Operacionais | Perfis e permissões devem ser definidos antes da implementação de operações administrativas. |
| RNF-26 | Ambientais | O ambiente real de hospedagem e implantação não foi definido nesta etapa acadêmica. |

## 4. Checklist de validação LAPIS

- [x] Histórico de versões preenchido.
- [x] Categorias de produto, externas e organizacionais consideradas.
- [x] Requisitos identificados e relacionados ao escopo.
- [ ] Metas numéricas de desempenho e disponibilidade definidas.
- [ ] Política institucional de retenção e tratamento confirmada.
- [ ] Ambiente real de implantação definido.
- [x] Integrações não confirmadas não foram tratadas como existentes.
- [x] Necessidade de internacionalização considerada em função do ator AT-05.
- [ ] Idiomas obrigatórios confirmados com os responsáveis institucionais.
- [ ] Revisão e validação pelas partes interessadas realizada.
