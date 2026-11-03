# 7. Diagramas UML (Sprint 1)

Os diagramas abaixo usam **Mermaid**, renderizado automaticamente pelo GitHub. O Mermaid não tem notação UML nativa para casos de uso, componentes e implantação, então usamos `flowchart` com a convenção visual equivalente. Nas próximas sprints os diagramas podem ser refeitos em draw.io/Astah e exportados como imagem para a pasta `uml/`.

## 7.1 Diagrama de Casos de Uso

```mermaid
flowchart LR
    EST(["👤 Estudante"])
    NEI(["👤 Equipe NEI/DRI"])
    COO(["👤 Coordenador de curso"])
    ADM(["👤 Administrador"])
    ACAD(["⚙️ Sistema Acadêmico"])
    SSO(["⚙️ Autenticação Institucional"])

    subgraph SIS["Sistema de Gestão de Oportunidades Internacionais (GOI)"]
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
    UC13 -. "«include»" .-> UC10
    UC4 -. "«include»" .-> UC3
    UC5 -. "«include»" .-> UC4
    UC14 -. "«extend» solicita complementação" .-> UC18
    UC5 -. "«include»" .-> UC18
    UC2 -. "«include»" .-> UC1

    ACAD --- UC4
    SSO --- UC1
```

### Descrição resumida dos principais casos de uso

| ID | Caso de uso | Ator principal | Pré-condição | Fluxo principal | Pós-condição |
|---|---|---|---|---|---|
| UC05 | Manifestar interesse | Estudante | Autenticado; edital aberto | 1. Seleciona oportunidade 2. Sistema verifica elegibilidade 3. Estudante confirma 4. Sistema registra manifestação com status *Registrada* 5. Notifica estudante | Manifestação criada |
| UC05 | (fluxo alternativo) | | | 2a. Aluno não elegível: sistema informa o motivo e não permite concluir | Nenhuma manifestação criada |
| UC10 | Cadastrar e manter edital | NEI/DRI | Autenticado com perfil NEI/DRI | 1. Informa dados 2. Define critérios (UC12) e documentos 3. Salva rascunho | Edital em rascunho |
| UC13 | Publicar edital | NEI/DRI | Edital completo (RN10) | 1. Solicita publicação 2. Sistema valida campos 3. Publica e notifica interessados | Edital publicado |
| UC14 | Analisar manifestações | NEI/DRI | Existem manifestações | 1. Filtra 2. Abre manifestação 3. Altera status/observação 4. Sistema notifica aluno | Status atualizado |

## 7.2 Diagrama de Componentes

```mermaid
flowchart TB
    subgraph CLI["Camada de Apresentação"]
        WEB["Aplicação Web Responsiva (SPA)"]
    end

    subgraph API["Camada de Aplicação / Back-end (API REST)"]
        GW["API Gateway / Controladores"]
        AUTH["Componente de Autenticação e Autorização"]
        EDT["Componente de Editais e Bolsas"]
        ELG["Componente de Elegibilidade"]
        MAN["Componente de Manifestações"]
        NOT["Componente de Notificações"]
        REL["Componente de Relatórios"]
        AUD["Componente de Auditoria"]
        INT["Adaptadores de Integração"]
    end

    subgraph DAT["Camada de Dados"]
        DB[("Banco de Dados Relacional")]
        FS[("Armazenamento de Arquivos / Anexos")]
    end

    subgraph EXT["Sistemas Externos / Institucionais"]
        SSO["Provedor de Identidade Institucional (SSO)"]
        ACAD["Sistema Acadêmico"]
        MAIL["Serviço de E-mail / Push"]
    end

    WEB -->|HTTPS / JSON| GW
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
    NOT --> MAIL
    INT --> SSO
    INT --> ACAD
```

| Componente | Responsabilidade | Requisitos |
|---|---|---|
| Autenticação e Autorização | Login via SSO e controle por perfil | RF23, RF24, RNF06 |
| Editais e Bolsas | CRUD, publicação, encerramento, histórico | RF01–RF07 |
| Elegibilidade | Avalia critérios do edital contra dados do aluno | RF04, RF11, RN05–RN07 |
| Manifestações | Registro, status, cancelamento, análise | RF12–RF14, RF17–RF19 |
| Notificações | Alertas de prazo e mudança de status | RF21, RF22, RN18 |
| Relatórios | Consultas agregadas e exportação CSV | RF20 |
| Auditoria | Registro de ações | RF07, RNF08 |
| Adaptadores de Integração | Isola SSO e sistema acadêmico (RS3) | RNF09 |

## 7.3 Diagrama de Implantação

```mermaid
flowchart TB
    subgraph USR["Dispositivos do usuário"]
        BR["Navegador Web (desktop / celular)\nArtefato: SPA"]
    end

    subgraph NUV["Infraestrutura de Hospedagem (Nuvem ou Data Center Unifor)"]
        LB["Balanceador / Proxy reverso HTTPS\n(TLS)"]
        subgraph APPN["Servidor de Aplicação"]
            APP["Serviço Back-end API REST\nArtefato: goi-api"]
            JOB["Agendador de tarefas\n(prazos e notificações)"]
        end
        subgraph DBN["Servidor de Banco de Dados"]
            DBS[("SGBD Relacional\nArtefato: goi-db")]
        end
        STO[("Armazenamento de arquivos\n(anexos de editais)")]
        BKP[("Backup diário")]
    end

    subgraph INS["Infraestrutura Institucional Unifor"]
        IDP["Provedor de Identidade (SSO)"]
        SAC["Sistema Acadêmico"]
    end

    subgraph SMTP["Serviço externo"]
        MAIL["Servidor SMTP / Push"]
    end

    BR -->|HTTPS 443| LB
    LB --> APP
    APP --> DBS
    APP --> STO
    JOB --> DBS
    JOB --> MAIL
    APP -->|OIDC / SAML| IDP
    APP -->|API REST ou integração a definir| SAC
    DBS --> BKP
```

**Premissas de implantação (a validar com a TI):** hospedagem, protocolo de SSO e forma de integração com o sistema acadêmico ainda não foram definidos e dependem de autorização institucional (RS3, premissas P1 e P2).
