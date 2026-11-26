# Especificação de Requisitos — ConectaGlobal

## 1. Convenções
- **RF:** requisito funcional.
- **RNF:** requisito não funcional.
- **Fonte:** identificador AD em `docs/03-analise-documental.md` ou DP em `docs/09-fontes-e-decisoes.md`.
- **Prioridade:** Must/Should/Could, definida pela equipe para o escopo acadêmico.
- Os requisitos descrevem o ConectaGlobal proposto; não são requisitos oficiais da Unifor.

## 2. Requisitos Funcionais

| ID | Requisito | Descrição verificável | Origem | Prioridade |
|---|---|---|---|---|
| RF-01 | Exibir catálogo de programas | O sistema deve apresentar os programas cadastrados com nome, categoria e resumo. | AD-02, DP-01 | Must |
| RF-02 | Pesquisar programas | O sistema deve permitir busca textual por nome e descrição. | DP-01 | Should |
| RF-03 | Filtrar programas | O sistema deve permitir filtrar por categoria/modalidade cadastrada. | AD-02, DP-01 | Should |
| RF-04 | Exibir detalhes do programa | O sistema deve apresentar descrição, público-alvo, modalidade e informações disponíveis. | AD-02 | Must |
| RF-05 | Exibir critérios publicados | O sistema deve apresentar os critérios associados à fonte e ao programa correspondente, sem generalizar critérios de um programa para outros. | AD-04, DP-02 | Must |
| RF-06 | Exibir documentos e providências | O sistema deve apresentar a lista informativa de documentos/providências descritos pela fonte oficial. | AD-05 | Must |
| RF-07 | Exibir etapas e próximos passos | O sistema deve apresentar as etapas publicadas e destacar quando o estudante deve procurar a DRI. | AD-03 | Must |
| RF-08 | Encaminhar para fonte oficial | O sistema deve disponibilizar links externos para a página DRI, edital ou contato correspondente. | AD-01, AD-10 | Must |
| RF-09 | Exibir aviso sobre seleção | O sistema deve informar que a aprovação na seleção não garante a aceitação pela instituição de destino, quando aplicável ao programa descrito. | AD-06 | Must |
| RF-10 | Exibir fonte e data de consulta | Cada página de conteúdo deve apresentar a fonte e a data em que a equipe consultou a fonte. | DP-03 | Must |
| RF-11 | Manter conteúdo do protótipo | O responsável editorial do protótipo deve poder cadastrar, editar, publicar e retirar conteúdo demonstrativo. | DP-04 | Could |
| RF-12 | Exibir perguntas frequentes | O sistema deve apresentar perguntas e respostas informativas baseadas nas páginas oficiais. | AD-03 a AD-06 | Should |

## 3. Requisitos Não Funcionais

| ID | Categoria LAPIS | Requisito | Verificação |
|---|---|---|---|
| RNF-01 | Capacidade de interação | Navegação e rótulos devem ser escritos em português claro, com termos consistentes com o glossário. | Revisão textual e teste de tarefas |
| RNF-02 | Acessibilidade | Componentes do protótipo devem possuir contraste, hierarquia, rótulos e alternativas textuais adequados; adotar WCAG 2.2 AA como referência de projeto, sem declarar certificação. | Checklist e inspeção manual |
| RNF-03 | Flexibilidade/compatibilidade | As telas devem adaptar-se a viewport móvel e desktop. | Inspeção em larguras de referência |
| RNF-04 | Segurança/privacidade | O escopo não deve solicitar nem armazenar dados pessoais, documentos ou credenciais do estudante. | Inspeção das telas e fluxos |
| RNF-05 | Adequação funcional | Conteúdo exibido deve possuir link para a fonte pública e data de consulta. | Conferência de todos os registros |
| RNF-06 | Manutenibilidade | Conteúdo deve ser estruturado de modo que descrição, critérios, documentos e links possam ser atualizados independentemente do layout. | Inspeção do modelo de conteúdo |
| RNF-07 | Compatibilidade | Links externos devem abrir a página de destino correspondente e indicar que o usuário está saindo do ConectaGlobal. | Teste de links |
| RNF-08 | Confiabilidade da informação | Quando houver divergência entre resumo do protótipo e fonte oficial, o usuário deve ser orientado a seguir o edital/regulamento vigente. | Inspeção de conteúdo e teste de cenário |

Não foram fixadas metas de disponibilidade, carga, latência, TLS, backup ou integração, pois o projeto não tem infraestrutura de produção definida.

## 4. Rastreabilidade

| Necessidade | Requisitos | Casos de uso |
|---|---|---|
| NEC-01 | RF-01, RF-02, RF-03 | CDU-01, CDU-02 |
| NEC-02 | RF-04 | CDU-03 |
| NEC-03 | RF-05 | CDU-03 |
| NEC-04 | RF-06, RF-07, RF-09 | CDU-03, CDU-04 |
| NEC-05 | RF-08 | CDU-04 |
| NEC-06 | RF-10, RF-11 | CDU-05 |

## 5. Exclusões explícitas
Não existem RFs para candidatura, análise de candidatura, mudança de status, notificações institucionais, leitura de dados acadêmicos, autenticação SSO ou gestão de convênios. Esses processos não serão inferidos a partir de páginas meramente informativas.
