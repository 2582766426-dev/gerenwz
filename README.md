# 柳智熙设计作品集 — GitHub 源码包

这是当前本地最新版的完整源码和图片资源，已移除原 Sites 项目绑定，并通过独立生产构建验证。

## 本地运行
安装 Node.js 22.13 或以上及 pnpm，然后在此目录执行：

    pnpm install --frozen-lockfile
    pnpm dev

## 构建和部署
本项目使用 React + Vinext + Cloudflare Workers。GitHub 用于保存源码；不能直接作为普通静态文件上传到 GitHub Pages。

构建：

    pnpm build

部署到自己的 Cloudflare 账号：

    pnpm exec wrangler login
    pnpm exec wrangler deploy --config dist/server/wrangler.json --name liuzhixi-portfolio

也可以在 Cloudflare Workers 中连接 GitHub 仓库，构建命令使用 pnpm build，部署命令使用上述 wrangler deploy 命令。首次部署需你自己的 Cloudflare 账号授权；本包不包含任何账号凭证。

## 上传 GitHub
先解压，再将本目录中的文件上传到仓库根目录，不要仅上传 ZIP 文件。建议用 GitHub Desktop 上传整份目录；其中有较大图片，浏览器逐文件上传可能受限。

源码包不含 node_modules、Git 历史、缓存、账号凭证或原 Sites 发布绑定。原网站项目未被改动。

## 内容说明
包含首页、个人介绍、精选项目及各级案例、四个品牌作品档案、其他作品漂移墙和全部资源。当前首页年份按此前输入保留为“2024-206年度”；若需改为 2024-2026，请修改 app/page.tsx。
