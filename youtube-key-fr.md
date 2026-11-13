# Flag Battle : votre clé API YouTube

Le mode streamer lit le chat de votre direct via la YouTube Data API. Sans clé, vous avez un essai de 5 minutes par jour ; avec votre propre clé gratuite, vous pouvez diffuser pendant des heures. Comptez environ 5 minutes.

## 1. Ouvrez Google Cloud

Allez sur [console.cloud.google.com](https://console.cloud.google.com/) et connectez-vous avec n'importe quel compte Google (pas forcément celui de votre chaîne). Acceptez les conditions si on vous le demande. Aucune carte bancaire n'est nécessaire.

## 2. Créez un projet

En haut de la page, cliquez sur le sélecteur de projet (**Select a project**), puis **New project**. N'importe quel nom convient, par exemple `flag-battle`. Cliquez sur **Create** et vérifiez qu'en haut le nouveau projet est sélectionné — tout le reste se fait dedans.

## 3. Activez YouTube Data API v3 — avant de créer la clé

Ouvrez [YouTube Data API v3](https://console.cloud.google.com/apis/library/youtube.googleapis.com) et cliquez sur **Enable**. Elle est activée quand le bouton devient **Manage**. Sans cette étape, la clé ne fonctionnera pas.

## 4. Créez la clé

Ouvrez [Credentials](https://console.cloud.google.com/apis/credentials) → **Create credentials** → **API key**. Dans la liste des restrictions d'API, cochez seulement **YouTube Data API v3**, puis cliquez sur **Create**. La fenêtre **API key created** affiche votre clé — copiez-la.

Si YouTube Data API v3 n'est pas dans la liste, revenez à l'étape 3. Laissez les restrictions d'application sur **None**.

## 5. Collez-la dans l'app

Dans Flag Battle : écran principal → **Paramètres** → mode **Duel** → **Mode streamer** → **Oui**. Touchez le bouton coller à côté de **Ta clé YouTube API v3** — pas dans le champ du texte d'indice en dessous. La clé est stockée uniquement sur votre téléphone, dans son stockage sécurisé, et n'est jamais affichée à l'écran.

## Si la clé est refusée

Le bloc **SUIVANT** indique pourquoi :

- **« YouTube Data API v3 est désactivée pour cette clé »** — faites l'étape 3 dans le même projet que la clé, puis attendez quelques minutes.
- **« les restrictions de la clé bloquent YouTube »** — ouvrez la clé dans [Credentials](https://console.cloud.google.com/apis/credentials) : les restrictions d'API doivent inclure **YouTube Data API v3**, les restrictions d'application doivent être sur **None**.
- **« clé YouTube invalide »** — la clé a été copiée incomplète : elle commence par `AIza` et fait 39 caractères.

Ensuite, revenez au menu et relancez le direct.

## Bon à savoir

- **C'est gratuit.** Le quota standard est de 10 000 unités par jour. En mode « Instantané », le chat arrive en temps réel et le quota suffit pour environ 6 heures de direct par jour ; « Économie » l'étire à environ 12 heures, avec jusqu'à 10 secondes de retard. Le mode se choisit dans l'app.
- **Le quota est remis à zéro à minuit, heure du Pacifique.** S'il est épuisé, l'app l'indique dans le bloc **SUIVANT** et les combats continuent avec des drapeaux au hasard.
- Utilisez ce projet uniquement pour Flag Battle, afin que rien d'autre ne consomme son quota.
- Pour révoquer la clé, supprimez-la dans [Credentials](https://console.cloud.google.com/apis/credentials).
