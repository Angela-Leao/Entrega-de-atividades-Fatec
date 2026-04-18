# Pontuação de motorista
```mermaid

flowchart TD
    A([Início]) --> B[Velocidade permitida]
    B --> C[Velocidade veículo]
    C --> D[Excesso]

    D --> E{Excesso <= 0}
    E -- Sim --> F[Sem infração]
    E -- Não --> G[Cálculo percentual]

    G --> H{Percentual <= 20%}
    H -- Sim --> I[Leve - 3 pontos]
    H -- Não --> J{Percentual <= 50}

    J -- Sim --> K[Grave - 5 pontos]
    J -- Não --> L[Gravíssima - 7 pontos]

    F --> M[Resultado]
    I --> M
    K --> M
    L --> M

    M --> N([Fim])
```
