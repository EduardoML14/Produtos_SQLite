# 🔎 ML-Product-Scraper

Web scraping de anúncios do Mercado Livre com armazenamento em banco de dados

![Python](https://img.shields.io/badge/Python-3.x-3572A5?style=flat-square&logo=python&logoColor=white)
![BeautifulSoup](https://img.shields.io/badge/BeautifulSoup4-4B8BBE?style=flat-square)
![SQLite](https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white)
![Status](https://img.shields.io/badge/Status-Concluído-success?style=flat-square)

---

## 📋 Sobre o projeto

Script Python que realiza web scraping de uma página de produto do Mercado Livre, extraindo título, preço e descrição do anúncio, e salvando os dados em um banco de dados SQLite local.

---

## ⚙️ Funcionalidades

- 🌐 Requisição HTTP com `User-Agent` customizado para simular navegador
- 🏷️ Extração de título, preço e descrição do anúncio via `BeautifulSoup`
- 💾 Armazenamento dos dados em banco SQLite
- 🔁 Substituição automática dos dados a cada nova execução

---

## 🗃️ Estrutura do banco de dados

Tabela: `produtos`

| Campo | Tipo | Descrição |
|---|---|---|
| `id` | INTEGER | Chave primária, auto incremento |
| `titulo` | TEXT | Título do anúncio |
| `preco` | TEXT | Preço exibido na página |
| `descricao` | TEXT | Descrição completa do produto |

---

## 🗂️ Estrutura do projeto

```
ml-product-scraper/
├── main.py
└── produtos.db     # Banco de dados gerado automaticamente
```

---

## 🧰 Tecnologias utilizadas

| Biblioteca | Uso |
|---|---|
| `requests` | Requisição HTTP à página do anúncio |
| `beautifulsoup4` | Parsing do HTML e extração dos dados |
| `sqlite3` | Armazenamento local dos dados |

---

## 🚀 Como executar

### Pré-requisitos

```bash
pip install requests beautifulsoup4
```

### Configuração

No arquivo `main.py`, substitua o link pelo anúncio que deseja raspar:

```python
link_anuncio = "https://produto.mercadolivre.com.br/MLB-{MLB}-seu-produto_JM"
```

### Rodando o script

```bash
python main.py
```

### Saída esperada

```
Dados do produto salvos com sucesso no banco de dados 'produtos.db'.
```

---

## ⚠️ Aviso

Este projeto é para fins educacionais. O uso de web scraping pode ir contra os **Termos de Serviço** do Mercado Livre. Para uso em produção, considere utilizar a [API oficial do Mercado Livre](https://developers.mercadolivre.com.br/).

---

## 🧑‍💻 Autor

Feito por **Eduardo Lima**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/eduardomoreiralima/)
[![Gmail](https://img.shields.io/badge/Gmail-D14836?style=flat-square&logo=gmail&logoColor=white)](mailto:limaedu.contato@gmail.com)
