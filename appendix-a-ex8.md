# 附录 A-练习 8：目录切换(pushd, popd)
这节练习中，你将学习如何使用 pushd 实现保存你的当前位置，并去一个新的位置，然后您将学习如何使用 popd 恢复保存位置。

## 做到这些

### Linux/OSX

```
$ cd temp
$ mkdir -p i/like/icecream
$ pushd i/like/icecream
~/temp/i/like/icecream ~/temp
$ popd
~/temp
$ pwd
~/temp
$ pushd i/like
~/temp/i/like ~/temp
$ pwd
~/temp/i/like
$ pushd icecream
~/temp/i/like/icecream ~/temp/i/like ~/temp
$ pwd
~/temp/i/like/icecream
$ popd
~/temp/i/like ~/temp
$ pwd
~/temp/i/like
$ popd
~/temp
$ pushd i/like/icecream
~/temp/i/like/icecream ~/temp
$ pushd
~/temp ~/temp/i/like/icecream
$ pwd
~/temp
$ pushd
~/temp/i/like/icecream ~/temp
$ pwd
~/temp/i/like/icecream
$
```

### Windows

```
> cd temp
> mkdir -p i/like/icecream


    Directory: C:\Users\zed\temp\i\like


Mode                LastWriteTime     Length Name
----                -------------     ------ ----
d----        12/20/2011  11:05 AM            icecream


> pushd i/like/icecream
> popd
> pwd

Path
----
C:\Users\zed\temp


> pushd i/like
> pwd

Path
----
C:\Users\zed\temp\i\like


> pushd icecream
> pwd

Path
----
C:\Users\zed\temp\i\like\icecream


> popd
> pwd

Path
----
C:\Users\zed\temp\i\like


> popd
>
```

## 你应该学到的

你使用这些命令进入了程序员的领土，这些命令是如何方便使用，我一定要教会你使用。这些命令让你暂时去到不同的目录，然后再回来，实现两个目录之间的轻松切换。

pushd 命令把你当前的目录放到一个 list 中，然后切换到另一个目录。就好像说"保存我在哪里，然后去下一个地方"

popd 命令把你之前存储的目录弹出来，然后带你回到那个目录。

最后， 在 Unix 上，如果你不带任何参数运行 pushd，将会在当前目录以及你之前最后一次保存的目录之间进行切换。这是来回切换两个目录的方法，但它在 Powershell 中不起作用。

## 更多练习

> - 使用这两个命令在你计算机上的所有目录中来回切换。
- 删除目录 i/like/icecream 再自己创建几个目录，在你新创建的目录间进行切换。
- 给自己解释下 pushd 和 popd 命令的输出。注意下，它是如何像一个堆栈一样工作的。
- 你已经知道这些, 但请记住 mkdir -p 将会创建整个路径，即使其中的目录都不存在。这是我在这节练习中首先要做的事情。