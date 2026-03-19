# Projeto de Análise de Dados - e-SUS Notifica (MG, RJ, SP)

Este repositório contém scripts e notebooks para análise de dados do **e-SUS Notifica**, com recortes dos estados de **Minas Gerais, Rio de Janeiro e São Paulo**.

## 📂 Estrutura do repositório

```
sgleve/
├── data/
│   └── processed/          # Parquets pré-processados (versionados via Git LFS)
├── notebooks/
│   ├── 01_preprocessamento.ipynb
│   ├── 02_analise_automatica.ipynb
│   ├── 03_analise_manual.ipynb
│   └── 04_modelagem_basica.ipynb
├── app/                    # ← App Streamlit 
│   ├── Home.py
│   └── pages/
│       └── 1_SHAP_Explorer.py
├── requirements.txt
└── README.md
```

## Dados

⚠️ Os CSVs brutos **não estão versionados**. Apenas os arquivos `.parquet`
em `data/processed/` são rastreados (via Git LFS).

Estados: MG · RJ · SP

## 📊 Dados

Os dados foram extraídos do [OpenDataSUS](https://opendatasus.saude.gov.br/),  
recortes do **e-SUS Notifica** referentes a casos de COVID-19.

- **Estados incluídos**: MG, RJ, SP

## Como rodar localmente

```bash
pip install -r requirements.txt
streamlit run app/Home.py
```

## 🚀 Etapas já implementadas

- [x] Organização do repositório  
- [x] Pré-processamento leve (padronização de colunas, remoção de linhas problemáticas, salvamento otimizado)  
- [x] Salvamento em formato **Parquet**  
- [x] Exploração inicial com **YData Profiling**  
- [x] Comparação entre estados com **SweetViz**  
- [x] Modelagem e análises mais avançadas
- [ ] App Streamlit

## 🛠️ Pré-requisitos

- Python 3.9+  
- Jupyter Notebook  
- Bibliotecas principais:
  ```bash
  pip install pandas numpy pyarrow fastparquet ydata-profiling sweetviz
