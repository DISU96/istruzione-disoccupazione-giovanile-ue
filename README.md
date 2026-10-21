# Istruzione, disoccupazione giovanile e crescita economica nei Paesi UE

Analisi esplorativa di dati Eurostat e Banca Mondiale per studiare come si associano istruzione, disoccupazione giovanile e crescita del PIL pro capite nei 27 Paesi dell’Unione Europea.

**Periodo analizzato:** 2014–2024  
**Strumenti:** Python, pandas, NumPy, Matplotlib, API Eurostat e Banca Mondiale

## Domanda di ricerca

Tra i Paesi dell’UE, come si associano il livello di istruzione dei giovani, la disoccupazione giovanile e la crescita economica? Le associazioni osservate nel confronto tra Paesi sono simili a quelle che emergono confrontando i cambiamenti dal 2014 al 2024?

## Dati

L’analisi combina indicatori pubblici:

- **Disoccupazione giovanile:** percentuale della forza lavoro tra 15 e 24 anni senza lavoro, disponibile e in cerca di occupazione. Fonte: [Banca Mondiale](https://data.worldbank.org/indicator/SL.UEM.1524.ZS).
- **Crescita del PIL pro capite:** variazione percentuale annua. Fonte: [Banca Mondiale](https://data.worldbank.org/indicator/NY.GDP.PCAP.KD.ZG).
- **Istruzione:** quota di persone tra 20 e 24 anni con almeno un’istruzione secondaria superiore. Fonte: [Eurostat](https://ec.europa.eu/eurostat/databrowser/view/tps00186/default/table).

Dopo l’unione degli indicatori, il dataset contiene **297 osservazioni**: 27 Paesi per 11 anni.

## Risultati principali

- Nel 2024, la media semplice della disoccupazione giovanile nei 27 Paesi è **15,77%**; la mediana è **15,09%**. I valori vanno dal **6,60%** al **26,63%**.
- Nel confronto tra Paesi nel 2024, la correlazione tra istruzione e disoccupazione giovanile è circa **−0,05**, quindi vicina a zero.
- Considerando i cambiamenti tra 2014 e 2024, la correlazione tra la variazione dell’istruzione e quella della disoccupazione giovanile è **−0,369** con Pearson e **−0,353** con Spearman.
- L’intervallo approssimato al 95% per la correlazione di Pearson è **[−0,657; 0,013]** e comprende zero. La stima è quindi incerta. L’analisi escludendo un Paese alla volta mantiene il segno negativo, ma la sua intensità varia.
- Nel 2024, la correlazione tra crescita del PIL pro capite e disoccupazione giovanile è circa **−0,08**, anch’essa vicina a zero.

## Interpretazione e limiti

I risultati descrivono associazioni nei dati e **non dimostrano rapporti di causa ed effetto**. L’indicatore di istruzione riguarda i 20–24enni, mentre quello di disoccupazione riguarda la forza lavoro tra 15 e 24 anni: le fasce d’età non coincidono. Inoltre, le statistiche descrittive assegnano lo stesso peso a ciascun Paese e non rappresentano una media ponderata della popolazione dell’UE.

## Come consultare il progetto

Il notebook `analisi_lavoro_giovanile_europa.ipynb` contiene i passaggi di acquisizione, pulizia, analisi e visualizzazione dei dati. Può essere aperto ed eseguito con [Google Colab](https://colab.research.google.com/).

## Fonti e documentazione

- [Banca Mondiale — documentazione API](https://datahelpdesk.worldbank.org/knowledgebase/articles/889392)
- [Eurostat — documentazione API](https://ec.europa.eu/eurostat/web/user-guides/data-browser/api-data-access/api-detailed-guidelines/api-statistics)
