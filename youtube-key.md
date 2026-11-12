# Flag Battle: your YouTube API key

Streamer mode reads your live chat through the YouTube Data API. Without a key you get a 5-minute trial a day; with your own free key you can stream for hours. It takes about 5 minutes.

## 1. Open Google Cloud

Go to [console.cloud.google.com](https://console.cloud.google.com/) and sign in with any Google account (it does not have to be your channel's account). Accept the terms if asked. No credit card is needed.

## 2. Create a project

At the top of the page click the project picker (**Select a project**), then **New project**. Any name works, for example `flag-battle`. Click **Create** and make sure the new project is selected at the top.

## 3. Turn on the YouTube Data API

Open [YouTube Data API v3](https://console.cloud.google.com/apis/library/youtube.googleapis.com) and click **Enable**.

## 4. Create the key

Open [Credentials](https://console.cloud.google.com/apis/credentials), click **Create credentials** → **API key**. Open the new key to edit it:

- **API restrictions** → **Restrict key** → tick only **YouTube Data API v3**. Then a leaked key can't be used for anything else.
- **Application restrictions** can stay **None**.

Click **Save**, then copy the key (**Show key** → copy).

## 5. Paste it into the app

In Flag Battle open **Settings → Duel → Streamer mode** and tap the paste button next to **Your YouTube API key**. The key is stored only on your phone, in its secure storage, and is never shown on screen.

## Good to know

- **It's free.** The standard quota is 10,000 units a day. In «Instant» mode the chat arrives in real time and the quota lasts about 6 hours of streaming a day; «Economy» stretches it to about 12 hours, with up to 10 seconds of delay. You pick the mode in the app.
- **The quota resets at midnight Pacific Time.** If it runs out, the app shows it in the **NEXT** block and fights go on with random flags.
- Use the project only for Flag Battle, so nothing else eats its quota.
- To revoke the key, delete it in [Credentials](https://console.cloud.google.com/apis/credentials).
