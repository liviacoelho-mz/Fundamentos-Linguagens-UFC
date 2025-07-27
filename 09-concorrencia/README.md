# Desafio 09 – Concorrência

Este desafio apresenta um exemplo de **concorrência com threads**, utilizando a linguagem **Python**. Também é explicada a diferença entre **threads** e **processos**.

---

## 🧵 Diferença entre Threads e Processos

| Conceito   | Threads                                 | Processos                                  |
|------------|-----------------------------------------|---------------------------------------------|
| Memória    | Compartilham o mesmo espaço             | Isolados uns dos outros                     |
| Criação    | Mais leves e rápidas                    | Mais pesados (carga maior no SO)            |
| Comunicação| Fácil (mesma memória)                   | Mais complexa (precisa de IPC)              |
| Uso comum  | Tarefas leves que rodam em paralelo     | Execução isolada, como scripts diferentes   |

---

## ⚙️ Exemplo: Simulação de Tarefas Concorrentes

### Código em Python:

```python
import threading
import time

def baixar_arquivos():
    for i in range(1, 6):
        print(f"📥 Baixando arquivo {i}")
        time.sleep(1)

def ler_arquivos():
    for letra in ['A', 'B', 'C', 'D', 'E']:
        print(f"📖 Lendo arquivo {letra}")
        time.sleep(1)

# Criando as threads
t1 = threading.Thread(target=baixar_arquivos)
t2 = threading.Thread(target=ler_arquivos)

# Iniciando as threads
t1.start()
t2.start()

# Espera ambas terminarem
t1.join()
t2.join()

print("✅ Tarefas finalizadas!")
```
### 🔍 Explicação
- Criamos duas funções que simulam tarefas independentes.
- Usamos o módulo `threading` do Python para rodá-las simultaneamente.
- `start()` inicia a execução paralela.
- `join()` garante que o programa espere ambas as tarefas terminarem.

### 🧠 Por que usar concorrência?
Concorrência é útil quando:
- Queremos melhorar o desempenho em tarefas paralelizáveis.
- Existem operações de espera (como leitura de arquivos, requisições web).
- Queremos uma interface responsiva que não trave.

## ✅ Conclusão
Com poucas linhas, conseguimos simular a execução paralela de tarefas. A concorrência com threads é poderosa em aplicações que precisam manipular múltiplas tarefas simultâneas de forma eficiente.
Para cargas muito pesadas (CPU-bound), o ideal seria usar o módulo `multiprocessing`.
