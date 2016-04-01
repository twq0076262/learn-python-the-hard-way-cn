# 附录 A-练习 5：改变当前路径 (cd)
这节练习中，你将学习如何使用 cd 命令从一个目录切换到另一个。

## 做到这些

我打算再一次给你解释这些会话的内容：

> - 你不需要输入 $ (Unix) 或 > (Windows).
- 你输入 stuff 然后敲回车。如果我是$ cd temp 你只需要输入 cd temp 然后回车。
- 输出会在你按下回车键之后展现，跟在另一个$ 或 > 提示符之后.
- 永远先回到 home 目录! 执行 pwd 和 cd ~。

### Linux/OSX

```
$ cd temp
$ pwd
~/temp
$ cd stuff
$ pwd
~/temp/stuff
$ cd things
$ pwd
~/temp/stuff/things
$ cd frank/
$ pwd
~/temp/stuff/things/frank
$ cd joe/
$ pwd
~/temp/stuff/things/frank/joe
$ cd alex/
$ pwd
~/temp/stuff/things/frank/joe/alex
$ cd john/
$ pwd
~/temp/stuff/things/frank/joe/alex/john
$ cd ..
$ cd ..
$ pwd
~/temp/stuff/things/frank/joe
$ cd ..
$ cd ..
$ pwd
~/temp/stuff/things
$ cd ../../..
$ pwd
~/
$ cd temp/stuff/things/frank/joe/alex/john
$ pwd
~/temp/stuff/things/frank/joe/alex/john
$ cd ../../../../../../../
$ pwd
~/
$
```

### Windows

```
> cd temp
> pwd

Path
----
C:\Users\zed\temp


> cd stuff
> pwd

Path
----
C:\Users\zed\temp\stuff


> cd things
> pwd

Path
----
C:\Users\zed\temp\stuff\things


> cd frank
> pwd

Path
----
C:\Users\zed\temp\stuff\things\frank


> cd joe
> pwd

Path
----
C:\Users\zed\temp\stuff\things\frank\joe


> cd alex
> pwd

Path
----
C:\Users\zed\temp\stuff\things\frank\joe\alex


> cd john
> pwd

Path
----
C:\Users\zed\temp\stuff\things\frank\joe\alex\john


> cd ..
> cd ..
> cd ..
> pwd

Path
----
C:\Users\zed\temp\stuff\things\frank


> cd ../..
> pwd

Path
----
C:\Users\zed\temp\stuff


> cd ..
> cd ..
> cd temp/stuff/things/frank/joe/alex/john
> cd ../../../../../../../
> pwd

Path
----
C:\Users\zed


>
```

## 你应该学到的

上节练习中你已经创建了所有的目录，你现在只需要使用 cd 命令，就能实现在它们之间进行切换。在上面我的会话中，我也使用 pwd 来检查我在哪里，所以一定记得不要输入命令 pwd 所输出的内容。比如，在第 3 行中，你看到~/temp，但是它是上面一个 pwd 命令的输出。所以不要输入这行。

你应该看到我如何使用.. 来移动到上一层目录的。

## 更多练习

学习在计算机上使用命令行模式(CLI)与图形用户界面(GUI)的一个非常重要的部分弄清楚他们是如何协同工作的。当我刚开始使用电脑时，是没有 GUI 的，我要做的一切都是用 DOS 提示符（命令行）来实现的.后来,当电脑变得足够强大,每个人都可以通过 GUI 操作电脑的时候,GUI 窗口和 CLI 目录文件夹协同使用对我来说是很简单的。

今天的大多数人，并不理解 CLI、路径和目录的概念。实际上，很难教会他们理解这些，唯一的学习方式是给你不断的使用 CLI，直到有一天你点击你在 GUI 中做的东西，而它能出现在 CLI 中。

做到这些的方法是你花一些时间找到你的 GUI 文件浏览器，然后通过你的 CLI 进入文件浏览器。这些是你下一步要做的事情：

> - 使用一个命令进入 joe 目录。
- 使用一个命令回到 temp 目录，但不能使用上面例子中的命令。
- 找到使用一个命令回到 "home 目录" 的方法。
- 进入你的文件目录，然后使用你的 GUI 文件浏览器找到这个目录。
- 进入你的下载目录，然后使用你的 GUI 文件浏览器找到这个目录。
- 使用你的 GUI 文件浏览器找到另一个目录，然后使用 cd 进入这个目录。
- 还记不记得你用引号包围一个名字中有空格的目录？你可以使用任何命令这么做。比如，你有一个目录叫做 I Have Fun，那你可以执行: cd "I Have Fun"