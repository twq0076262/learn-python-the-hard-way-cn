# 附录 A-练习 4：创建一个路径 (mkdir)
这节练习，你将学习如果使用 mkdir 命令创建一个新的目录（文件夹）。

## 做到这些

记住！ 你要先回到你的 home 目录！在你做这节练习之前，先执行 pwd 和 cd ~操作。 在你做本附录的所有练习之前，都先回到 home 目录！

### Linux/OSX

```
$ pwd
$ cd ~
$ mkdir temp
$ mkdir temp/stuff
$ mkdir temp/stuff/things
$ mkdir -p temp/stuff/things/frank/joe/alex/john
$
```

### Windows

```
> pwd
> cd ~
> mkdir temp


    Directory: C:\Users\zed


Mode                LastWriteTime     Length Name
----                -------------     ------ ----
d----        12/17/2011   9:02 AM            temp


> mkdir temp/stuff


    Directory: C:\Users\zed\temp


Mode                LastWriteTime     Length Name
----                -------------     ------ ----
d----        12/17/2011   9:02 AM            stuff


> mkdir temp/stuff/things


    Directory: C:\Users\zed\temp\stuff

Mode                LastWriteTime     Length Name
----                -------------     ------ ----
d----        12/17/2011   9:03 AM            things


> mkdir temp/stuff/things/frank/joe/alex/john


    Directory: C:\Users\zed\temp\stuff\things\frank\joe\alex


Mode                LastWriteTime     Length Name
----                -------------     ------ ----
d----        12/17/2011   9:03 AM            john


>
```

这是我唯一一次给你列出 pwd 和 cd ~ 命令。 它们预计会在每次练习中使用。随时使用它们。

## 你应该学到的

现在我们已经开始学习输入多个命令。这些都是可以运行 mkdir 的方式。 mkdir 是做什么的？它能创建目录。你为什么问这个？你应该用你的索引卡片练习记忆这些命令。如果你不知道"mkdir 创建目录"，那你应该继续使用索引卡练习。

创建一个目录是什么意思？你也可以把目录叫做文件夹。他们是同一种东西。 所有你上面做的事情是创建目录内的目录。这也可以叫做“路径”这是一个跟你说 "第一 temp, 然后 stuff, 接下来 things，这就是我想要的"的方式。这在你的计算机硬盘上就是一系列树形结构的文件夹。

> **NOTE:** 在本附录中，我在所有路径中使用 / (slash) 字符，因为现在他们在所有计算机上都能正常工作。然而， Windows 系统使用者需要知道，你们也可以使用\ (backslash)。

## 更多练习

> - "path" 的概念可能会使你迷惑。别担心。我们将用他们做更多的练习，然后你就会理解了。
- 在 temp 目录下创建 20 个其他的目录，这 20 个目录要在不同的层级上。通过你的图形文件浏览器看看你创建的目录。
- 试试看创建一个名字中带有空格且被双引号包起来的目录：mkdir "I Have Fun"
- 如果 temp 目录已经存在，那么你将得到一个错误。使用 cd 改变当前工作目录，然后再尝试创建不同目录。在 Windows 中，桌面是一个好地方。