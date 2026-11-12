# Flag Battle : votre clé API YouTube

Le mode streamer lit le chat de votre direct via la YouTube Data API. Sans clé, vous avez un essai de 5 minutes par jour ; avec votre propre clé gratuite, vous pouvez diffuser pendant des heures. Comptez environ 5 minutes.

## 1. Ouvrez Google Cloud

Allez sur [console.cloud.google.com](https://console.cloud.google.com/) et connectez-vous avec n'importe quel compte Google (pas forcément celui de votre chaîne). Acceptez les conditions si on vous le demande. Aucune carte bancaire n'est nécessaire.

## 2. Créez un projet

En haut de la page, cliquez sur le sélecteur de projet (**Select a project**), puis sur **New project**. N'importe quel nom convient, par exemple `flag-battle`. Cliquez sur **Create** et vérifiez que le nouveau projet est sélectionné en haut.

## 3. Activez la YouTube Data API

Ouvrez [YouTube Data API v3](https://console.cloud.google.com/apis/library/youtube.googleapis.com) et cliquez sur **Enable**.

## 4. Créez la clé

Ouvrez [Credentials](https://console.cloud.google.com/apis/credentials) et cliquez sur **Create credentials** → **API key**. Ouvrez la nouvelle clé pour la modifier :

- **API restrictions** → **Restrict key** → cochez uniquement **YouTube Data API v3**. Ainsi, une clé divulguée ne servira à rien d'autre.
- **Application restrictions** peut rester sur **None**.

Cliquez sur **Save**, puis copiez la clé (**Show key** → copier).

## 5. Collez-la dans l'app

Dans Flag Battle, ouvrez **Paramètres → Duel → Mode streamer** et touchez le bouton Coller à côté du champ de la clé API YouTube. La clé est stockée uniquement sur votre téléphone, dans son stockage sécurisé, et n'est jamais affichée à l'écran.

## Bon à savoir

- **C'est gratuit.** Le quota standard est de 10 000 unités par jour. En mode « Instantané », le chat arrive en temps réel et le quota suffit pour environ 6 heures de direct par jour ; « Économie » l'étire à environ 12 heures, avec jusqu'à 10 secondes de retard. Le mode se choisit dans l'app.
- **Le quota est remis à zéro à minuit, heure du Pacifique.** S'il est épuisé, l'app l'indique dans le bloc **SUIVANT** et les combats continuent avec des drapeaux au hasard.
- Utilisez ce projet uniquement pour Flag Battle, afin que rien d'autre ne consomme son quota.
- Pour révoquer la clé, supprimez-la dans [Credentials](https://console.cloud.google.com/apis/credentials).
