# My Study Life · Personal Edition V4.7

## V4.7 更新
- 「重要文件与入境准备」改为 12 项可勾选清单，进度条和勾选状态保存在本地。
- 购物信息恢复二手、免费领取和物品交换分类：Arc UNSW Second Life Hub、UNSW reuse、Gumtree Freebies、Facebook Marketplace、Facebook Buy Swap Sell、Buy Nothing / Pay It Forward、Freecycle、Trash Nothing、Ziilch、Vinnies / Salvos、The Bower（Marrickville 与 Summer Hill 实体店及线上商店）。
- 增加澳洲年度购物节点：Black Friday、Cyber Monday、Boxing Day、EOFY、Afterpay Day、Click Frenzy、Prime Day、Singles' Day、Back to School 等；明确区分已公布日期与待公布日期。
- 抵澳航班设置移至首页倒计时下方的折叠卡片。
- 个人事件添加与事件管理移至首页日历下方的折叠卡片。
- 删除独立「个人工具」侧边栏和页面。
- 数据导出 / 导入移动到个人资料页面。
- 首页「本月花销」增加快捷记账表单，可直接记录今天的消费。
- 调整工作台左右栏比例和高度分布，减少右栏明显过长的问题。
- 增加三套可切换主题：暖阳米杏（原配色）、明亮日间（更白）、柔和夜间（灰绿暖灰，不使用纯黑背景）。

## 数据兼容
继续使用 `my-study-life-v3` 原有本地数据键，个人资料、航班、事件、待办、课表、预算、固定支出和消费记录继续保留。
新增的入境文件清单保存在本地，并随 JSON 备份导出 / 导入；主题选择保存在本地。
数据不会自动云同步。更换设备或浏览器前，请在「个人资料」页面导出 JSON 备份。

## 购物节日日期说明
2026 Black Friday：11 月 27 日；Cyber Monday：11 月 30 日。
2027 Black Friday：11 月 26 日；Cyber Monday：11 月 29 日。
Boxing Day：每年 12 月 26 日；EOFY 为 6 月 30 日财年结束前后。
Click Frenzy、Afterpay Day、Prime Day 等促销活动的 2027 具体日期应以主办方后续公告为准，网站没有将未公布日期写成已确认。

## 部署
1. 解压 ZIP。
2. 将 `index.html`、`manifest.json`、`sw.js`、`icon.svg`、`README.md` 五个文件上传到现有 GitHub 仓库根目录并覆盖。
3. Commit changes，等待 GitHub Pages 部署。
4. 重新打开网站；若仍显示旧版，清理旧 PWA 缓存后重新添加到主屏幕。
