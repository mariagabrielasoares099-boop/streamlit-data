# Diário de Bordo — Streamlit Data

Registro do que foi feito em cada dia de trabalho, atualizado ao encerrar o expediente. Entradas mais recentes no topo.

---

## 2026-11-27

- Organização das aulas:
  - `aula_probabilidade.ipynb` passou a se chamar `aula_ 01_probabilidade.ipynb` e ganhou uma célula de apresentação.
  - Criado o `Dicionário.txt`, com anotações sobre kernel, bibliotecas, `scipy.stats` e a coluna `Order Date`.
- Configuração do ambiente no Antigravity:
  - Instalados `ipykernel`, `matplotlib`, `numpy`, `pandas` e `scipy` no `.venv`.
- Aula 2, distribuições discretas (`aula_02_distribuicoes_discretas.ipynb`):
  - Importação das bibliotecas e leitura do CSV com `parse_dates=['Order Date']`: 9.994 linhas × 9 colunas.
  - **Erros resolvidos na leitura do CSV:** `df + pd.read_csv(...)` gerava `NameError` e `TypeError`; o correto é `df = pd.read_csv(...)`.
  - **Erro de sintaxe:** a marcação ` ```python `, usada para formatar código em conversas, não deve ser colada na célula.
  - **Binomial (próximo passo):** 10 pedidos, sucesso = ser de Tecnologia. Valores esperados: p ≈ 0,1848, P(X = 3) ≈ 0,1812, P(X ≤ 3) ≈ 0,9043, P(X > 3) ≈ 0,0957 e média ≈ 1,85.
- Aula 3, regra empírica (`aula_03_regra_empírica.ipynb`):
  - Notebook criado, com a apresentação do tema: curva de densidade (PDF) sobre um histograma normalizado (`density=True`) e distribuição uniforme.

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
