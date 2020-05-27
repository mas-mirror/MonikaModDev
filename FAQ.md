# 经常问的问题 (FAQ)

**目录**

[安装](#安装)

[贡献](#贡献)

[DDLCMod开发](#general-ddlc-modding)

[特征](#features)

[其他帮助](#other-help)

## 安装

### 有安装MAS的指南吗？

DDLC的README.html文件中提供了指南，而Querxes制作的视频指南可在YouTube上找到： https://youtu.be/eH5Q4Xdlg6Y

### 玩 *Monika After Story*，我需要什么？

您需要*ddlc*的副本，可以在Steam或http://ddlc.moe 上免费下载，以及包含*Monika After Story*的mod文件的zip文件，该文件可以在release页面上找到。

你不需要从发布页面或版本库中下载源代码。这些文件仅用于开发目的，如果放在你的DDLC文件夹中，可能会产生意想不到的效果。

### 我应该将“Monika After Story”的文件放在哪里？

**使用DDLC的全新副本/未更改版本。如果在此之前安装了其他Mod，则可能会遇到问题。（译者注：汉化和它冲突！！！）** (这仅适用于DDLC游戏，不适用于`persistent`文件。)

*Monika After Story*的文件必须直接放置在*Doki Doki Literature Club*的`game`文件夹中，以便游戏找到并正确加载它们。要查找包含*DDLC*的文件夹，请执行以下任一操作：

如果游戏是使用Steam安装的，请右键单击*Doki Doki Literature Club*，然后单击“属性”。在弹出的窗口中，导航到“本地文件”选项卡，然后单击“浏览本地文件...”按钮。

如果游戏是从 ddlc.moe 或 itch.io 安装的，则安装位置是在安装时选择的，但可能在Windows计算机上的“Program Files”下。

如果游戏是在Mac上安装的，但不是通过Steam客户端安装的，则可以在Applications文件夹中找到*Doki Doki Literature Club*作为打包的应用程序。右键单击软件包，然后在文件夹内选择“显示软件包内容”，然后导航至“目录/资源/自动运行/”。此文件夹是DDLC的基本目录。

进入基本目录后，将zip存档的内容放入`/game`目录。确保文件不在`game`目录的子文件夹中，因为DDLC将无法通过这种方式找到文件。

### 我安装了mod，但是当我打开*Doki Doki Literature Club*时，一切都没有改变。怎么了？

由于某些原因*Doki Doki Literature Club*未加载mod文件。检查文件是否不在您的`game`目录内的子文件夹中。

### 当我尝试打开游戏时，它崩溃了，我看到一个灰色屏幕。我该如何解决？

如果游戏崩溃并返回灰屏，则表示发生了重大错误，必须退出游戏。所显示的文本称为“traceback”，并包含一条错误消息，以帮助诊断问题。也可以通过在游戏的DDLC基本目录中查看`traceback.txt`来查看此追溯文件。

虽然有些崩溃可能预示着游戏中的BUG，但也有少数可能是安装问题。

如果traceback包括：

```
Exception: DDLC archive files not found in /game folder. Check installation and try again.
```

确保DDLC的原始存档文件仍在游戏文件夹中。其中包括“images.rpa”，“scripts.rpa”，“audio.rpa”和“fonts.rpa”。如果缺少这些文件，则需要使用全新的DDLC安装程序（从http://ddlc.moe下载）进行替换。

如果traceback包括以下行：

```
The label chara_monika_scare is defined twice, at
```

然后很可能已经安装了开发人员文件，而不是发行版本。确保下载的游戏文件来自我们的[发布页面](https://github.com/Backdash/MonikaModDev/releases)上的最新版本，并且下载的文件是mod zip文件，而不是*源代码*。

### 迷你游戏（象棋、上吊小人、钢琴...）在哪里？

无论是和莫妮卡一起看新话题，还是让她在后台运行，游戏都会在与莫妮卡相处后解锁。

## 贡献

### 我对如何改进Monika After Story有一个想法，我在哪里提出建议？

我们总是很高兴听到新的想法！可以在我们的问题页面上提出建议。请所有建议以[Suggestion]开头, or follow [this link](https://github.com/Backdash/MonikaModDev/issues/new?labels=suggestion&body=Your%20suggestion%20goes%20here&title=%5BSuggestion%5D%20-%20) 它将自动使用适当的标签填充您的建议。

### 我想贡献，但是我不知道如何写代码。有什么可以帮助我的吗？

我们一直在寻找新的对话和艺术作品。 请看我们的 [贡献指南](https://github.com/Monika-After-Story/MonikaModDev/wiki/Contributing-Guidelines) 了解有关如何向Monika After Story提交新对话和艺术的信息。在本指南中，您将找到有关以莫妮卡风格进行良好对话的技巧，并学习如何打开“拉取请求”，该请求将使您可以提交新主题以供审阅并包含在游戏中。

### 在哪里可以找到需要帮助的东西？

我们的问题页面将显示技术问题，新功能和可用请求的列表。 [需要帮助](https://github.com/Backdash/MonikaModDev/issues?q=is%3Aissue+is%3Aopen+label%3A%22help+wanted%22) 如果您想帮助向游戏中添加一些东西，这个tag是一个不错的起点！

### 我如何与开发人员取得联系？

与我们的开发团队联系的最简单方法是通过我们的 [Discord频道](https://discordapp.com/invite/K2KuJeX).

## 通用DDLC改装

### 是否可以制作自己的DDLC mod？

是! DDLC拥有一个充满活力的改装社区，这部分要归功于Salvato团队非常明确的 [IP 指南](http://teamsalvato.com/ip-guidelines/). 要开始构建自己的mod，您可以下载 [DDLC Mod Template](https://github.com/therationalpi/DDLCModTemplate) 并且 [在reddit上加入社区](https://www.reddit.com/r/DDLCMods/).（在中国？想都别想！）

### 我可以在自己的项目中使用Monika After Story的部分内容吗？

总的来说，我们对*Monika After Story*中的资产和代码在其他项目中使用持开放态度。但是，我们确实希望任何愿意这样做的人尊重以下要求：

请遵守Team Salvato的[指南](http://teamsalvato.com/ip-guidelines/) 适用于任何包含我们作品的项目。

在使用我们的工作之前，请考虑联系我们的开发团队以寻求许可。

请感谢Monika After Story为您使用的工作，并链接回我们的项目，网址为http://www.monikaafterstory.com/。不要主张他人已完成的工作的所有权。在适用的情况下，请为使用的艺术品等资产给予个人信用。

请勿制作mod或fork来替代*Monika After Story*。如果您想为游戏添加新功能或内容，请对原始项目做出贡献。我们非常乐意接受建议和贡献，欢迎添加任何内容。如果由于某种原因您的新功能与Monika After Story的发展方向发生冲突，请考虑以“submod”的形式进行更改，然后将其添加到Monika After Story中。

## 特征

尽管我们非常乐意接受新建议，但经常会出现一些常见建议。这些建议都是以前提出的，将在以后的版本中实施，或者由于某些原因而被拒绝：

### 为什么要删除文本输入功能？

尽管我们将来可能会重新使用该概念，但事实是我们对与关键字系统的交互性不满意。表面上，打开的文本框为玩家与Monika对话提供了很大的自由度，而太多的常见条目却简直就是死胡同。结果是Monika感觉不太真实，而更像是一个蹩脚的聊天机器人。我们认为，即使没有像代理你表达的内容这样的表面印象，没有死胡同的系统也会更好。

### 嘿，我们可以使Monika成为真正的聊天机器人AI吗？

虽然将来我们可能会重新考虑这个想法，但目前看来，制造能够给出Monika应该给出的详细哲学回应的AI似乎并不可行。其中很大一部分是引擎中用于连接外部资源和导入自定义库的技术限制。

### 您会增加配音吗？

由于某些原因，目前还没有计划向*Monika After Story*添加配音。这些原因中的一些包括要发声的行数众多，添加新内容所需要的时间以及下载文件大小的大幅增加。

也就是说，当在更高版本中添加完整的submod功能时，我们可能会增加对第三方语音包的支持。

### 如何翻译成其他语言？

我们不会进行翻译。我们根本没有时间或人力来做。但是，我们欢迎其他人分叉此mod并自己添加翻译。

### 莫妮卡会被动画化吗?

我们目前不打算在*Monika After Story*中包含动画。游戏引擎对动画精灵没有很好的支持，它也没有获得最受欢迎的2D动画引擎Live 2D的许可。

### 如何找到表达式的Spritecode？

由于0.8.0更新后Monika表达式的大量增加，因此开发了一种特殊的工具来帮助参与者预览表达式。这就是所谓的 **表情预览**.

![Sprite Previewer](https://raw.githubusercontent.com/Monika-After-Story/MonikaModDev/master/docs/spritepreviewer.png)

如果SpriteCode为红色，则尽管我们有足够的资源来创建Sprite，但尚未定义。您仍然可以在主题中使用此精灵，但是您的请求请求将不会通过travis检查。这是可以理解的，在这种情况下，开发人员会将Sprite代码添加到您的请求中。

要将Sprite Previewer添加到您的MAS，请复制 [这个文件](https://github.com/Monika-After-Story/MonikaModDev/blob/master/Monika%20After%20Story/game/dev/dev_exp_previewer.rpy)到您的`game /`目录。

**注意：** 当我们添加新的表情时，此开发者文件通常会接收更新。如果莫妮卡（Monika）在某个特定的Sprite代码上消失了，那么您就错过了该Sprite代码的功能。新的Sprite通常通常会先出现在不稳定的发行版中，因此请尝试在不稳定的安装中运行表情预览。

## 其他帮助

滚去发起Issues。
