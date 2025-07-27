# Desafio 04 – Tipos de Dados

Neste desafio, será feita uma comparação entre os sistemas de **tipagem** de três linguagens de programação: **Python**, **C** e **JavaScript**. Serão apresentados exemplos comentados para destacar as características de **tipagem estática/dinâmica**, **forte/fraca** e o comportamento em **conversões de tipos**.

---

## 🐍 Python

### Características:
- **Tipagem Dinâmica**: o tipo é definido em tempo de execução.
- **Tipagem Forte**: não permite misturar tipos diferentes sem conversão explícita.

### Exemplo:

```python
x = 10          # x é um inteiro
print(type(x))  # <class 'int'>

x = "dez"       # Agora x é uma string
print(type(x))  # <class 'str'>

# Operação inválida entre tipos diferentes
print("10" + 5)  # TypeError
```
### Comentário:
Em Python, variáveis não têm tipo fixo. O tipo é atribuído ao valor, não à variável. Entretanto, tentar combinar tipos incompatíveis gera erro.
## 🧱 C
### Características:
- **Tipagem Estática:** o tipo é definido em tempo de compilação.
- **Tipagem Fraca/Moderada:** permite algumas conversões implícitas.

### Exemplo:
```
#include <stdio.h>

int main() {
    int x = 10;
    // x = "dez"; // Erro de compilação: tipos incompatíveis

    float y = 5.7;
    int z = (int)y; // Cast explícito
    printf("%d\n", z); // Saída: 5

    return 0;
}
```

### Comentário:
Em C, você deve declarar o tipo da variável. Conversões entre tipos são possíveis com casting, mas misturar tipos errados sem cuidado pode gerar comportamento indefinido.

## 🌐 JavaScript
### Características:
- **Tipagem Dinâmica:** tipos são atribuídos em tempo de execução.
- **Tipagem Fraca:** converte automaticamente entre tipos quando necessário.

### Exemplo:
```
let x = 10;
x = "dez"; // Permitido

console.log(typeof x); // string

console.log("10" + 5); // "105" → coerção automática para string
console.log("10" - 5); // 5   → coerção automática para número
```
### Comentário:
JavaScript realiza coerção implícita entre tipos. Isso facilita a programação rápida, mas pode causar bugs difíceis de detectar se não for bem controlado.

## 📝 Comparação Geral

| Linguagem  | Tipagem  | Forte ou Fraca | Conversão Automática? | Observações                             |
| ---------- | -------- | -------------- | --------------------- | --------------------------------------- |
| Python     | Dinâmica | Forte          | Não                   | Erros em operações inválidas            |
| C          | Estática | Fraca/Moderada | Parcialmente          | Requer casts explícitos em muitos casos |
| JavaScript | Dinâmica | Fraca          | Sim                   | Pode causar erros inesperados           |

## ✅ Conclusão
Cada linguagem apresenta um sistema de tipos com diferentes graus de rigidez e flexibilidade. Escolher uma ou outra depende do objetivo: segurança e controle (C), agilidade com segurança (Python), ou flexibilidade para scripts e web (JavaScript).
