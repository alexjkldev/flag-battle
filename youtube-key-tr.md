# Flag Battle: YouTube API anahtarınız

Yayıncı modu, canlı yayınınızın sohbetini YouTube Data API üzerinden okur. Anahtar olmadan günde 5 dakikalık deneme hakkınız olur; kendi ücretsiz anahtarınızla saatlerce yayın yapabilirsiniz. Yaklaşık 5 dakika sürer.

## 1. Google Cloud'u açın

[console.cloud.google.com](https://console.cloud.google.com/) adresine gidin ve herhangi bir Google hesabıyla oturum açın (kanalınızın hesabı olması gerekmez). İstenirse şartları kabul edin. Kredi kartı gerekmez.

## 2. Proje oluşturun

Sayfanın üstünde proje seçiciye (**Select a project**), ardından **New project**'e tıklayın. Herhangi bir ad olur, örneğin `flag-battle`. **Create**'e tıklayın ve üstte yeni projenin seçili olduğundan emin olun.

## 3. YouTube Data API'yi etkinleştirin

[YouTube Data API v3](https://console.cloud.google.com/apis/library/youtube.googleapis.com) sayfasını açın ve **Enable**'a tıklayın.

## 4. Anahtarı oluşturun

[Credentials](https://console.cloud.google.com/apis/credentials) sayfasını açın, **Create credentials** → **API key**'e tıklayın. Yeni anahtarı düzenlemek için açın:

- **API restrictions** → **Restrict key** → yalnızca **YouTube Data API v3**'ü işaretleyin. Böylece sızan bir anahtar başka hiçbir şey için kullanılamaz.
- **Application restrictions** **None** olarak kalabilir.

**Save**'e tıklayın ve anahtarı kopyalayın (**Show key** → kopyala).

## 5. Uygulamaya yapıştırın

Flag Battle'da **Ayarlar → Düello → Yayıncı modu**'nu açın ve YouTube API anahtarı alanının yanındaki yapıştır düğmesine dokunun. Anahtar yalnızca telefonunuzda, güvenli depolama alanında saklanır ve ekranda asla gösterilmez.

## Bilmekte fayda var

- **Ücretsizdir.** Standart kota günde 10.000 birimdir. «Anında» modunda sohbet gerçek zamanlı gelir ve kota günde yaklaşık 6 saatlik yayına yeter; «Tasarruf» bunu en fazla 10 saniye gecikmeyle yaklaşık 12 saate çıkarır. Modu uygulamada seçersiniz.
- **Kota Pasifik saatiyle gece yarısı sıfırlanır.** Biterse uygulama bunu **SIRADAKİ** bloğunda gösterir ve dövüşler rastgele bayraklarla sürer.
- Kotayı başka bir şey tüketmesin diye projeyi yalnızca Flag Battle için kullanın.
- Anahtarı iptal etmek için [Credentials](https://console.cloud.google.com/apis/credentials) sayfasında silin.
