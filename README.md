# Data Processing and API Project

Ce projet est structuré en trois parties principales :
1. Collecte de données
2. Normalisation/Standardisation
3. API pour exposer les données

## Structure du projet

```
project/
│
├── src/
│   ├── collectors/          # Scripts de collecte de données
│   ├── normalizers/         # Scripts de normalisation
│   └── api/                 # API FastAPI
│
├── data/
│   ├── raw/                 # Données brutes
│   └── processed/           # Données traitées
│
└── tests/                   # Tests unitaires
```

## Installation

1. Créer un environnement virtuel :
```
python -m venv venv
source venv/bin/activate  # Linux/Mac
.\venv\Scripts\activate   # Windows
```

2. Installer les dépendances :
```
pip install -r requirements.txt
```

## Utilisation

1. Collecter les données :
```python
from src.collectors.data_collector import DataCollector
collector = DataCollector()
data = collector.collect_data("source_name")
```

2. Normaliser les données :
```python
from src.normalizers.data_normalizer import DataNormalizer
normalizer = DataNormalizer()
normalized_data = normalizer.normalize_data(data)
```

3. Lancer l'API :
```
uvicorn src.api.main:app --reload
```

L'API sera accessible à l'adresse : http://localhost:8000
