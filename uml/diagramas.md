# Diagramas — ConectaGlobal

## 1. Observação metodológica

Os diagramas abaixo representam uma visão conceitual da solução. Não são decisões técnicas aprovadas pela TI da Unifor. Componentes, infraestrutura, integrações, disponibilidade e capacidade deverão ser confirmados antes de qualquer implementação.

Os casos de uso detalhados estão em [docs/07-casos-de-uso.md](../docs/07-casos-de-uso.md).

## 2. Diagrama geral de casos de uso

```mermaid
flowchart LR
    Estudante["AT-01 Estudante"]
    Operador["AT-02 Operador NEI/DRI"]
    Coordenador["AT-03 Coordenador"]
    Admin["AT-04 Administrador"]
    Academico["AT-05 Sistema acadêmico"]
    SSO["AT-06 SSO institucional"]
    Mensageria["AT-07 Serviço de mensagens"]

    subgraph CG["ConectaGlobal"]
      UC1(("CDU-01 Manter oportunidade"))
      UC2(("CDU-02 Consultar oportunidades"))
      UC3(("CDU-03 Verificar pré-elegibilidade"))
      UC4(("CDU-04 Registrar manifestação"))
      UC5(("CDU-05 Acompanhar manifestação"))
      UC6(("CDU-06 Analisar manifestação"))
      UC7(("CDU-07 Consultar documentos"))
      UC8(("CDU-08 Enviar notificação"))
      UC9(("CDU-09 Consultar painel/relatórios"))
      UC10(("CDU-10 Autenticar/controlar acesso"))
    end

    Estudante --- UC2
    Estudante --- UC3
    Estudante --- UC4
    Estudante --- UC5
    Estudante --- UC7
    Operador --- UC1
    Operador --- UC6
    Operador --- UC9
    Coordenador --- UC9
    Admin --- UC10
    Estudante --- UC10
    Operador --- UC10
    SSO --- UC10
    Academico --- UC3
    Mensageria --- UC8
    UC1 -. evento .-> UC8
    UC6 -. evento .-> UC8
```

## 3. Diagrama conceitual de componentes

```mermaid
flowchart TB
    Browser["Navegador do usuário"]
    UI["Interface web responsiva"]
    API["Camada de serviços / API"]
    Auth["Autenticação e autorização"]
    Opp["Gestão de oportunidades"]
    Elig["Critérios e pré-elegibilidade"]
    Manifest["Manifestações e análise"]
    Notify["Notificações"]
    Report["Consultas e relatórios"]
    Audit["Histórico e auditoria"]
    DB[("Base de dados")]
    Files[("Armazenamento de documentos")]
    SSO["SSO institucional — integração proposta"]
    Acad["Sistema acadêmico — integração proposta"]
    Mail["Serviço de mensagens — integração proposta"]

    Browser --> UI
    UI --> API
    API --> Auth
    API --> Opp
    API --> Elig
    API --> Manifest
    API --> Notify
    API --> Report
    API --> Audit
    Auth --> DB
    Opp --> DB
    Opp --> Files
    Elig --> DB
    Elig -. se autorizado .-> Acad
    Manifest --> DB
    Notify -. se aprovado .-> Mail
    Report --> DB
    Audit --> DB
    Auth -. se aprovado .-> SSO
```

## 4. Diagrama conceitual de implantação

```mermaid
flowchart TB
    User["Estudante / Operador / Coordenador"]
    Client["Navegador web"]
    Edge["Camada de acesso web"]
    App["Ambiente de aplicação"]
    DB[("Banco de dados")]
    Storage[("Armazenamento de documentos")]
    Backup[("Backup")]
    SSO["SSO institucional (dependência externa)"]
    Academic["Sistema acadêmico (dependência externa)"]
    Email["Serviço de mensagens (dependência externa)"]

    User --> Client
    Client --> Edge
    Edge --> App
    App --> DB
    App --> Storage
    DB --> Backup
    Storage --> Backup
    App -. integração autorizada .-> SSO
    App -. integração autorizada .-> Academic
    App -. integração autorizada .-> Email
```

## 5. Limitações e decisões em aberto

- Os diagramas de componentes e implantação não determinam tecnologia, provedor, número de servidores, balanceador ou arquitetura de alta disponibilidade.
- A integração com SSO, sistema acadêmico e serviço de mensagens é hipotética.
- A camada de armazenamento de documentos é proposta; formato, limite, retenção e acesso precisam de definição.
- A participação do coordenador é potencial e depende de validação.
- O diagrama geral não substitui diagramas de atividades UML por fluxo, que podem ser produzidos durante o detalhamento dos casos de uso.
- A modelagem deve ser revisada quando as regras de negócio e os atores forem confirmados.

## 6. Histórico

| Versão | Data | Alteração |
|---|---|---|
| 1.0 | 26/11/2026 | Atualização dos diagramas e explicitação de integrações e arquitetura como hipóteses. |
