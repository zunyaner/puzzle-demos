# 推理解谜原型演示（puzzle-demos）

面向手机与桌面的两款**原创**短篇推理解谜单页原型，无 CDN、无外部素材，可直接用浏览器打开。

> 与任何已出版小说或现有仓库中的游戏无关；案件为新编写。

## 在线试玩（GitHub Pages）

- 首页：https://zunyaner.github.io/puzzle-demos/
- [侦探卷宗 dossier.html](https://zunyaner.github.io/puzzle-demos/dossier.html)
- [电脑侦查 forensics.html](https://zunyaner.github.io/puzzle-demos/forensics.html)
- [灰荆庄园 manor.html](https://zunyaner.github.io/puzzle-demos/manor.html)（恐怖，约 15 分钟，建议戴耳机）
- [生日惊喜 birthday.html](https://zunyaner.github.io/puzzle-demos/birthday.html)（手机友好 · [编辑器](https://zunyaner.github.io/puzzle-demos/birthday.html?edit=1)）
- [海龟汤馆 haiguitang.html](https://zunyaner.github.io/puzzle-demos/haiguitang.html)（情境推理）

预计单局约 15–25 分钟。

## 原型 1 · 侦探卷宗 `dossier.html`

**案件**：云栖公寓 9-1502，软件工程师方予安遇害；保险箱现金未动，黑色 U 盘失踪。

**玩法**：

1. 从左侧证据堆把材料钉到软木板（点击或拖拽）。
2. 点选两份证据，标记「关联」或「矛盾」。正确比对会解锁新文档；错误仅短暂提示，不指路。
3. 线索足够后提交结案报告：自由填写凶手 / 时间 / 手法 / 动机（接受同义表述；仅反馈哪一栏未通过）。
4. 可用存档 / 读档（`localStorage`）。

**风格**：卷宗纸张 + 软木板。

## 原型 4 · 电脑侦查 `forensics.html`

**案件**：锦科软件工程师林晓舟的工作电脑取证；涉嫌向竞争对手泄露核心算法。

**玩法**：

1. 在仿 Windows 桌面上打开邮件、即时通、浏览器历史、日历、便签、我的文档与回收站。
2. 从回收站还原已删草稿；用散落线索拼出加密压缩包密码。
3. 查看图片元数据（EXIF 风格备注）等。
4. 提交结论：联系了谁、转移/藏匿了什么、大约何时。

**风格**：深灰系统界面，中文标签。

## 恐怖原型 · 灰荆庄园 `manor.html`

**故事**：1899 年，遗产鉴定员艾达·莫尔来到灰荆庄园清点遗物，大门在身后锁死。庄园里游荡着一个高瘦的身影——当年的保姆。

**玩法**：

1. 第一人称手电探索 8 个房间（门厅、画廊、书房、餐厅、二楼走廊、主卧、育婴室、地下室）；物品只有被手电照到才看得见，电池会耗尽。
2. 听声辨位：脚步、门轴、低语、心跳提示她的方向与距离；她进屋前躲进衣柜/床底/桌下，搜寻时按住「屏息」（气息有限）。被抓到回到最近检查点。
3. 谜题：画像顺序、撕碎照片拼合、八音盒旋律；集齐 5 页日记可解锁真结局。
4. 理智值：黑暗与目击会降低理智，低理智时画面色散、暗角、幻听。
5. 自动存档（`localStorage`）、暂停菜单、手机触控；设置中可「减弱惊吓与闪烁」（系统开启减少动态效果时默认开启）。

画面全部由 Canvas 2D / SVG 程序化绘制，声音全部由 WebAudio 合成，无任何外部资源。

## 生日惊喜 `birthday.html`

温馨向生日小站：拆信封 → 吹蜡烛（点击或可选麦克风）→ 烟花与旋律 → 回忆卡片 → 打字机信件。支持 `prefers-reduced-motion` 与静音。

**定制**：文件顶部 `CONFIG` 对象；或打开 `?edit=1` 填表、上传照片（客户端压缩为 data URL），点「生成我的生日页」下载独立 HTML 发送。

## 海龟汤馆 `haiguitang.html`

**玩法**：阅读匪夷所思的「结局」，只用是非问句逼近真相；馆主回答「是 / 不是 / 无关 / 重要」。可随时提交自由文本推理（同义可通过，只提示仍缺哪类信息）。「放弃」下折叠剧透。

**题量**：8 道原创汤，难度入门→进阶，题材含悬疑、温情、反转、黑色幽默。进度存 `localStorage`。

**双模式**：

1. **离线规则引擎（默认）**：关键词 / 意图匹配、同义、否定与「是不是」处理。
2. **可选 AI**：设置里填 OpenAI 兼容 Base URL / API Key / 模型（仅存本机）。系统提示持有秘密故事，回复约束为四词。失败自动回退离线。注意 https Pages 无法请求明文 `http://` 内网地址（混合内容）。

## 本地打开

克隆后用浏览器直接打开对应 HTML，或任意静态服务器托管本目录。仓库含 `.nojekyll` 以便 Pages 原样发布。

## 文件

| 文件 | 说明 |
|------|------|
| `dossier.html` | 侦探卷宗 |
| `forensics.html` | 电脑侦查 |
| `manor.html` | 灰荆庄园（恐怖） |
| `birthday.html` | 生日惊喜 |
| `haiguitang.html` | 海龟汤馆 |
| `.nojekyll` | 禁用 Jekyll 处理 |
| `README.md` | 本说明 |

## 作者

为用户严严 王制作的演示原型。提交身份：`zunyaner`。
