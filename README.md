# DeepSeek 中转站

一个零依赖、单文件的 DeepSeek 聊天中转界面。浏览器直连 DeepSeek 官方接口，自带密钥、流式输出，进入即可用。

## 功能

- **免密码**：打开页面即可使用，无需访问密码。
- **浏览器直连**：经 DeepSeek 官方 `https://api.deepseek.com` 中转，已验证该接口支持浏览器跨域（CORS），无需自建后端。
- **流式输出**：逐字显示，支持停止生成。
- **显示思考过程**：默认使用 `deepseek-reasoner`，AI 回复前的推理过程以可折叠面板（「💡 思考过程」）实时展示，生成完成后自动收起；历史消息中也可点开回看。设置里可切换为 `deepseek-chat`（更快更省，无思考过程）。
- **轻量 Markdown**：代码块 / 行内代码渲染、自动换行。
- **本地持久化**：对话历史、API Key、接口地址、模型、温度均保存在本机 `localStorage`，不离开浏览器；刷新或重开后历史仍在，左侧可切换多个会话。
- **可换中转地址**：接口地址可改成任意 OpenAI 兼容的中转节点。

## 使用

1. 部署后打开页面（首次会自动弹出设置窗）。
2. 点右上角「设置」（或首次弹窗），填写你的 DeepSeek API Key（`sk-...`）。
3. 在底部输入消息，Enter 发送 / Shift+Enter 换行。

> 密钥由 DeepSeek 官方发放：https://platform.deepseek.com/

## 部署（GitHub Pages）

仓库已含 `index.html`，在仓库 **Settings → Pages** 中选择分支 `main`、目录 `/ (root)` 即可。约 1–2 分钟后访问：

`https://baicai1145141919.github.io/deepseek/`

## 说明

- 本站无访问密码门禁，打开即用；所有请求由你的浏览器直接发往所填接口地址。
- 本站不存储、不上传你的 API Key；历史对话仅保存在你本机浏览器 `localStorage`，换设备/清数据会丢失。
