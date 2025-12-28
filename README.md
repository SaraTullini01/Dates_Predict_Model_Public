# 🌴 Date Quality Detector

### Progetto di Deep Learning - Corso di Laurea Magistrale
**Sviluppata da:** Sara Tullini, Negri Davide e Chesta Lorenzo

---

## 📌 Descrizione del Progetto
Questo repository ospita un sistema di visione artificiale basato su **Deep Learning** progettato per la classificazione automatica della qualità dei datteri. Il focus principale è l'identificazione della **"Loose Skin"** (distacco della pelle), un difetto qualitativo comune, distinguendo i frutti deteriorati da quelli sani.

L'applicazione integra un modello neurale addestrato in ambiente cloud (Google Colab) con un'interfaccia web interattiva sviluppata in **Streamlit** per l'inferenza locale.



---

## 🧠 Architettura del Modello
Per massimizzare l'accuratezza con un dataset ottimizzato, è stata utilizzata la tecnica del **Transfer Learning**. Partendo da una rete preaddestrata su ImageNet e aggiungendo layer specifici finali per adattare il modello al dataset a disposizione.



---

## 🛠️ Sfide Tecniche e Soluzioni
Durante lo sviluppo sono state implementate soluzioni specifiche per superare ostacoli di portabilità:

1.  **Compatibilità Cross-Version:** È stata risolta l'incompatibilità tra Keras 3 (usato da Colab) e Keras 2 (ambiente locale) con il caricamento dei soli pesi (`weights-only`) tramite mappatura per nome dei layer.
2.  **User Experience (UX):** L'interfaccia Streamlit è stata potenziata con CSS personalizzato per offrire un design pulito, pulsanti centrati e feedback visivi chiari sui risultati dell'analisi.

---

## 📂 Struttura del Repository
* `app.py`: Il cuore dell'applicazione web Streamlit.
* `pesi_finali.h5`: File contenente i pesi del modello addestrato.
* `W_i_Datteri_final.ipynb`: Notebook Jupyter con il codice di training originale.
* `requirements.txt`: Elenco delle librerie Python necessarie (TensorFlow, Streamlit, Pillow, Numpy).

---

## 🚀 Installazione e Utilizzo

### 1. Clonazione
```bash
git clone [https://github.com/SaraTullini01/Dates_Predict_Model.git](https://github.com/SaraTullini01/Dates_Predict_Model.git)
cd Dates_Predict_Model
```

### 2. Configurazione ambiente di lavoro
```bash
pip install -r requirements.txt
```

### 3. Esecuzione
```bash
streamlit run app.py
```

## 📈 Sviluppi Futuri
Sebbene il modello sia funzionale, sono previsti miglioramenti per aumentarne la precisione:

- Fine-tuning: Sblocco degli ultimi blocchi di DenseNet per specializzare il modello sulla texture specifica dei datteri.

- Data Augmentation: Incremento della varietà del dataset per gestire diverse condizioni di illuminazione.
