# Flag Battle：取得你的 YouTube API 金鑰

實況主模式透過 YouTube Data API 讀取你直播的聊天室。沒有金鑰時每天只能試用 5 分鐘；有了你自己的免費金鑰，就能連續直播好幾個小時。整個過程大約 5 分鐘。

## 1. 開啟 Google Cloud

前往 [console.cloud.google.com](https://console.cloud.google.com/)，用任何 Google 帳戶登入（不必是頻道使用的帳戶）。如有提示，請接受條款。不需要信用卡。

## 2. 建立專案

點選頁面頂端的專案選擇器（**Select a project**），再點選 **New project**。名稱不拘，例如 `flag-battle`。點選 **Create**，並確認頂端已選取新專案。

## 3. 啟用 YouTube Data API

開啟 [YouTube Data API v3](https://console.cloud.google.com/apis/library/youtube.googleapis.com)，點選 **Enable**。

## 4. 建立金鑰

開啟 [Credentials](https://console.cloud.google.com/apis/credentials)，點選 **Create credentials** → **API key**。開啟新金鑰進行編輯：

- **API restrictions** → **Restrict key** → 只勾選 **YouTube Data API v3**。這樣即使金鑰外洩，也無法用於其他用途。
- **Application restrictions** 可以保持 **None**。

點選 **Save**，然後複製金鑰（**Show key** → 複製）。

## 5. 貼到應用程式中

在 Flag Battle 中開啟 **設定 → 決鬥 → 實況主模式**，輕觸 YouTube API 金鑰欄位旁的貼上按鈕。金鑰只儲存在你手機的安全儲存空間中，絕不會顯示在畫面上。

## 小提醒

- **完全免費。** 標準配額為每天 10,000 個單位。每 8 秒讀取一次聊天室，約可直播 4.4 小時/天（每 5 秒 ≈ 2.8 小時，每 10 秒 ≈ 5.6 小時）；間隔可在應用程式中選擇。
- **配額會在太平洋時間午夜重設。** 用完時，應用程式會在 **下一場** 區塊中提示，對戰會以隨機旗幟繼續。
- 請只將此專案用於 Flag Battle，以免其他用途消耗配額。
- 如需撤銷金鑰，請在 [Credentials](https://console.cloud.google.com/apis/credentials) 中將其刪除。
