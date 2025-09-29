# Projeto de Análise de Dados - e-SUS Notifica (MG, RJ, SP)

Este repositório contém scripts e notebooks para análise de dados do **e-SUS Notifica**, com recortes dos estados de **Minas Gerais, Rio de Janeiro e São Paulo**.

## 📂 Estrutura do repositório
```data/ # Dados (originais ignorados pelo Git)
data/processed/ # Dados processados (parquet, feather, csv.gz)
notebooks/ # Notebooks de pré-processamento e exploração
src/ # Funções auxiliares
```
⚠️ **Observação**: os arquivos CSV originais **não estão versionados**, apenas os processados em `data/processed/`.

## 📊 Dados

Os dados foram extraídos do [OpenDataSUS](https://opendatasus.saude.gov.br/),  
recortes do **e-SUS Notifica** referentes a casos de COVID-19.

- **Estados incluídos**: MG, RJ, SP


## 🚀 Etapas já implementadas

- [x] Organização do repositório  
- [x] Pré-processamento leve (padronização de colunas, remoção de linhas problemáticas, salvamento otimizado)  
- [x] Salvamento em formato **Parquet**  
- [ ] Exploração inicial com **YData Profiling**  
- [ ] Comparação entre estados com **SweetViz**  
- [ ] Modelagem e análises mais avançadas  

## 🛠️ Pré-requisitos

- Python 3.9+  
- Jupyter Notebook  
- Bibliotecas principais:
  ```bash
  pip install pandas numpy pyarrow fastparquet ydata-profiling sweetviz
