
# 📖 Guida Operativa e Manuale Utente: Viewer 2 (LS Software)

## 📋 Indice dei Contenuti

1. [Panoramica dell'Applicazione]()
2. [Dashboard e Monitoraggio di Stato]()
3. [Configurazione di Sistema (Settings)]()
* [3.1 Personalizzazione Interfaccia Grafica]()
* [3.2 Configurazione Connessione ()
* [3.3 Gestione Log, Report e Diagnostica]()
* [3.4 Moduli Aggiuntivi e Applicazioni Web]()
* [3.5 Mappatura Cartelle Parametri (.csv)]()
* [3.6 Personalizzazione Dashboard e Area Memoria Sidebar]()
* [3.7 Licenza, Modalità Sviluppatore e Aggiornamenti]()


4. [Editor CSV (Modifica Parametri)]()
5. [Traffic Monitor (Analisi Bus CAN)]()
6. [Modulo Parrot (CAN Replay & Invia Excel)]()
* [6.1 Invio Messaggi CAN tramite File Excel]()
* [6.2 Riproduzione Tracce CAN (.trc)]()


7. [Modulo XMT]()
8. [Ispezione e Monitoraggio Registri PLC]()
9. [Installazione certificati]()
10. [Aggiornamento]()

## 1. Panoramica dell'Applicazione

**Viewer 2** (sviluppato da *LS / Systemada*) è una suite software industriale avanzata per l'interfacciamento, la diagnostica, la configurazione dei parametri e l'analisi della rete su bus CAN ed Ethernet per centraline e PLC.

| Struttura Interfaccia | Descrizione |
| --- | --- |
| **Barra Superiore** | Mostra data, ora di sistema, stato batteria (100%) e logo del brand LS. |
| **Sidebar (Barra Laterale)** | Menu di navigazione principale per accedere alle varie sezioni. |
| **Area di Lavoro** | Spazio centrale dinamico per la configurazione e il monitoraggio. |


## 2. Dashboard e Monitoraggio di Stato

![Schermata Dashboard - Mostra le 4 schede principali dello stato di sistema.](media\dashboard.png)

### 🛠️ Come accedere

Cliccare sull'icona **Dashboard** (la prima in alto nella barra laterale).

### ⚙️ Funzionalità

La Dashboard mostra le quattro metriche di stato del **System Status**:

* **CAN Bus**: Indica lo stato di connessione hardware (*Connected* / *Disconnected*).
* **Bus load**: Carico percentuale di banda occupato sul bus CAN.
* **Fast Messages**: Conteggio dei messaggi CAN ad alta frequenza (intervallo $< 80\text{ ms}$).
* **Active IDs**: Numero totale di ID CAN attivi rilevati.


## 3. Configurazione di Sistema (Settings)

![Schermata Settings - Pannello generale con le impostazioni di connessione, tema e percorsi.](media\settings.png)

---

### 3.1 Personalizzazione Interfaccia Grafica

* **Dark Mode**: Switch posizionato in alto a destra per alternare tema scuro e chiaro.
* **Posizione Barra Laterale**: Permette di spostare la barra laterale tra *Sinistra* e *Destra*.
* **App Accent Color**: Selezione della palette di colori (viola, blu, verde, giallo, ecc.) per personalizzare gli elementi attivi dell'app.

---

### 3.2 Configurazione Connessione (CAN Bus / Ethernet / SFTP)

#### A. Connessione CAN Bus

1. Nel blocco **Connection Interface**, selezionare **CAN Bus**.
2. Impostare il **CAN Configuration** / Baudrate (es. `250 kbit/s`).
3. Selezionare l'interfaccia hardware dal menu **CAN Interface / Channel** (es. `PCAN-USB 1`).
4. Definire il **PLC Node ID (Dec)** (default `32`).

#### B. Connessione Ethernet

1. Selezionare la scheda **Ethernet**.
2. Configurare **PLC IP Address** (es. `192.168.82.247`), **Porta** (`8000`) e **Node ID** (`32`).

#### C. Parametri SFTP

Compilare i campi **Indirizzo IP** (es. `172.29.138.181`), **Username** (`root`), **Password** e **Porta** (`2222`) per il trasferimento remoto dei log.

---

### 3.3 Gestione Log, Report e Diagnostica

* **Scarica BBox / Scarica Error Report**: Pulsanti dedicati per estrarre direttamente dalla centralina i file di report diagnostico.
* **Rollover / Comando**: Caselle drag-and-drop dove trascinare file di comando per la centrale.

---

### 3.4 Moduli Aggiuntivi e Applicazioni Web

Switch ON/OFF per abilitare nel menu laterale i moduli integrati:

* **AI Assistant**: Assistente intelligente per la guida operativa.
* **MCarView**: Interfaccia web centralina (Porta 8191).
* **MCarConn**: Configurazione modem (Porta 8090).
* **Telecamere**: Visualizzazione stream video.
* **Web**: Pagine web custom dal dispositivo.

---

### 3.5 Mappatura Cartelle Parametri (.csv)

![Schermata Selezione Cartella - Finestra per la modifica del percorso di un progetto.](media\projects.png)

#### 🛠️ Come cambiare percorso ad un progetto (es. Daxx):

1. Individuare la riga del progetto nella lista (es. *Entero Esse*, *FP30*, *Daxx*).
2. Cliccare sull'icona della **matita rossa** (**Modifica**).
3. Nella finestra pop-up *Modifica Cartella Parametri*, cliccare su **Sfoglia**.
4. Selezionare il percorso del progetto (es. `D:\systemada\management\projects\...`).
5. Cliccare su **Seleziona cartella** e poi su **Salva**.
6. Per rendere il progetto predefinito, cliccare sulla **spunta verde**.

---

### 3.6 Personalizzazione Dashboard e Area Memoria Sidebar

* **Personalizzazione Dashboard**: Switch per nascondere o mostrare i blocchi *System Status*, *Hardware Training*, *Quick Actions*, *Barra di Stato*, *Monitoraggio Sistema*, *Firmware & Device Info*.
* **Sidebar Memory Areas**: Attivazione dei pulsanti per la memoria PLC sulla barra laterale (`WORDP`, `DWORDP`, `BYTEM`, `MAPLOGICI`, `MAPLOGICO`, ecc.).

---

### 3.7 Licenza, Modalità Sviluppatore e Aggiornamenti

* **Inizializzazione Centrale (Reset)**: Ripristina i parametri di fabbrica.
* **Licenza Software**: Visualizza lo stato (`Affinix - Assolutia`), l'ID Macchina e permette l'attivazione/rimozione delle chiavi.
* **Modalità Sviluppatore**: Attivazione tramite codice OTP.
* **Controlla aggiornamenti**: Pulsante in basso per verificare nuove versioni (es. *Viewer 2 Versione 10.0.0 Build 0*).


## 4. Editor CSV (Modifica Parametri)

![Schermata Editor CSV - Tabella di editing delle variabili di configurazione.](media\editor.png)

### 🛠️ Come accedere

Cliccare sull'icona **Editor CSV** / **Parametri** nella barra laterale.

### ⚙️ Come funziona:

1. Scegliere la tabella dal menu a tendina in alto a destra (es. `MAPLOGICO`, `WORDP`).
2. Configurare i parametri riga per riga:
* **Min / Max**: Range consentito (es. `-32768` a `32767`).
* **Unità**: Unità di misura (`rpm`, `bar`, `°C`, `0.1s`).
* **Formato**: Formato di visualizzazione (`dec`, `hex`, `bin`).
* **Nascosto**: Checkbox per rendere visibile o meno la variabile all'utente.
* **Nome e Descrizione**: Definizione della variabile (es. `engRpmMax` - *Ad[rpm] max motore*).


3. Utilizzare **+ Aggiungi riga** per creare nuove variabili o la **Cestino rosso** per eliminarle.
4. Cliccare su **Salva** in alto a destra.


## 5. Traffic Monitor (Analisi Bus CAN)

![Schermata Traffic Monitor - Monitoraggio live dei pacchetti CAN.](media\can_monitor.png)

### 🛠️ Come accedere

Cliccare sull'icona del segnale antenna nella barra laterale.

### ⚙️ Come funziona:

Visualizza la tabella del traffico CAN in tempo reale con le seguenti colonna dati:

* **ID (Hex)** | **Type** | **DLC** | **Data Bytes** | **Count** | **Cycle (ms)**


## 6. Modulo Parrot (CAN Replay & Invia Excel)

![Schermata Parrot - Invia Excel - Interfaccia per la trasmissione dei messaggi PDO caricati da Excel.](media\parrot_excel.png)

---

### 6.1 Invio Messaggi CAN tramite File Excel

1. Selezionare la scheda **Invia Excel** in alto.
2. Cliccare su **Carica XLSX** e selezionare il file di mappatura (es. `25002_Comm_V02.xlsx`).
3. L'app caricherà i gruppi PDO (es. `PDO1 (0x181)`, `PDO2 (0x281)`, `PDO3 (0x381)`, `PDO4 (0x481)`).
4. **Modifica valori**:
* Espandere la freccia a lato del PDO.
* Impostare le variabili (es. `bm.emergency`, `bm.engSpeed`) tramite toggle o campi numerici.


5. **Trasmissione**:
* Scegliere la frequenza (es. `100 ms`).
* Cliccare su **Avvia** (blu) per inviare. Cliccare su **Stop** (rosso) per interrompere.



---

### 6.2 Riproduzione Tracce CAN (.trc)

1. Aprire la scheda **Replay TRC**.
2. Cliccare su **Carica TRC** e selezionare un log (es. `noCharging.trc`).
3. Utilizzare i comandi multimediali:
* **Play (Verde)**: Avvia il replay sul bus CAN.
* **Pausa**: Mette in pausa il flusso.
* **Stop**: Interrompe la riproduzione.
* **Loop (Ripeti)**: Riproduce la traccia in ciclo continuo.


## 7. Modulo XMT

### 🛠️ Come accedere

Cliccare sull'icona **XMT** nella barra laterale.

### ⚙️ Come funziona:

1. Cliccare su **Apri file .xmt** al centro o in alto a destra.
2. Caricare il file `.xmt` compatibile con *PCAN-View* per trasmettere o analizzare tracce di messaggi su bus CAN.

## 8. Ispezione e Monitoraggio Registri PLC

![Schermata Ispezione Registri PLC - Tabella per la lettura e il polling continuativo delle variabili WORDP / MAPLOGICI.](media\param.png)

### 🛠️ Come accedere

Cliccare su una delle voci abilitate nella barra laterale (es. `WORDP`, `DWORDP`, `BYTEM`, `MAPLOGICI`, `MAPLOGICO`).

### ⚙️ Guida alle Funzioni:

1. **Lettura Singola / Selezione Range**:
* Impostare **Start ID** (es. `0`) e **Amount** (es. `10`).
* Cliccare su **Request Read** per aggiornare i valori.


2. **Polling Continuo (Loop)**:
* Attivare il toggle **Loop** in alto a sinistra per aggiornare costantemente i dati in tempo reale.


3. **Importazione / Esportazione**:
* **Import CSV**: Carica la configurazione da file esterno.
* **Export CSV**: Salva la tabella dei registri corretta in formato `.csv`.


4. **Struttura Dati**:
* Visualizzazione completa di `ID`, `Name`, `Value`, `Min`, `Max` e `Description`.

## 9. Installazione certificati

<video controls>
  <source src="installazione_certificati.mp4" type="video/mp4">
</video>

## 10. Aggiornamento

<video controls>
  <source src="aggiornamento.mp4" type="video/mp4">
</video>