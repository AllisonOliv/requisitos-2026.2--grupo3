# Especificação de Requisitos — ConectaGlobal

## 1. Convenções

- **RF:** requisito funcional.
- **RNF:** requisito não funcional.
- **[D]:** originado de informação documentada no material da disciplina.
- **[H]:** hipótese ainda não validada com stakeholders.
- **[P]:** proposta de especificação para revisão.
- **MoSCoW:** Must (essencial), Should (importante), Could (desejável), Won't (fora desta entrega).

Os requisitos são propostas acadêmicas baseadas nos artefatos disponíveis. Sua inclusão não significa validação institucional.

## 2. Requisitos Funcionais

| ID | Nome | Descrição | Origem/rastreabilidade | Prioridade | Situação |
|---|---|---|---|---|---|
| RF01 | Cadastrar oportunidade | O sistema deve permitir ao perfil autorizado cadastrar uma oportunidade com título, descrição, instituição, modalidade e período. | NEC-05 / F-01 | Must | [P] |
| RF01.1 | Anexar material da oportunidade | O sistema deve permitir associar documentos e links à oportunidade. | NEC-02 / F-01 | Should | [P] |
| RF02 | Manter publicação | O sistema deve permitir editar, publicar, retirar de publicação, encerrar e arquivar uma oportunidade conforme permissão. | NEC-05 / F-01 | Must | [P] |
| RF03 | Cadastrar bolsa | O sistema deve permitir registrar informações de bolsa vinculadas ou não a uma oportunidade, incluindo condições e vigência quando informadas. | NEC-02 / F-01 | Should | [P] |
| RF04 | Configurar critérios | O sistema deve permitir cadastrar critérios de elegibilidade por oportunidade, incluindo tipo, operador e valor esperado. | NEC-02/03 / F-04 | Must | [D]/[P] |
| RF05 | Cadastrar documentos requeridos | O sistema deve permitir informar documentos exigidos e instruções por oportunidade. | NEC-02 / F-03/F-10 | Must | [P] |
| RF06 | Definir responsável pela atualização | O sistema deve permitir associar um responsável à manutenção da oportunidade. | NEC-05 / F-01 | Should | [H] |
| RF07 | Registrar histórico de alterações | O sistema deve registrar alterações relevantes em oportunidades e critérios, com autor e data. | NEC-05 / F-01 | Should | [P] |
| RF08 | Pesquisar oportunidades | O sistema deve permitir pesquisar oportunidades por texto e filtros disponíveis. | NEC-01 / F-02 | Must | [P] |
| RF09 | Consultar detalhes | O sistema deve apresentar detalhes, instituição, critérios, prazos, documentos e situação de publicação. | NEC-01/02 / F-02/F-03 | Must | [D]/[P] |
| RF10 | Consultar calendário | O sistema deve apresentar prazos de oportunidades em calendário ou listagem cronológica. | NEC-02 / F-03 | Could | [P] |
| RF11 | Verificar pré-elegibilidade | O sistema deve comparar os dados disponíveis do estudante com os critérios configurados e apresentar resultado preliminar e justificativa. | NEC-03 / F-05 | Should | [D]/[H] |
| RF12 | Registrar manifestação | O sistema deve permitir ao estudante registrar manifestação de interesse enquanto a oportunidade aceitar manifestações. | NEC-04 / F-06 | Must | [D]/[P] |
| RF13 | Cancelar manifestação | O sistema deve permitir ao estudante cancelar sua manifestação enquanto as regras da oportunidade permitirem. | NEC-04 / F-06 | Should | [P] |
| RF14 | Consultar situação | O sistema deve permitir ao estudante consultar a situação atual de sua manifestação. | NEC-04 / F-07 | Must | [D]/[P] |
| RF15 | Consultar checklist documental | O sistema deve apresentar documentos exigidos e o estado de entrega de cada documento, quando essa etapa estiver habilitada. | NEC-02/04 / F-10 | Should | [P] |
| RF16 | Favoritar oportunidade | O sistema poderá permitir ao estudante salvar oportunidades para consulta posterior. | NEC-01 / evolução | Could | [P] |
| RF17 | Consultar manifestações | O sistema deve permitir ao perfil autorizado listar e filtrar manifestações por oportunidade, estudante e situação. | NEC-06 / F-08 | Must | [P] |
| RF18 | Analisar manifestação | O sistema deve permitir ao perfil autorizado atualizar a situação de uma manifestação e registrar justificativa quando aplicável. | NEC-06 / F-08 | Must | [P] |
| RF19 | Solicitar complementação | O sistema deve permitir ao responsável solicitar documento ou informação complementar e registrar a pendência. | NEC-06 / F-09 | Should | [P] |
| RF20 | Gerar relatórios | O sistema deve permitir consultar e exportar relatórios básicos de oportunidades e manifestações, conforme permissões. | NEC-08 / F-12 | Should | [H] |
| RF21 | Notificar eventos relevantes | O sistema deve notificar usuários sobre eventos configurados, como prazo próximo, mudança de situação ou nova oportunidade compatível, conforme preferências e canal aprovado. | NEC-07 / F-11 | Should | [H] |
| RF22 | Notificar alterações em oportunidade | O sistema deve notificar estudantes com manifestação ativa quando mudanças relevantes em prazo ou critérios forem publicadas. | NEC-07 / F-11 | Should | [P] |
| RF23 | Autenticar usuário | O sistema deve autenticar usuários antes de permitir acesso a funções restritas. | Transversal / F-13 | Must | [P] |
| RF24 | Controlar permissões | O sistema deve restringir operações conforme perfil e autorização atribuída. | Transversal / F-13 | Must | [P] |
| RF25 | Consultar por curso | O sistema poderá permitir ao coordenador autorizado consultar manifestações vinculadas ao seu curso. | NEC-08 / F-14 | Could | [H] |
| RF26 | Relacionar instituição parceira | O sistema deve permitir associar oportunidade à instituição parceira e, se aplicável, registrar referência à vigência do acordo. | NEC-02 / F-01 | Should | [H] |

### 2.1 Observações sobre requisitos funcionais

- RF11 não pode ser interpretado como decisão de aprovação. A pré-elegibilidade é apenas uma indicação preliminar.
- RF26 não pressupõe que o sistema gerencie convênios. O cadastro de referência à instituição e eventual validade do acordo depende de confirmação.
- RF03 foi classificado como Should/R2 para manter coerência com o roadmap original, no qual o módulo de bolsas aparece em R2.
- RF25 permanece Could, pois a participação dos coordenadores não foi confirmada.

## 3. Requisitos Não Funcionais

Os RNFs abaixo foram reorganizados nas categorias LAPIS. Metas quantitativas sem evidência institucional são propostas a validar, não níveis de serviço aprovados.

| ID | Categoria LAPIS | Requisito | Verificação proposta | Situação |
|---|---|---|---|---|
| RNF01 | Capacidade de interação / usabilidade | A interface deve permitir que um estudante encontre os detalhes de uma oportunidade a partir do catálogo sem navegação desnecessária e com rótulos compreensíveis. | Teste de usabilidade com tarefas definidas; meta de passos a validar | [P] |
| RNF02 | Capacidade de interação / acessibilidade | A interface deve buscar conformidade com WCAG 2.1 nível AA. | Avaliação automatizada e inspeção manual de acessibilidade | [P] |
| RNF03 | Flexibilidade / compatibilidade | A interface deve adaptar-se a dispositivos móveis e desktop e funcionar nos navegadores suportados pela instituição. | Testes nos navegadores e dispositivos definidos pela TI | [P] |
| RNF04 | Eficiência de desempenho | Consultas ao catálogo devem responder em até 2 segundos para 95% das requisições sob carga de referência. | Teste de carga; volume de usuários simultâneos a definir com TI | [P] |
| RNF04.1 | Eficiência de desempenho | O painel gerencial deve suportar o volume de manifestações definido pela área responsável, sem degradação incompatível com o uso. | Teste de carga com volume realista; base de 5.000 registros é hipótese a validar | [H] |
| RNF05 | Confiabilidade | A disponibilidade esperada deve ser definida pela instituição antes de eventual implantação. A meta de 99% registrada anteriormente permanece proposta não validada. | Monitoramento e cálculo de disponibilidade após definição de janela e exclusões | [H] |
| RNF06 | Segurança | A comunicação entre cliente e servidor deve utilizar protocolo seguro com configuração aprovada pela TI. | Inspeção de configuração TLS | [P] |
| RNF06.1 | Segurança | Dados pessoais e documentos armazenados devem possuir proteção adequada em repouso, conforme arquitetura e política institucional. | Revisão de arquitetura e configuração de armazenamento | [P] |
| RNF06.2 | Segurança | A solução não deve armazenar senhas institucionais localmente quando utilizar provedor SSO. | Revisão de arquitetura e teste de autenticação | [H] |
| RNF07 | Privacidade | O tratamento de dados pessoais deve observar a LGPD e as políticas institucionais, com finalidade, acesso e retenção definidos. | Revisão de privacidade e validação pelo responsável institucional | [D]/[P] |
| RNF08 | Confiabilidade / auditabilidade | Operações relevantes de cadastro, publicação e alteração de situação devem manter registro de autor, data e ação. | Inspeção dos registros de auditoria | [P] |
| RNF09 | Flexibilidade / interoperabilidade | Integrações externas, se aprovadas, devem utilizar interfaces documentadas e autorizadas pela instituição. | Revisão de contrato e teste de integração | [H] |
| RNF10 | Capacidade de interação / internacionalização | O idioma inicial deve ser definido com a área responsável. Português é a proposta inicial; inglês e espanhol dependem de validação de escopo. | Revisão das telas e conteúdo | [H] |
| RNF11 | Manutenibilidade | A solução deve manter documentação atualizada de seus componentes e interfaces, caso seja implementada. | Revisão da documentação técnica | [P] |
| RNF12 | Confiabilidade | A política de backup, retenção e restauração deve seguir os padrões institucionais. A retenção de 30 dias registrada anteriormente é proposta a validar. | Teste de restauração e inspeção da política | [H] |
| RNF13 | Eficiência / confiabilidade | O prazo de entrega de notificações deve ser definido conforme canal e serviço institucional. A meta anterior de até 5 minutos é hipótese. | Teste de envio e medição de latência após definição do serviço | [H] |

## 4. Rastreabilidade funcional

| Necessidade | Funcionalidades | Casos de uso |
|---|---|---|
| NEC-01 | F-02 | CDU-02 |
| NEC-02 | F-03, F-04, F-10 | CDU-01, CDU-02, CDU-07 |
| NEC-03 | F-05 | CDU-03 |
| NEC-04 | F-06, F-07, F-10 | CDU-04, CDU-05, CDU-07 |
| NEC-05 | F-01 | CDU-01 |
| NEC-06 | F-08, F-09 | CDU-06 |
| NEC-07 | F-11 | CDU-08 |
| NEC-08 | F-12, F-14 | CDU-09 |

## 5. Histórico

| Versão | Data | Alteração |
|---|---|---|
| 1.0 | 26/11/2026 | Reorganização dos requisitos, ajuste de prioridades e classificação de RNFs por categorias LAPIS; metas sem validação identificadas como hipóteses. |
