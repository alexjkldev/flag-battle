# Flag Battle: a sua chave da API do YouTube

O modo streamer lê o chat da sua transmissão em direto através da YouTube Data API. Sem chave tem um teste de 5 minutos por dia; com a sua própria chave gratuita pode transmitir durante horas. Demora cerca de 5 minutos.

## 1. Abra o Google Cloud

Aceda a [console.cloud.google.com](https://console.cloud.google.com/) e inicie sessão com qualquer conta Google (não tem de ser a do seu canal). Aceite os termos, se for pedido. Não é preciso cartão de crédito.

## 2. Crie um projeto

No topo da página, clique no seletor de projetos (**Select a project**) e depois em **New project**. Qualquer nome serve, por exemplo `flag-battle`. Clique em **Create** e confirme que o novo projeto está selecionado no topo — tudo o resto faz-se nele.

## 3. Ative a YouTube Data API v3 — antes de criar a chave

Abra a [YouTube Data API v3](https://console.cloud.google.com/apis/library/youtube.googleapis.com) e clique em **Enable**. Está ativa quando o botão muda para **Manage**. Sem este passo, a chave não funciona.

## 4. Crie a chave

Abra [Credentials](https://console.cloud.google.com/apis/credentials) → **Create credentials** → **API key**. Na lista de restrições de API, assinale só **YouTube Data API v3** e clique em **Create**. A janela **API key created** mostra a sua chave — copie-a.

Se a YouTube Data API v3 não estiver na lista, volte ao passo 3. Deixe as restrições de aplicação em **None**.

## 5. Cole-a na app

No Flag Battle: ecrã principal → **Definições** → modo **Duelo** → **Modo streamer** → **Lig.**. Toque no botão de colar junto a **A sua chave da API v3 do YouTube** — não no campo do texto de dica por baixo. A chave fica só no seu telemóvel, no armazenamento seguro, e nunca é mostrada no ecrã.

## Se a chave for recusada

O bloco **SEGUINTES** mostra o motivo:

- **«A YouTube Data API v3 está desativada para esta chave»** — faça o passo 3 no mesmo projeto da chave e aguarde alguns minutos.
- **«as restrições da chave bloqueiam o YouTube»** — abra a chave em [Credentials](https://console.cloud.google.com/apis/credentials): as restrições de API têm de incluir **YouTube Data API v3** e as de aplicação ficar em **None**.
- **«chave do YouTube inválida»** — a chave foi copiada incompleta: começa por `AIza` e tem 39 caracteres.

Depois volte ao menu e inicie o direto de novo.

## É bom saber

- **É gratuito.** A quota padrão é de 10 000 unidades por dia. No modo «Instantânea» o chat chega em tempo real e a quota chega para cerca de 6 horas de direto por dia; «Poupança» estica-a para cerca de 12 horas, com até 10 segundos de atraso. O modo escolhe-se na app.
- **A quota é reposta à meia-noite, hora do Pacífico.** Se se esgotar, a app mostra-o no bloco **SEGUINTES** e os combates continuam com bandeiras aleatórias.
- Use o projeto apenas para a Flag Battle, para que nada mais gaste a quota.
- Para revogar a chave, elimine-a em [Credentials](https://console.cloud.google.com/apis/credentials).
