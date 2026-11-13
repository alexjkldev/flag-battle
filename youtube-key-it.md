# Flag Battle: la tua chiave API di YouTube

La modalità streamer legge la chat della tua diretta tramite la YouTube Data API. Senza chiave hai una prova di 5 minuti al giorno; con la tua chiave gratuita puoi trasmettere per ore. Ci vogliono circa 5 minuti.

## 1. Apri Google Cloud

Vai su [console.cloud.google.com](https://console.cloud.google.com/) e accedi con un qualsiasi account Google (non per forza quello del canale). Accetta i termini se richiesto. Non serve la carta di credito.

## 2. Crea un progetto

In alto nella pagina fai clic sul selettore dei progetti (**Select a project**), poi su **New project**. Va bene qualsiasi nome, per esempio `flag-battle`. Fai clic su **Create** e controlla che in alto sia selezionato il nuovo progetto — tutto il resto si fa lì.

## 3. Attiva YouTube Data API v3 — prima di creare la chiave

Apri [YouTube Data API v3](https://console.cloud.google.com/apis/library/youtube.googleapis.com) e fai clic su **Enable**. È attiva quando il pulsante diventa **Manage**. Senza questo passaggio la chiave non funziona.

## 4. Crea la chiave

Apri [Credentials](https://console.cloud.google.com/apis/credentials) → **Create credentials** → **API key**. Nell'elenco delle restrizioni API spunta solo **YouTube Data API v3** e fai clic su **Create**. Nella finestra **API key created** c'è la tua chiave — copiala.

Se YouTube Data API v3 non è nell'elenco, torna al passaggio 3. Lascia le restrizioni delle applicazioni su **None**.

## 5. Incollala nell'app

In Flag Battle: schermata principale → **Impostazioni** → modalità **Duello** → **Modalità streamer** → **On**. Tocca il pulsante incolla accanto a **La tua chiave API v3 di YouTube** — non nel campo del testo suggerimento sotto. La chiave resta solo sul tuo telefono, nella memoria protetta, e non viene mai mostrata sullo schermo.

## Se la chiave viene rifiutata

Il blocco **PROSSIMI** mostra il motivo:

- **«YouTube Data API v3 è disattivata per questa chiave»** — esegui il passaggio 3 nello stesso progetto della chiave e attendi qualche minuto.
- **«le restrizioni della chiave bloccano YouTube»** — apri la chiave in [Credentials](https://console.cloud.google.com/apis/credentials): tra le restrizioni API deve esserci **YouTube Data API v3**, le restrizioni delle applicazioni su **None**.
- **«chiave YouTube non valida»** — la chiave è stata copiata a metà: inizia con `AIza` ed è lunga 39 caratteri.

Poi torna al menu e avvia di nuovo la diretta.

## Buono a sapersi

- **È gratis.** La quota standard è di 10.000 unità al giorno. In modalità «Istantanea» la chat arriva in tempo reale e la quota basta per circa 6 ore di diretta al giorno; «Risparmio» la allunga a circa 12 ore, con fino a 10 secondi di ritardo. La modalità si sceglie nell'app.
- **La quota si azzera a mezzanotte, ora del Pacifico.** Se finisce, l'app lo mostra nel riquadro **PROSSIMI** e gli scontri continuano con bandiere casuali.
- Usa il progetto solo per Flag Battle, così nient'altro consuma la sua quota.
- Per revocare la chiave, eliminala in [Credentials](https://console.cloud.google.com/apis/credentials).
