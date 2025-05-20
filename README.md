  
# Análise de Dados – **Brazilian E-commerce Public Dataset by Olist**

> Projeto completo para avaliação de Engenharia de Dados & Data Analytics  
> **Autor:** _Seu Nome Aqui_ &nbsp;|&nbsp; **Data:** Maio / 2025  

---

## 🌟 Visão Geral

Este repositório contém todo o processo de **ETL → EDA → Modelagem → Dashboards** aplicado ao dataset público da Olist (≈ 100 k pedidos entre 2016-2018).

| Etapa | Descrição | Notebook |
|-------|-----------|----------|
| 1 | **Preparação dos Dados** – limpeza, normalização, modelo relacional | `notebooks/01_preparacao_dados.ipynb` |
| 2 | **Análise Exploratória (EDA)** – perguntas-chave + gráficos | `notebooks/02_eda.ipynb` |
| 3 | **Solução de Negócio** – retenção, predição de atrasos, RFM-Clustering, satisfação | `notebooks/03_problemas_negocio.ipynb` |
| 4 | **Dashboards Interativos** – vendas no tempo, mapa de calor, avaliação × entrega, análise de vendedores | `notebooks/04_dashboards.ipynb` |



---

## 📂 Estrutura do Repositório

 

.
├─ data/                 # ⇦ coloque aqui o zip original ou os CSVs extraídos
├─ notebooks/
│  ├─ 01\_preparacao\_dados.ipynb
│  ├─ 02\_eda.ipynb
│  ├─ 03\_problemas\_negocio.ipynb
│  └─ 04\_dashboards.ipynb
├─ src/                  # funções utilitárias (ETL, features, plots)
├─ requirements.txt
└─ README.md

 `

---

## ⚙️ Requisitos

| Ferramenta | Versão mínima |
|------------|---------------|
| Python | 3.9 |
| pandas | 2.0 |
| numpy | 1.25 |
| scikit-learn | 1.4 |
| matplotlib / seaborn | 3.8 / 0.13 |
| plotly | 5.21 |
| ipywidgets | 8.x |
| haversine | 2.8 |

Instalação rápida:

 bash
# via pip
python -m venv venv
source venv/bin/activate        # Windows: .\venv\Scripts\activate
pip install -r requirements.txt

# via conda
conda env create -n olist_env -f environment.yml
conda activate olist_env
 `

---

## 🚀 Como Executar Localmente

1. **Clone** o repositório e coloque `olist.zip` (ou CSVs) em `data/`.
2. **Ative** o ambiente (`venv` ou `conda`).
3. Rode `jupyter notebook` ou `jupyter lab` e abra os notebooks na ordem 01 → 04.

> Caso use Notebook clássico, habilite widgets:
> `jupyter nbextension enable --py widgetsnbextension`

---

## 🏁 Principais Resultados

| Insight / Métrica               | Valor                                             |
| ------------------------------- | ------------------------------------------------- |
| Clientes recorrentes            | **≈ 14 %** fazem ≥ 2 compras                      |
| Categoria com maior faturamento | **health\_beauty**                                |
| Acurácia do modelo de atraso    | **95 %**, recall de atrasos **60 %**              |
| Variáveis-chave (atraso)        | `delivery_time`, `shipping_time`, `total_payment` |
| Cluster “Campeões” (RFM)        | 4 % dos clientes → 18 % do faturamento            |

---

## 📊 Dashboards

| Painel                  | Descrição                                                                   | Screenshot                                    |
| ----------------------- | --------------------------------------------------------------------------- | --------------------------------------------- |
| **Vendas no Tempo**     | Linha mensal filtrável por **estado** & **categoria** (Plotly + ipywidgets) | ![vendas](assets/dashboard_vendas.gif)        |
| **Mapa de Calor**       | Choropleth: concentração de vendas por estado                               | ![mapa](assets/choropleth.png)                |
| **Avaliação × Entrega** | Boxplot + scatter interativo                                                | ![avaliacao](assets/avaliacao_vs_entrega.png) |
| **Vendedores**          | Top-10 + seleção detalhada (volume, score, SLA)                             | ![vendedores](assets/vendedores.gif)          |

---

## 🛠️ Próximos Passos

* Balancear classes (SMOTE) e testar LightGBM.
* Usar distância geográfica como feature adicional.
* Automatizar ETL com **Airflow** e publicar painéis no **Metabase**.
* Notificar proativamente pedidos com probabilidade > 50 % de atraso.

---

## 📄 Licença

Código sob licença MIT – consulte `LICENSE`.

---

## 🙋‍♂️ Autor

Seu Nome · [LinkedIn](https://linkedin.com/in/seunome) · [seunome@email.com](mailto:seunome@email.com)
Contribuições e sugestões são bem-vindas!

 
 
