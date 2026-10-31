[简体中文](#简体中文) | [English](#english)

---

## 简体中文

# echo-focus Lite

echo-focus Lite 是一款 macOS 菜单栏专注与陪伴应用。它可以记录专注时段、根据前台应用和浏览器域名提供轻量提醒，并通过你自行配置的 AI 服务进行角色对话。

> **仅限成年人使用：用户必须年满 18 周岁；如所在地区的法定成年年龄更高，则必须达到该年龄。未成年人不得使用本软件。**

## 下载

最新版本：**[echo-focus Lite 1.1](https://github.com/rkny6/echo-focus-releases/releases/latest)**（`echo-focus-lite-1.1.dmg`，SHA-256 见发布说明）。历史版本见 [Releases](https://github.com/rkny6/echo-focus-releases/releases) 页面，每个版本的发布说明标明版本号、系统要求和校验信息。

## 主要功能

- **专注计时与统计**：记录专注时段并查看历史和统计。
- **专注提醒**：可根据前台应用和浏览器当前页面的域名，辅助判断专注状态。判断由启发式规则完成，可能出错，不适用于考核或绩效评估。实际表现和靠谱程度见[分心提醒的实际表现](#分心提醒的实际表现)。
- **AI 角色对话**：可配置兼容的 AI 服务商、模型和 API key；软件不附带 AI 服务，相关费用由用户承担。
- **奖励与个性化**：专注奖励、礼物、外观、角色资料和提醒偏好。免费版可能有每日额度或可用内容限制。

## 分心提醒的实际表现

只在**专注进行中**出现。它根据前台应用和浏览器当前页面的类型做粗略判断，**并不理解你在做什么**。

**能期待什么**

- 分心后不会立刻提醒，也不会让你等太久；具体时机每次不同，不会定点出现。
- 一开始专注就已经停在分心页面上，同样会被注意到；安静地待着不动也不会被漏掉。
- 同一段分心不会被反复催。短暂切出去处理一下再回来，也不会被当成新的分心。
- 你离开电脑时不会提醒。
- 提醒之后如果长时间没有回到工作，角色会自己收住，不再继续催；下一次专注重新开始。
- 看课程、讲座、教程类视频时，开启「允许读取视频标题」后更可能被当作学习而不被打扰。

**靠谱程度**

判断是启发式的，误判和漏判都会发生，而且**漏判更常见**：

- 不常见的网站和应用、公司内网工具，通常被当作中性，不会提醒。
- 无痕/隐私窗口，或未授予浏览器相关权限时，读不到页面内容，不会提醒。
- 涉及银行、邮箱、密码管理等敏感站点时，应用完全不读取也不记录，因此这类场景不会提醒。
- 在分心类网站上做正经事（查资料、看文档、工作要用的论坛）可能被算作分心。
- 提醒的措辞由 AI 生成，需要你自行配置 AI 服务；没有配置或那次生成失败时，提醒不会出现。
- 关闭「专注提醒」后不再有系统横幅，角色仍可能在应用窗口里说话。「非专注时段打扰」是另一个开关，与此无关。

因此请把它当作一个会出错的粗略提示：不要用于考核、绩效、工时统计或自控打卡，也不要因为没被提醒就认定自己没分心。

## 系统要求

- macOS 13 Ventura 或更新版本
- Intel 或 Apple Silicon Mac（通用二进制）
- 浏览器域名判断、通知等功能需要用户主动授予相应的 macOS 权限；可在系统设置中撤销

## 安装与首次打开

1. 从 [Releases](https://github.com/rkny6/echo-focus-releases/releases) 下载 DMG。
2. 打开 DMG，将 `echo-focus Lite` 拖到「应用程序」，然后推出磁盘映像。
3. 本应用使用 **ad-hoc 签名，未经 Apple 公证**。macOS 可能会阻止首次打开。这是当前分发方式的限制，不代表已经通过 Apple 的安全审查。
4. 首次打开时，在「应用程序」中按住 Control 点击应用，选择「打开」，并在系统提示中确认。若该选项不可用，可先尝试打开一次，再到「系统设置 → 隐私与安全性」选择「仍要打开」。

ad-hoc 签名不包含开发者证书身份，因此 macOS 可能在应用更新后再次请求自动化权限。安装前请确认下载来源，并查看相应版本的校验信息。

## 隐私摘要

- 浏览器地址只用于本机判断域名。绝大多数时候浏览记录只是本机状态；唯一可能把**网站域名**发给 AI 服务商的场合，是专注中触发分心提醒的那一次，且受设置中「提醒时说出网站名称」控制（默认开启，关闭后不含任何域名）；开启「允许读取视频标题」（默认关闭）时还可能包含视频页面标题。应用名称、分类统计、对话内容及角色设定等，可能会发送到**你自行配置的 AI 服务端点**以生成回复。
- 应用不截屏、不记录键盘输入，也没有账号、遥测或崩溃上报。
- 数据保存在本机；卸载应用本身不会自动删除用户数据。
- API key 当前保存在 macOS 偏好设置中，而非 Keychain。建议使用独立且设有消费上限的 API key。

详细的数据处理说明和数据删除步骤见每个 DMG 内附的隐私政策与安装指南。

## 免责声明

AI 生成的对话、提醒和总结可能不准确、不完整或不适合某些情境。本软件不提供医疗、心理、法律、财务或投资建议。专注分类可能误判，不应作为正式考核依据。使用浏览器或活动判断功能前，请确认你有权在当前设备和工作环境中使用此类功能；公司设备或受监控环境可能受雇佣协议和内部政策约束。

软件按「现状」提供，不保证无错误或持续可用。完整免责声明随每个 DMG 提供。

## 许可

echo-focus Lite 是**专有软件，不是开源软件**。依据最终用户许可协议，仅授权个人、非商业用途。未经许可方事先书面许可，不得商业使用、修改或制作衍生版本、转售、再分发、托管安装包，或移除产品与版权标识。可以分享本仓库或官方发布页面的链接。

完整许可条款见每个 DMG 内附的 `LICENSE` 文档。README 摘要不替代完整协议。

---

## English

# echo-focus Lite

echo-focus Lite is a macOS menu-bar app for focus and companionship. It can record focus sessions, offer lightweight prompts based on the frontmost app and browser domain, and provide character conversations through an AI service that you configure yourself.

> **Adults only: users must be at least 18 years old, or older if the age of majority in their jurisdiction is higher. Minors must not use this Software.**

## Download

Latest release: **[echo-focus Lite 1.1](https://github.com/rkny6/echo-focus-releases/releases/latest)** (`echo-focus-lite-1.1.dmg`, SHA-256 in the release notes). Older versions are on the [Releases](https://github.com/rkny6/echo-focus-releases/releases) page; each release states its version, system requirements, and verification information.

## Features

- **Focus timer and history**: record focus sessions and review history and statistics.
- **Focus prompts**: optionally use the frontmost app and the current browser domain to help estimate focus. This heuristic can be wrong and is not suitable for reviews or performance evaluations. See [How distraction prompts actually behave](#how-distraction-prompts-actually-behave) for what to expect.
- **AI character conversations**: configure a compatible AI provider, model, and API key. No AI service is included; provider charges are your responsibility.
- **Rewards and personalization**: focus rewards, gifts, appearance, character settings, and reminder preferences. The free edition may have daily limits or a limited catalog.

## How distraction prompts actually behave

They only appear **while a focus session is running**. They make a rough guess from the frontmost app and the kind of page you have open, and **do not understand what you are actually doing**.

**What to expect**

- A prompt does not arrive immediately, and you will not be left waiting long either. The timing differs each time and is never at a fixed moment.
- Being on a distracting page when the session starts is noticed just the same, and sitting quietly without touching the keyboard will not be missed.
- The same stretch of distraction is not brought up repeatedly. Stepping away briefly and coming back is not treated as a new one.
- Nothing happens while you are away from the machine.
- If you do not return to work for a while after a prompt, the character backs off instead of pushing further, and the next session starts fresh.
- When you are watching lectures, courses, or tutorials, enabling "Allow reading video titles" makes it more likely to be treated as learning and left alone.

**How reliable it is**

The judgment is heuristic. Both false positives and misses happen, and **misses are more common**:

- Uncommon sites and apps, and internal company tools, are usually treated as neutral and produce nothing.
- Private or incognito windows cannot be read, and neither can any browser without the relevant permission granted.
- For sensitive sites such as banking, webmail, and password managers, the app reads and records nothing at all, so those cases are never flagged.
- Doing legitimate work on a distracting site (research, documentation, a work forum) can be counted as distraction.
- Prompt wording is AI-generated and needs your own configured AI service. Without one, or if that generation fails, no prompt appears.
- With "Focus prompts" off there are no system banners, though the character may still speak in the app window. "Nudges outside focus" is a separate, unrelated switch.

Treat it as a rough prompt that is sometimes wrong: not for performance reviews, timesheets, attendance, or self-tracking, and do not assume you were not distracted just because nothing appeared.

## System requirements

- macOS 13 Ventura or later
- Intel or Apple Silicon Mac (universal binary)
- Browser-domain detection and notifications require the corresponding macOS permissions, which you can grant or revoke in System Settings

## Installation and first launch

1. Download the DMG from [Releases](https://github.com/rkny6/echo-focus-releases/releases).
2. Open the DMG, drag `echo-focus Lite` to Applications, then eject the disk image.
3. The app is **ad-hoc signed and not notarized by Apple**. macOS may block the first launch. This is a limitation of the current distribution method; it does not mean Apple has reviewed the app for safety.
4. In Applications, Control-click the app, choose **Open**, and confirm the system prompt. If that option is unavailable, try opening it once, then use **System Settings → Privacy & Security → Open Anyway**.

Ad-hoc signing does not identify a developer certificate, so macOS may ask you to grant Automation permission again after an app update. Verify the download source and check the release's verification information before installing.

## Privacy summary

- Browser addresses are used for local domain classification. Browsing records normally stay on your machine; the one case where a **site domain** may reach an AI provider is the distraction prompt during a focus session, controlled by "Name the site in reminders" in settings (on by default; with it off no domain is included). With "Allow reading video titles" enabled (off by default), a video page title may also be included. App names, classification statistics, conversation content, and character settings may be sent to **the AI endpoint you configure** to generate responses.
- The app does not take screenshots or log keystrokes, and has no accounts, telemetry, or crash reporting.
- Data is stored locally; removing the app does not automatically remove its user data.
- API keys are currently stored in macOS preferences, not Keychain. Consider using a dedicated API key with a spending limit.

See the privacy policy and installation guide included with each DMG for details on data handling and deletion.

## Disclaimer

AI-generated dialogue, prompts, and summaries may be inaccurate, incomplete, or unsuitable for some situations. The Software does not provide medical, psychological, legal, financial, or investment advice. Focus classification may be wrong and should not be used for formal evaluation. Before using browser or activity detection, make sure you are permitted to do so on your device and in your work environment; company devices and monitored workplaces may be subject to employment agreements and internal policies.

The Software is provided "as is" without a guarantee of error-free or uninterrupted operation. The full disclaimer is included with each DMG.

## Licence

echo-focus Lite is **proprietary software, not open source**. The End User Licence Agreement permits personal, non-commercial use only. Without the Licensor's prior written permission, you may not use it commercially, modify it or make derivative versions, resell or redistribute it, host its installer, or remove product and copyright notices. You may share a link to this repository or the official release page.

See the `LICENSE` document included with each DMG for the full terms. This README summary does not replace the agreement.
