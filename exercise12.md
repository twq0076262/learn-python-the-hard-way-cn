# exercise11.提问
丛这节开始我们要恢复之前的脚步。我已经出过很多打印相关的练习，让你习惯写简单的东西，但简单的东西都有点无聊。我们现在要做的是把数据读到你的程序里边去。这可能对你有点难度，你可能一下子不明白，不过你需要相信我，无论如何把习题做了再说。只要做几个练习你就明白了。

一般软件做的事情主要就是下面几条：

> 1.接收人的输入.
2.改变输入.
3.打印改变后的输入值

到目前为止你只做了打印字符串，但还不会接收或者修改人的输入。你也许还不知道“输入(input)”是什么意思。但是在代码中输入这个单词还是跟以前一样的，所以闲话少说，我们还是开始做点练习看你能不能明白。下一个习题里边我们会给你更多的解释。

```
print "How old are you?",
age = raw_input()
print "How tall are you?",
height = raw_input()
print "How much do you weigh?",
weight = raw_input()

print "So, you're %r old, %r tall and %r heavy." % (
    age, height, weight)
```

> **NOTE:** 注意我在每行 print 后面加了个逗号(comma) ,了吧？这样的话 print 就不会输出新行符而结束这一行跑到下一行去了。

## 你看到的结果

```
$ python ex11.py
How old are you? 38
How tall are you? 6'2"
How much do you weigh? 180lbs
So, you're '38' old, '6\'2"' tall and '180lbs' heavy.
```

## 附加题

> 1.上网查一下 Python 的 raw_input 实现的是什么功能。
2.你能找到它的别的用法吗？测试一下你上网搜索到的例子。
3.用类似的格式再写一段，把问题改成你自己的问题
4.结合转义序列，想想为什么最后一行'6\'2"' 里边有一个\' 序列。单引号需要被转义，从而防止它被识别为字符串的结尾。有没有注意到这一点？

## 常见问题

### Q:如何接收用户输入的数字，用来进行数学计算？

> 这略微复杂一些,你可以试试用 x = int(raw_input()) 将通过 raw_input()获得的字符串转化成整数。

### Q:我用 raw_input("6'2")输入我的身高值，但是它没有生效。

> 你应该在你的终端里输入，而不是把输入值写到 raw_input()的括号里。首先请检查你的代码是否和我提供的样例一样，然后执行这个脚本，当收到提示的时候，再输入你的身高。

### Q:为什么你在第 8 行代码的时候换行了，而没有让这句代码在一行上？

> 这样做的目的是让一行代码少于 80 个字符，这是一种 Python 程序员喜欢的代码风格，如果你喜欢，你也可以把它们放在一行里。

### Q:input() 和 raw_input()有什么区别?

> 在 Python 代码里 input()方法将会改变你输入的东西，但是这个方法存在安全问题，请尽量避免使用它。

### Q:什么情况下我应该在输入的字符串前面加一个 u， 比如 u'35'？

> 在 Python 中用这种方式告诉你这是一个 Unicode 编码的字符串。用%s 格式可以让你正常打印。