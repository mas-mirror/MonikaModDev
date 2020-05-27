# 编程风格

我们没有严格的风格指南，但这里有几个惯例：

### 缩进

**四个空格缩进。**

### 标签

标签名称应为小写并用下划线分隔(`monika_twitter`). 
如果对相关子程序使用多个标签，在它们前面加上前缀 `mas` ，以及子程序的名称也加上这个 (即: `mas_coolfungame_flowstart`). **此规则的例外情况：** 莫妮卡主题/问候/告别，尽管这在未来可能会改变。

保留某些前缀：

- `greeting` - 用于日常问候语
- `i_greeting` - 用于特殊的互动问候语
- `ch30` - 用于关键章节30标签
- `monika` - 几乎用于每个莫妮卡话题
- `joke` - 用于笑话系统
- `m_joke` - 也用于笑话系统
- `mas_poem` - 用于写诗系统
- `game` - 用于小游戏
- `vv` - 用于更新相关材料
- `v` - 还是用于更新相关材料
- `bye` - 用于告别

可能还有更多，所以一般来说，要注意你使用的标签。


### store

在Renpy中，store就像namespace，只是不能有嵌套的namespace。我们建议对store中的相关数据、常量和函数进行分组，以避免干扰全局namespace。

创建存储：
```python
init python in mas_store_name:
    var1 = 1
    var2 = 2
    ...

# 或者
define mas_store_name.var1 = 1
define mas_store_name.var2 = 2
```

访问store：
```python
store.mas_store_name.var1 = 1

# 或者
python:
    import store.mas_store_name as mas_store_name
    mas_store_name.var1 = 1
```

我们使用多个不同的store对不同的数据进行分组。当决定建立一个新的store时，确保它还没有被使用。在store名称前加上前缀 `mas_`.

`persistent` 就像一个store，但它是一个特殊的被保存到磁盘的store。
**仅当需要保存来自多个会话的数据时才使用此选项** 。
稍后再讨论...

### 功能

如果函数非常特定于子程序或流，请考虑将其放在store中，并在必要时导入。如果一个函数可以推广到许多用例中， 那么 在常规的`init python`块中创建它（这使它成为全局的）。 **用mas前缀全局函数**

对于文档，块注释（#）或文档字符串（"""）都可以。我们不强制使用特定的方法来记录函数，但是注意函数的功能、输入和输出变量、返回的内容以及它假设的变量将是一个良好的开端：

```python
def mas_someKindOfFunction(var1, var2, var3=None):
    """
    这个函数做了一些事情。小心使用。

    IN:
        var1 - value of something
        var3 - like the most value of something
            (Default: None)

    OUT:
        var2 - contains modified reference to something

    RETURNS:
        a copy of var2

    ASSUMES:
        persistent.var4 
    """
```
对于函数名，camelCase或小写下划线都可以。

### Persistent

这种类似于store的东西将数据保存到磁盘，这就是renpy如何跟踪数据。
因为它已经装载了游戏保存的数据， **如果可以的话就不要用这个**. (即： 不使用Persistent来检查是否已看到事件，请使用 `renpy.seen_label` 或者`seen_event`.

**在所有持久变量名前加上前缀 `_mas_`.** (我们正在将所有当前创建的`persistent`值转换为正确的前缀)

### 常量

当您多次使用常量而不是文本时，请定义它们。使用大写下划线（UPPERCASE_UNDERSCORES）命名。

**屏幕上使用的文字是一个例外**. 如果*没*
用`nopredict`调用，那么请尽可能使用文字，因为renpy特别优化了
屏幕与文字。

### 变量

请把这些描述性的东西做得很好。它不需要像Java一样，只要足够多就可以了。
要让人很容易弄清楚它是什么。使用缩写或缩略语是
很好的做法。命名时使用小写字母_下划线（lowercase_underscores）。

### 注释

请大家写注释。虽然python的可读性很好，但知道python的高层次的原因或高层次的效果做事情是有帮助的。

### 长度

再说一次，不是真的强制执行，而是保持合理。我个人限制在80列，但超过这一限制，大概120列就可以了。
**例外是Renpy代码。** Renpy代码不能总是分成多行。

### 资源文件

您使用的任何资源文件必须在 `mod_assets/` 文件夹. 如果您有大量资源文件，请将它们分组到子文件夹中。

### 第三方

如果不使用外部程序包就可以做到，则无需
外部软件包。例外情况必须与开发团队讨论。如果您要添加的库超过一兆字节，几乎可以肯定**不会**允许你的pr。
