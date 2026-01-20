# 📊 PROGETTO DI CLASSIFICAZIONE: PREDIZIONE DELLA POPOLARITA' DI SPOTIFY


## 📖 Introduzione
Questo progetto universitario analizza le classifiche di **Spotify** (applicazione per la musica) analizzando i brani più ascoltati negli anni 2009-2025. Attraverso un approccio data-driven, l'analisi mira a identificare i fattori di popolarita' e segmentare le canzoni in cluster in base ai fattori di popolarita' e costruire un modello predittivo per prevedere la popolarita' di una canzone.

---

## 🎯 Motivazioni e Obiettivi
Il settore della musica è caratterizzato da vari elementi che influenzano la popolarita' di una canzone, come ad esempio la qualità del brano, la sua durata, la sua tonalita' e la sua durata.
**L'obiettivo di questo progetto è duplice:**
1.  **Analitico:** Comprendere *perché* una canzone diventa popolare. 
2.  **Strategico:** Fornire strumenti (cluster e modelli predittivi) per prevedere la popolarita' di una canzone.

---

## 📁 Struttura del Progetto
progetto_big_data/
├── archive/
│   └── spotify_data clean.csv       # Dataset pulito (Kaggle) con metadati audio
├── progetto.ipynb                    # Notebook principale (Analisi, Clustering e ML)
├── README.md                         # Sintesi del progetto e istruzioni per l'uso
├── requirements.txt                  # Requisiti per l'installazione

## ⚙️ Metodologia
Il progetto segue un flusso di lavoro strutturato in 5 fasi principali:

### 1. Setup e caricamento dei dati
- Preparazione dei dati e dell'ambiente di lavoro. Vengono iportate le librerie necssarie e caricato il dataset.
- Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, TensorFlow.

### 2. Data Cleaning e preparazione modello
-   Preparazione dei dati per il modello, vengono eliminate le informazioni non utili , come ID e nomi dei brani.
-   Creazione della variabile target, si trasforma la popolarità da un numero continuo ad una variabile binaria (0 o 1) usando la mediana come soglia per garantie un bilanciamento dei dati.
-   Suddivisione e normalizzazione dei dati

### 3. Analisi esplorativa dei dati (EDA)
-   Esplorazione dei dati per capire le caratteristiche dei brani.
-   Calcolo e visualizzazione della correlazione tra le variabili
-   Analisi temporale: osservazione di come sono cambiate le caratteristiche dei brani negli anni.
-   Analisi dei contenuti. Top 10 brani più popolari e top 10 brani meno popolari
-   Clustering (K-Means): utilizzo dell'apprendimento non supervisionato per raggruppare le canzoni in "profili" musicali simili. Utilizzo dell Metodo del Gomito (Elbow Method) per determinare matematicamente il numero ottimale di gruppi.

### 4. Modellazione e Addestramento dei dati
-   Preprazione dei dati e addestramento di due modelli:
    - Scikit-learn (per la interpretabilità)
    - TensorFlow (per dimostrare l'uso delle reti neurali).

### 5. Perfomance dei modelli e scelta ottimale
-   Misura dell'efficacia dei modelli e conclusioni strategiche per il business.
-   Metriche di Valutazione: Non si guarda solo l'accuratezza totale, ma si analizza la Matrice di Confusione per vedere quanti falsi positivi (hit previste che falliscono) produce il modello. Si utilizza Precision (precisione delle hit previste) e Recall (capacità di trovare tutte le hit reali).
-   Feature Importance: Vengono identificati i "driver" del successo. Se la durata o il numero della traccia nell'album risultano determinanti, vengono forniti consigli pratici agli artisti.


---

## 🔑 Risultati Chiave

Dall'analisi del dataset Spotify (2009-2025) sono emersi i seguenti insight fondamentali:

- Distribuzione del Successo: Utilizzando la mediana come soglia, il dataset risulta perfettamente bilanciato: il 50% dei brani è classificato come "Alta Popolarità", garantendo al modello una base di addestramento equa.

- Driver del Successo (Feature Importance): La durata del brano e il numero della traccia nell'album sono i fattori predittivi più forti. I dati suggeriscono che brani con una durata ottimale e posizionati all'inizio della tracklist hanno una probabilità significativamente maggiore di diventare delle hit.

- Insight sui Cluster: L'analisi K-Means ha identificato gruppi distinti, tra cui un cluster di "Potenziali Hit da Classifica" (brani brevi e ritmati) e uno di "Contenuti da Album" (brani più lunghi o posizionati a fine disco), permettendo una segmentazione strategica del catalogo.

- Evoluzione Temporale: È stata rilevata una variazione costante nelle caratteristiche audio dal 2009 al 2025, confermando che i modelli di successo non sono statici ma evolvono con i gusti del pubblico.

- Performance dei Modelli: * La Regressione Logistica ha fornito un'accuratezza solida e un'ottima interpretabilità per decisioni di business.

- La Rete Neurale (TensorFlow) ha mostrato capacità superiori nel catturare relazioni non lineari, portando l'accuratezza complessiva a un livello competitivo per la predizione in tempo reale.
---

## 🚀 Installazione e Utilizzo

Per eseguire il progetto in locale:

1.  **Clona la repository** (o scarica la cartella):
    ```bash
    git clone <repository-url>
    cd progetto_big_data
    ```

2.  **Installa le dipendenze:**
    ```bash
    pip install -r requirements.txt
    ```

3.  **Avvia Jupyter Notebook:**
    ```bash
    jupyter notebook
    ```
    Apri il file `notebooks/progetto.ipynb` ed esegui le celle sequenzialmente.

---

## 🛠️ Tecnologie Utilizzate
-   **Python**: Linguaggio principale.
-   **Pandas & NumPy**: Manipolazione e analisi dati.
-   **Matplotlib & Seaborn**: Visualizzazione dati.
-   **Scikit-Learn**: Machine Learning (K-Means, Logistic Regression, Preprocessing).
-   **TensorFlow**: Machine Learning (Neural Network).

---

**Autrice:** Chiara Casali o Caseli
**Corso:** Laboratorio di Big Data, Data Mining e Data Analytics
**Anno Accademico:** 2025/2026