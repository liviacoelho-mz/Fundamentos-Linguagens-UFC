# Desafio 14 – Tendências em Linguagens de Programação

Neste desafio, foi realizada uma análise crítica sobre a linguagem **Rust**, considerada uma das linguagens emergentes mais promissoras da atualidade.

---

## 🦀 O que é Rust?

**Rust** é uma linguagem de programação de sistemas desenvolvida pela **Mozilla**, com foco em:
- **Segurança de memória sem garbage collector**
- **Concorrência segura**
- **Alto desempenho**

Rust é compilada e oferece segurança semelhante à de linguagens como Java, com desempenho comparável ao C/C++.

---

## 🚀 Principais características

| Característica            | Descrição                                                                 |
|---------------------------|---------------------------------------------------------------------------|
| Segurança de memória      | Evita vazamentos e ponteiros inválidos sem coletor de lixo                |
| Sistema de ownership      | Modelo único que controla a posse dos dados                               |
| Concorrência segura       | Impede condições de corrida em tempo de compilação                        |
| Zero-cost abstractions    | Abstrações que não impactam no desempenho                                 |
| Performance de sistemas   | Ideal para criação de sistemas embarcados, motores de jogos, etc.         |
| Ecossistema moderno       | `cargo` para gerenciamento de pacotes e `crates.io` como repositório      |

---

## 💡 Por que Rust está em alta?

- Considerada a **linguagem mais amada** por vários anos consecutivos na pesquisa do Stack Overflow
- Usada por empresas como **Dropbox, Cloudflare, Microsoft, Amazon e Google**
- Possui **documentação excelente**, **ferramentas robustas** e **uma comunidade muito ativa**

---

## 🧪 Exemplo básico em Rust

```rust
fn main() {
    let nome = "Lívia";
    println!("Olá, {}!", nome);
}
```
### 🧠 Crítica e visão analítica
Rust oferece soluções elegantes para problemas clássicos da programação de baixo nível, como:
- Gerenciamento manual de memória
- Condições de corrida
- Bugs difíceis de rastrear
No entanto, possui curva de aprendizado acentuada, especialmente devido ao sistema de ownership e borrow checker. Para novos desenvolvedores, pode parecer intimidadora no início.

## ✅ Conclusão
Rust é uma linguagem poderosa, moderna e segura, com um futuro promissor tanto para desenvolvimento de sistemas quanto para aplicações que exigem performance e confiabilidade.
Sua adoção está crescendo tanto no mercado quanto na academia, e é uma ótima aposta para quem busca se destacar em áreas como:
- Programação de sistemas
- Computação embarcada
- Desenvolvimento Web com WebAssembly
