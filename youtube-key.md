# Flag Battle: your YouTube API key

Streamer mode reads your live chat through the YouTube Data API. Without a key you get a 5-minute trial a day; with your own free key you can stream for hours. It takes about 5 minutes.

## 1. Open Google Cloud

Go to [console.cloud.google.com](https://console.cloud.google.com/) and sign in with any Google account (it does not have to be your channel's account). Accept the terms if asked. No credit card is needed.

## 2. Create a project

At the top of the page click the project picker (**Select a project**), then **New project**. Any name works, for example `flag-battle`. Click **Create**, then check that the new project is selected at the top — everything below happens in it.

## 3. Turn on YouTube Data API v3 — before creating the key

Open [YouTube Data API v3](https://console.cloud.google.com/apis/library/youtube.googleapis.com) and click **Enable**. It's on when the button changes to **Manage**. Without this step the key won't work.

## 4. Create the key

Open [Credentials](https://console.cloud.google.com/apis/credentials) → **Create credentials** → **API key**. In the API restrictions list tick only **YouTube Data API v3**, then click **Create**. The **API key created** window shows your key — copy it.

If YouTube Data API v3 isn't in the list, go back to step 3. Leave the application restrictions at **None**.

## 5. Paste it into the app

In Flag Battle: main screen → **Settings** → mode **Duel** → **Streamer mode** → **On**. Tap the paste button next to **Your YouTube API v3 key** — not into the hint text field below it. The key is stored only on your phone, in its secure storage, and is never shown on screen.

## If the key is rejected

The **NEXT** block shows why:

- **«YouTube Data API v3 is off for this key»** — do step 3 in the same project the key belongs to, then wait a few minutes.
- **«key restrictions block YouTube»** — open the key in [Credentials](https://console.cloud.google.com/apis/credentials): API restrictions must include **YouTube Data API v3**, application restrictions must be **None**.
- **«YouTube key is invalid»** — the key was copied incompletely: it starts with `AIza` and is 39 characters long.

After fixing it, go back to the menu and start the stream again.

## Good to know

- **It's free.** The standard quota is 10,000 units a day. In «Instant» mode the chat arrives in real time and the quota lasts about 6 hours of streaming a day; «Economy» stretches it to about 12 hours, with up to 10 seconds of delay. You pick the mode in the app.
- **The quota resets at midnight Pacific Time.** If it runs out, the app shows it in the **NEXT** block and fights go on with random flags.
- Use the project only for Flag Battle, so nothing else eats its quota.
- To revoke the key, delete it in [Credentials](https://console.cloud.google.com/apis/credentials).
