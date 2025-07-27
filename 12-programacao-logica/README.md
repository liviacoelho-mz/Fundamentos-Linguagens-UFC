# Desafio 12 – Programação Lógica

Neste desafio, utilizamos a linguagem **Prolog** para modelar um pequeno problema lógico no contexto de **genealogia**.

---

## 👨‍👩‍👧‍👦 Problema: Relações Familiares

Queremos representar relações como:
- Pai
- Mãe
- Filho
- Irmão
- Avô

E permitir consultas lógicas como:
- "Quem são os irmãos de Ana?"
- "Quem é avô de João?"

---

## 🧑‍💻 Código em Prolog:

```prolog
% Fatos
pai(joao, maria).
pai(joao, jose).
mae(ana, maria).
mae(ana, jose).
pai(jose, pedro).
mae(maria, julia).

% Regras
irmao(X, Y) :-
    pai(P, X), pai(P, Y),
    mae(M, X), mae(M, Y),
    X \= Y.

avo(X, Y) :-
    pai(X, Z), pai(Z, Y);
    pai(X, Z), mae(Z, Y).

filho(X, Y) :-
    pai(Y, X);
    mae(Y, X).
```
## 🧪 Exemplos de consultas
```
?- irmao(maria, jose).
true.

?- avo(joao, pedro).
true.

?- filho(pedro, jose).
true.

?- filho(julia, maria).
true.

?- irmao(maria, julia).
false.
```

## 🔍 Explicação dos conceitos

| Conceito         | Como foi usado                                               |
| ---------------- | ------------------------------------------------------------ |
| **Fatos**        | Declaram informações diretas (`pai(joao, maria)`)            |
| **Regras**       | Criam inferência lógica (`irmao(X, Y)`)                      |
| **Consultas**    | O usuário pergunta e o sistema infere a resposta             |
| **Backtracking** | Prolog testa todas as possibilidades para encontrar soluções |

## ✅ Conclusão
A programação lógica é útil quando precisamos representar conhecimento e raciocinar sobre ele. Prolog permite modelar relações complexas com poucas linhas, sendo ideal para resolver problemas de dedução, genealogia, quebra-cabeças, e IA simbólica.

