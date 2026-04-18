```mermaid
flowchart TD
    A([Início]) --> B[Leia A, B, C]

    B --> C{A < B + C?}
    C -->|Não| X[Não forma triângulo]
    X --> Z([Fim])

    C -->|Sim| D{B < A + C?}
    D -->|Não| X

    D -->|Sim| E{C < A + B?}
    E -->|Não| X

    E -->|Sim| F{A == B e B == C?}
    
    F -->|Sim| G[Equilatero]
    G --> Z

    F -->|Não| H{A == B ou A == C ou B == C?}
    
    H -->|Sim| I[Isosceles]
    I --> Z

    H -->|Não| J[Escaleno]
    J --> Z
