# DER – Diagrama de Implementação Relacional

```mermaid
erDiagram
    TAREFA {
        string id PK
        string titulo
        string descricao
        date data
        string hora
        boolean concluida
        string categoria_id FK
    }

    CATEGORIA {
        string id PK
        string nome
        string cor
    }

    NOTIFICACAO {
        string id PK
        string tarefa_id FK
        date data
        string hora
        boolean ativada
    }

    CATEGORIA ||--o{ TAREFA : "classifica"
    TAREFA ||--o{ NOTIFICACAO : "agenda"