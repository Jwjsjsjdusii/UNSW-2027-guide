# My Study Life · Personal Edition V3.0

一个面向个人使用的静态留学生活管理网站，初始资料按 UNSW 2027 项目交接信息设置。

## 文件
- `index.html`：完整网站
- `manifest.json`：PWA 配置
- `sw.js`：基础离线缓存
- `icon.svg`：应用图标

## 发布到 GitHub Pages
1. 解压 ZIP。
2. 将四个网站文件上传到现有仓库根目录。
3. 覆盖同名文件并 Commit changes。
4. Settings → Pages → Deploy from a branch → `main` → `/(root)` → Save。
5. 等待部署完成后打开原 GitHub Pages 网址。

## 数据与隐私
- 无注册、无登录、无服务器、无数据库。
- 个人资料、航班、事件、预算和待办保存在当前浏览器的 LocalStorage。
- 不同浏览器/设备不会自动同步。
- 请定期在「个人工具」导出 JSON 备份。
- 当前版本没有 Offer 文件上传或 AI 解析，也没有实时航班 API。

## 重要说明
页面中的个人日期来自用户提供的项目计划。UNSW 2027 校历、迎新、主课日期及签证政策需以官方最新信息核实。网站不构成移民、法律、税务或租赁建议。
