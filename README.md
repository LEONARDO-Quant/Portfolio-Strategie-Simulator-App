<p align="center">
  <img src="docs/banner" alt="Bannière du projet" width="1000" height="250"/>
</p> 

# Portfolio Strategy Simulator App

Projet de niveau master 1 dans le cadre de la formation Sorbonne Data Analytics.   
Application de modèles économétriques dans l'analyse stratégique d'un portefeuille d'actifs : Évaluation de la performance, analyse du risque et recommandations stratégiques pour un portefeuille d’actions diversifié.

## Contexte

La gestion d’un portefeuille d’actions nécessite une analyse rigoureuse des performances et des risques associés.
Ce projet vise à fournir une analyse stratégique permettant de maximiser le rendement tout en maîtrisant le risque, grâce à Python et aux outils de data science financière.

## Objectifs 🎯

* Évaluer la performance historique du portefeuille.
* Mesurer le risque et la volatilité des actifs.
* Identifier les corrélations et diversifications optimales.
* Proposer des recommandations stratégiques pour l’allocation future du portefeuille.

## Méthodologie ⚙️

1. Collecte des données : prix historiques des actions, indices de marché, données financières publiques.

2. Nettoyage et préparation : gestion des valeurs manquantes, normalisation des données.

3. Analyse exploratoire : visualisation des rendements, corrélations, volatilité.

4. Optimisation de portefeuille : calcul du ratio de Sharpe, frontiere efficiente, allocation optimale.

5. Reporting stratégique : graphiques et recommandations basées sur l’analyse.

## Résultats 📈

1. Analyse détaillée de la performance de chaque action et du portefeuille global.

2. Visualisation des corrélations et identification des actifs fortement liés.

3. Recommandations d’allocation optimisée pour maximiser le rendement/risk ratio.

<p align="center">
  <img src="docs/screenshot" width="800" height="250"/> 
</p> 


## Technologies utilisées 🧠

Python : Pandas, NumPy, Matplotlib, Seaborn, SciPy, Streamlit, Plotly.express.  
Bibliothèques financières : Yfinance.    
Jupyter Notebook    
GitHub

## Installation

git clone https://github.com/LeyoPuka/Premier-projet-python.git  
pip install -r requirements.txt

## Structure

```
Portfolio-Strategie-Simulator-App/
├─ app.py                # Lanceur Streamlit
├─ docs/
├─ src/
│  ├─ __init__.py
│  ├─ data.py           # Chargement des données (yfinance, CSV)
│  ├─ outils.py         # Aides (sanitise, pct_returns)
│  ├─ types.py          # Dataclasses (BacktestResult)
│  ├─ metrics.py        # KPIs (Sharpe, Sortino, Drawdown, VaR, beta/alpha)
│  ├─ strategies.py     # Stratégies (Buy&Hold, MA Crossover, Vol Target)
│  └─ optimizer.py      # Markowitz max Sharpe
└─ requirements.txt
```

## Fonctionnalités

- **Données** : yfinance (ajusté) ou CSV avec colonne `Date`, colonnes = tickers.
- **Stratégies** : Buy&Hold, moving-average crossover, volatility targeting (equal-weight).
- **KPIs** : CAGR, volatilité annualisée, Sharpe, Sortino, max drawdown, VaR 95%, beta/alpha vs benchmark.
- **Optimisation** : Markowitz max Sharpe (fallback random si SciPy absent).
- **Export** : CSV Equity & Returns, sauvegarde / chargement de configurations JSON.

> Usage éducatif uniquement. Aucune garantie de performance.
