# Projet : Surveillance ECG en temps réel avec Edge AI

## Description
Ce projet permet de surveiller les battements cardiaques en temps réel à l’aide d’un **capteur ECG AD8232** et de modèles d’apprentissage profond (**CNN**) déployés avec **TensorFlow Lite**.  
Les signaux ECG sont analysés pour détecter différents types de battements cardiaques, et les résultats peuvent être visualisés via **ThingBoard**.


## Classes de battements
- **N (Normal)** : battement cardiaque normal  
- **S (SVEB)** : battement ectopique supraventriculaire  
- **V (VEB)** : battement ectopique ventriculaire  
- **F (Fusion)** : battement mixte normal + ectopique  
- **Q (Unknown)** : battement non classifié ou bruit  

## Limitations
- Capteur un seul canal → moins précis qu’un ECG médical 12 dérivations  
- Classes **N, S, V** détectables si le signal est propre  
- Classes **F, Q** difficiles à détecter  

## Fonctionnalités
1. Lecture des signaux ECG en temps réel  
2. Classification via modèle CNN TFLite  
3. Visualisation et alertes sur ThingBoard  

## Installation
```bash
git clone https://github.com/username/nom-du-projet.git
cd nom-du-projet
pip install tensorflow pandas numpy matplotlib scikit-learn imbalanced-learn seaborn
