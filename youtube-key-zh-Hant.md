# Flag Battle：取得你的 YouTube API 金鑰

實況主模式透過 YouTube Data API 讀取你直播的聊天室。沒有金鑰時每天只能試用 5 分鐘；有了你自己的免費金鑰，就能連續直播好幾個小時。整個過程大約 5 分鐘。

## 1. 開啟 Google Cloud

前往 [console.cloud.google.com](https://console.cloud.google.com/)，用任何 Google 帳戶登入（不必是頻道使用的帳戶）。如有提示，請接受條款。不需要信用卡。

## 2. 建立專案

在頁面頂端點擊專案選擇器（**Select a project**），再點 **New project**。名稱隨意，例如 `flag-battle`。點擊 **Create**，並確認頂端已選取新專案——後續操作都在這個專案中完成。

## 3. 啟用 YouTube Data API v3——在建立金鑰之前

開啟 [YouTube Data API v3](https://console.cloud.google.com/apis/library/youtube.googleapis.com)，點擊 **Enable**。按鈕變成 **Manage** 即表示已啟用。略過這一步，金鑰將無法使用。

## 4. 建立金鑰

開啟 [Credentials](https://console.cloud.google.com/apis/credentials) → **Create credentials** → **API key**。在 API 限制清單中只勾選 **YouTube Data API v3**，然後點擊 **Create**。**API key created** 視窗會顯示你的金鑰——複製它。

如果清單中沒有 YouTube Data API v3，請回到第 3 步。應用程式限制保持 **None**。

## 5. 貼到應用程式

在 Flag Battle 中：主畫面 → **設定** → 模式 **決鬥** → **實況主模式** → **開**。點擊 **你的 YouTube API v3 金鑰** 旁的貼上按鈕——不是下方的提示文字欄位。金鑰只儲存在你手機的安全儲存空間，絕不會顯示在畫面上。

## 如果金鑰被拒絕

原因會顯示在 **下一場** 區塊：

- **「此金鑰未啟用 YouTube Data API v3」**——在金鑰所屬的同一專案完成第 3 步，然後等幾分鐘。
- **「金鑰限制封鎖了 YouTube」**——在 [Credentials](https://console.cloud.google.com/apis/credentials) 開啟金鑰：API 限制中必須有 **YouTube Data API v3**，應用程式限制應為 **None**。
- **「YouTube 金鑰無效」**——金鑰沒有複製完整：它以 `AIza` 開頭，共 39 個字元。

修正後回到選單，重新開始直播。

## 小提醒

- **完全免費。** 標準配額為每天 10,000 個單位。在「即時」模式下聊天室訊息即時送達，配額約夠直播 6 小時/天；「節省」模式可延長到約 12 小時，延遲最多 10 秒。模式可在應用程式中選擇。
- **配額會在太平洋時間午夜重設。** 用完時，應用程式會在 **下一場** 區塊中提示，對戰會以隨機旗幟繼續。
- 請只將此專案用於 Flag Battle，以免其他用途消耗配額。
- 如需撤銷金鑰，請在 [Credentials](https://console.cloud.google.com/apis/credentials) 中將其刪除。
