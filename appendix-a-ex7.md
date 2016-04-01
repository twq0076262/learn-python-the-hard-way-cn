# 附录 A-练习 7：删除路径 (rmdir)
这节练习中，你将学习如何删除一个空目录。

## 做到这些

### Linux/OSX

```
$ cd temp
$ ls
stuff
$ cd stuff/things/frank/joe/alex/john/
$ cd ..
$ rmdir john
$ cd ..
$ rmdir alex
$ cd ..
$ ls
joe
$ rmdir joe
$ cd ..
$ ls
frank
$ rmdir frank
$ cd ..
$ ls
things
$ rmdir things
$ cd ..
$ ls
stuff
$ rmdir stuff
$ pwd
~/temp
$
```

> **Warning:** 如果你在 Mac OSX 上尝试执行 rmdir 命令，即使你确认这个目录是空的，但是计算机仍拒绝删除该目录，那么实际上应该是有一个名为.DS_Store 的文件。这种情况下，你可以输入 rm -rf `<dir>` 来执行删除操作(将 `<dir> `替换为你要删除的目录名)。

### Windows

```
> cd temp
> ls


    Directory: C:\Users\zed\temp


Mode                LastWriteTime     Length Name
----                -------------     ------ ----
d----        12/17/2011   9:03 AM            stuff


> cd stuff/things/frank/joe/alex/john/
> cd ..
> rmdir john
> cd ..
> rmdir alex
> cd ..
> rmdir joe
> cd ..
> rmdir frank
> cd ..
> ls


    Directory: C:\Users\zed\temp\stuff


Mode                LastWriteTime     Length Name
----                -------------     ------ ----
d----        12/17/2011   9:14 AM            things


> rmdir things
> cd ..
> ls


    Directory: C:\Users\zed\temp


Mode                LastWriteTime     Length Name
----                -------------     ------ ----
d----        12/17/2011   9:14 AM            stuff


> rmdir stuff
> pwd

Path
----
C:\Users\zed\temp


> cd ..
>
```

## 你应该学到的

现在我把这些命令混合起来了，所以你需要加倍注意，并确保你输入了正确的命令。每次你犯一个错误，都是因为你没有仔细看。如果你发现自己犯了不少错误，那么休息以下，或者退出练习一天。你总是需要明天再试一次的。

这个例子中，你学习了如何删除一个目录。很简单，你只需要在该目录的上一级目录，输入 rmdir `<dir>`, 把`<dir>` 替换成你要删除的目录名。

## 更多练习

> - 创建 20 个以上的目标，再把他们都删除。
- 创建一个深度为 10 的单一路径的目录，然后每次删除其中的一个。
- 如果你尝试删除一个不为空的目录，你会得到一个错误。在后面的练习中我会告诉你如何删除这样的目录。