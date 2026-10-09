# 隐私站点部署说明

本目录是易识 / WrenRec 的隐私政策 + 开源许可 + 支持页静态站点，部署到 GitHub Pages 后供 App 内「开源许可」入口及 App Store Connect 后台引用。

## 部署步骤

1. 在 GitHub 账号 `Kn0688` 下新建公开仓库，建议命名 **`wrenrec-privacy`**（若用别的名字，需同步改 App 内链接，见下）。
2. 把本目录三个 html 文件推到仓库根目录（`index.html` / `licenses.html` / `support.html`）。
3. 仓库 Settings → Pages → Source 选 `main` 分支根目录，保存。
4. 约 1 分钟后站点生效，地址为：
   - 隐私政策：`https://kn0688.github.io/wrenrec-privacy/`（App Store Connect「隐私政策 URL」填这个）
   - 开源许可：`https://kn0688.github.io/wrenrec-privacy/licenses.html`（App 内 AboutView 已指向此地址）
   - 支持页：`https://kn0688.github.io/wrenrec-privacy/support.html`（App Store Connect「支持 URL」填这个）
5. 部署后用浏览器（最好手机 Safari + 关代理）逐个打开三个页面确认可访问。

## 关联代码位置

- App 内许可页入口：`SenseTranscription/Views/AboutView.swift` 的 `licensesURL`（已指向上述 licenses.html，仓库改名要同步改这里）
- 联系邮箱单一事实来源：`SenseTranscription/Utils/AppContact.swift`（站点 support.html 中邮箱与之保持一致）
- 许可清单底稿：仓库根目录 `开源许可清单.md`（升级依赖后复核并更新 licenses.html）

## 注意

- GitHub Pages 国内访问稳定性一般，上架后如收到用户打不开反馈，再考虑迁移到有备案的国内托管。
- 站点内容（生效日期、许可列表）随版本更新，改完 push 即生效。
