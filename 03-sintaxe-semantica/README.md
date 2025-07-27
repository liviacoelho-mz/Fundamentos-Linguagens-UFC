# Desafio 03 - Descrições Sintáticas e Semânticas

## 🎯 Objetivo

Criar uma linguagem fictícia simples, com uma mini-gramática que defina sua estrutura sintática, e exemplos de análise léxica e sintática.

---

## 🧪 Linguagem Fictícia: MiniLang

A **MiniLang** é uma linguagem de brinquedo criada para este desafio. Seu propósito é didático: demonstrar conceitos básicos de sintaxe e semântica.

### 🔤 Alfabeto

- Letras minúsculas e maiúsculas
- Dígitos (0–9)
- Símbolos especiais: `+`, `-`, `*`, `/`, `=`, `;`, `(`, `)`

---

## 📘 Gramática da MiniLang (BNF simplificada)

```bnf
<programa>       ::= <decl_comando>+
<decl_comando>   ::= <declaracao> | <atribuicao> | <impressao>

<declaracao>     ::= "int" <id> ";"
<atribuicao>     ::= <id> "=" <expressao> ";"
<impressao>      ::= "print" "(" <id> ")" ";"

<expressao>      ::= <id> | <numero> | <expressao> <op> <expressao>
<op>             ::= "+" | "-" | "*" | "/"

<id>             ::= letra (letra | digito)*
<numero>         ::= digito+
```
## 💡 Exemplo de Código em MiniLang
int x;
x = 5 + 3;
print(x);

## 🔍 Análise Léxica (Tokenização)
```
| Token | Tipo                   |
| ----- | ---------------------- |
| int   | Palavra-chave          |
| x     | Identificador          |
| ;     | Delimitador            |
| x     | Identificador          |
| =     | Operador de atribuição |
| 5     | Número                 |
| +     | Operador               |
| 3     | Número                 |
| ;     | Delimitador            |
| print | Palavra-chave          |
| (     | Delimitador            |
| x     | Identificador          |
| )     | Delimitador            |
| ;     | Delimitador            |
```
## 🧠 Análise Sintática
A estrutura do código segue a gramática:

- int x; → <declaracao>
- x = 5 + 3; → <atribuicao> com <expressao> aninhada
- print(x); → <impressao>

## 🔧 Possível Expansão Semântica
- Verificar se x foi declarado antes da atribuição.
- Garantir que x seja do tipo correto.
- Impedir divisão por zero em <expressao>.

## ✅ Conclusão
A criação da MiniLang permite visualizar claramente como funcionam regras sintáticas e a importância da análise léxica. Esses conceitos são fundamentais para a construção de compiladores e interpretadores reais.
