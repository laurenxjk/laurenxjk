def calcular_operacao():
    operacao = input().strip()
    
    matriz = []
    for linha_matriz in range(12):
        linha = []
        for coluna_matriz in range(12):
            linha.append(float(input()))
        matriz.append(linha)
    
    elementos_acima_diagonal_principal = []
    for linha_matriz in range(12):
        for coluna_matriz in range(12):
            if coluna_matriz < linha_matriz:
                elementos_acima_diagonal_principal.append(matriz[linha_matriz][coluna_matriz])
    
    if operacao == 'S':
        resultado = sum(elementos_acima_diagonal_principal)
    elif operacao == 'M':
        resultado = sum(elementos_acima_diagonal_principal) / len(elementos_acima_diagonal_principal)
    
    print(f"{resultado:.1f}")

if __name__ == "__main__":
    calcular_operacao()
