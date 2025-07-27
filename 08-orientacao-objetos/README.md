# Desafio 08 – Programação Orientada a Objetos

Neste desafio, foi modelada uma hierarquia simples de classes no domínio **veículos**, utilizando a linguagem **Python**. O objetivo é demonstrar os conceitos de:
- **Herança**
- **Encapsulamento**
- **Polimorfismo**

---

## 🚗 Domínio: Veículos

Criamos uma **classe base** `Veiculo`, e duas subclasses `Carro` e `Moto`.

Cada veículo possui:
- Atributos: `marca`, `modelo`, `ano`
- Métodos: `ligar()` e `exibir_informacoes()`

As subclasses sobrescrevem o método `ligar()` para comportamentos específicos.

---

## 🧑‍💻 Código:

```python
class Veiculo:
    def __init__(self, marca, modelo, ano):
        self.marca = marca
        self.modelo = modelo
        self.ano = ano

    def ligar(self):
        print("O veículo está ligando...")

    def exibir_informacoes(self):
        print(f"{self.ano} {self.marca} {self.modelo}")


class Carro(Veiculo):
    def ligar(self):
        print("O carro está ligando com chave eletrônica.")


class Moto(Veiculo):
    def ligar(self):
        print("A moto está ligando com botão de ignição.")


# Demonstração

carro1 = Carro("Toyota", "Corolla", 2020)
moto1 = Moto("Honda", "CG 160", 2022)

carro1.exibir_informacoes()
carro1.ligar()

print()

moto1.exibir_informacoes()
moto1.ligar()
```
## 🧠 Explicação dos conceitos:

| Conceito           | Onde aparece                                                                                     |
| ------------------ | ------------------------------------------------------------------------------------------------ |
| **Herança**        | `Carro` e `Moto` herdam de `Veiculo`                                                             |
| **Polimorfismo**   | O método `ligar()` é sobrescrito em cada subclasse                                               |
| **Encapsulamento** | Os atributos são definidos no construtor `__init__()` e acessados apenas pelos métodos da classe |

## ✅ Conclusão
A Programação Orientada a Objetos permite reutilização de código, organização hierárquica e extensibilidade.
Este exemplo mostra como aplicar herança e polimorfismo em uma estrutura simples com clareza e legibilidade.
