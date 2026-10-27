# 均匀性 AI 智能分析系统 · 交互演示

这是一个**纯前端、单文件**的可交互看板演示，基于公开仓库 `feature/kanban-onboarding-tour` 分支的 Vue 3 前端构建。

## 直接打开

双击 `index.html`，或拖入 Chrome / Edge 即可。无需安装、无需启动服务、无需联网。

## 说明

- 所有规格、机台、批次、条码、参数和测量值均为**浏览器内程序生成的合成数据**，与真实生产记录无关。
- 所有 `/api` 请求由页面内置的 Mock 适配器拦截，不会访问任何后端。
- 包含：CPK 趋势 / Yield 不良趋势、核心规格行动表、工序流转桑基图、全量最佳路径、参数推荐、机台组合分析、物料批次追溯、单胎 Barcode 明细、5 步新手引导。
- 顶部「新手引导」按钮可重新播放 5 步交互式引导。

## 部署到 GitHub Pages

1. 在 GitHub 新建 public 仓库，例如 `tire-weight-demo`（不要勾选 README / .gitignore / license）。
2. 把本目录的 `index.html` 和 `.nojekyll` 上传到仓库根目录并提交。
3. 仓库 **Settings → Pages**：
   - Source: `Deploy from a branch`
   - Branch: `main`，目录 `/ (root)`
   - Save
4. 约 1 分钟后访问：`https://yeeiiii.github.io/tire-weight-demo/`

`.nojekyll` 用于跳过 Jekyll 处理，可留空；不上传也能正常打开本页面。

## 在 PPT 中使用

- 推荐：PPT 里放一个按钮/文字，超链接到上面的 GitHub Pages 地址。
- 也可以：把 `index.html` 和 PPT 放在同一文件夹，超链接使用相对路径 `index.html`，整个文件夹一起分发。
- PowerPoint 不能把 HTML 直接嵌入幻灯片内运行；需要静态展示时请用截图或录屏。
