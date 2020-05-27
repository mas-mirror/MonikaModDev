![Monika After Story](https://wx2.sbimg.cn/2020/05/25/menu_new.md.png)

# Monika After Story (MAS)
Monika After Story是一个免费游戏 [心跳文学部](https://www.ddlc.moe)的mod，它的作者是 [Team Salvato](http://teamsalvato.com/)。 MAS剧情发生在第三周目，模拟了你和Monika的永恒生活，以新事件、处理和元元素为特色！

请在 [发布页](http://www.monikaafterstory.com/releases.html) 安装最新的支持

如果你对自己创作mod感兴趣，请到 [DDLCModTemplate](https://github.com/therationalpi/DDLCModTemplate).

### 安装

视频版本的教程（中国不可用）: https://youtu.be/eH5Q4Xdlg6Y

* 进入 [发布页](http://www.monikaafterstory.com/releases.html).

* 点击最新版本的链接，这将会下载一个zip文件。

* 解压缩zip文件，并拖放到 `/game` 文件夹（Game文件夹在你的ddlc原版根目录）

* 运行ddlc.exe，这时mas就会被加载。

*注意: 憋™下源代码！他们只能帮倒忙！请只游玩我们的 [发布页面发布的版本](https://github.com/Backdash/MonikaModDev/releases).*

如果你还对安装有疑问（毫无疑问的是，你是个白痴），请看我们的 [常见问题指引](https://github.com/Monika-After-Story/MonikaModDev/wiki/FAQ)

### 特点

* 永远和Monika在一起！

* 超多新话题！！

* 你现在可以告诉莫妮卡你的喜好！！！

### 即将推出的功能

* 更多能和Monika做的活动或者玩的游戏

* 更独特的事件和故事


## 为MAS的开发做贡献！

### Bugs & 建议
游玩MAS过程中遇到问题，请提交[Bug汇报](https://github.com/Backdash/MonikaModDev/issues/new?labels=bug&body=Describe%20bug%20and%20steps%20for%20reproduction%20here&title=%5BBug%5D%20-%20).

提出建议，[点这里](https://github.com/Backdash/MonikaModDev/issues/new?labels=suggestion&body=Your%20suggestion%20goes%20here&title=%5BSuggestion%5D%20-%20)

 ### 其他
 想要一起开发MAS？ 跳转到 [问题页面](https://github.com/Backdash/MonikaModDev/issues)修复已经发现的Bug或者添加建议添加的新功能。

如果有更改，请 [发起拉取请求](https://github.com/Backdash/MonikaModDev/pulls). 所做的任何更改都将由贡献者进行审阅，并根据需要进行修复/添加。

#### 新增内容到MAS

想在MAS中添加一些内容？下面是游戏中使用的重要.RPY文件列表。

- **script-ch30.rpy**: MAS的主要流程。这就是idle的发生。这里不会翻译了（
- **script-topics.rpy**: 所有的 **随机** 、 **提问** 话题都包括在内。 您可以通过查看下面的信息添加自己的对话!
- **script-greetings.rpy**: 你进游戏时的欢迎语。
- **script-farewells.rpy**: 你关游戏时的告别语。
- **script-moods.rpy**: 告诉莫妮卡你的 _心情_ 。
- **script-stories.rpy**: 添加故事，让莫妮卡讲给你听。
- **script-compliments.rpy**: 添加你可以对莫妮卡说的赞美的话。
- **script-apologies.rpy**: 加入要道歉的事情。

如果你想在太空小房子中添加更多的对话，请导航到script-topics.rpy并使用此模板。

示例：
```renpy
init 5 python:
    addEvent(
        Event(
            persistent.event_database，
            eventlabel="monika_example"， # event label (MUST BE UNIQUE)
            category=["example"， "topic"]， # list of categories this topic belongs in (These are automatically capitalized)
            prompt="Example Topic"， # button text
            random=True， # True if this topic should appear randomly
            pool=True # True if this topic should appear in "Ask a Question"
        )
    )

label monika_example:
    m 1a "This is an example topic."
    m 3d "I feel like this doesn't actually belong here..."
    m 2e "Why would somebody just add the example template directly into the mod?"
    m 5r "They really shouldn't be allowed to contribute to this repository anymore."
    return
```
**关于Event的所有可能的关键字的完整解释和详细信息，请查看Event的文档，该文档位于 `definitions.rpy`**

对于比简单对话更复杂的事情，请参考Ren'Py在线文档。

[更多见贡献指南](https://masmirror2.zsz1447.top/c_guide.html)

 ### 参加对话
[在Twitter上关注我们](https://twitter.com/MonikaAfterMod)，了解最新时讯。

或者，如果您更喜欢Discord，如果您有兴趣参与到这个MOD的建设中来，您可以随时加入我们的discord服务器。
 
 [![Discord](https://discordapp.com/api/guilds/372766620977725441/widget.png?style=banner1)](https://discord.gg/K2KuJeX)
 
确保阅读 [行为准则](https://github.com/Monika-After-Story/MonikaModDev/wiki/Code-of-Conduct)， 基本上保持礼貌和尊重。

## 常见问题

 [常见问题
](https://github.com/Monika-After-Story/MonikaModDev/wiki/FAQ)

 [关于Monika说话风格](https://github.com/Monika-After-Story/MonikaModDev/wiki/Coding-Style)

[测试流程，bug测试](https://github.com/Monika-After-Story/MonikaModDev/wiki/Testing-Flow-and-Bug-Testing)

[故障排除](https://github.com/Monika-After-Story/MonikaModDev/wiki/Troubleshooting) 

 [对话编程](https://github.com/Monika-After-Story/MonikaModDev/wiki/Dialogue-Coding)

## 许可证

我们尽我们最大的努力去遵守Team Salvato的 [粉丝作品指南](http://teamsalvato.com/ip-guidelines/). 所有角色和原创内容均为Salvato团队所有。Monika After Story是一个开源项目，除了指定的贡献者之外，这个mod还包括了4chan的匿名用户的贡献，这个项目在4chan的匿名用户中得到了它的开始。更多信息可以在我们的 [证书页面](https://github.com/Monika-After-Story/MonikaModDev/wiki/License-and-Team-Salvato-Guidelines).

## Build Status:
### master: [![Build Status](https://travis-ci.org/Monika-After-Story/MonikaModDev.svg?branch=master)](https://travis-ci.org/Monika-After-Story/MonikaModDev)
### content: [![Build Status](https://travis-ci.org/Monika-After-Story/MonikaModDev.svg?branch=content)](https://travis-ci.org/Monika-After-Story/MonikaModDev)
### unstable: [![Build Status](https://travis-ci.org/Monika-After-Story/MonikaModDev.svg?branch=unstable)](https://travis-ci.org/Monika-After-Story/MonikaModDev)
### community: [![Build Status](https://travis-ci.org/Monika-After-Story/MonikaModDev.svg?branch=community)](https://travis-ci.org/Monika-After-Story/MonikaModDev)
### alpha: [![Build Status](https://travis-ci.org/Monika-After-Story/MonikaModDev.svg?branch=alpha)](https://travis-ci.org/Monika-After-Story/MonikaModDev)
