# 律巢相册（LyraNest Photo）

<p align="center">
  <img src="docs/images/lyranest-photo.png" alt="LyraNest Photo" width="150" />
</p>

<p align="center">把飞牛 fnOS 官方相册，搬到你自己的手机、平板、电脑和电视上。</p>

<p align="center">
  <a href="https://github.com/WHWgogogo/LyraNest-Photo/releases/latest"><img src="https://img.shields.io/github/v/release/WHWgogogo/LyraNest-Photo?display_name=tag&label=Release" alt="Latest Release" /></a>
  <a href="https://github.com/WHWgogogo/LyraNest-Photo/releases/latest"><img src="https://img.shields.io/badge/Platform-Android%20%7C%20Windows%20%7C%20Android%20TV-4f46e5" alt="Platforms" /></a>
  <a href="https://github.com/WHWgogogo/LyraNest-Photo/releases/latest"><img src="https://img.shields.io/badge/Platform-iOS%20%7C%20macOS-000000?logo=apple&logoColor=white" alt="Apple Platforms" /></a>
  <a href="#harmonyos-客户端开发中"><img src="https://img.shields.io/badge/HarmonyOS-%E5%BC%80%E5%8F%91%E4%B8%AD-orange" alt="HarmonyOS" /></a>
  <img src="https://img.shields.io/badge/License-Proprietary-red" alt="Proprietary" />
</p>

<p align="center">
  <a href="https://github.com/WHWgogogo/LyraNest-Photo/releases/latest">下载最新版</a> ·
  <a href="releases/0.1.0/CHANGELOG.md">更新日志</a> ·
  <a href="#安装与使用">安装说明</a> ·
  <a href="https://qm.qq.com/q/L6YzvpLAwU">加入 QQ 群</a> ·
  <a href="https://github.com/WHWgogogo">作者主页</a>
</p>

> ### 发行版仓库说明
>
> 本仓库用于发布律巢相册的安装包与更新记录：**安装包以 GitHub Release 附件形式提供**，仓库本身只保留文档，不包含任何源代码、构建脚本、接口文档或设计资料。
>
> 律巢相册是**闭源软件**：源代码不对外开放，也未授权任何个人或组织以任何形式复制、反编译、二次打包、二次分发或用于衍生开发。保留所有权利。

当前稳定版本：`0.1.0`

交流 QQ 群：`1098566175`

> **HarmonyOS 客户端开发中** —— 鸿蒙端正在开发，敬请期待；完成后会同步在本仓库发布安装包。

律巢相册是你自己飞牛（fnOS）NAS 相册的**第三方独立客户端**。照片和视频始终保存在你自己的 NAS 上，客户端只做浏览、备份与管理，不经由任何第三方服务器中转。

律巢相册提供 Android、Windows、Android TV 以及 **iOS / macOS（无签名，需自行侧载）** 客户端，HarmonyOS NEXT 版本正在开发中。

## 0.1.0 首发说明

这是律巢相册的首个公开版本。

### 连接飞牛相册

- **多种线路自动选择**：支持内网地址、外网地址与 FNID 连接方式，自动探测并记录当前可用线路。
- **完整登录链路**：支持账号密码登录、TOTP 二次验证与安全邮箱验证；会话仅保存在系统安全存储中，重启免重复登录。
- **会话自愈**：Cookie / 令牌失效时统一走重新认证流程，网络不可达时保留登录态并给出可见提示，不把用户直接踢回登录页。

### 浏览与查看

- **时间线**：按年 / 月 / 日聚合，连续分页加载，带月份索引侧栏，可持久显示月份标题。
- **相册与聚合入口**：用户相册、目录浏览、收藏、共享（他人共享 / 我的共享 / 分享链接）、人物、地点、标签、智能分类、媒体类型、回收站、地图相册、回忆。
- **搜索**：按飞牛相册索引搜索，索引不可用时自动重建后重试。
- **照片查看**：缩略图网格、原图与预览查看、照片详情（拍摄时间、设备、拍摄参数、位置）。
- **视频播放**：在线播放视频；Windows 端使用内嵌播放器，也可下载后用系统播放器播放。
- **批量操作**：多选后可收藏、添加到相册、删除；查看大图时可下载原图与分享。

### 备份与维护

- **手机相册备份**：把系统相册按相册维度增量备份到 NAS 指定目录，带上传台账去重、失败重试与前台服务保活。
- **缩略图批量生成**：自动扫描缺失缩略图的照片，勾选后再批量入队，并显示排队与完成进度。
- **诊断与日志**：可在应用内查看运行日志，并一键导出诊断日志用于反馈问题。

### 音乐相册（可选）

- 可在主导航中开启「音乐相册」页，配合 [LyraNest（律巢）](https://github.com/WHWgogogo/LyraNest) 音乐服务，用照片与音乐一起放映。
- 音乐凭据与飞牛凭据完全隔离，未登录音乐服务时不会触碰相册会话。

### 多端形态

- **Android 手机 / 平板**：竖屏底部导航与横屏主从结构自适应，支持拖动框选。
- **Windows 桌面**：无边框窗口与自绘窗口条，支持窗口拖动、最小化、最大化与关闭。
- **Android TV**：全遥控器可操作的 10-foot 界面、扫码登录、横屏锁定。
- **Android TV 兼容版**：独立包名，可与正式 TV 端在同一台电视上并存安装，面向 Android 5.0 电视与老盒子。
- **iOS / iPadOS**：提供**无签名**版本，需要用户自行侧载安装。
- **macOS**：提供**无签名**版本，首次打开需手动移除系统隔离标记。
- **HarmonyOS NEXT**：开发中，敬请期待。

完整记录见 [`releases/0.1.0/CHANGELOG.md`](releases/0.1.0/CHANGELOG.md)。

## 功能简介

- **直连你的 NAS**：内网 / 外网 / FNID 三种入口，登录后所有请求直达你的飞牛设备。
- **时间线与相册**：时间线聚合、用户相册、目录浏览、收藏、共享、人物、地点、标签、智能分类、媒体类型、回收站、地图相册、回忆。
- **照片与视频**：缩略图网格、原图查看、EXIF 详情、视频在线播放、批量收藏 / 添加 / 删除。
- **手机相册备份**：按相册增量备份到 NAS，失败重试与去重台账。
- **缩略图维护**：批量生成缺失缩略图并跟踪队列进度。
- **音乐相册**：与 LyraNest 音乐服务联动放映（可选）。
- **多端覆盖**：Android 手机 / 平板、Windows 桌面、Android TV、Android 5 电视兼容版，以及无签名的 iOS / macOS 版本；HarmonyOS 版本开发中。

## 界面预览

> 截图整理中，后续版本会在这里补充手机端、Windows 端、TV 端与 Apple 端的实际界面。

## 下载

请前往 [GitHub 最新发行版](https://github.com/WHWgogogo/LyraNest-Photo/releases/latest) 下载。该链接会在新版本发布后自动指向最新稳定版。

| 文件 | 适用设备 |
| --- | --- |
| `LyraNest-Photo-0.1.0-android-arm64.apk` | Android 手机 / 平板（ARM64，Android 7.0 及以上） |
| `LyraNest-Photo-0.1.0-windows-x64.zip` | Windows 10 / 11 x64 桌面端 |
| `LyraNest-Photo-TV-0.1.0-arm64-v8a.apk` | Android TV / 电视盒子（ARM64） |
| `LyraNest-Photo-TV-0.1.0-armeabi-v7a.apk` | Android TV / 电视盒子（ARM32） |
| `LyraNest-Photo-TV-Android5-0.1.0-arm64.apk` | Android 5.0 电视 / 老盒子（ARM64，兼容版） |
| `LyraNest-Photo-TV-Android5-0.1.0-arm.apk` | Android 5.0 电视 / 老盒子（ARM32，兼容版） |
| `LyraNest-Photo-0.1.0-ios-unsigned.ipa` | iPhone / iPad（**无签名**，需自行侧载） |
| `LyraNest-Photo-0.1.0-macos-unsigned.zip` | macOS（**无签名**，解压后需移除隔离标记） |

> ⚠️ `ios` 与 `macos` 附件是**无签名构建**：iOS 需要你用侧载工具自签安装，macOS 首次打开需要手动放行，详见 [安装与使用](#安装与使用)。下载前请先看清文件名中的平台与架构。

> 每个版本都保留独立的 GitHub Release 与附件，不会覆盖旧版本。安装包**只作为 Release 附件发布，不进入版本库**，所以本仓库始终只含文档，体积不会随版本增长。
> GitHub Release 附件页会显示每个附件的 SHA-256 摘要，可直接用于校验下载文件的完整性。

## 仓库结构

```text
README.md                       发行说明与下载入口
releases/<版本>/CHANGELOG.md     该版本的更新日志
docs/images/                    README 使用的图片
```

本仓库不含源代码、构建脚本与安装包。源码构建流程产出的安装包（APK / IPA / ZIP）直接上传为对应版本的 GitHub Release 附件，不进版本库。

## 安装与使用

### Android 手机 / 平板

1. 下载 `LyraNest-Photo-<版本>-android-arm64.apk`。
2. 在手机上允许「安装未知来源应用」后安装。
3. 首次启动填写飞牛 NAS 地址（内网、外网或 FNID 三选一），登录你的飞牛账号。
4. 如账号已开启二次验证，按提示完成 TOTP 或安全邮箱验证。

### Windows 桌面端

1. 下载 `LyraNest-Photo-<版本>-windows-x64.zip`。
2. 解压到任意目录（**不要单独把 exe 拖出来**，`data` 目录必须与 exe 同级）。
3. 运行 `lyranest_photo.exe`，填写 NAS 地址并登录。

### iOS / iPadOS（无签名，需自行侧载）

> 该版本**不做代码签名，也不在 App Store 上架**，需要你自己完成签名与安装。这不是安装包损坏。

1. 下载 `LyraNest-Photo-<版本>-ios-unsigned.ipa`。
2. 用 AltStore、Sideloadly 等侧载工具，配合你自己的 Apple ID 重签后安装到设备。
3. 需要知道的限制：
   - 用免费 Apple ID 签名时，应用 **7 天后会失效**，需要重新签名安装；
   - 依赖正式签名证书的能力（例如推送通知）在自签版本上不可用；
   - 侧载与重签的具体步骤取决于你的工具和系统版本，请以所用工具的说明为准。

### macOS（无签名，需自行解除隔离）

> 该版本**未签名、未公证**，macOS 首次打开会提示「已损坏」或「无法验证开发者」，这是预期现象，不代表文件有问题。

1. 下载 `LyraNest-Photo-<版本>-macos-unsigned.zip`，解压得到应用。
2. 首次打开：右键点击应用 → **打开** → 在弹窗中再次确认；或者执行下面的命令移除隔离标记：

   ```bash
   xattr -dr com.apple.quarantine /Applications/你的应用名.app
   ```

3. 若仍被拦截，到「系统设置 → 隐私与安全性」中允许该应用运行。

### Android TV / 电视盒子

1. 先确认电视的 CPU 架构，再选择 ARM64 或 ARM32 的 TV 安装包；Android 5.0 及更老的设备请选择「兼容版」。
2. 通过 U 盘或电视端的文件管理器安装 APK。
3. 律巢相册 TV 与律巢相册 TV 兼容版**包名不同**，可以在同一台电视上并存安装。
4. 登录方式与手机端一致，也支持扫码授权。

### HarmonyOS 客户端开发中

HarmonyOS NEXT 客户端正在开发，尚未发布。完成后会在本仓库同步提供安装包，敬请期待。

## 客户端与兼容性

| 客户端 | 包名 | 架构 | 最低系统 |
| --- | --- | --- | --- |
| Android 手机 / 平板 | `com.lyranest.photo` | arm64-v8a | Android 7.0（API 24） |
| Windows 桌面端 | —（`lyranest_photo.exe`） | x64 | Windows 10 x64 |
| 律巢相册 TV | `com.lyranest.phototv` | arm64-v8a、armeabi-v7a | Android 7.0（API 24） |
| 律巢相册 TV 兼容版 | `com.lyranest.phototv.android5` | armeabi-v7a、arm64-v8a | Android 5.0（API 21） |
| iOS / iPadOS（无签名） | `com.lyranest.photo` | arm64 | 以对应 Release 说明为准 |
| macOS（无签名） | `com.lyranest.photo` | Apple 芯片、Intel | 以对应 Release 说明为准 |
| HarmonyOS NEXT | — | — | 开发中，敬请期待 |

**服务端要求**：一台已安装并启用官方相册的飞牛 fnOS 设备，客户端通过你平时打开飞牛管理界面的地址访问。

## 隐私说明

- 相册、视频与账号信息只在你自己的设备与自己的飞牛 NAS 之间传输，不经过任何第三方服务器中转。
- 客户端不接入第三方统计、广告或埋点 SDK。
- 登录会话保存在系统安全存储中，不写入普通配置、日志或诊断导出文件。
- 诊断日志只包含浏览、备份与网络行为记录，不含账号、密码、令牌与照片内容。

## 常见问题

**需要自己搭服务器吗？**

不需要。律巢相册只连接你自己的飞牛 NAS，没有官方中转服务，也不需要额外的服务端部署。

**为什么不开源？**

律巢相册是闭源项目，因此本仓库只提供安装包与更新记录。请勿尝试反编译、二次打包或转载安装包。

**和飞牛官方 App 是什么关系？**

律巢相册是第三方独立客户端，与飞牛官方没有隶属关系。它使用飞牛设备上的相册接口，若飞牛后续升级调整接口，客户端会跟进适配。

**连不上 NAS 怎么办？**

依次确认：NAS 与设备在同一局域网、飞牛管理界面可以正常打开、内网地址填写了正确端口（默认 `5666`）。若内网不通，可改用外网地址或 FNID。

**TV 上装不上或找不到图标？**

先确认 CPU 架构是否选对；Android 5.0 及更老的设备必须使用「TV 兼容版」。两台 TV 客户端包名不同，可同时安装。

**为什么 iOS / macOS 版本要自己侧载？**

这两个版本是**无签名构建**，没有 Apple 开发者签名与公证，也不在 App Store 上架，所以需要你自己动手一次：iOS 用侧载工具重签安装，macOS 手动移除隔离标记后打开。这样发布的版本不依赖商店审核，更新节奏更自由。

**鸿蒙端什么时候发布？**

HarmonyOS NEXT 客户端正在开发中，完成后会在这里同步发布安装包，敬请期待。

**更新日志在哪里？**

每个版本的详细内容在 `releases/<版本>/CHANGELOG.md`，也会同步展示在对应的 GitHub Release 正文中。

**怎么反馈问题？**

在 [Issues](https://github.com/WHWgogogo/LyraNest-Photo/issues) 提交，或加入 QQ 群 `1098566175`。反馈时请附上「关于律巢相册 → 导出诊断日志」生成的文件，并说明客户端版本与设备型号。

## 版本与校验

- 每个版本都保留独立 GitHub Release 与附件，不覆盖历史版本。
- 安装包只存在于 GitHub Release 附件中，不进入版本库；历史版本请到 [Releases](https://github.com/WHWgogogo/LyraNest-Photo/releases) 页面按版本号查找。
- README 的下载入口使用 GitHub `releases/latest`，始终指向最新稳定发行版。
- 建议核对 Release 页面展示的 SHA-256 摘要后再安装。

## 相关项目

- [LyraNest（律巢）](https://github.com/WHWgogogo/LyraNest)：自托管音乐服务，律巢相册的「音乐相册」功能可与它联动。
- [律巢相册最新发行版](https://github.com/WHWgogogo/LyraNest-Photo/releases/latest)：本仓库的下载页。
- [作者主页](https://github.com/WHWgogogo)。

## 版权声明

Copyright © WHWgogogo. All rights reserved.

律巢相册（LyraNest Photo）为闭源软件。未经作者书面许可，任何人不得复制、修改、反编译、反汇编、二次打包、二次分发或以其他方式使用本软件的安装包及其任何部分。本仓库仅用于分发正式发行版本。
