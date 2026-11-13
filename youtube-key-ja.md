# Flag Battle：YouTube API キーの取得方法

ストリーマーモードは YouTube Data API を通じてライブ配信のチャットを読み取ります。キーがない場合は1日5分のお試しのみですが、ご自身の無料キーがあれば何時間でも配信できます。所要時間は約5分です。

## 1. Google Cloud を開く

[console.cloud.google.com](https://console.cloud.google.com/) を開き、任意の Google アカウントでログインします（チャンネルのアカウントでなくてもかまいません）。求められたら利用規約に同意してください。クレジットカードは不要です。

## 2. プロジェクトを作成

ページ上部のプロジェクト選択（**Select a project**）をクリックし、**New project** を選びます。名前は何でも構いません（例：`flag-battle`）。**Create** をクリックし、上部で新しいプロジェクトが選択されていることを確認します。以降の作業はすべてこのプロジェクトで行います。

## 3. YouTube Data API v3 を有効化 — キーを作る前に

[YouTube Data API v3](https://console.cloud.google.com/apis/library/youtube.googleapis.com) を開き、**Enable** をクリックします。ボタンが **Manage** に変われば有効です。この手順がないとキーは動作しません。

## 4. キーを作成

[Credentials](https://console.cloud.google.com/apis/credentials) → **Create credentials** → **API key**。API の制限リストで **YouTube Data API v3** だけにチェックを入れ、**Create** をクリックします。**API key created** の画面にキーが表示されるのでコピーします。

リストに YouTube Data API v3 がない場合は、手順 3 に戻ってください。アプリケーションの制限は **None** のままにします。

## 5. アプリに貼り付け

Flag Battle で：メイン画面 → **設定** → モード **デュエル** → **ストリーマーモード** → **オン**。**YouTube API v3 キー** の横の貼り付けボタンをタップします（その下のヒント文の欄ではありません）。キーはスマホの安全な保存領域にだけ保存され、画面に表示されることはありません。

## キーが拒否された場合

理由は **次** ブロックに表示されます：

- **「このキーで YouTube Data API v3 が無効です」** — キーと同じプロジェクトで手順 3 を行い、数分待ってください。
- **「キーの制限で YouTube がブロックされています」** — [Credentials](https://console.cloud.google.com/apis/credentials) でキーを開き、API の制限に **YouTube Data API v3** があること、アプリケーションの制限が **None** であることを確認します。
- **「YouTube キーが無効です」** — キーのコピーが途中で切れています。キーは `AIza` で始まる 39 文字です。

修正したらメニューに戻り、配信をもう一度開始してください。

## 知っておくと便利なこと

- **無料です。** 標準の割り当ては1日10,000ユニットです。「即時」モードではチャットがリアルタイムで届き、1日約6時間の配信に足ります。「節約」では最大10秒の遅れと引き換えに約12時間まで延びます。モードはアプリで選べます。
- **割り当ては太平洋時間の午前0時にリセットされます。** 使い切ると、アプリの **次** ブロックに表示され、対戦はランダムな国旗で続きます。
- 割り当てを他の用途で消費しないよう、このプロジェクトは Flag Battle 専用にしてください。
- キーを無効にするには、[Credentials](https://console.cloud.google.com/apis/credentials) で削除します。
