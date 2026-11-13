# Flag Battle: sua chave da API do YouTube

O modo streamer lê o chat da sua live pela YouTube Data API. Sem chave você tem um teste de 5 minutos por dia; com sua própria chave gratuita você pode transmitir por horas. Leva uns 5 minutos.

## 1. Abra o Google Cloud

Acesse [console.cloud.google.com](https://console.cloud.google.com/) e entre com qualquer conta Google (não precisa ser a do seu canal). Aceite os termos, se pedir. Não precisa de cartão de crédito.

## 2. Crie um projeto

No topo da página, clique no seletor de projetos (**Select a project**) e depois em **New project**. Qualquer nome serve, por exemplo `flag-battle`. Clique em **Create** e confira se o novo projeto está selecionado no topo — todo o resto é feito nele.

## 3. Ative a YouTube Data API v3 — antes de criar a chave

Abra a [YouTube Data API v3](https://console.cloud.google.com/apis/library/youtube.googleapis.com) e clique em **Enable**. Ela está ativa quando o botão muda para **Manage**. Sem este passo a chave não vai funcionar.

## 4. Crie a chave

Abra [Credentials](https://console.cloud.google.com/apis/credentials) → **Create credentials** → **API key**. Na lista de restrições de API, marque só **YouTube Data API v3** e clique em **Create**. A janela **API key created** mostra sua chave — copie-a.

Se a YouTube Data API v3 não estiver na lista, volte ao passo 3. Deixe as restrições de aplicativo em **None**.

## 5. Cole no app

No Flag Battle: tela inicial → **Configurações** → modo **Duelo** → **Modo streamer** → **Lig.**. Toque no botão de colar ao lado de **Sua chave da API v3 do YouTube** — não no campo do texto de dica abaixo. A chave fica só no seu celular, no armazenamento seguro, e nunca aparece na tela.

## Se a chave for recusada

O bloco **PRÓXIMOS** mostra o motivo:

- **«YouTube Data API v3 está desativada para esta chave»** — faça o passo 3 no mesmo projeto da chave e espere alguns minutos.
- **«as restrições da chave bloqueiam o YouTube»** — abra a chave em [Credentials](https://console.cloud.google.com/apis/credentials): as restrições de API devem incluir **YouTube Data API v3** e as de aplicativo ficar em **None**.
- **«chave do YouTube inválida»** — a chave foi copiada pela metade: ela começa com `AIza` e tem 39 caracteres.

Depois volte ao menu e comece a live de novo.

## Bom saber

- **É grátis.** A cota padrão é de 10.000 unidades por dia. No modo «Instantânea» o chat chega em tempo real e a cota dá para cerca de 6 horas de live por dia; «Economia» estica para cerca de 12 horas, com até 10 segundos de atraso. O modo é escolhido no app.
- **A cota é zerada à meia-noite no horário do Pacífico.** Se acabar, o app mostra isso no bloco **PRÓXIMOS** e as lutas continuam com bandeiras aleatórias.
- Use o projeto só para o Flag Battle, para que nada mais gaste a cota.
- Para revogar a chave, exclua-a em [Credentials](https://console.cloud.google.com/apis/credentials).
