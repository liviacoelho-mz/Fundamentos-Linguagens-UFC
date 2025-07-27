# Desafio 06 – Subprogramas

Este desafio consiste em implementar exemplos de funções que demonstrem a **passagem de parâmetros por valor e por referência** em linguagens diferentes.

As linguagens utilizadas foram **C** e **Python**.

---

## 🧱 Exemplo em C

### Código:

```c
#include <stdio.h>

// Passagem por valor
void dobrar_valor(int x) {
    x = x * 2;
}

// Passagem por referência
void dobrar_referencia(int *x) {
    *x = *x * 2;
}

int main() {
    int a = 10;

    dobrar_valor(a);
    printf("Após dobrar_valor: %d\n", a);  // Ainda é 10

    dobrar_referencia(&a);
    printf("Após dobrar_referencia: %d\n", a);  // Agora é 20

    return 0;
}
```
### Comentário:
- Na função `dobrar_valor`, a variável é copiada: alterações não afetam o original.
- Na função `dobrar_referencia`, usamos um ponteiro: alterações afetaram diretamente a variável original.

## 🐍 Exemplo em Python


### Código:
```
# Passagem por valor com tipo imutável (int)
def dobrar_valor(x):
    x = x * 2
    print("Dentro da função (int):", x)

# Passagem por referência com tipo mutável (lista)
def dobrar_lista(lst):
    for i in range(len(lst)):
        lst[i] *= 2

a = 10
dobrar_valor(a)
print("Fora da função (int):", a)  # Ainda é 10

lista = [1, 2, 3]
dobrar_lista(lista)
print("Fora da função (lista):", lista)  # [2, 4, 6]
```
### Comentário:
- Em Python, inteiros são imutáveis, então x é apenas uma cópia.
- Listas são mutáveis, então lst é uma referência: alterações afetam a variável original fora da função.

## ✅ Conclusão
Cada linguagem trata a passagem de parâmetros de forma distinta:
- C diferencia claramente por valor (cópia) e por referência (ponteiros).
- Python não tem ponteiros, mas o comportamento muda com base no tipo de dado:
    - Imutáveis → cópia do valor (como se fosse "por valor")
    -  Mutáveis → referência ao objeto original
Essa distinção é essencial para entender os efeitos colaterais das funções em diferentes linguagens.
