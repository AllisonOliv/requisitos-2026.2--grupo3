# Descrição dos Diagramas UML

## 1. Casos de Uso
O diagrama apresenta quatro atores: Estudante, Gestor de oportunidades, Avaliador e Administrador. O estudante consulta oportunidades, verifica requisitos, registra candidatura, gerencia documentos e acompanha o andamento. O gestor cadastra e mantém oportunidades e consulta relatórios. O avaliador analisa candidaturas. O administrador gerencia usuários e perfis.

## 2. Componentes
A aplicação é organizada em interface web, autenticação/controle de acesso, gestão de oportunidades, consulta/elegibilidade, gestão de candidaturas, documentos, notificações e relatórios. Os módulos persistem dados no banco de dados. O módulo de documentos utiliza armazenamento próprio para arquivos.

## 3. Implantação
A implantação conceitual contém o navegador do usuário, o ambiente que hospeda a aplicação web e o ambiente de dados, com banco de dados e armazenamento de documentos. A comunicação entre navegador e aplicação ocorre por HTTPS em uma implantação real.

## 4. Consistência
Os diagramas refletem os requisitos RF-01 a RF-13 e os casos de uso UC-01 a UC-13. Não foram representados sistemas externos nem integração com a DRI, pois não fazem parte do escopo definido.
