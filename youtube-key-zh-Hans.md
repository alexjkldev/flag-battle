# Flag Battle：获取你的 YouTube API 密钥

主播模式通过 YouTube Data API 读取你直播的聊天。没有密钥时每天只能试用 5 分钟；有了你自己的免费密钥，就可以连续直播好几个小时。整个过程大约 5 分钟。

## 1. 打开 Google Cloud

访问 [console.cloud.google.com](https://console.cloud.google.com/)，用任意 Google 账号登录（不必是频道所用的账号）。如有提示，请接受条款。无需信用卡。

## 2. 创建项目

点击页面顶部的项目选择器（**Select a project**），然后点击 **New project**。名称随意，例如 `flag-battle`。点击 **Create**，并确认顶部已选中新项目。

## 3. 启用 YouTube Data API

打开 [YouTube Data API v3](https://console.cloud.google.com/apis/library/youtube.googleapis.com)，点击 **Enable**。

## 4. 创建密钥

打开 [Credentials](https://console.cloud.google.com/apis/credentials)，点击 **Create credentials** → **API key**。打开新密钥进行编辑：

- **API restrictions** → **Restrict key** → 只勾选 **YouTube Data API v3**。这样即使密钥泄露，也无法用于其他用途。
- **Application restrictions** 可以保持 **None**。

点击 **Save**，然后复制密钥（**Show key** → 复制）。

## 5. 粘贴到应用中

在 Flag Battle 中打开 **设置 → 决斗 → 主播模式**，点按 YouTube API 密钥栏旁边的粘贴按钮。密钥只保存在你手机的安全存储中，绝不会显示在屏幕上。

## 须知

- **完全免费。** 标准配额为每天 10,000 个单位。每 8 秒读取一次聊天，约可直播 4.4 小时/天（每 5 秒 ≈ 2.8 小时，每 10 秒 ≈ 5.6 小时）；间隔可在应用中选择。
- **配额在太平洋时间午夜重置。** 用完后，应用会在 **下一场** 区块中提示，对战将继续使用随机旗帜。
- 请只将该项目用于 Flag Battle，以免其他用途消耗配额。
- 如需撤销密钥，请在 [Credentials](https://console.cloud.google.com/apis/credentials) 中将其删除。
