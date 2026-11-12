# Flag Battle: a sua chave da API do YouTube

O modo streamer lê o chat da sua transmissão em direto através da YouTube Data API. Sem chave tem um teste de 5 minutos por dia; com a sua própria chave gratuita pode transmitir durante horas. Demora cerca de 5 minutos.

## 1. Abra o Google Cloud

Aceda a [console.cloud.google.com](https://console.cloud.google.com/) e inicie sessão com qualquer conta Google (não tem de ser a do seu canal). Aceite os termos, se for pedido. Não é preciso cartão de crédito.

## 2. Crie um projeto

No topo da página, clique no seletor de projetos (**Select a project**) e depois em **New project**. Qualquer nome serve, por exemplo `flag-battle`. Clique em **Create** e confirme que o novo projeto está selecionado no topo.

## 3. Ative a YouTube Data API

Abra [YouTube Data API v3](https://console.cloud.google.com/apis/library/youtube.googleapis.com) e clique em **Enable**.

## 4. Crie a chave

Abra [Credentials](https://console.cloud.google.com/apis/credentials) e clique em **Create credentials** → **API key**. Abra a nova chave para a editar:

- **API restrictions** → **Restrict key** → selecione apenas **YouTube Data API v3**. Assim, uma chave divulgada não serve para mais nada.
- **Application restrictions** pode ficar em **None**.

Clique em **Save** e copie a chave (**Show key** → copiar).

## 5. Cole-a na app

Na Flag Battle, abra **Definições → Duelo → Modo streamer** e toque no botão de colar junto ao campo da chave da API do YouTube. A chave fica apenas no seu telemóvel, no armazenamento seguro, e nunca é mostrada no ecrã.

## É bom saber

- **É gratuito.** A quota padrão é de 10 000 unidades por dia. No modo «Instantânea» o chat chega em tempo real e a quota chega para cerca de 6 horas de direto por dia; «Poupança» estica-a para cerca de 12 horas, com até 10 segundos de atraso. O modo escolhe-se na app.
- **A quota é reposta à meia-noite, hora do Pacífico.** Se se esgotar, a app mostra-o no bloco **SEGUINTES** e os combates continuam com bandeiras aleatórias.
- Use o projeto apenas para a Flag Battle, para que nada mais gaste a quota.
- Para revogar a chave, elimine-a em [Credentials](https://console.cloud.google.com/apis/credentials).
