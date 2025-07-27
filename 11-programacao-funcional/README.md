# Desafio 11 – Programação Funcional

Neste desafio, implementamos uma solução no paradigma **funcional**, utilizando **recursão** e **funções de alta ordem** em **Python**.

---

## 🎯 Objetivo:

Criar um programa funcional que:
- Filtre notas aprovadas (>= 7)
- Some essas notas
- Conte quantas foram aprovadas usando **recursão**

---

## 🧑‍💻 Código em Python:

```python
from functools import reduce

# Lista de notas
notas = [5.5, 8.0, 9.5, 6.7, 7.2, 4.3, 10.0]

# Função de alta ordem: filtra as notas maiores ou iguais a 7
notas_aprovadas = list(filter(lambda nota: nota >= 7, notas))

# Função de alta ordem: soma as notas aprovadas
soma_aprovadas = reduce(lambda x, y: x + y, notas_aprovadas)

# Função recursiva para contar elementos
def contar(lista):
    if not lista:
        return 0
    return 1 + contar(lista[1:])

# Chamadas
print("Notas:", notas)
print("Aprovadas:", notas_aprovadas)
print("Soma das aprovadas:", soma_aprovadas)
print("Quantidade de aprovadas:", contar(notas_aprovadas))
```
### 🔍 Conceitos aplicados:

| Conceito             | Onde foi usado                                     |
| -------------------- | -------------------------------------------------- |
| Função de alta ordem | `filter()` e `reduce()` com `lambda`               |
| Recursão             | Função `contar()`                                  |
| Imutabilidade        | `notas_aprovadas` é uma nova lista                 |
| Funções puras        | Todas as funções não modificam nada fora do escopo |

### 🧠 Por que programação funcional?
- Facilita reutilização de código
- Reduz efeitos colaterais
- Mais legibilidade e clareza para operações com listas, transformações e lógica declarativa

## ✅ Conclusão
A programação funcional permite resolver problemas de forma mais expressiva e concisa. Neste exemplo, usamos funções puras, recursão e funções de alta ordem, simulando um mini sistema de avaliação de notas com foco na clareza e modularidade do código.
