# 部署到 yeeiiii 账号 · 操作清单

> 前提：浏览器已登录 GitHub 账号 `yeeiiii`。仓库建议命名为 `tire-weight-demo`，公开（Public）。

## 方式 A：网页上传（最简单，不需要令牌）

1. 打开 https://github.com/new
2. Repository name 填 `tire-weight-demo`
3. 选择 **Public**
4. 不要勾选 “Add a README file”“Add .gitignore”“Choose a license”
5. 点击 **Create repository**
6. 在新仓库页面点击 **uploading an existing file**
7. 把本文件夹里的 `index.html` 和 `.nojekyll` 拖进去
8. Commit changes
9. 进入 **Settings → Pages**
   - Source 选 **Deploy from a branch**
   - Branch 选 **main**，目录选 **/ (root)**
   - 点击 **Save**
10. 等待约 1 分钟，访问：
    `https://yeeiiii.github.io/tire-weight-demo/`

## 方式 B：本地 git 推送（需要已配置 GitHub 凭据）

在本文件夹打开 Git Bash：

```bash
git init
git config user.name "yeeiiii"
# 建议使用 GitHub 提供的 noreply 邮箱，或你账号绑定的邮箱
git config user.email "你的邮箱"
git add index.html README.md .nojekyll
git commit -m "Add interactive uniformity dashboard demo"
git branch -M main
git remote add origin https://github.com/yeeiiii/tire-weight-demo.git
git push -u origin main
```

推送时如果弹出 Git Credential Manager 登录窗口，按提示登录 `yeeiiii` 即可。推送完成后仍需在 **Settings → Pages** 中选择 `main` / `(root)` 并 Save。

## 验证

- 打开 `https://yeeiiii.github.io/tire-weight-demo/`
- 页面应显示“服务正常”、趋势图、核心规格行动表、物料批次分析
- 点击顶部“新手引导”应出现 5 步引导

## 注意

- 免费账号的 Pages 仅对 **Public** 仓库开放；Private 仓库需要 GitHub Pro/Team。
- 页面所有数据均为合成数据，不包含真实规格、机台、IP 或品牌信息。
- 更新页面时，替换仓库根目录的 `index.html` 并提交即可，约 1 分钟生效。
