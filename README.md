# 墨语 · 手写 AI 笔记

在平板上手写，AI（DeepSeek）用蓝色手写体在你的字下方回应。整个应用只有一个 `index.html` 文件，不需要服务器。

## 部署到 GitHub Pages

1. 登录 GitHub，点右上角 **+ → New repository**，仓库名例如 `inkai`，选 **Public**，然后点 Create。
2. 在仓库页面点 **Add file → Upload files**，把 `index.html` 和 `manifest.json` 拖进去，点 **Commit changes**。
3. 进入 **Settings → Pages**：Source 选 **Deploy from a branch**，Branch 选 `main` 和 `/ (root)`，点 Save。
4. 等 1–2 分钟，访问 `https://你的用户名.github.io/inkai/`。

## 在华为 M6 上使用

1. 用 **Chrome** 打开上面的网址，不要用华为自带浏览器。
2. Chrome 菜单 → **添加到主屏幕**，之后就像 App 一样从桌面打开。
3. 第一次打开会弹出设置：
   - **API Key**：在 https://platform.deepseek.com 申请（以 `sk-` 开头）。
   - 接口地址 `https://api.deepseek.com`，模型 `deepseek-flash`，这两项保持默认即可。
   - 点 **测试连接**，看到“连接成功”就可以了。
4. 用笔写字，停笔 2.5 秒后会自动发给 AI，也可以点 **问 AI** 立即发送。

## 操作说明

| 操作 | 说明 |
|---|---|
| 书写 | 手写笔或手指 |
| 上下滚动 | 双指拖动；如果开了“只用手写笔书写”，单指就能拖动 |
| 橡皮 | 点“橡皮”后擦掉碰到的笔画；碰到 AI 写的回复，整段删除 |
| 撤销 / 清页 | 清页会同时清掉 AI 对这一页的对话记忆 |
| 多本笔记 | 左上角下拉框切换；标题会自动取你写的第一句话 |
| 自定义 AI | 在设置里写额外要求，例如“你是我的英语老师，用英文回复并纠正我的语法” |

## 说明

- 笔记保存在平板浏览器本地（localStorage）。**清除 Chrome 数据会丢失笔记。**
- API Key 只保存在本机，只会发给你填写的接口地址。仓库是公开的，但里面不包含 Key。
- 费用：每次大约用几百个 token，`deepseek-flash` 每次不到一分钱。
- 如果屏幕底部出现红色错误信息，把它截图发出来就能定位问题。
