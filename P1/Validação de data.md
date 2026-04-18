
```mermaid
flowchart TD
    A([Início]) --> B[Leia dia, mês e ano]
    B --> C{Mês valido (1-12)}

    C -- Não --> Z[Data inválida]
    Z --> F([Fim])

    C -- Sim --> D{fevereiro}

    D -- Sim --> E{Ano bissexto}
    E -- Sim --> G{Dia entre 1 e 29}
    E -- Nao --> H{Dia entre 1 e 28}

    G -- Sim --> V[Data válida]
    G -- Nao --> Z

    H -- Sim --> V
    H -- Nao --> Z

    D -- Nao --> I{Mês 4 6 9 11}
    I -- Sim --> J{Dia entre 1 e 30}
    I -- Nao --> K{Dia entre 1 e 31}

    J -- Sim --> V
    J -- Nao --> Z

    K -- Sim --> V
    K -- Nao --> Z

    V --> F
