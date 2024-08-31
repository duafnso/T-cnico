# Tecnico

1 -- C --
int INDICE = 13, SOMA = 0, K = 0;

Enquanto K < INDICE faça {
   K = K + 1;
   SOMA = SOMA + K;
}

Imprimir(SOMA);

Portanto, o valor final da variável SOMA será 91.


2 -- Python -- 

def fibonacci(n):
    a, b = 0, 1
    while b < n:
        a, b = b, a + b
    return b == n or n == 0

numero = int(input("Informe um número: "))

if fibonacci(numero):
    print(f"O número {numero} pertence à sequência de Fibonacci.")
else:
    print(f"O número {numero} não pertence à sequência de Fibonacci.")

3 -- Python --
import json

# Exemplo de dados em JSON
dados = '''[
    {"dia": 1, "valor": 22174.1664},
    {"dia": 2, "valor": 24537.6698},
  _ {"dia": 3, "valor": 26139.6134},
    {"dia": 4, "valor": 0.0},
    {"dia": 5, "valor": 0.0},
    {"dia": 6, "valor": 26742.6612},
    {"dia": 7, "valor": 0.0},
    {"dia": 8, "valor": 42889.2258},
    {"dia": 9, "valor": 46251.174},
    {"dia": 10, "valor": 11191.4722},
    {"dia": 11, "valor": 0.0},
    {"dia": 12, "valor": 0.0},
    {"dia": 13, "valor": 3847.4823},
    {"dia": 14, "valor": 373.7838},
    {"dia": 15, "valor": 2659.7563},
    {"dia": 16, "valor": 48924.2448},
    {"dia": 17, "valor": 18419.2614},
    {"dia": 18, "valor": 0.0},
    {"dia": 19, "valor": 0.0},
    {"dia": 20, "valor": 35240.1826},
    {"dia": 21, "valor": 43829.1667},
    {"dia": 22, "valor": 18235.6852},
    {"dia": 23, "valor": 4355.0662},
    {"dia": 24, "valor": 13327.1025},
    {"dia": 25, "valor": 0.0},
    {"dia": 26, "valor": 0.0},
    {"dia": 27, "valor": 25681.8318},
    {"dia": 28, "valor": 1718.1221},
    {"dia": 29, "valor": 13220.495},
    {"dia": 30, "valor": 8414.61}
]'''

faturamento = json.loads(dados)

# Filtrar os dias com faturamento acima de 0
valores = [dia["valor"] for dia in faturamento if dia["valor"] > 0]

menor_valor = min(valores)
maior_valor = max(valores)
media_mensal = sum(valores) / len(valores)

dias_acima_da_media = sum(1 for valor in valores if valor > media_mensal)

print(f"Menor valor de faturamento: {menor_valor}")
print(f"Maior valor de faturamento: {maior_valor}")
print(f"Dias com faturamento acima da média: {dias_acima_da_media}")

4 -- Python --
faturamento = {
    "SP": 67836.43,
    "RJ": 36678.66,
    "MG": 29229.88,
    "ES": 27165.48,
    "Outros": 19849.53
}

total = sum(faturamento.values())

for estado, valor in faturamento.items():
    percentual = (valor / total) * 100
    print(f"{estado}: {percentual:.2f}%")


5 -- Python --

def inverter_string(s):
    invertida = ""
    for char in s:
        invertida = char + invertida
    return invertida

string = input("Informe uma string: ")
print(f"String invertida: {inverter_string(string)}")
