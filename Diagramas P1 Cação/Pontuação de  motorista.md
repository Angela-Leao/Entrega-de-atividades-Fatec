# Pontuação de motorista

```mermaid
flowchart TD
    A([Inicio]) --> B[Leia velocidade permitida]
    B-->C[Leia velocidade do veiculo]    
    C-->D[Calculo de excesso = vel_veiculo - vel_permitida]

    D-->E{Excesso <= 0?}

    E--Sim --> F[Sem infracao\n0 pontos]
    E--Nao --> G[Calculo de percentual = (excesso / vel_permitida) * 100]

    G-->H{Percentual <= 20?}

    H--Sim --> I[Infracao leve\n3 pontos]
    H--Nao --> J{Percentual <= 50?}

    J--Sim --> K[Infracao grave\n5 pontos]
    J--Nao --> L[Infracao gravissima\n7 pontos]

    F-->M[Mostrar resultados]
    I-->M
    K-->M
    L-->M

    M-->N([Fim])
```
