# 附录 A-练习 10：复制文件 (cp)
这节练习中你将使用 cp 命令从一个位置复制一个文件到另一个位置。

## 做到这些

### Linux/OSX

```
$ cd temp
$ cp iamcool.txt neat.txt
$ ls
iamcool.txt neat.txt
$ cp neat.txt awesome.txt
$ ls
awesome.txt iamcool.txt neat.txt
$ cp awesome.txt thefourthfile.txt
$ ls
awesome.txt  iamcool.txt  neat.txt  thefourthfile.txt
$ mkdir something
$ cp awesome.txt something/
$ ls
awesome.txt iamcool.txt  neat.txt  something  thefourthfile.txt
$ ls something/
awesome.txt
$ cp -r something newplace
$ ls newplace/
awesome.txt
$
```

### Windows

```
> cd temp
> cp iamcool.txt neat.txt
> ls


    Directory: C:\Users\zed\temp


Mode                LastWriteTime     Length Name
----                -------------     ------ ----
-a---        12/22/2011   4:49 PM          0 iamcool.txt
-a---        12/22/2011   4:49 PM          0 neat.txt


> cp neat.txt awesome.txt
> ls


    Directory: C:\Users\zed\temp


Mode                LastWriteTime     Length Name
----                -------------     ------ ----
-a---        12/22/2011   4:49 PM          0 awesome.txt
-a---        12/22/2011   4:49 PM          0 iamcool.txt
-a---        12/22/2011   4:49 PM          0 neat.txt


> cp awesome.txt thefourthfile.txt
> ls


    Directory: C:\Users\zed\temp


Mode                LastWriteTime     Length Name
----                -------------     ------ ----
-a---        12/22/2011   4:49 PM          0 awesome.txt
-a---        12/22/2011   4:49 PM          0 iamcool.txt
-a---        12/22/2011   4:49 PM          0 neat.txt
-a---        12/22/2011   4:49 PM          0 thefourthfile.txt


> mkdir something


    Directory: C:\Users\zed\temp


Mode                LastWriteTime     Length Name
----                -------------     ------ ----
d----        12/22/2011   4:52 PM            something


> cp awesome.txt something/
> ls


    Directory: C:\Users\zed\temp


Mode                LastWriteTime     Length Name
----                -------------     ------ ----
d----        12/22/2011   4:52 PM            something
-a---        12/22/2011   4:49 PM          0 awesome.txt
-a---        12/22/2011   4:49 PM          0 iamcool.txt
-a---        12/22/2011   4:49 PM          0 neat.txt
-a---        12/22/2011   4:49 PM          0 thefourthfile.txt


> ls something


    Directory: C:\Users\zed\temp\something


Mode                LastWriteTime     Length Name
----                -------------     ------ ----
-a---        12/22/2011   4:49 PM          0 awesome.txt


> cp -recurse something newplace
> ls newplace


    Directory: C:\Users\zed\temp\newplace


Mode                LastWriteTime     Length Name
----                -------------     ------ ----
-a---        12/22/2011   4:49 PM          0 awesome.txt

>
```

## 你应该学到的

现在你会复制文件了。这是简单的只获取一个文件，并复制到一个新文件。在这个练习中，我也创建了一个新目录，并将文件复制到该目录中。

我要告诉你一个关于程序员和系统管理员的秘密了。他们很懒，我也很懒，我的朋友们也很懒。这就是为什么我们要使用电脑。我们喜欢让电脑为我们做无聊的事情。在目前的练习中，为了使你了解这些命令，你需要重复键入这些枯燥的命令，但通常都不是这样的。通常，如果你发现自己正在做一些无聊或重复的事情，有可能已经有程序员找到更容易做到的方法了。只是你不知道这件事。

关于程序员的另一个秘密是，他们并不像你想象的那样聪明。如果你过多的思考要输入的内容，那你肯呢过就搞错了。相反，想象一下对你来说一个命令的名字是什么。可能是一个名字或者一些类似你认为的缩写。如果你仍然无法搞清楚，那么问问周围的人或者上网找找答案。但愿这不是跟 ROBOCOPY 一样愚蠢的东西。

## 更多练习

> - 使用 cp -r 命令，复制一个包含文件的目录。
- 复制一个文件到你的 home 目录或桌面。
- 在你的 GUI 中找到这些文件，并用文本编辑器打开它们。
- 请注意，为什么有时候我会在一个目录的结尾用一个/ (slash) ？这可以确保该文件确实是一个目录，如果没有这个目录，我就会得到一个错误。