<!-- common contents -->

<div align="center">
    <img width="160" src="/logo.svg" alt="logo"><br/>
    projectGDT - for a more connected Minecraft world!<br/>
    QQ Group:
    <a href="https://qm.qq.com/cgi-bin/qm/qr?k=jNFTovEpc0WDFtbSbUMrbQ0NyUgDpnCu&jump_from=webapi&authKey=6oBQQeoeB6gA7+AljJK7AV1IUEjkk/HpkvxrBNgAQtpxPtw230h4GQrp56nTw81I">
        162779544
    </a>
</div>

---

# projectGDT

一个致力于方便 Minecraft 服主管理玩家、方便玩家了解和加入 Minecraft 服务器的项目。

## 计划与进度

### 多平台身份绑定

- [x] 多重审核模式：无需审核 / 填写问卷
- [x] projectGDT 账户与 QQ 号绑定
- [x] projectGDT 账户与 Minecraft 账号 (Java 正版、LittleSkin 外置登录、基岩版) 绑定

### 信息发布与交流

- [x] 服主在线申请接入，填写相关资料、Logo 和封面链接、和 Markdown 格式的介绍文本
- [x] 浏览已经接入 projectGDT 的所有服务器
- [x] 浏览已加入的服务器的玩家
- [ ] 查看与每一位玩家的共同服务器

### 网页端管理

- [x] 插件上报玩家在线状态
- [x] 踢出、封禁玩家

### 群服互通

- [ ] 强互通，群成员列表 = 服务器玩家列表
- [ ] 白名单
- [ ] 玩家加群自动审批

## 模块与所用技术

### 网站前端 ([gdt-frontend](https://github.com/projectGDT/gdt-frontend))

projectGDT 的用户界面。

**语言**：ECMAScript & HTML (TSX), CSS

**框架**：[Node.js](https://nodejs.org/), [React](https://react.dev/), [Next.js](https://nextjs.org/), [Material UI](https://mui.com/)

另外，也用到了开源字体 Inter、Noto Sans、JetBrains Mono。

### 后端 ([gdt-backend](https://github.com/projectGDT/gdt-backend))

projectGDT 的后台，承担了维护玩家与服务器数据、认证、响应 HTTP 请求、与 QQ Bot 通讯，以及分发文件的任务。

**语言**：ECMAScript (TypeScript)

**框架**：[Node.js](https://nodejs.org/), [Express.js](https://expressjs.com/), [Prisma](https://prisma.io/)

### Spigot 插件 ([gdt-connector](https://github.com/projectGDT/connector))

安装在 Spigot 服务端，承担 Minecraft 服务端与网站后端之间的通讯。

**语言**：Java

**框架**：[Spigot](https://spigotmc.org/)

### Bot (gdt-bot)

QQ 机器人，用于监听群成员列表，保持与后端的同步。

**语言**：C#

**框架**：[Lagrange.Core](https://github.com/LagrangeDev/Lagrange.Core)

以上是软设比赛终审之前将要完成的部分。

---

## We won't stop here!

此项目将会继续开发，预计将在暑假完成后续工作并部署。

以下是比赛结束后将继续实现的内容：

- [ ] Java 版离线账户免认证自动进服
- [ ] Mod 服自动下载和更新整合包
- [ ] 部分兼容 PCL2
- [ ] 基于 Rust 和 [Tauri](https://tauri.app/) 的 Minecraft 启动器
- [ ] 查看玩家在线时长、背包、统计数据等