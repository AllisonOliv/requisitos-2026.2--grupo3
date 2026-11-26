# Diagramas UML — ConectaGlobal

Os modelos abaixo estão em PlantUML para manter a notação UML explícita. O arquivo-fonte completo está em [`diagramas.puml`](diagramas.puml).

## 1. Diagrama de Casos de Uso

```plantuml
@startuml
left to right direction
skinparam packageStyle rectangle
actor "Estudante da Unifor" as Estudante
actor "Responsável editorial\n(do protótipo acadêmico)" as Editor
actor "Portal oficial da DRI" as DRI
rectangle "ConectaGlobal" {
  usecase "Consultar Catálogo\nde Programas" as UC01
  usecase "Pesquisar e Filtrar\nProgramas" as UC02
  usecase "Consultar Detalhes\ne Critérios" as UC03
  usecase "Consultar Próximos Passos\ne Acessar Canal Oficial" as UC04
  usecase "Manter Conteúdo\nInformativo do Protótipo" as UC05
}
Estudante --> UC01
Estudante --> UC02
Estudante --> UC03
Estudante --> UC04
Editor --> UC05
DRI --> UC04 : link externo / fonte
@enduml
```

## 2. Diagrama de Componentes

```plantuml
@startuml
skinparam componentStyle rectangle
actor "Estudante" as Estudante
component "Interface Web" as UI
component "Catálogo e Pesquisa" as Catalogo
component "Detalhes e Conteúdo" as Conteudo
component "Referências e Links Oficiais" as Links
database "Repositório de Conteúdo\nacadêmico" as DB
component "Portal DRI\n(externo)" as DRI
Estudante --> UI
UI --> Catalogo
UI --> Conteudo
Catalogo --> DB
Conteudo --> DB
Conteudo --> Links
Links ..> DRI : navegação externa\nsem API
@enduml
```

## 3. Diagrama de Implantação

```plantuml
@startuml
node "Dispositivo do estudante" {
  artifact "Navegador Web" as Browser
}
node "Ambiente de demonstração\n(ConectaGlobal)" {
  node "Hospedagem do protótipo" {
    artifact "Aplicação Web" as App
    database "Conteúdo demonstrativo" as DB
  }
}
cloud "Internet" as Internet
node "Portal oficial da DRI" as DRI
Browser --> Internet
Internet --> App
App --> DB
Browser ..> DRI : abre link externo
@enduml
```

## Notas
- O portal DRI é acessado por navegação externa; não há API ou integração presumida.
- O repositório de conteúdo é conceitual para o protótipo; não representa banco institucional.
- O responsável editorial é um papel do protótipo acadêmico, não uma atribuição oficial da DRI.
