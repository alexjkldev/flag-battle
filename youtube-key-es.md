# Flag Battle: tu clave de la API de YouTube

El modo streamer lee el chat de tu directo mediante la YouTube Data API. Sin clave tienes una prueba de 5 minutos al día; con tu propia clave gratuita puedes emitir durante horas. Se tarda unos 5 minutos.

## 1. Abre Google Cloud

Ve a [console.cloud.google.com](https://console.cloud.google.com/) e inicia sesión con cualquier cuenta de Google (no tiene que ser la de tu canal). Acepta las condiciones si te lo pide. No hace falta tarjeta.

## 2. Crea un proyecto

Arriba, haz clic en el selector de proyectos (**Select a project**) y luego en **New project**. Cualquier nombre sirve, por ejemplo `flag-battle`. Pulsa **Create** y comprueba que arriba está seleccionado el proyecto nuevo.

## 3. Activa la YouTube Data API

Abre [YouTube Data API v3](https://console.cloud.google.com/apis/library/youtube.googleapis.com) y pulsa **Enable**.

## 4. Crea la clave

Abre [Credentials](https://console.cloud.google.com/apis/credentials) y pulsa **Create credentials** → **API key**. Abre la clave nueva para editarla:

- **API restrictions** → **Restrict key** → marca solo **YouTube Data API v3**. Así, si la clave se filtra, no servirá para nada más.
- **Application restrictions** puede quedarse en **None**.

Pulsa **Save** y copia la clave (**Show key** → copiar).

## 5. Pégala en la app

En Flag Battle abre **Ajustes → Duelo → Modo streamer** y toca el botón de pegar junto al campo de la clave de la API de YouTube. La clave se guarda solo en tu móvil, en su almacenamiento seguro, y nunca se muestra en pantalla.

## Conviene saber

- **Es gratis.** La cuota estándar es de 10.000 unidades al día. En el modo «Al instante» el chat llega en tiempo real y la cuota da para unas 6 horas de directo al día; «Ahorro» la estira a unas 12 horas, con hasta 10 segundos de retraso. El modo se elige en la app.
- **La cuota se reinicia a medianoche, hora del Pacífico.** Si se agota, la app lo muestra en el bloque **SIGUIENTE** y los combates siguen con banderas al azar.
- Usa el proyecto solo para Flag Battle, para que nada más gaste su cuota.
- Para revocar la clave, bórrala en [Credentials](https://console.cloud.google.com/apis/credentials).
