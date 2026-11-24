# My Study Life · Personal Edition V4.3

## 文件说明
- `index.html`：网站主页面与交互逻辑。
- `manifest.json`：PWA 应用名称、图标和安装显示配置。
- `sw.js`：Service Worker，负责基础离线缓存和版本更新。
- `icon.svg`：网站/PWA 图标。
- `README.md`：部署说明。

## GitHub Pages 部署
将以上五个文件全部上传到 GitHub 仓库根目录，覆盖同名旧文件并提交。确认仓库 Settings → Pages 已启用 `main` 分支的 `/(root)` 部署。

## 数据说明
用户资料、航班、日历事件、待办和花销保存在当前浏览器本地。跨设备前请先在网站内导出 JSON 备份。PWA 离线缓存不等于云同步。
