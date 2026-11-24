# My Study Life V5.1 — Zero Cost Edition

基于 V5.0 增量更新。就医与保险独立；原保单 IndexedDB 和原个人数据键保留。同一网址、浏览器、未清理数据时无需重新上传。保单仍不跨设备同步，也没有应用级加密。

## 前端部署
上传 index.html、manifest.json、sw.js、icon.svg、insurance-ai.js 到原 GitHub Pages 仓库根目录，覆盖旧文件。README 可选。不要更改原网址。刷新页面，若仍显示旧版，请关闭旧标签页后重开。保单预览和本地条款搜索不需要 AI。PDF.js 从固定版本 CDN 加载，仅在本地处理文件；扫描 PDF 和图片暂需手动录入。搜索片段可能不完整，需核对。不要在公共设备保存保单。

## Cloudflare 免费后端（首次必须配置）
1. 注册 Cloudflare，保持 Workers Free，绝不升级 Workers Paid。免费层是硬性费用保护；本代码不能替代账户套餐检查。选用账户免费可用的模型，不启用收费产品。
2. 安装 Node.js，在终端进入 worker 目录，运行 npm install，再运行 npx wrangler login。
3. 编辑 wrangler.toml 的 ALLOWED_ORIGIN 为实际 GitHub Pages 源，例如 https://abc.github.io（无路径、无末尾斜线）。保持 AI 和 Durable Object 绑定。运行 npx wrangler deploy。
4. 运行 npx wrangler secret put ACCESS_KEY，输入自行生成的长随机口令，不要提交到 GitHub。记录部署输出的 HTTPS workers.dev 地址。
5. 打开保险页面的 AI 服务设置，填写 Worker 地址和口令，点击连接。口令仅存于标签页会话，地址本地保存。此版为个人/受控测试，共享口令并非学生账户认证，不适合直接公开给大量学生；公开上线需独立身份认证和个人限额。
6. 提取 PDF，搜索条款，检查实际发送文字和问题，手动去除姓名、保单号、地址、健康信息等，勾选授权后发送。仅提交选中条款和问题，不提交文件原件。模型回复不保证正确，核对原文。

## 额度与限制
Cloudflare Workers Free 每天 10000 Neurons，UTC 00:00 重置。全站另有每日 100 次请求硬上限（失败也计入），Durable Object 串行事务保留配额；达到上限或收到 Cloudflare 3036 时暂停，前端显示本地恢复时间及倒计时，重置后自动检查。其他错误不冒充额度耗尽。100 次是自设保护，不是 Neurons 的换算；实际模型免费额度可能先耗尽。其他服务或账户共享额度也可能导致更早暂停。保持 Free 计划才可避免超额收费。尚未实现个人账户限额、自动脱敏、OCR、持久化 AI 答案缓存或完整保单自动摘要；当前支持选段解读和问答。

## 检查
worker 目录运行 npm test，模拟鉴权、请求校验、AI 返回、3036、暂停及 UTC 跨日恢复。真实 Cloudflare 账户和浏览器端交互仍需部署后验收。

官方资料：https://developers.cloudflare.com/workers-ai/platform/pricing/ 及 https://developers.cloudflare.com/workers-ai/platform/errors/
