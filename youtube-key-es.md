# Flag Battle: tu clave de la API de YouTube

El modo streamer lee el chat de tu directo mediante la YouTube Data API. Sin clave tienes una prueba de 5 minutos al día; con tu propia clave gratuita puedes emitir durante horas. Se tarda unos 5 minutos.

## 1. Abre Google Cloud

Ve a [console.cloud.google.com](https://console.cloud.google.com/) e inicia sesión con cualquier cuenta de Google (no tiene que ser la de tu canal). Acepta las condiciones si te lo pide. No hace falta tarjeta.

## 2. Crea un proyecto

Arriba de la página pulsa el selector de proyectos (**Select a project**) y luego **New project**. Cualquier nombre sirve, por ejemplo `flag-battle`. Pulsa **Create** y comprueba que arriba está seleccionado el proyecto nuevo — todo lo demás se hace en él.

## 3. Activa YouTube Data API v3 — antes de crear la clave

Abre [YouTube Data API v3](https://console.cloud.google.com/apis/library/youtube.googleapis.com) y pulsa **Enable**. Está activada cuando el botón cambia a **Manage**. Sin este paso la clave no funcionará.

## 4. Crea la clave

Abre [Credentials](https://console.cloud.google.com/apis/credentials) → **Create credentials** → **API key**. En la lista de restricciones de API marca solo **YouTube Data API v3** y pulsa **Create**. En la ventana **API key created** aparece tu clave — cópiala.

Si YouTube Data API v3 no está en la lista, vuelve al paso 3. Deja las restricciones de aplicación en **None**.

## 5. Pégala en la app

En Flag Battle: pantalla principal → **Ajustes** → modo **Duelo** → **Modo streamer** → **Sí**. Pulsa el botón de pegar junto a **Tu clave de la API v3 de YouTube** — no en el campo de texto de la pista de debajo. La clave se guarda solo en tu teléfono, en su almacenamiento seguro, y nunca se muestra en pantalla.

## Si la clave es rechazada

El bloque **SIGUIENTE** muestra el motivo:

- **«YouTube Data API v3 está desactivada para esta clave»** — haz el paso 3 en el mismo proyecto de la clave y espera unos minutos.
- **«las restricciones de la clave bloquean YouTube»** — abre la clave en [Credentials](https://console.cloud.google.com/apis/credentials): en las restricciones de API debe estar **YouTube Data API v3** y las de aplicación en **None**.
- **«la clave de YouTube no es válida»** — la clave se copió incompleta: empieza por `AIza` y tiene 39 caracteres.

Después vuelve al menú e inicia el directo de nuevo.

## Conviene saber

- **Es gratis.** La cuota estándar es de 10.000 unidades al día. En el modo «Al instante» el chat llega en tiempo real y la cuota da para unas 6 horas de directo al día; «Ahorro» la estira a unas 12 horas, con hasta 10 segundos de retraso. El modo se elige en la app.
- **La cuota se reinicia a medianoche, hora del Pacífico.** Si se agota, la app lo muestra en el bloque **SIGUIENTE** y los combates siguen con banderas al azar.
- Usa el proyecto solo para Flag Battle, para que nada más gaste su cuota.
- Para revocar la clave, bórrala en [Credentials](https://console.cloud.google.com/apis/credentials).
