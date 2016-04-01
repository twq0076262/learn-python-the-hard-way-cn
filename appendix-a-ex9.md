# 附录 A-练习 9：生成一个空文件(Touch, New-Item)
这节练习中，你将学习使用 touch(Windows 中是 new-item)命令创建一个空文件。

## 做到这些

### Linux/OSX

```
$ cd temp
$ touch iamcool.txt
$ ls
iamcool.txt
$
```

### Windows

```
> cd temp
> New-Item iamcool.txt -type file
> ls


    Directory: C:\Users\zed\temp


Mode                LastWriteTime     Length Name
----                -------------     ------ ----
-a---        12/17/2011   9:03 AM            iamcool.txt


>
```

## 你应该学到的

你已经学会了如何创建一个空文件。在 Unix 中使用 touch 命令,它也改变了文件的修改时间。我只用这个命令还创建空文件。在 Windows 上，没有这命令，所以你要学习如何使用 New-Item 命令，这个命令可以创建空文件也可以创建创建一个新目录。

## 更多练习

> - Unix: 创建一个目录，进入它并在里面创建一个文件。然后回到他的上一级目录，执行 rmdir 命令，你将会得到一个错误。尝试想一想为什么会有这个错。
- Windows: 做同样的事情，但你不会看到这个错误。你将会得到一个提示，询问你是否真的要删除该目录。