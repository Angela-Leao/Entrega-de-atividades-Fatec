
```mermaid
flowchart TD
    A([Início]) --> B[Leia dia, mês e ano]
    B --> C{Meses válidos são de 1 a 12}

    C -- Não --> Z[Data inválida]
    Z --> F([Fim])

    C -- Sim --> D{fevereiro}

    D -- Sim --> E{Ano bissexto}
    E -- Sim --> G{Dias entre 1 e 29}
    E -- Não --> H{Dias entre 1 e 28}

    G -- Sim --> V[Data válida]
    G -- Não --> Z

    H -- Sim --> V
    H -- Não --> Z

    D -- Não --> I{Meses 4, 6,9, 11}
    I -- Sim --> J{Dia entre 1 e 30}
    I -- Não --> K{Dia entre 1 e 31}

    J -- Sim --> V
    J -- Não --> Z

    K -- Sim --> V
    K -- Não --> Z

    V --> F
