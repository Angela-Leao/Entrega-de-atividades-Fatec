
```mermaid
flowchart TD
A([Início]) --> B[Leia dia, mês e ano]
B --> C{Mês válido? (1-12)}
C -->|Não| Z[Mostrar "Data inválida"] --> F([Fim])
C -->|Sim| D{Mês = 2?}
D -->|Sim| E{Ano bissexto?}
E -->|Sim| G{Dia entre 1 e 29?}
E -->|Não| H{Dia entre 1 e 28?}
G -->|Sim| V[Mostrar "Data válida"] --> F
G -->|Não| Z
H -->|Sim| V
H -->|Não| Z
D -->|Não| I{Mês ∈ 4,6,9,11?}
I -->|Sim| J{Dia entre 1 e 30?}
I -->|Não| K{Dia entre 1 e 31?}
J -->|Sim| V
J -->|Não| Z
K -->|Sim| V
K -->|Não| Z
