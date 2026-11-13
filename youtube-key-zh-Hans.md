# Flag Battle：获取你的 YouTube API 密钥

主播模式通过 YouTube Data API 读取你直播的聊天。没有密钥时每天只能试用 5 分钟；有了你自己的免费密钥，就可以连续直播好几个小时。整个过程大约 5 分钟。

## 1. 打开 Google Cloud

访问 [console.cloud.google.com](https://console.cloud.google.com/)，用任意 Google 账号登录（不必是频道所用的账号）。如有提示，请接受条款。无需信用卡。

## 2. 创建项目

在页面顶部点击项目选择器（**Select a project**），然后点 **New project**。名称随意，例如 `flag-battle`。点击 **Create**，并确认顶部已选中新项目——后面的操作都在这个项目里完成。

## 3. 启用 YouTube Data API v3——在创建密钥之前

打开 [YouTube Data API v3](https://console.cloud.google.com/apis/library/youtube.googleapis.com)，点击 **Enable**。按钮变成 **Manage** 即表示已启用。跳过这一步，密钥将无法使用。

## 4. 创建密钥

打开 [Credentials](https://console.cloud.google.com/apis/credentials) → **Create credentials** → **API key**。在 API 限制列表中只勾选 **YouTube Data API v3**，然后点击 **Create**。**API key created** 窗口会显示你的密钥——复制它。

如果列表里没有 YouTube Data API v3，请回到第 3 步。应用限制保持 **None**。

## 5. 粘贴到应用

在 Flag Battle 中：主界面 → **设置** → 模式 **决斗** → **主播模式** → **开**。点击 **你的 YouTube API v3 密钥** 旁边的粘贴按钮——不是下方的提示文字输入框。密钥只保存在你手机的安全存储中，绝不会显示在屏幕上。

## 如果密钥被拒绝

原因会显示在 **下一场** 区域：

- **“此密钥未启用 YouTube Data API v3”**——在密钥所属的同一项目中完成第 3 步，然后等几分钟。
- **“密钥限制阻止了 YouTube”**——在 [Credentials](https://console.cloud.google.com/apis/credentials) 中打开密钥：API 限制中必须有 **YouTube Data API v3**，应用限制应为 **None**。
- **“YouTube 密钥无效”**——密钥没有复制完整：它以 `AIza` 开头，共 39 个字符。

修正后回到菜单，重新开始直播。

## 须知

- **完全免费。** 标准配额为每天 10,000 个单位。在「即时」模式下聊天实时到达，配额约够直播 6 小时/天；「节省」模式可延长到约 12 小时，延迟最多 10 秒。模式可在应用中选择。
- **配额在太平洋时间午夜重置。** 用完后，应用会在 **下一场** 区块中提示，对战将继续使用随机旗帜。
- 请只将该项目用于 Flag Battle，以免其他用途消耗配额。
- 如需撤销密钥，请在 [Credentials](https://console.cloud.google.com/apis/credentials) 中将其删除。
