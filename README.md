# oral-microbiome-ml

# 🦠 Microbioma Oral — Classificação NT vs ND

Projeto de Machine Learning desenvolvido durante estágio supervisionado no
**LaBiOmicS — Laboratório de Bioinformática e Ciências Ômicas (NPT/UMC)**.

## 📌 Objetivo

Investigar se a composição taxonômica do microbioma oral é capaz de distinguir
indivíduos **Neurotípicos (NT)** de **Neurodivergentes (ND)** por meio de modelos
preditivos de aprendizado de máquina.

## 📊 Dataset

- **Fonte:** BioProject PRJNA362687 — NCBI SRA
- **Amostras:** 111 (58 NT / 53 ND)
- **Variáveis:** 10 filos bacterianos

## 🛠️ Tecnologias

![Python](https://img.shields.io/badge/Python-3.12-blue)
![XGBoost](https://img.shields.io/badge/XGBoost-green)
![LightGBM](https://img.shields.io/badge/LightGBM-yellow)
![TPOT](https://img.shields.io/badge/TPOT-AutoML-orange)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-grey)

## ⚙️ Pipeline

1. Carregamento e exploração dos dados (EDA)
2. Pré-processamento com `StandardScaler`
3. Validação cruzada estratificada (`StratifiedKFold`)
4. Otimização com `RandomizedSearchCV`
5. Modelos de Boosting: `XGBoost` e `LightGBM`
6. AutoML com `TPOT`
7. Análise de importância das variáveis

## 📈 Resultados

| Modelo | AUC (Teste) |
|--------|------------|
| XGBoost | 0.716 |
| LightGBM | 0.708 |
| TPOT | 0.500* |

*O TPOT apresentou limitações de compatibilidade no ambiente Colab (Python 3.12).

## 🧬 Variáveis Mais Relevantes

| Posição | Filo | Importância |
|---------|------|------------|
| 1º | p__Patescibacteria | 0.3044 |
| 2º | p__Spirochaetota | 0.1461 |
| 3º | p__Firmicutes | 0.1351 |

## 📁 Estrutura

├── oral_microbiome.csv       # Dataset
├── microbioma_oral_ml.ipynb  # Notebook principal
└── README.md

**Thainá Esther Soares da Silva**
Engenharia de Software — UMC
Estágio supervisionado no LaBiOmicS/NPT — 2026
