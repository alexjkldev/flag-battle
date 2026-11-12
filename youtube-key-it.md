# Flag Battle: la tua chiave API di YouTube

La modalità streamer legge la chat della tua diretta tramite la YouTube Data API. Senza chiave hai una prova di 5 minuti al giorno; con la tua chiave gratuita puoi trasmettere per ore. Ci vogliono circa 5 minuti.

## 1. Apri Google Cloud

Vai su [console.cloud.google.com](https://console.cloud.google.com/) e accedi con un qualsiasi account Google (non per forza quello del canale). Accetta i termini se richiesto. Non serve la carta di credito.

## 2. Crea un progetto

In alto fai clic sul selettore di progetto (**Select a project**), poi su **New project**. Va bene qualsiasi nome, ad esempio `flag-battle`. Fai clic su **Create** e controlla che in alto sia selezionato il nuovo progetto.

## 3. Attiva la YouTube Data API

Apri [YouTube Data API v3](https://console.cloud.google.com/apis/library/youtube.googleapis.com) e fai clic su **Enable**.

## 4. Crea la chiave

Apri [Credentials](https://console.cloud.google.com/apis/credentials) e fai clic su **Create credentials** → **API key**. Apri la nuova chiave per modificarla:

- **API restrictions** → **Restrict key** → seleziona solo **YouTube Data API v3**. Così una chiave trapelata non potrà essere usata per altro.
- **Application restrictions** può restare su **None**.

Fai clic su **Save** e copia la chiave (**Show key** → copia).

## 5. Incollala nell'app

In Flag Battle apri **Impostazioni → Duello → Modalità streamer** e tocca il pulsante Incolla accanto al campo della chiave API di YouTube. La chiave resta solo sul tuo telefono, nell'archivio sicuro, e non viene mai mostrata sullo schermo.

## Buono a sapersi

- **È gratis.** La quota standard è di 10.000 unità al giorno. Leggendo la chat ogni 8 secondi basta per circa 4,4 ore di diretta al giorno (ogni 5 s ≈ 2,8 h, ogni 10 s ≈ 5,6 h); l'intervallo si sceglie nell'app.
- **La quota si azzera a mezzanotte, ora del Pacifico.** Se finisce, l'app lo mostra nel riquadro **PROSSIMI** e gli scontri continuano con bandiere casuali.
- Usa il progetto solo per Flag Battle, così nient'altro consuma la sua quota.
- Per revocare la chiave, eliminala in [Credentials](https://console.cloud.google.com/apis/credentials).
