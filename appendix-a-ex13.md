# 附录 A-练习 13：输出文件 (cat)
你要为这节练习做更多的准备工作，你要习惯于在一个程序中创建文件，然后通过命令行访问这个文件。使用上节练习中用过的文本编辑器，新建一个叫做 test2.txt 的文件，这一次直接将他保存在你的 temp 目录中.

## 做到这些

### Linux/OSX

```
$ less test2.txt
[displays file here]
$ cat test2.txt
I am a fun guy.
Don't you know why?
Because I make poems,
that make babies cry.
$ cat test.txt
Hi there this is cool.
$
```

### Windows

```
> more test2.txt
[displays file here]
> cat test2.txt
I am a fun guy.
Don't you know why?
Because I make poems,
that make babies cry.
> cat test.txt
Hi there this is cool.
>
```

请记住，当我说 [displays file here]的时候，我只是缩写了命令的真实输出，所以我没有给你展示确切的一切。

## 你应该学到的

你喜欢我的诗吗？你已经知道第一个命令，我只是让你检查你的文件是否存在。然后你使用 cat 输出该文件到屏幕上。这个命令会将整个文件内容不分页不间断的输出到屏幕上。为了证明这一点，我需要你同样使用该命令输出 I test.txt，这个文件会输出一大堆文字。

## 更多练习

> - 创建更多的文本文件，并使用 cat 命令输出文件内容。
- Unix: 尝试命令 cat test.txt test2.txt 看看它做了什么。
- Windows: 尝试命令 cat test.txt,test2.txt 看看它做了什么。