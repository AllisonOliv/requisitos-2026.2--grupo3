# Partes Interessadas e Atores — ConectaGlobal

## 1. Partes interessadas
| ID | Parte interessada | Expectativa/interesse | Influência no projeto |
|---|---|---|---|
| ST-01 | Estudantes | Encontrar oportunidades, conhecer requisitos, enviar solicitações e acompanhar o andamento. | Alta |
| ST-02 | Gestores de oportunidades | Manter oportunidades, prazos, critérios e documentos atualizados. | Alta |
| ST-03 | Avaliadores | Analisar solicitações e registrar atualizações de situação. | Média/alta |
| ST-04 | Administrador do sistema | Controlar usuários, perfis e permissões. | Média |
| ST-05 | Equipe de desenvolvimento | Definir, modelar, implementar e documentar o produto acadêmico. | Alta |
| ST-06 | Docente | Avaliar a qualidade dos artefatos e a evolução da solução. | Alta |

Os grupos e papéis são abstrações adotadas para o projeto. Não representam atribuição oficial de uma unidade institucional.

## 2. Atores do sistema
| ID | Ator | Objetivo | Principais casos de uso |
|---|---|---|---|
| AT-01 | Estudante | Consultar oportunidades, registrar candidatura e acompanhar solicitações próprias. | UC-01 a UC-06 |
| AT-02 | Gestor de oportunidades | Criar e manter oportunidades e acompanhar o fluxo de solicitações. | UC-07, UC-08, UC-10, UC-11 |
| AT-03 | Avaliador | Analisar solicitações e atualizar seu status. | UC-09 |
| AT-04 | Administrador | Gerenciar usuários e perfis de acesso. | UC-12 |

## 3. Responsabilidades e limites
- O estudante só consulta e altera suas próprias solicitações, respeitando o estado do processo.
- O gestor mantém os dados das oportunidades e pode consultar as solicitações relacionadas conforme permissão.
- O avaliador registra análise e atualização de status, sem administrar parâmetros gerais.
- O administrador gerencia acesso e perfis, sem substituir a decisão de avaliação.
- A equipe do projeto define os papéis para fins acadêmicos; sua nomenclatura poderá ser refinada na SRS, sem alterar a separação de responsabilidades.

## 4. Premissas
1. Cada usuário autenticado possui um perfil que determina suas permissões.
2. Uma oportunidade publicada pode receber candidaturas dentro do prazo configurado.
3. A análise é realizada por usuário autorizado.
4. Não se pressupõe integração com sistemas externos.
