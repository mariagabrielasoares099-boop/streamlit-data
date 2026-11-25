# 📊 Streamlit Data: minha jornada em Engenharia de Dados

![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![pandas](https://img.shields.io/badge/pandas-150458?logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?logo=numpy&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?logo=jupyter&logoColor=white)
![Status](https://img.shields.io/badge/status-em%20desenvolvimento-yellow)

Projeto de portfólio da minha **formação em Engenharia de Dados**. Aqui registro, na prática, a construção da base técnica da carreira: leitura e análise de dados com Python, estatística aplicada e versionamento com Git e GitHub.

## 🎯 Objetivo

Aplicar conceitos de probabilidade a uma base de vendas, **conferindo cada resultado por dois caminhos**: pela fórmula estatística e pela contagem direta nos dados com pandas.

## 🗂️ Base de dados

[`superstore_sales.csv`](superstore_sales.csv), da base de exemplo **Superstore Sales**:

- **9.994 registros** de vendas e **9 colunas**, sem valores vazios
- Período: janeiro de 2014 a dezembro de 2017
- 4 regiões, 49 estados, 3 categorias, 17 subcategorias e 3 segmentos de clientes

| Coluna | Conteúdo |
|---|---|
| `Order Date` | Data do pedido (formato mês/dia/ano) |
| `Region` / `State` | Região e estado da venda |
| `Category` / `Sub-Category` | Categoria e subcategoria do produto |
| `Segment` | Segmento do cliente |
| `Sales` / `Profit` | Valor da venda e lucro |
| `Quantity` | Quantidade de itens |

## 🔎 Análises e resultados

Notebook: [`aula_probabilidade.ipynb`](aula_probabilidade.ipynb)

| Conceito | Pergunta | Resultado |
|---|---|---|
| Probabilidade simples | Qual a chance de um registro ser de Technology? | **18,48%** (1.847 de 9.994) |
| Distribuição por categoria | Como as vendas se dividem entre as categorias? | Office Supplies **60,30%**, Furniture **21,22%**, Technology **18,48%** |
| Regra do complemento | Qual a chance de **não** ser Technology? | **81,52%** |
| Adição (eventos excludentes) | Technology **ou** Furniture? | **39,70%** |
| Adição (regra geral) | Technology **ou** região West? | **44,54%** |
| Probabilidade condicional | Technology, **dado que** a região é West? | **18,70%** |

### Probabilidade de cada categoria dentro de cada região

| Região | Furniture | Office Supplies | Technology |
|---|---:|---:|---:|
| Central | 20,71% | 61,21% | 18,08% |
| East | 21,10% | 60,11% | 18,79% |
| South | 20,49% | 61,42% | 18,09% |
| West | 22,07% | 59,23% | 18,70% |

💡 **Leitura dos dados:** a proporção de Technology varia pouco entre as regiões (de 18,08% a 18,79%) e fica próxima da proporção geral (18,48%). Nesta base, saber a região acrescenta pouca informação sobre a chance de a venda ser de tecnologia.

## 🛠️ Tecnologias e habilidades praticadas

- **Python** com **pandas** e **NumPy**
- Leitura e inspeção de arquivos CSV
- Filtros com máscaras booleanas, `value_counts`, `isin` e `crosstab`
- **Estatística:** probabilidade simples, complemento, regra da adição e probabilidade condicional
- **Jupyter Notebook** e ambiente virtual (`venv`)
- **Git e GitHub:** branches, commits e pull requests
- Documentação contínua em [diário de bordo](DIARIO.md)

## 📁 Estrutura do projeto

| Arquivo | Descrição |
|---|---|
| [`aula_probabilidade.ipynb`](aula_probabilidade.ipynb) | Aula 1: probabilidade aplicada às vendas |
| [`superstore_sales.csv`](superstore_sales.csv) | Base de vendas utilizada |
| [`DIARIO.md`](DIARIO.md) | Registro do que foi feito em cada dia de trabalho |

## ▶️ Como executar

Pré-requisitos: [Python](https://www.python.org/downloads/) e [Git](https://git-scm.com/) instalados. Os comandos abaixo são para o PowerShell, no Windows.

```powershell
git clone https://github.com/mariagabrielasoares099-boop/streamlit-data.git
cd streamlit-data
python -m venv .venv
.venv\Scripts\activate
pip install pandas numpy jupyter
jupyter notebook
```

No navegador, abra o notebook `aula_probabilidade.ipynb` e execute as células em ordem.

## 🏆 Conquistas

### Conhecimentos adquiridos neste projeto

- [x] Ambiente virtual Python criado e base de vendas carregada com pandas
- [x] Probabilidade simples e distribuição por categoria
- [x] Regra do complemento
- [x] Regra da adição, para eventos excludentes e no caso geral
- [x] Probabilidade condicional e tabela cruzada com `crosstab`
- [x] Versionamento com Git e GitHub, incluindo branch e pull request

### Especializações e certificados

- [x] **Microsoft Power BI Para Business Intelligence e Data Science**, Data Science Academy: 72h, 98% de aproveitamento, concluído em 27/08/2026
- [x] **IA na Prática: Como Dados Bem Estruturados Fazem a Diferença**, Fundação Bradesco e Microsoft: 2h, concluído em 27/08/2026

### Outros cursos

- **IA Generativa**, Digital College: 72h

## 👩‍💻 Autora

**Maria Gabriela Soares**, em formação em Engenharia de Dados.

GitHub: [@mariagabrielasoares099-boop](https://github.com/mariagabrielasoares099-boop)
