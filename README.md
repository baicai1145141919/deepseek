# DeepSeek 中转站

一个零依赖、单文件的 DeepSeek 聊天中转界面。浏览器直连 DeepSeek 官方接口，自带密钥、密码门禁、流式输出。

## 功能

- **密码门禁**：进入页面需输入访问密码（默认 `fwgzgaojiarui`），未解锁看不到聊天界面。
- **浏览器直连**：经 DeepSeek 官方 `https://api.deepseek.com` 中转，已验证该接口支持浏览器跨域（CORS），无需自建后端。
- **流式输出**：逐字显示，支持停止生成。
- **两种模型**：`deepseek-chat` 与 `deepseek-reasoner`（带「思考过程」折叠展示）。
- **轻量 Markdown**：代码块 / 行内代码渲染、自动换行。
- **本地持久化**：API Key、接口地址、模型、温度、系统提示词均保存在本机 `localStorage`，不离开浏览器。
- **可换中转地址**：接口地址可改成任意 OpenAI 兼容的中转节点。

## 使用

1. 部署后打开页面，输入访问密码进入。
2. 点右上角「设置」，填写你的 DeepSeek API Key（`sk-...`）。
3. 在底部输入消息，Enter 发送 / Shift+Enter 换行。

> 密钥由 DeepSeek 官方发放：https://platform.deepseek.com/

## 部署（GitHub Pages）

仓库已含 `index.html`，在仓库 **Settings → Pages** 中选择分支 `main`、目录 `/ (root)` 即可。约 1–2 分钟后访问：

`https://baicai1145141919.github.io/deepseek/`

## 说明

- 访问密码写在 `index.html` 的 `ACCESS_PASSWORD` 常量中，属于**前端基本门禁**，仅阻挡随意访问，并非强认证（任何能看源码的人都能读到）。如需更强保护，应改用服务端校验。
- 本站不存储、不上传你的 API Key；所有请求由你的浏览器直接发往所填接口地址。
