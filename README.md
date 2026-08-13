# Stock-Price-Prediction-Using-

https://youtu.be/QIUxPv5PJOY?si=ZaQI9qtTUcJhvtzz

 Résumé de la vidéo & Code Python
Résumé de la vidéo
Dans cette vidéo issue de la chaîne Computer Science, l'auteur présente une méthode complète pour prédire les prix de clôture de l'action Apple Inc. (AAPL) à l'aide d'un réseau de neurones récurrent de type LSTM (Long Short-Term Memory) sous Python (avec Keras et TensorFlow).

Étapes principales du tutoriel :
Importation des bibliothèques : pandas_datareader, numpy, pandas, scikit-learn (MinMaxScaler), keras (Sequential, Dense, LSTM) et matplotlib [cite: 1].
Récupération des données : Téléchargement de l'historique boursier d'Apple depuis Yahoo Finance entre 2012 et fin 2019 [cite: 1].
Visualisation : Affichage de la courbe historique du prix de clôture (Close) [cite: 1].
Préparation & Normalisation : Extraction du prix de clôture, mise à l'échelle des données entre 0 et 1 avec MinMaxScaler [cite: 1].
Création des ensembles d'entraînement (Training) :
Utilisation d'une fenêtre glissante de 60 jours passés pour prédire le prix du 61ème jour [cite: 1].
Redimensionnement (Reshape) des tableaux NumPy en 3D ([samples, time steps, features]) requis par l'architecture LSTM [cite: 1].
Construction & Entraînement du modèle LSTM :
Première couche LSTM à 50 neurones (return_sequences=True) [cite: 1].
Seconde couche LSTM à 50 neurones (return_sequences=False) [cite: 1].
Couche dense intermédiaire à 25 neurones puis couche de sortie à 1 neurone [cite: 1].
Compilation avec l'optimiseur adam et la perte mean_squared_error [cite: 1].
Entraînement (fit) avec un batch size de 1 sur 1 epoch [cite: 1].
Évaluation & Visualisation des prédictions :
Calcul de la métrique RMSE (Root Mean Squared Error) [cite: 1].
Graphique comparatif entre les prix réels de validation et les prix prédits par le modèle [cite: 1].
Test de prédiction sur une date spécifique : Prédiction du prix de clôture pour le 18 décembre 2019 à partir des 60 jours précédents, puis comparaison avec le prix réel observé [cite: 1
