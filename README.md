# 听书 — 隐私政策与支持页

「听书 - 本地小说朗读」App 的官网静态页，托管在 GitHub Pages。

## 页面

| 文件 | 内容 | 用途 |
|---|---|---|
| `index.html` | 隐私政策 | App Store Connect 的「隐私政策网址」填这个 |
| `support.html` | 支持与帮助 | App Store Connect 的「支持网址」填这个 |
| `404.html` | 404 页 | 路径写错时给出入口，不留死链 |

## 部署

通过 `.github/workflows/deploy.yml` 自动发布：

1. 推送到 `main` 分支 → Actions 自动构建并发布到 GitHub Pages
2. 仓库 **Settings → Pages → Build and deployment → Source** 选 **GitHub Actions**

## 修改方式

直接改对应 HTML 文件，push 即生效。

- 隐私政策正文在 `index.html` 的 `<h2>` 段落里
- 生效日期在 `index.html` 的 `<p class="meta">`
- 联系方式在 `index.html` 与 `support.html` 底部（同一邮箱，改一处记得改另一处）
- 两页样式在各自 `<style>` 块里，改一处样式需同步另一处

## 注意

- 政策里「生效日期」和「适用版本」需要随版本更新
- App 内 About 页展示的链接指向这里，迁移后需同步更新 App Store Connect 里的网址
