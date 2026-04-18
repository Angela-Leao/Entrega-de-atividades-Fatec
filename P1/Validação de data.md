
```mermaid
flowchart TD
    A([Inicio]) --> B[Leia dia, mes e ano]
    B --> C{Mes valido 1-12}

    C -- Nao --> Z[Data invalida]
    Z --> F([Fim])

    C -- Sim --> D{Mes igual a 2}

    D -- Sim --> E{Ano bissexto}
    E -- Sim --> G{Dia entre 1 e 29}
    E -- Nao --> H{Dia entre 1 e 28}

    G -- Sim --> V[Data valida]
    G -- Nao --> Z

    H -- Sim --> V
    H -- Nao --> Z

    D -- Nao --> I{Mes 4 6 9 11}
    I -- Sim --> J{Dia entre 1 e 30}
    I -- Nao --> K{Dia entre 1 e 31}

    J -- Sim --> V
    J -- Nao --> Z

    K -- Sim --> V
    K -- Nao --> Z

    V --> F
