# My Study Life V4.9

## 本次更新
- 首页日历自动标记 NSW 悉尼 2026 与 2027 年全州公共假日（包括补休日），日期依据 NSW Government。
- Bank Holiday 不是全州公共假日，已明确排除；地方性区域假日不包含在悉尼日历。
- 公共假日不写入个人事件存储，也不需要自己添加；点击日期可查看假日名称。
- 购物节中日期已确定者有「加到我的日历」/「点击移除」按钮；不会重复添加，且可从首页事件管理删除。
- 黑五、Cyber Monday 等是按日历规则确定的日期，不能保证该日每个商家都有促销。
- 2027 日期尚未确认的 Afterpay Day、Prime Day、Click Frenzy 等不提供错误的固定日期按钮。
- 兼容原 localStorage 数据键 my-study-life-v3 与所有 V4.8 数据。

## 部署
解压后将 index.html、manifest.json、sw.js、icon.svg、README.md 五个文件上传到 GitHub 仓库根目录并覆盖，Commit changes。

官方假日来源：https://www.nsw.gov.au/about-nsw/public-holidays
