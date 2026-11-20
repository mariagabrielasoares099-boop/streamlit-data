# Streamlit Data

Projeto de estudos em análise de dados com Python (pandas/numpy) e, futuramente, dashboards em Streamlit, usando o dataset **Superstore Sales**.

## Conteúdo

| Arquivo | Descrição |
|---|---|
| `superstore_sales.csv` | Base de vendas (9.994 pedidos; colunas: Order Date, Region, State, Category, Sub-Category, Segment, Sales, Profit, Quantity) |
| `aula_probabilidade.ipynb` | Notebook da aula de probabilidade aplicada aos pedidos |
| `DIARIO.md` | Diário de bordo: registro do que foi feito a cada dia de trabalho |

## Como rodar

```powershell
python -m venv .venv
.venv\Scripts\activate
pip install pandas numpy jupyter streamlit
jupyter notebook aula_probabilidade.ipynb
```

## Diário de bordo

O registro diário fica em [DIARIO.md](DIARIO.md), atualizado ao final de cada expediente.
