# 7. Diagramas UML (Sprint 1)

Os diagramas usam **Mermaid**, renderizado automaticamente pelo GitHub. O Mermaid não tem notação UML nativa para casos de uso, componentes e implantação; por isso usamos `flowchart` com a convenção visual equivalente. Nas próximas sprints os diagramas poderão ser refeitos em draw.io/Astah e exportados como imagem para a pasta `uml/`.

## 7.1 Diagrama de Casos de Uso

> Todos os casos de uso exigem **UC01 Autenticar**. Para não poluir o diagrama, essa dependência não foi desenhada com setas.

```mermaid
flowchart LR
    EST(["«ator» Estudante"])
    NEI(["«ator» Equipe NEI/DRI"])
    COO(["«ator» Coordenador de curso"])
    ADM(["«ator» Administrador"])
    ACAD(["«sistema externo» Sistema Acadêmico"])
    SSO(["«sistema externo» SSO Institucional"])

    subgraph SIS["ConectaGlobal"]
        UC1(["UC01 Autenticar"])
        UC2(["UC02 Buscar e filtrar oportunidades"])
        UC3(["UC03 Consultar detalhe da oportunidade"])
        UC4(["UC04 Verificar pré-elegibilidade"])
        UC5(["UC05 Manifestar interesse"])
        UC6(["UC06 Acompanhar status da manifestação"])
        UC7(["UC07 Cancelar manifestação"])
        UC8(["UC08 Gerenciar checklist de documentos"])
        UC9(["UC09 Consultar calendário de prazos"])
        UC10(["UC10 Cadastrar e manter edital"])
        UC11(["UC11 Cadastrar e manter bolsa"])
        UC12(["UC12 Definir critérios de elegibilidade"])
        UC13(["UC13 Publicar ou encerrar edital"])
        UC14(["UC14 Analisar manifestações"])
        UC15(["UC15 Gerar relatórios"])
        UC16(["UC16 Consultar manifestações do curso"])
        UC17(["UC17 Gerenciar usuários e perfis"])
        UC18(["UC18 Enviar notificações"])
        UC19(["UC19 Solicitar complementação de documentos"])
    end

    EST --- UC2
    EST --- UC3
    EST --- UC4
    EST --- UC5
    EST --- UC6
    EST --- UC7
    EST --- UC8
    EST --- UC9

    NEI --- UC10
    NEI --- UC11
    NEI --- UC13
    NEI --- UC14
    NEI --- UC15

    COO --- UC16
    ADM --- UC17

    UC10 -. "«include»" .-> UC12
    UC5 -. "«include»" .-> UC4
    UC5 -. "«include»" .-> UC18
    UC14 -. "«include»" .-> UC18
    UC19 -. "«extend»" .-> UC14

    SSO --- UC1
    ACAD --- UC4
```

### Descrição resumida dos principais casos de uso

| ID | Caso de uso | Ator principal | Pré-condição | Fluxo principal | Pós-condição |
|---|---|---|---|---|---|
| UC05 | Manifestar interesse | Estudante | Autenticado; edital aberto | 1. Seleciona oportunidade 2. Sistema verifica elegibilidade (UC04) 3. Estudante confirma 4. Sistema registra manifestação com status *Registrada* 5. Notifica estudante (UC18) | Manifestação criada |
| UC05 | (fluxo alternativo) | | | 2a. Estudante não elegível: sistema informa o motivo e não permite concluir | Nenhuma manifestação criada |
| UC10 | Cadastrar e manter edital | NEI/DRI | Autenticado com perfil NEI/DRI | 1. Informa dados 2. Define critérios (UC12) e documentos 3. Salva rascunho | Edital em rascunho |
| UC13 | Publicar edital | NEI/DRI | Edital completo (RN10) | 1. Solicita publicação 2. Sistema valida campos 3. Publica e notifica interessados | Edital publicado |
| UC14 | Analisar manifestações | NEI/DRI | Existem manifestações | 1. Filtra 2. Abre manifestação 3. Altera status com justificativa 4. Sistema notifica o aluno (UC18) | Status atualizado |
| UC19 | Solicitar complementação | NEI/DRI | Manifestação em análise | 1. Informa o que falta 2. Status vira *Pendência de documentos* 3. Aluno é notificado | Pendência registrada |

## 7.2 Diagrama de Componentes

```mermaid
flowchart TB
    subgraph CLI["Camada de Apresentação"]
        WEB["Aplicação Web Responsiva (SPA)<br/>acesso por navegador e celular"]
    end

    subgraph API["Camada de Aplicação (API REST)"]
        GW["API Gateway / Controladores"]
        AUTH["Autenticação e Autorização"]
        EDT["Editais e Bolsas"]
        ELG["Elegibilidade"]
        MAN["Manifestações"]
        NOT["Notificações"]
        REL["Relatórios"]
        AUD["Auditoria"]
        INT["Adaptadores de Integração"]
    end

    subgraph DAT["Camada de Dados"]
        DB[("Banco de Dados Relacional")]
        FS[("Armazenamento de Documentos")]
    end

    subgraph EXT["Sistemas Externos"]
        SSO["SSO Institucional"]
        ACAD["Sistema Acadêmico"]
        MAIL["Serviço de E-mail / Push"]
    end

    WEB -->|"HTTPS / JSON"| GW
    GW --> AUTH
    GW --> EDT
    GW --> MAN
    GW --> REL
    MAN --> ELG
    MAN --> NOT
    EDT --> NOT
    EDT --> ELG
    AUTH --> INT
    ELG --> INT
    EDT --> AUD
    MAN --> AUD
    EDT --> DB
    MAN --> DB
    ELG --> DB
    REL --> DB
    AUD --> DB
    EDT --> FS
    MAN --> FS
    NOT --> MAIL
    INT --> SSO
    INT --> ACAD
```

| Componente | Responsabilidade | Requisitos |
|---|---|---|
| Autenticação e Autorização | Login via SSO e controle por perfil | RF23, RF24, RNF06 |
| Editais e Bolsas | Cadastro, publicação, encerramento, histórico, documentos exigidos | RF01–RF07, RF26 |
| Elegibilidade | Avalia critérios do edital contra dados do aluno | RF04, RF11, RN05–RN07 |
| Manifestações | Registro, status, cancelamento, análise, justificativa | RF12–RF14, RF17–RF19 |
| Notificações | Alertas de prazo e mudança de status | RF21, RF22, RN18 |
| Relatórios | Consultas agregadas e exportação CSV/PDF | RF20 |
| Auditoria | Registro de ações | RF07, RNF08 |
| Adaptadores de Integração | Isolam SSO e sistema acadêmico (risco RS3) | RNF09 |

## 7.3 Diagrama de Implantação

```mermaid
flowchart TB
    subgraph USR["Nó: Dispositivo do usuário"]
        BR["Navegador Web (desktop / iOS / Android)<br/>Artefato: SPA"]
    end

    subgraph NUV["Nó: Infraestrutura de Hospedagem (nuvem ou data center)"]
        LB["Balanceador de carga / Proxy reverso<br/>HTTPS (TLS 1.2+)"]
        subgraph CL["Cluster de Aplicação"]
            APP1["Servidor de Aplicação 01<br/>Artefato: conectaglobal-api"]
            APP2["Servidor de Aplicação 02<br/>Artefato: conectaglobal-api"]
        end
        JOB["Agendador de tarefas<br/>(prazos e notificações)"]
        DBS[("Servidor de Banco de Dados<br/>Artefato: conectaglobal-db")]
        STO[("Armazenamento de documentos")]
        BKP[("Backup diário")]
    end

    subgraph INS["Nó: Infraestrutura Institucional Unifor"]
        IDP["SSO Institucional"]
        SAC["Sistema Acadêmico"]
    end

    subgraph TER["Nó: Serviço de terceiros"]
        MAIL["Provedor de E-mail / Push"]
    end

    BR -->|"HTTPS 443"| LB
    LB --> APP1
    LB --> APP2
    APP1 -->|"TCP / SQL"| DBS
    APP2 -->|"TCP / SQL"| DBS
    APP1 -->|"HTTPS"| STO
    JOB --> DBS
    JOB -->|"HTTPS / SMTP"| MAIL
    APP1 -->|"OIDC / SAML"| IDP
    APP1 -->|"API REST (a definir)"| SAC
    DBS --> BKP
```

**Premissas de implantação (a validar com a TI):** hospedagem, protocolo de SSO e forma de integração com o sistema acadêmico ainda não foram definidos e dependem de autorização institucional (risco RS3, premissas P1 e P2). A conexão com a infraestrutura Unifor pode exigir VPN.
