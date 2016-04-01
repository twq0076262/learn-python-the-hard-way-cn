# 附录 A-练习 6：列出当前路径 (ls)
这节练习中你将学习如何使用 ls 命令列出一个目录下的所有内容。

## 做到这些

开始之前，确认你已经 cd 回到 temp 的上一层目录。.如果你不知道你在哪里，使用 pwd 找到你的位置，然后移动到正确的目录下。

### Linux/OSX

```
$ cd temp
$ ls
stuff
$ cd stuff
$ ls
things
$ cd things
$ ls
frank
$ cd frank
$ ls
joe
$ cd joe
$ ls
alex
$ cd alex
$ ls
$ cd john
$ ls
$ cd ..
$ ls
john
$ cd ../../../
$ ls
frank
$ cd ../../
$ ls
stuff
$
```

### Windows

```
> cd temp
> ls


    Directory: C:\Users\zed\temp


Mode                LastWriteTime     Length Name
----                -------------     ------ ----
d----        12/17/2011   9:03 AM            stuff


> cd stuff
> ls


    Directory: C:\Users\zed\temp\stuff


Mode                LastWriteTime     Length Name
----                -------------     ------ ----
d----        12/17/2011   9:03 AM            things


> cd things
> ls


    Directory: C:\Users\zed\temp\stuff\things


Mode                LastWriteTime     Length Name
----                -------------     ------ ----
d----        12/17/2011   9:03 AM            frank


> cd frank
> ls


    Directory: C:\Users\zed\temp\stuff\things\frank


Mode                LastWriteTime     Length Name
----                -------------     ------ ----
d----        12/17/2011   9:03 AM            joe


> cd joe
> ls


    Directory: C:\Users\zed\temp\stuff\things\frank\joe


Mode                LastWriteTime     Length Name
----                -------------     ------ ----
d----        12/17/2011   9:03 AM            alex


> cd alex
> ls


    Directory: C:\Users\zed\temp\stuff\things\frank\joe\alex


Mode                LastWriteTime     Length Name
----                -------------     ------ ----
d----        12/17/2011   9:03 AM            john


> cd john
> ls
> cd ..
> ls


    Directory: C:\Users\zed\temp\stuff\things\frank\joe\alex


Mode                LastWriteTime     Length Name
----                -------------     ------ ----
d----        12/17/2011   9:03 AM            john


> cd ..
> ls


    Directory: C:\Users\zed\temp\stuff\things\frank\joe


Mode                LastWriteTime     Length Name
----                -------------     ------ ----
d----        12/17/2011   9:03 AM            alex


> cd ../../..
> ls


    Directory: C:\Users\zed\temp\stuff


Mode                LastWriteTime     Length Name
----                -------------     ------ ----
d----        12/17/2011   9:03 AM            things


> cd ..
> ls


    Directory: C:\Users\zed\temp


Mode                LastWriteTime     Length Name
----                -------------     ------ ----
d----        12/17/2011   9:03 AM            stuff


>
```

## 你应该学到的

ls 能列出你当前目录中的所有内容。你可以看到我用 cd 切换到不同的目录下，然后列出该目录下的所有内容，这样，我就知道我接下来要到哪个目录中去了。

ls 命令有很多的命令选项，当我们学习 help 命令之后，你将会学习如何得到这些命令选项的帮助信息。

## 更多练习

> - 输入这里的每一个命令！你必须亲手输入这些命令来学习他们。只是读他们并不够。
- 在 Unix 中, 在 temp 目录下试试命令 ls -lR。
- 在 Windows 中也可以试试 dir -R.
- 使用 cd 进入到你计算机上的其他目录，然后使用 ls 看看当前目录里有什么。
- 将你遇到的新问题更新到你的笔记本中。我知道你可能已经有一些问题了，因为我并没有覆盖这些命令的所有点。
- 记住，如果你迷路了，使用 ls 和 pwd 找到你在哪里，然后使用 cd 去到你要去的目录。