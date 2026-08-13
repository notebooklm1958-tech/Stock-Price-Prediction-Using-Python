# Stock-Price-Prediction-Using-

https://youtu.be/QIUxPv5PJOY?si=ZaQI9qtTUcJhvtzz

# Stock Price Prediction Using LSTM

[![Lien de la vidéo YouTube](https://img.shields.io/badge/YouTube-Regarder_la_vid%C3%A9o-red?style=for-the-badge&logo=youtube)](https://youtu.be/QIUxPv5PJOY?si=ZaQI9qtTUcJhvtsz)

## 📌 Résumé du projet & Code Python

Dans ce projet, basé sur le tutoriel de **Computer Science**, nous présentons une méthode complète pour prédire le prix de l'action **Apple Inc. (AAPL)** à l'aide d'un réseau de neurones récurrent **LSTM (Long Short-Term Memory)** sous Python (avec Keras et TensorFlow).

---

## 🛠️ Étapes principales du tutoriel

1. **Importation des bibliothèques** :
   * `pandas`, `scikit-learn` (`MinMaxScaler`), `keras` (`Sequential`, `Dense`, `LSTM`) et `matplotlib`.

2. **Collecte des données** :
   * Téléchargement de l'historique boursier d'Apple depuis fin 2019.

3. **Visualisation** :
   * Affichage de la courbe historique du prix d'action.

4. **Préparation & Normalisation** :
   * Extraction du prix de clôture.
   * Mise à l'échelle entre 0 et 1 avec `MinMaxScaler`.
   * Création des ensembles d'entraînement avec une fenêtre glissante de 60 jours passés pour prédire le prix du 61ème jour.
   * Redimensionnement (Reshape) des tableaux NumPy en 3D (`[samples, time steps, features]`).

5. **Construction & Entraînement du modèle LSTM** :
   * **1ère couche LSTM** à 50 neurones (`return_sequences=True`).
   * **2ème couche LSTM** (`return_sequences=False`).
   * **Couche Dense intermédiaire** à 25 neurones.
   * **Couche de sortie** à 1 neurone.
   * **Compilation** : Optimiseur `Adam` et perte `MSE` (Mean Squared Error).
   * **Entraînement (`fit`)** : `batch_size = 1` sur `1 epoch`.

6. **Évaluation** :
   * Prédiction et comparaison avec les données réelles.
