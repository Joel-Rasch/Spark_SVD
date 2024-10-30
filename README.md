# Spark SVD - Singulärwertzerlegung für große Matrizen

Dieses Repository bietet eine skalierbare Implementierung der Singulärwertzerlegung (SVD) mithilfe von Apache Spark. Es ist darauf ausgelegt, sehr große Matrizen effizient zu verarbeiten und nutzt dabei parallele Verarbeitung und verteilte Datenhandhabung.

## Projektübersicht

Diese Implementierung der SVD ist speziell für Matrizen mit einer großen Anzahl an Spalten ausgelegt. Das Repository wurde im Rahmen des Moduls **Datenanalyse in Big Data** erstellt 

## Merkmale

- **Verteilte SVD**: Nutzt die verteilten Rechenkapazitäten von Spark, um SVD auf Matrizen durchzuführen, die die lokalen Speichergrenzen überschreiten.
- **Angepasste Bibliotheken**: Verwendet Spark MLlib nicht für die SVD, sondern setzt auf angepassten Code und Bibliotheken wie NumPy für Matrixoperationen.
- **Effizientes Speichermanagement**: Optimiert für große Datensätze (z. B. 30 000 Zeilen x 1 000 Spalten) und darauf ausgelegt, die Datensammlung auf dem Driver-Knoten zu minimieren.

## Verwendung des Codes:

Zum starten, muss das repository geklont werden und anschließend "docker-compose up --build" in einer shell eingegeben werden.
Auf localhost:8888 befindet sich das Jupyter Spark Notebook und auf Port 8080 ist der Spark Master, bei wechem die Worker eingesehen werden können.
Anpassungen, wie RAM oder Anzahl der Kerne müssen in der docker-compose.yml datei durchgeführt werden
