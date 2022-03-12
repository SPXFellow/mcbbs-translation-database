# MCBBS 博文翻译仓库

这里是由 SPX Fellow 运营的 MCBBS 博文翻译仓库。

## 收录范围

- 官网博文（`minecraft-net`）
- Feedback 文章（`feedback`）
- Help 文章（`help`）

## Workflow

### 新建翻译

下面介绍本仓库的 workflow 供参考。

首先，clone 本仓库并新建一个 branch，命名为 `<source>/<文字 ID>`。若结果超过了 255 个字符，则进行缩减。如：

- <https://www.minecraft.net/zh-hans/article/minecraft-java-edition-1-18-2> 对应 `minecraft-net/minecraft-java-edition-1-18-2`
- <https://help.minecraft.net/hc/en-us/articles/4415922646541--Minecraft-no-longer-available-for-non-Amazon-devices-in-the-Amazon-store-> 对应 `help/4415922646541--Minecraft-no-longer-available-for-non-Amazon-devices-in-the-Amazon-store-`
- <https://feedback.minecraft.net/hc/en-us/articles/4675499616013-Minecraft-Beta-Preview-1-18-30-22-23> 对应 `feedback/4675499616013-Minecraft-Beta-Preview-1-18-30-22-23`

其次，用 VSCode 在对应目录下创建 `0000-<文字 ID>.bbcode` 文件，并将经 SPXX 转换过的 BBCode 贴入。在文章最前面，你需要加上一段用 YAML 表示的 metadata。格式如下：

```yaml
---
verison: 1.0 # 请不要更改此项
title: Minecraft Java Edition 1.18.2 # 文章原文标题
link: https://www.minecraft.net/zh-hans/article/minecraft-java-edition-1-18-2 # 链接
source: minecraft-net # 文章源，与 branch 名前半部分一致。
identifier:
  numeric: 0000 # 数字 ID，此项不应更改
  literal: minecraft-net/minecraft-java-edition-1-18-2 # 文字 ID 与 branch 名一致
date: 2022-02-28 # 日期，注意格式
license: CC-BY-SA-4.0 # 许可证，请使用 SPDX ID。我们定义 No Emeralds 许可证的 ID 为 No-Emeralds-1.0
translators: # 翻译者列表，请填写 MCBBS ID
  -
  -
  -
  -
mcbbs:
  posted: false # 是否已经发布至 MCBBS
  tid: 0 # TID
  title: [Minecraft.net | NEWSLORD] SPG We Love U!!!!!!!!!!!!!!!! # MCBBS 文章标题
  link: https://www.mcbbs.net/thread-0-1-1.html # 帖子链接
  user: 混乱 # 发布帖子的用户名
  date: 1970-01-01 # 发布帖子的日期。
  updated: 1970-01-01 # 最后更新日期。
---
```

随后，向本仓库提交并向 `main` 发起 Pull Request，记得将其标注为 Draft。

现在，你可以开启 Live Share，并将链接发入群中。如果您需要中途离开并关闭 session，请先保存内容并 commit。

翻译完成后，你就可以关闭 Live Share，并将翻译好的文件 push 到你的 branch 中。你可以将本文发布到 MCBBS 上并更新 metadata。记得 at
其他贡献者，让版主给他们加分。并把你的 PR Mark as Ready。

最后，SPX Fellow 成员会给你的帖子分配 ID 并 merge 你的 PR。请留意你的 Inbox，记得查看你的帖子是否有新的 patch。

### 更新翻译

你可以随时通过 Pull Request 更新翻译。注意 branch 名称应为 `<用户名>-patch-<文章 ID>-<日期>`。如 `Dianliang233-patch-0001-2022-03-12`。

SPX Fellow 将会尽力联系原作者，将你的 patch 更新至 MCBBS 并申请给你加分。若联系失败，我们允许你另行发布翻译。
