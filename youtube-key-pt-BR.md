# Flag Battle: sua chave da API do YouTube

O modo streamer lê o chat da sua live pela YouTube Data API. Sem chave você tem um teste de 5 minutos por dia; com sua própria chave gratuita você pode transmitir por horas. Leva uns 5 minutos.

## 1. Abra o Google Cloud

Acesse [console.cloud.google.com](https://console.cloud.google.com/) e entre com qualquer conta Google (não precisa ser a do seu canal). Aceite os termos, se pedir. Não precisa de cartão de crédito.

## 2. Crie um projeto

No topo da página, clique no seletor de projetos (**Select a project**) e depois em **New project**. Qualquer nome serve, por exemplo `flag-battle`. Clique em **Create** e confira se o novo projeto está selecionado no topo.

## 3. Ative a YouTube Data API

Abra [YouTube Data API v3](https://console.cloud.google.com/apis/library/youtube.googleapis.com) e clique em **Enable**.

## 4. Crie a chave

Abra [Credentials](https://console.cloud.google.com/apis/credentials) e clique em **Create credentials** → **API key**. Abra a nova chave para editar:

- **API restrictions** → **Restrict key** → marque só **YouTube Data API v3**. Assim, uma chave vazada não serve para mais nada.
- **Application restrictions** pode ficar em **None**.

Clique em **Save** e copie a chave (**Show key** → copiar).

## 5. Cole no app

No Flag Battle, abra **Configurações → Duelo → Modo streamer** e toque no botão de colar ao lado do campo da chave da API do YouTube. A chave fica só no seu celular, no armazenamento seguro, e nunca aparece na tela.

## Bom saber

- **É grátis.** A cota padrão é de 10.000 unidades por dia. No modo «Instantânea» o chat chega em tempo real e a cota dá para cerca de 6 horas de live por dia; «Economia» estica para cerca de 12 horas, com até 10 segundos de atraso. O modo é escolhido no app.
- **A cota é zerada à meia-noite no horário do Pacífico.** Se acabar, o app mostra isso no bloco **PRÓXIMOS** e as lutas continuam com bandeiras aleatórias.
- Use o projeto só para o Flag Battle, para que nada mais gaste a cota.
- Para revogar a chave, exclua-a em [Credentials](https://console.cloud.google.com/apis/credentials).
