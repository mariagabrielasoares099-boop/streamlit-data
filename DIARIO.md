# Diário de Bordo — Streamlit Data

Registro do que foi feito em cada dia de trabalho, atualizado ao encerrar o expediente. Entradas mais recentes no topo.

---

## 2026-11-23

- Continuação da aula de probabilidade (`aula_probabilidade.ipynb`), com novas células:
  - **Regra da adição (eventos mutuamente excludentes):** P(Technology ou Furniture) = P(Tech) + P(Furn) ≈ **0,397**, conferida com `.isin(...)`, com o mesmo resultado.
  - **Regra da adição geral (eventos que se sobrepõem):** P(Technology ou West) = P(Tech) + P(West) − P(Tech e West) ≈ **0,4454**, conferida com o operador `|`, com o mesmo resultado.
  - **Probabilidade condicional:** P(Technology | West) ≈ **0,187**, calculada por filtro e pela fórmula P(A e B) / P(B). Fica próxima da P(Technology) geral (0,1848).
  - **Tabela de probabilidades condicionais:** `pd.crosstab(Region, Category, normalize="index")` mostra a proporção de cada categoria dentro de cada região (cada linha soma 1). A Technology fica entre 0,1808 (Central) e 0,1879 (East).

---

## 2026-11-19

- Criado o ambiente virtual (`.venv`) e adicionada a base `superstore_sales.csv` (9.994 linhas × 9 colunas).
- Aula de probabilidade (`aula_probabilidade.ipynb`):
  - Ativação do pandas e numpy, leitura do CSV e inspeção inicial (`shape` e `head`).
  - **Probabilidade simples:** pedidos de Tecnologia / total de pedidos = 1.847 / 9.994 ≈ **0,1848**.
  - **Todas as probabilidades de uma vez:** `value_counts(normalize=True)` na coluna `Category` → Office Supplies ≈ 0,6030, Furniture ≈ 0,2122, Technology ≈ 0,1848.
  - **Regra do complemento (1 − P):** probabilidade de *não* ser Tecnologia = 1 − 0,1848 ≈ **0,8152**, conferida contando direto (`!= 'Technology'`), com o mesmo resultado.
