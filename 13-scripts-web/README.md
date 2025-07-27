# Desafio 13 – Scripts e Web

Neste desafio, desenvolvemos um **script Python** que automatiza o download de uma **imagem aleatória de gato** a partir de uma **API pública**.

---

## 🐱 Objetivo

Criar um script para:
1. Fazer uma requisição GET para uma API
2. Obter o link de uma imagem
3. Baixar e salvar essa imagem localmente

---

## 🧑‍💻 Código em Python

```python
import requests

def baixar_gato():
    url = "https://api.thecatapi.com/v1/images/search"
    resposta = requests.get(url)

    if resposta.status_code == 200:
        dados = resposta.json()
        imagem_url = dados[0]['url']
        print("Imagem encontrada:", imagem_url)

        imagem = requests.get(imagem_url)
        if imagem.status_code == 200:
            with open("gato.png", "wb") as f:
                f.write(imagem.content)
            print("Imagem salva como 'gato.png'")
        else:
            print("Erro ao baixar a imagem.")
    else:
        print("Erro ao acessar a API.")

baixar_gato()
```
### 🔍 Explicação
| Parte do código   | O que faz                                      |
| ----------------- | ---------------------------------------------- |
| `requests.get()`  | Faz requisições HTTP GET                       |
| `resposta.json()` | Converte JSON para dicionário Python           |
| `with open(...)`  | Salva a imagem localmente como arquivo binário |

### 💡 Contexto e utilidade
Esse tipo de script pode ser adaptado para:
- Automatizar downloads de imagens, PDFs, etc.
- Integrar com APIs de clima, moedas, notícias
- Ser executado diariamente com um agendador como `cron`

## ✅ Conclusão
Scripts são ferramentas poderosas para automatizar tarefas repetitivas. Python, com suas bibliotecas simples e diretas, é ideal para esse tipo de automação leve com APIs web.
