# Diagrama de Classes – TimeX

```mermaid
classDiagram

class Tarefa {
  +id: string
  +titulo: string
  +descricao: string
  +data: Date
  +hora: string
  +concluida: boolean
  +categoriaId: string
}

class Categoria {
  +id: string
  +nome: string
  +cor: string
}

class Notificacao {
  +id: string
  +tarefaId: string
  +data: Date
  +hora: string
  +ativada: boolean
}

Tarefa --> Categoria : pertence a
Tarefa --> Notificacao : pode ter