# Diagramas do Projeto - DISC Framework

Este arquivo contém diagramas que podem ser visualizados ou importados para ferramentas como Excalidraw (via Mermaid).

## Fluxo de Avaliação DISC

```mermaid
graph TD
    A[Usuário chega à Home] --> B{Logado?}
    B -- Não --> C[Cadastro/Login via Allauth]
    B -- Sim --> D[Acessar Teste DISC]
    C --> D
    D --> E[Preencher Questionário]
    E --> F[Processamento de Médias]
    F --> G[Salvar ResultadoDISC]
    G --> H[Associar ao Usuário]
    H --> I[Exibir Resultado Personalizado]
    I --> J[Insights de Carreira]
```

## Arquitetura de Módulos

```mermaid
graph LR
    subgraph Django Project
    A[assessment_disc_project]
    end
    
    A --> B(core)
    A --> C(disc)
    A --> D(user_auth)
    
    B --> |Templates/Static| E[Web Pages]
    C --> |Logic| F[Assessment Engine]
    D --> |Identity| G[User Management]
    
    F --> H[(Database)]
    G --> H
```

## Modelo de Dados

```mermaid
classDiagram
    class CustomUser {
        +String email
        +String username
        +ForeignKey outcome_disc
    }
    class ResultadoDISC {
        +Float dominante
        +Float influente
        +Float estabilidade
        +Float conformado
        +DateTime created_at
    }
    class Pergunta {
        +String texto
        +String perfil
    }
    CustomUser "1" --> "0..1" ResultadoDISC : possui
    Pergunta "n" --o "1" ResultadoDISC : contribui
```
