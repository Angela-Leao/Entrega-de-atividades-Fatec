# Pontuação de motorista

```mermaid
flowchart TD
    A([Inicio]) --> B[Leia velocidade permitida]
    B -->C[Leia velocidade do veículo]
    
    C -->D[Cálculo de excesso = vel_veiculo - vel_permitida]

    D -->E{Excesso <= 0}

    E --Sim -->F[Sem infração= 0 pontos]
    E --Não -->G[Cáculo de percentual = (excesso / vel_permitida) * 100]

    G -->H{Percentual <= 20}

    H --Sim-->I[Infração leve = 3 pontos]
    H --Não -->J{Percentual > 20 <=50}

    J --Sim -->K[Infração grave = 5 pontos]
    J --Nao -->L[Infração gravíssima = 7 pontos]

    F --> M[Mostrar resultados]
    I --> M
    K --> M
    L --> M

    M --> N([Fim])
```
