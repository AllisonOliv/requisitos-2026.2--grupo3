# Especificação Inicial de Casos de Uso — ConectaGlobal

## Atores
- **AT-01 Estudante**
- **AT-02 Gestor de oportunidades**
- **AT-03 Avaliador**
- **AT-04 Administrador do sistema**

## UC-01 — Consultar oportunidades
**Objetivo:** permitir que o estudante visualize oportunidades publicadas.  
**Ator principal:** Estudante.  
**Pré-condições:** existem oportunidades cadastradas.  
**Fluxo principal:**
1. O estudante acessa a área de oportunidades.
2. O sistema recupera as oportunidades publicadas e disponíveis.
3. O sistema apresenta a lista com informações resumidas.
4. O estudante seleciona uma oportunidade para consultar seus detalhes.  
**Alternativas:** se não houver oportunidades disponíveis, o sistema informa que não há resultados.  
**Pós-condições:** nenhuma informação é alterada.  
**Requisitos:** RF-01.

## UC-02 — Pesquisar e filtrar oportunidades
**Objetivo:** localizar oportunidades com base em critérios de pesquisa.  
**Ator principal:** Estudante.  
**Pré-condições:** o estudante acessa a área de oportunidades.  
**Fluxo principal:**
1. O estudante informa um termo ou seleciona filtros.
2. O sistema valida os parâmetros.
3. O sistema apresenta as oportunidades compatíveis.
4. O estudante pode limpar ou alterar os filtros.  
**Alternativas:** se nenhum resultado corresponder, o sistema apresenta mensagem informativa.  
**Pós-condições:** a lista é apresentada conforme os filtros.  
**Requisitos:** RF-02.

## UC-03 — Consultar detalhes da oportunidade
**Objetivo:** apresentar informações completas de uma oportunidade.  
**Ator principal:** Estudante.  
**Pré-condições:** a oportunidade existe e está disponível para consulta.  
**Fluxo principal:**
1. O estudante seleciona uma oportunidade.
2. O sistema apresenta descrição, modalidade, destino, período, prazos e situação.
3. O estudante consulta as informações apresentadas.  
**Alternativas:** se a oportunidade tiver sido encerrada, o sistema informa a situação e não oferece nova candidatura.  
**Pós-condições:** nenhuma informação é alterada.  
**Requisitos:** RF-03.

## UC-04 — Consultar requisitos e documentos
**Objetivo:** permitir que o estudante conheça os critérios e documentos de uma oportunidade.  
**Ator principal:** Estudante.  
**Pré-condições:** a oportunidade possui critérios ou documentos cadastrados.  
**Fluxo principal:**
1. O estudante acessa a seção de requisitos.
2. O sistema apresenta os critérios associados à oportunidade.
3. O sistema apresenta a lista de documentos exigidos.
4. O sistema informa que a verificação de compatibilidade não garante aprovação.  
**Alternativas:** se não houver critérios ou documentos cadastrados, o sistema informa essa condição.  
**Pós-condições:** nenhuma informação é alterada.  
**Requisitos:** RF-04.

## UC-05 — Registrar candidatura
**Objetivo:** registrar a manifestação de interesse/candidatura do estudante em uma oportunidade.  
**Ator principal:** Estudante.  
**Pré-condições:** estudante autenticado; oportunidade publicada e dentro do prazo.  
**Fluxo principal:**
1. O estudante seleciona a opção de candidatura.
2. O sistema apresenta os dados e as condições da oportunidade.
3. O estudante confirma a intenção de candidatar-se.
4. O sistema verifica prazo e existência de candidatura ativa duplicada.
5. O sistema registra a candidatura com status inicial “Enviada”.
6. O sistema confirma o registro ao estudante.  
**Alternativas:** se o prazo estiver encerrado, o sistema impede o envio e informa o motivo; se já existir candidatura ativa, o sistema informa a existência do registro.  
**Pós-condições:** candidatura registrada e vinculada ao estudante e à oportunidade.  
**Requisitos:** RF-05; regras RN-06 a RN-09.

## UC-06 — Gerenciar documentos da candidatura
**Objetivo:** permitir que o estudante envie e consulte documentos associados à candidatura.  
**Ator principal:** Estudante.  
**Pré-condições:** existe candidatura do estudante em estado que permite edição documental.  
**Fluxo principal:**
1. O estudante acessa sua candidatura.
2. O sistema apresenta os documentos exigidos e os já anexados.
3. O estudante seleciona um documento e realiza o envio.
4. O sistema valida formato, tamanho e vínculo com a candidatura.
5. O sistema armazena o documento e confirma a operação.  
**Alternativas:** se o arquivo for inválido, o sistema informa o problema e solicita novo envio.  
**Pós-condições:** documento associado à candidatura.  
**Requisitos:** RF-06.

## UC-07 — Acompanhar candidatura
**Objetivo:** permitir que o estudante acompanhe a situação de sua candidatura.  
**Ator principal:** Estudante.  
**Pré-condições:** estudante autenticado e com candidatura registrada.  
**Fluxo principal:**
1. O estudante acessa suas candidaturas.
2. O sistema lista as candidaturas vinculadas ao estudante.
3. O estudante seleciona uma candidatura.
4. O sistema apresenta status atual, histórico e datas de atualização.  
**Alternativas:** se não houver candidaturas, o sistema informa que ainda não existem registros.  
**Pós-condições:** nenhuma informação é alterada.  
**Requisitos:** RF-07.

## UC-08 — Consultar notificações
**Objetivo:** permitir que o estudante consulte avisos relacionados às suas candidaturas.  
**Ator principal:** Estudante.  
**Pré-condições:** existem notificações associadas ao usuário.  
**Fluxo principal:**
1. O estudante acessa a área de notificações.
2. O sistema apresenta os avisos em ordem cronológica.
3. O estudante seleciona um aviso para consultar seu conteúdo.  
**Alternativas:** se não houver avisos, o sistema apresenta estado vazio informativo.  
**Pós-condições:** notificações permanecem disponíveis para consulta.  
**Requisitos:** RF-08.

## UC-09 — Cadastrar oportunidade
**Objetivo:** permitir que o gestor registre uma nova oportunidade.  
**Ator principal:** Gestor de oportunidades.  
**Pré-condições:** gestor autenticado e autorizado.  
**Fluxo principal:**
1. O gestor acessa o cadastro de oportunidades.
2. O sistema apresenta o formulário.
3. O gestor informa dados, prazos, critérios e documentos.
4. O gestor solicita salvar como rascunho.
5. O sistema valida os campos e registra a oportunidade.  
**Alternativas:** se houver dados obrigatórios ausentes ou inválidos, o sistema indica os campos a corrigir.  
**Pós-condições:** oportunidade cadastrada como rascunho.  
**Requisitos:** RF-09.

## UC-10 — Manter e publicar oportunidade
**Objetivo:** permitir que o gestor atualize a situação e os dados de uma oportunidade.  
**Ator principal:** Gestor de oportunidades.  
**Pré-condições:** gestor autenticado; oportunidade cadastrada.  
**Fluxo principal:**
1. O gestor seleciona uma oportunidade.
2. O sistema apresenta os dados atuais.
3. O gestor altera informações ou seleciona publicar, suspender ou encerrar.
4. O sistema valida os dados e as condições de publicação.
5. O sistema salva a alteração e apresenta confirmação.  
**Alternativas:** se os dados mínimos estiverem incompletos, o sistema impede a publicação e informa os campos pendentes.  
**Pós-condições:** oportunidade atualizada e situação registrada.  
**Requisitos:** RF-10; regras RN-01 a RN-03 e RN-14.

## UC-11 — Analisar candidatura
**Objetivo:** permitir que o avaliador consulte uma candidatura e registre sua análise.  
**Ator principal:** Avaliador.  
**Pré-condições:** avaliador autenticado e autorizado; candidatura existente.  
**Fluxo principal:**
1. O avaliador acessa a fila de candidaturas.
2. O sistema apresenta candidaturas disponíveis para análise.
3. O avaliador seleciona uma candidatura.
4. O sistema apresenta dados e documentos permitidos.
5. O avaliador registra a análise e seleciona o novo status.
6. O sistema registra status, data e responsável.
7. O sistema disponibiliza a atualização para acompanhamento do estudante.  
**Alternativas:** se houver documentação pendente, o avaliador pode selecionar “Pendente de documentação”.  
**Pós-condições:** histórico da candidatura atualizado.  
**Requisitos:** RF-11; regras RN-11 e RN-12.

## UC-12 — Gerar relatórios
**Objetivo:** permitir que o gestor consulte indicadores básicos do sistema.  
**Ator principal:** Gestor de oportunidades.  
**Pré-condições:** gestor autenticado e autorizado; existem registros para consulta.  
**Fluxo principal:**
1. O gestor acessa a área de relatórios.
2. O gestor informa período e filtros disponíveis.
3. O sistema consolida oportunidades e candidaturas conforme os filtros.
4. O sistema apresenta os resultados.  
**Alternativas:** se não houver registros no período, o sistema informa ausência de dados.  
**Pós-condições:** relatório apresentado sem alterar registros operacionais.  
**Requisitos:** RF-12.

## UC-13 — Gerenciar usuários e perfis
**Objetivo:** permitir que o administrador mantenha contas e permissões.  
**Ator principal:** Administrador do sistema.  
**Pré-condições:** administrador autenticado e autorizado.  
**Fluxo principal:**
1. O administrador acessa a área de usuários.
2. O sistema apresenta os usuários cadastrados.
3. O administrador cadastra, ativa, desativa ou altera o perfil de um usuário.
4. O sistema valida a operação e registra a alteração.  
**Alternativas:** se os dados forem inválidos, o sistema informa os campos a corrigir.  
**Pós-condições:** cadastro ou perfil atualizado.  
**Requisitos:** RF-13.

## Observações
As especificações são iniciais e serão aprofundadas na SRS da P2. As transições de status, regras de anexos, campos de cadastro e permissões devem ser detalhados e testáveis na próxima etapa.
