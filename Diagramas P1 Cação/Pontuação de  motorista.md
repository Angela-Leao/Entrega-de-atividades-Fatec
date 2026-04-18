# Pontuação de motorista
```mermaid

flowchart TD
    A([Início]) --> B[Velocidade permitida]
    B --> C[Velocidade veículo]
    C --> D[Excesso]

    D --> E{Excesso <= 0}
    E -- Sim --> F[Sem infração]
    E -- Nao --> G[Cálculo percentual]

    G --> H{Percentual <= 20}
    H -- Sim --> I[Leve - 3 pontos]
    H -- Nao --> J{Percentual <= 50}

    J -- Sim --> K[Grave - 5 pontos]
    J -- Nao --> L[Gravíssima - 7 pontos]

    F --> M[Resultado]
    I --> M
    K --> M
    L --> M

    M --> N([Fim])
```
