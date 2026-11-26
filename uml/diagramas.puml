# Diagramas do ConectaGlobal

Diagramas em Mermaid com apresentação visual ilustrada para facilitar a leitura no GitHub. Os ícones são apenas recursos visuais; os atores, funcionalidades e relações seguem os documentos de requisitos e casos de uso.

## 1. Diagrama de Casos de Uso

```mermaid
flowchart LR
    subgraph ATORES["👥 Atores do sistema"]
      direction TB
      EST["🎓 AT-01<br/>Estudante"]
      NEI["🏢 AT-02<br/>Equipe do NEI"]
      COORD["🧑‍🏫 AT-03<br/>Coordenador de curso"]
      PROF["👩‍🏫 AT-04<br/>Professor"]
      IN["🌎 AT-05<br/>Estudante estrangeiro recebido"]
      EX["🧳 AT-06<br/>Ex-intercambista"]
      ADM["⚙️ AT-07<br/>Administrador"]
    end

    subgraph SISTEMA["🌐 ConectaGlobal — Sistema de Gestão de Oportunidades Internacionais"]
      direction TB
      subgraph MOD1["🎓 Módulo do Estudante"]
        UC01(["🔎 CDU-01<br/>Consultar oportunidades"])
        UC02(["📝 CDU-02<br/>Verificar elegibilidade inicial"])
        UC03(["📨 CDU-03<br/>Registrar candidatura"])
        UC04(["📍 CDU-04<br/>Acompanhar candidatura"])
        UC10(["📚 CDU-10<br/>Consultar recursos de preparação"])
      end
      subgraph MOD2["🏢 Módulo de Gestão — NEI"]
        UC05(["📢 CDU-05<br/>Gerenciar oportunidades"])
        UC06(["🤝 CDU-06<br/>Gerenciar convênios e bolsas"])
        UC07(["📋 CDU-07<br/>Analisar candidaturas"])
        UC08(["🔔 CDU-08<br/>Gerenciar notificações"])
        UC09(["📊 CDU-09<br/>Consultar relatórios gerenciais"])
      end
      subgraph MOD3["🌍 Pós-intercâmbio e colaboração"]
        UC11(["💬 CDU-11<br/>Compartilhar relatos e participar de mentoria"])
        UC12(["🤝 CDU-12<br/>Participar de atividades colaborativas"])
        UC13(["🧭 CDU-13<br/>Consultar recursos de integração"])
      end
      subgraph MOD4["🛠️ Administração"]
        UC14(["🔐 CDU-14<br/>Gerenciar usuários e permissões"])
      end
    end

    EST --> UC01
    EST --> UC02
    EST --> UC03
    EST --> UC04
    EST --> UC10
    EST --> UC11
    EST --> UC12
    NEI --> UC05
    NEI --> UC06
    NEI --> UC07
    NEI --> UC08
    NEI --> UC09
    COORD --> UC07
    PROF --> UC12
    IN --> UC12
    IN --> UC13
    EX --> UC11
    EX --> UC12
    ADM --> UC14

    classDef student fill:#E8F2FF,stroke:#3676C8,color:#17365D,stroke-width:1.5px;
    classDef management fill:#FFF1DF,stroke:#C77B20,color:#653B0B,stroke-width:1.5px;
    classDef community fill:#E9F7EF,stroke:#39865B,color:#174B30,stroke-width:1.5px;
    classDef admin fill:#F0EAFE,stroke:#7856B8,color:#39245F,stroke-width:1.5px;
    class EST,UC01,UC02,UC03,UC04,UC10 student;
    class NEI,COORD,UC05,UC06,UC07,UC08,UC09 management;
    class PROF,IN,EX,UC11,UC12,UC13 community;
    class ADM,UC14 admin;
```

## 2. Diagrama de Componentes

```mermaid
flowchart TB
  subgraph CLIENTE["📱 Camada de apresentação"]
    WEB["🖥️ Interface Web"]
    MOBILE["📲 Interface responsiva para dispositivos móveis"]
  end

  subgraph APLICACAO["⚙️ ConectaGlobal — serviços da aplicação"]
    AUTH["🔐 Autenticação e autorização"]
    OPORT["🌐 Gestão de oportunidades"]
    CONV["🤝 Convênios e bolsas"]
    ELEG["✅ Verificação de elegibilidade"]
    CAND["📨 Gestão de candidaturas"]
    DOC["📁 Documentos e checklist"]
    NOTIF["🔔 Notificações"]
    REL["📊 Relatórios gerenciais"]
    PREP["📚 Preparação e conteúdos"]
    COL["💬 Colaboração e pós-intercâmbio"]
    ADMIN["🛠️ Administração de usuários"]
  end

  subgraph DADOS["🗄️ Persistência"]
    DB[("🗃️ Banco de dados do ConectaGlobal")]
  end

  WEB --> AUTH
  MOBILE --> AUTH
  WEB --> OPORT
  MOBILE --> OPORT
  WEB --> CAND
  MOBILE --> CAND
  AUTH --> OPORT
  AUTH --> CAND
  AUTH --> ADMIN
  OPORT --> CONV
  CAND --> ELEG
  CAND --> DOC
  CAND --> NOTIF
  CAND --> REL
  WEB --> PREP
  MOBILE --> PREP
  WEB --> COL
  MOBILE --> COL

  OPORT --> DB
  CONV --> DB
  ELEG --> DB
  CAND --> DB
  DOC --> DB
  NOTIF --> DB
  REL --> DB
  PREP --> DB
  COL --> DB
  ADMIN --> DB

  classDef front fill:#E8F2FF,stroke:#3676C8,color:#17365D,stroke-width:1.5px;
  classDef service fill:#EAF7F0,stroke:#39865B,color:#174B30,stroke-width:1.5px;
  classDef storage fill:#FFF1DF,stroke:#C77B20,color:#653B0B,stroke-width:1.5px;
  class WEB,MOBILE front;
  class AUTH,OPORT,CONV,ELEG,CAND,DOC,NOTIF,REL,PREP,COL,ADMIN service;
  class DB storage;
```

## 3. Diagrama de Implantação

```mermaid
flowchart TB
  subgraph DISPOSITIVO["👤 Dispositivo do usuário"]
    BROWSER["🌐 Navegador Web"]
    APPCLIENT["📱 Acesso por dispositivo móvel"]
  end

  subgraph SERVIDOR["☁️ Ambiente de aplicação proposto"]
    FRONT["🖥️ Interface do ConectaGlobal"]
    API["⚙️ API / Serviços de negócio"]
  end

  subgraph PERSISTENCIA["🗄️ Ambiente de dados proposto"]
    DATABASE[("🗃️ Servidor de banco de dados")]
  end

  BROWSER -->|"HTTPS — conexão segura (proposta)"| FRONT
  APPCLIENT -->|"HTTPS — conexão segura (proposta)"| FRONT
  FRONT --> API
  API -->|"Acesso controlado aos dados"| DATABASE

  classDef client fill:#E8F2FF,stroke:#3676C8,color:#17365D,stroke-width:1.5px;
  classDef app fill:#EAF7F0,stroke:#39865B,color:#174B30,stroke-width:1.5px;
  classDef data fill:#FFF1DF,stroke:#C77B20,color:#653B0B,stroke-width:1.5px;
  class BROWSER,APPCLIENT client;
  class FRONT,API app;
  class DATABASE data;
```

## Observações

- A implantação é uma representação lógica proposta, não uma infraestrutura já contratada ou implementada.
- Não foram incluídos sistemas externos porque nenhuma integração técnica foi confirmada na documentação-base.
- A DRI não aparece como ator, componente ou nó: é somente referência visual para a etapa de telas.
- O ator **Equipe do NEI** foi preservado como responsável pelas funções de gestão.
- Para rastreabilidade, os códigos CDU correspondem à especificação em [`docs/08-casos-de-uso.md`](../docs/08-casos-de-uso.md), e os atores AT à relação em [`docs/02-partes-interessadas-e-atores.md`](../docs/02-partes-interessadas-e-atores.md).
