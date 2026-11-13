# Flag Battle: YouTube API anahtarınız

Yayıncı modu, canlı yayınınızın sohbetini YouTube Data API üzerinden okur. Anahtar olmadan günde 5 dakikalık deneme hakkınız olur; kendi ücretsiz anahtarınızla saatlerce yayın yapabilirsiniz. Yaklaşık 5 dakika sürer.

## 1. Google Cloud'u açın

[console.cloud.google.com](https://console.cloud.google.com/) adresine gidin ve herhangi bir Google hesabıyla oturum açın (kanalınızın hesabı olması gerekmez). İstenirse şartları kabul edin. Kredi kartı gerekmez.

## 2. Proje oluşturun

Sayfanın üstünde proje seçiciye (**Select a project**), ardından **New project**'e tıklayın. Herhangi bir ad olur, örneğin `flag-battle`. **Create**'e tıklayın ve üstte yeni projenin seçili olduğunu kontrol edin — sonraki her şey onun içinde yapılır.

## 3. YouTube Data API v3'ü açın — anahtarı oluşturmadan önce

[YouTube Data API v3](https://console.cloud.google.com/apis/library/youtube.googleapis.com) sayfasını açın ve **Enable**'a tıklayın. Düğme **Manage** olduğunda açılmıştır. Bu adım olmadan anahtar çalışmaz.

## 4. Anahtarı oluşturun

[Credentials](https://console.cloud.google.com/apis/credentials) → **Create credentials** → **API key**. API kısıtlamaları listesinde yalnızca **YouTube Data API v3**'ü işaretleyin ve **Create**'e tıklayın. **API key created** penceresinde anahtarınız görünür — kopyalayın.

Listede YouTube Data API v3 yoksa 3. adıma dönün. Uygulama kısıtlamalarını **None** bırakın.

## 5. Uygulamaya yapıştırın

Flag Battle'da: ana ekran → **Ayarlar** → **Düello** modu → **Yayıncı modu** → **Açık**. **YouTube API v3 anahtarın** alanının yanındaki yapıştır düğmesine dokunun — altındaki ipucu metni alanına değil. Anahtar yalnızca telefonunuzda, güvenli depolamada saklanır ve ekranda asla gösterilmez.

## Anahtar reddedilirse

Nedeni **SIRADAKİ** bloğunda görünür:

- **«bu anahtar için YouTube Data API v3 kapalı»** — anahtarın ait olduğu projede 3. adımı yapın ve birkaç dakika bekleyin.
- **«anahtar kısıtlamaları YouTube’u engelliyor»** — anahtarı [Credentials](https://console.cloud.google.com/apis/credentials) içinde açın: API kısıtlamalarında **YouTube Data API v3** olmalı, uygulama kısıtlamaları **None** olmalı.
- **«YouTube anahtarı geçersiz»** — anahtar eksik kopyalanmış: `AIza` ile başlar ve 39 karakterdir.

Ardından menüye dönüp yayını yeniden başlatın.

## Bilmekte fayda var

- **Ücretsizdir.** Standart kota günde 10.000 birimdir. «Anında» modunda sohbet gerçek zamanlı gelir ve kota günde yaklaşık 6 saatlik yayına yeter; «Tasarruf» bunu en fazla 10 saniye gecikmeyle yaklaşık 12 saate çıkarır. Modu uygulamada seçersiniz.
- **Kota Pasifik saatiyle gece yarısı sıfırlanır.** Biterse uygulama bunu **SIRADAKİ** bloğunda gösterir ve dövüşler rastgele bayraklarla sürer.
- Kotayı başka bir şey tüketmesin diye projeyi yalnızca Flag Battle için kullanın.
- Anahtarı iptal etmek için [Credentials](https://console.cloud.google.com/apis/credentials) sayfasında silin.
