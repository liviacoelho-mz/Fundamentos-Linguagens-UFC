# Desafio 10 – Gerenciamento de Memória

Este desafio apresenta uma comparação entre o gerenciamento de memória em duas linguagens de programação com paradigmas distintos: **C** e **Java**.

---

## 🧠 O que é gerenciamento de memória?

É o processo de **alocar**, **usar** e **liberar** memória durante a execução de um programa. Ele pode ser feito **manualmente** ou de forma **automática** pela linguagem.

---

## 🔍 Comparativo entre C e Java

| Característica                     | C                                          | Java                                      |
|-----------------------------------|--------------------------------------------|-------------------------------------------|
| Tipo de gerenciamento             | Manual                                     | Automático (Garbage Collector)            |
| Alocação de memória               | Via `malloc`, `calloc`                     | Via `new`                                  |
| Liberação de memória              | Via `free`                                 | Coletor de lixo decide quando liberar      |
| Riscos comuns                     | Vazamento de memória, uso de ponteiro inválido | Pausas do GC, consumo imprevisível de memória |
| Controle do programador           | Total controle                             | Menor controle, maior segurança            |
| Facilidade de uso                 | Exige cuidado e atenção                    | Mais fácil para o desenvolvedor            |
| Desempenho                        | Muito eficiente quando bem gerenciado      | Pode ser afetado pelo GC em tempo real     |

---

## 🧪 Exemplos

### Em C (manual):

```c
#include <stdio.h>
#include <stdlib.h>

int main() {
    int *ptr = (int*) malloc(sizeof(int));
    *ptr = 42;
    printf("%d\n", *ptr);
    free(ptr); // Liberação manual
    return 0;
}
```
## Em Java (automático):
```
public class Exemplo {
    public static void main(String[] args) {
        Integer x = new Integer(42);
        System.out.println(x);
        // Não precisa liberar memória: o GC faz isso!
    }
}
```
## ✅ Conclusão
A forma como cada linguagem trata a memória afeta a performance, a segurança e a complexidade do desenvolvimento.
- C exige mais responsabilidade, mas oferece controle total.
- Java abstrai o processo, permitindo ao desenvolvedor focar na lógica sem se preocupar com a liberação manual.
Ambas as abordagens têm vantagens, e a escolha depende do contexto da aplicação.
