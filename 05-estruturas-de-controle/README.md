# Desafio 05 – Estruturas de Controle

Este desafio consiste na criação de um programa simples com uso de **estruturas de seleção, repetição e controle de fluxo**, dentro de um contexto original. A linguagem utilizada foi **Python**.

---

## 💰 Contexto: Cofrinho Virtual

Criamos um programa interativo em que o usuário pode simular um cofrinho virtual, com as seguintes funcionalidades:
- Depositar valores
- Sacar valores
- Ver saldo
- Encerrar o programa

O código usa:
- `while` como laço de repetição principal
- `if/elif/else` para seleção de ações
- `break` para sair do loop
- `continue` para ignorar operações inválidas

---

## 🧑‍💻 Código:

```python
saldo = 0.0

print("=== Bem-vindo ao Cofrinho Virtual ===")

while True:
    print("\nEscolha uma opção:")
    print("1 - Depositar")
    print("2 - Sacar")
    print("3 - Ver saldo")
    print("4 - Sair")

    opcao = input("Digite o número da opção desejada: ")

    if opcao == "1":
        valor = float(input("Digite o valor para depositar: "))
        if valor <= 0:
            print("Valor inválido.")
            continue
        saldo += valor
        print(f"Depósito de R${valor:.2f} realizado com sucesso!")

    elif opcao == "2":
        valor = float(input("Digite o valor para sacar: "))
        if valor > saldo:
            print("Saldo insuficiente.")
            continue
        saldo -= valor
        print(f"Saque de R${valor:.2f} realizado com sucesso!")

    elif opcao == "3":
        print(f"Seu saldo atual é: R${saldo:.2f}")

    elif opcao == "4":
        print("Encerrando o cofrinho... Até logo!")
        break

    else:
        print("Opção inválida. Tente novamente.")
```
## ✅ Estruturas usadas:
```
| Estrutura      | Onde foi usada                               |
| -------------- | -------------------------------------------- |
| `while`        | Loop principal para manter o menu ativo      |
| `if/elif/else` | Verificação da opção escolhida               |
| `break`        | Encerra o programa quando o usuário digita 4 |
| `continue`     | Ignora depósitos/saques inválidos            |
```
## 🧠 Conclusão
Este exercício mostra como estruturas básicas de controle podem ser usadas para simular sistemas simples. A lógica do programa é flexível e pode ser expandida com facilidade para incluir funcionalidades como histórico de transações, limites diários, entre outros.


