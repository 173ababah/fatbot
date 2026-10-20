# 肥鱼 · fatbot

一只住在 QQ 里的鲸鱼娘的介绍页。

> 这是一个纯静态站点，没有任何账号、密钥、服务器地址或聊天数据。

## 站点内容

| 区块 | 讲什么 |
|---|---|
| Hero | 她是谁，一句话印象 |
| 她是谁 | 性格、说话方式 |
| 会什么 | 搜图、记忆、表情包、贴表情（20 类情绪）、读链接、按群分寸 |
| 小脾气 | 让她闭嘴 / 口头禅复读 / 好感度机制 |
| 声音 | 语音链路、三种情绪音色 |
| 怎么做的 | 技术栈与消息处理流程 |

## 本地预览

直接用浏览器打开 `index.html` 即可，无需构建、无依赖、无外部请求。

## 部署

### Cloudflare Pages（推荐）

**方式一：连 Git 仓库（最简单）**

1. 打开 Cloudflare Dashboard → **Workers & Pages** → **Create** → **Pages** → **Connect to Git**
2. 选择本仓库，分支 `main`
3. 构建命令留空，输出目录填 `/`（纯静态）
4. 保存并部署

**方式二：命令行（wrangler）**

```bash
npm i -g wrangler
wrangler pages deploy . --project-name=th34bot
```

**方式三：GitHub Actions**

仓库里已经带好 `.github/workflows/deploy-cloudflare.yml`，
在仓库 **Settings → Secrets and variables → Actions** 里加两个 secret：

| Secret | 内容 |
|---|---|
| `CLOUDFLARE_API_TOKEN` | Cloudflare API Token（权限：Cloudflare Pages:Edit） |
| `CLOUDFLARE_ACCOUNT_ID` | 账号 ID（Dashboard 右下角 / URL 里能看到） |

之后每次 push 到 `main` 会自动部署。

## 隐私说明

- 没有 QQ 号、群号、账号、密码、密钥、IP
- 没有真实聊天截图（页面里的对话是排版用的示例）
- 不加载任何第三方脚本、字体或统计

## License

MIT
