# exercise45.你来制作一个游戏
你要开始学会自食其力了。通过阅读这本书你应该已经学到了一点，那就是你需要的所有的信息网上都有，你只要去搜索就能找到。唯一困扰你的就是如何使用正确的词汇进行搜索。学到现在，你在挑选搜索关键字方面应该已经有些感觉了。现在已经是时候了，你需要尝试写一个大的项目，并让它运行起来。

以下是你的需求：

> 1.制作一个截然不同的游戏。
2.使用多个文件，并使用 import 调用这些文件。确认自己知道 import 的用法。
3.对于每个房间使用一个 class，class 的命名要能体现出它的用处(例如 GoldRoom、KoiPondRoom)。
4.你的执行器代码应该了解这些房间，所以创建一个类来调用并且记录这些房间。有很多种方法可以达到这个目的，不过你可以考虑让每个房间返回下一个房间，或者设置一个变量，让它指定下一个房间是什么。

其他的事情就全靠你了。花一个星期完成这件任务，做一个你能做出来的最好的游戏。使用你学过的任何东西（类，函数，字典，列表……）来改进你的程序。这节课的目的是教你如何构建 class 出来，而这些 class 又能调用到其它 Python 文件中的 class。

我不会详细地告诉你告诉你怎样做，你需要自己完成。试着下手吧，编程就是解决问题的过程，这就意味着你要尝试各种可能性，进行实验，经历失败，然后丢掉你做出来的东西重头开始。当你被某个问题卡住的时候，你可以向别人寻求帮助，并把你的代码贴出来给他们看。如果有人刻薄你，别理他们，你只要集中精力在帮你的人身上就可以了。持续修改和清理你的代码，直到它完整可执行为止，然后再研究一下看它还能不能被改进。

祝你好运，下个星期你做出游戏后我们再见。

## 评估你的游戏

这节练习的目的是检查评估你的游戏。也许你只完成了一半，卡在那里没有进行下去，也许你勉强做出来了。不管怎样，我们将串一下你应该弄懂的一些东西，并确认你的游戏里有使用到它们。我们将学习如何用正确的格式构建 class，使用 class 的一些通用习惯，另外还有很多的“书本知识”让你学习。

为什么我会让你先行尝试，然后才告诉你正确的做法呢？因为从现在开始你要学会“自给自足”，以前是我牵着你前行，以后就得靠你自己了。后面的习题我只会告诉你你的任务，你需要自己去完成，在你完成后我再告诉你如何可以改进你的作业。

一开始你会觉得很困难并且很不习惯，但只要坚持下去，你就会培养出自己解决问题的能力。你还会找出创新的方法解决问题，这比从课本中拷贝解决方案强多了。

## 函数的风格

以前我教过的怎样写好函数的方法一样是适用的，不过这里要添加几条：

> - 由于各种各样的原因，程序员将 class (类)里边的函数称作 method （方法）。很大程度上这只是个市场策略（用来推销 OOP），不过如果你把它们称作“函数”的话，是会有啰嗦的人跳出来纠正你的。如果你觉得他们太烦了，你可以告诉他们从数学方面演示一下“函数”和“方法”究竟有什么不同，这样他们会很快闭嘴的。
- 在你使用 class 的过程中，很大一部分时间是告诉你的 class 如何“做事情”。给这些函数命名的时候，与其命名成一个名词，不如命名为一个动词，作为给 class 的一个命令。就和 list 的 pop (抛出)函数一样，它相当于说：“嘿，列表，把这东西给我 pop 出去。”它的名字不是 remove_from_end_of_list ，因为即使它的功能的确是这样，这一串字符也不是一个命令。
- 让你的函数保持简单小巧。由于某些原因，有些人开始学习 class 后就会忘了这一条。

## 类的风格

> - 你的 class 应该使用 “camel case（驼峰式大小写）”，例如你应该使用 SuperGoldFactory 而不是 super_gold_factory。
- 你的 __init__不应该做太多的事情，这会让 class 变得难以使用。
- 你的其它函数应该使用 “underscore format（下划线隔词）”，所以你可以写 my_awesome_hair， 而不是 myawesomehair 或者 MyAwesomeHair。
- 用一致的方式组织函数的参数。如果你的 class 需要处理 users、dogs、和 cats，就保持这个次序（特别情况除外）。如果一个函数的参数是(dog, cat, user)，另一个的是(user, cat, dog) ，这会让函数使用起来很困难。
- 不要对全局变量或者来自模组的变量进行重定义或者赋值，让这些东西自顾自就行了。
- 不要一根筋式地维持风格一致性，这是思维力底下的妖怪喽啰做的事情。一致性是好事情，不过愚蠢地跟着别人遵从一些白痴口号是错误的行为——这本身就是一种坏的风格。好好为自己着想吧。
- 永远永远都使用 class Name(object)的方式定义 class，否则你会碰到大麻烦。

## 代码风格

> - 为了以方便他人阅读，为自己的代码字符之间留下一些空白。你将会看到一些很差的程序员，他们写的代码还算通顺，但字符之间没有任何空间。这种风格在任何编程语言中都是坏习惯，人的眼睛和大脑会通过空白和垂直对齐的位置来扫描和区隔视觉元素，如果你的代码里没有任何空白，这相当于为你的代码上了迷彩装。
- 如果一段代码你无法朗读出来，那么这段代码的可读性可能就有问题。如你找不到让某个东西易用的方法，试着也朗读出来。这样不仅会逼迫你慢速而且真正仔细阅读过去，还会帮你找到难读的段落，从而知道那些代码的易读性需要作出改进。
- 学着模仿别人的风格写 Python 程序，直到哪天你找到你自己的风格为止。
- 一旦你有了自己的风格，也别把它太当回事。程序员工作的一部分就是和别人的代码打交道，有的人审美就是很差。相信我，你的审美某一方面一定也很差，只是你从未意识到而已。
- 如果你发现有人写的代码风格你很喜欢，那就模仿他们的风格。

## 好的注释

> - 有程序员会告诉你，说你的代码需要有足够的可读性，这样你就无需写注释了。他们会以自己接近官腔的声音说“所以你永远都不应该写代码注释。”这些人要么是一些顾问型的人物，如果别人无法使用他们的代码，就会付更多钱给他们让他们解决问题。要么他们能力不足，从来没有跟别人合作过。别理会这些人，好好写你的注释。
- 写注释的时候，描述清楚为什么你要这样做。代码只会告诉你“这样实现”，而不会告诉你“为什么要这样实现”，而后者比前者更重要。
- 当你为函数写文档注释的时候，记得为别的代码使用者也写些东西。你不需要狂写一大堆，但一两句话写写这个函数的用法还是很有用的。
- 最后要说的是，虽然注释是好东西，太多的注释就不见得是了。而且注释也是需要维护的，你要尽量让注释短小精悍一语中的，如果你对代码做了更改，记得检查并更新相关的注释，确认它们还是正确的。

## 为你的游戏评分

现在我要求你假装成我，板起脸来，把你的代码打印出来，然后拿一支红笔，把代码中所有的错误都标出来。你要充分利用你在本章以及前面学到的知识。等你批改完了，我要求你把所有的错误改对。这个过程我需要你多重复几次，争取找到更多的可以改进的地方。使用我前面教过的方法，把代码分解成最细小的单元一一进行分析。

这个练习的目的是训练你对于细节的关注程度。等你检查完自己的代码，再找一段别人的代码用这种方法检查一遍。把代码打印出来，检查出所有代码和风格方面的错误，然后试着在不改坏别人代码的前提下把它们修改正确、

这周我要求你的事情就是批改和纠错，包含你自己的代码和别人的代码，再没有别的了。这节习题难度还是挺大，不过一旦你完成了任务，你学过的东西就会牢牢记在脑中。