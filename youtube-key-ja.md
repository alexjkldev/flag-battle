# Flag Battle：YouTube API キーの取得方法

ストリーマーモードは YouTube Data API を通じてライブ配信のチャットを読み取ります。キーがない場合は1日5分のお試しのみですが、ご自身の無料キーがあれば何時間でも配信できます。所要時間は約5分です。

## 1. Google Cloud を開く

[console.cloud.google.com](https://console.cloud.google.com/) を開き、任意の Google アカウントでログインします（チャンネルのアカウントでなくてもかまいません）。求められたら利用規約に同意してください。クレジットカードは不要です。

## 2. プロジェクトを作成する

ページ上部のプロジェクト選択（**Select a project**）をクリックし、**New project** をクリックします。名前は何でもかまいません（例：`flag-battle`）。**Create** をクリックし、上部で新しいプロジェクトが選択されていることを確認します。

## 3. YouTube Data API を有効にする

[YouTube Data API v3](https://console.cloud.google.com/apis/library/youtube.googleapis.com) を開き、**Enable** をクリックします。

## 4. キーを作成する

[Credentials](https://console.cloud.google.com/apis/credentials) を開き、**Create credentials** → **API key** をクリックします。新しいキーを開いて編集します。

- **API restrictions** → **Restrict key** → **YouTube Data API v3** のみにチェックを入れます。これで、キーが漏れても他の用途には使えません。
- **Application restrictions** は **None** のままでかまいません。

**Save** をクリックし、キーをコピーします（**Show key** → コピー）。

## 5. アプリに貼り付ける

Flag Battle で **設定 → デュエル → ストリーマーモード** を開き、YouTube API キー欄の横にある貼り付けボタンをタップします。キーはお使いのスマートフォンの安全なストレージにのみ保存され、画面に表示されることはありません。

## 知っておくと便利なこと

- **無料です。** 標準の割り当ては1日10,000ユニットです。チャットを8秒ごとに読み取ると、1日約4.4時間の配信に足ります（5秒ごと ≈ 2.8時間、10秒ごと ≈ 5.6時間）。間隔はアプリで選べます。
- **割り当ては太平洋時間の午前0時にリセットされます。** 使い切ると、アプリの **次** ブロックに表示され、対戦はランダムな国旗で続きます。
- 割り当てを他の用途で消費しないよう、このプロジェクトは Flag Battle 専用にしてください。
- キーを無効にするには、[Credentials](https://console.cloud.google.com/apis/credentials) で削除します。
