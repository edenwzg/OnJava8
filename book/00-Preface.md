<div align="left">
<img src="https://raw.githubusercontent.com/LingCoder/OnJava8/master/images/level_1_title.png" alt="level_1_title" />
</div>

# 前言

本书基于Java 8版本来教授目前最惯用的Java编程形式。在此之前，我的另一本Java书籍《Thinking in Java》第4版（Java编程思想 Prentice Hall 2006）对于Java 5的编程依然有指导意义。Java 5是用于Android编程的语言版本。

随着Java 8的出现，这门语言在许多地方发生了翻天覆地的变化。新的Java代码在使用和实现上与以往不尽相同。这也是为什么时隔两年后我创作了这本新书。《On Java 8》旨在面向已具有编程基础的开发者们。对于初学者，可以先在 [Code.org](Code.org) 或者 [Khan Academy](https://www.khanacademy.org/computing/computer-programming)等网站上补充必要的前置知识。同时，[OnJava8.com](www.OnJava8.com)上也有免费的《Thinking in C》专题知识。

与几年前我们依赖印刷媒体相比，像YouTube，博客和StackOverflow这样的网站让寻找答案变得非常容易。请将这些与坚持不懈的努力相结合。你可以将本书作为你的编程入门书籍。同样她也适用于想要扩展知识的在职程序员。每次在世界各地的演讲中,我都非常感谢《Thinking in Java》这本书给我带来的所有荣誉。事实证明，这些荣誉对我现在的[Reinventing Business](http://www.reinventing-business.com)项目中和加强外界与公司的联系是非常宝贵的。最后,写这本书的原因之一是支持我[Reinventing Business](http://www.reinventing-business.com)重塑，似乎下一个合乎逻辑的步骤是实际创建一个所谓的蓝绿色组织（Teal Organization）。我希望这本书可以成为该项目的一种众筹。

![level_2_title](../images/level_2_title.png)

## 教学目标

每章教授一个或一组相关的概念，并且这些知识不依赖于尚未学习到的章节。这样以来，学习者可以在当前知识的背景框架下循序渐进地掌握JAVA。

本书的教学目标：


1. 循序渐进地呈现学习内容，以便于你在不依赖后置知识框架的情况下轻松完成现有的学习任务，同时尽量保证前面章节的内容在后面的学习中得到运用。如果确有必要引入我们还没学习到的知识概念，我会做个简短地介绍。

2. 尽可能地使用简单和简短的示例，方便读者理解。而不强求引入解决实际问题的例子。因为我发现，相比解决某个实际问题，读者更乐于看到自己真正理解了示例的每个细节。或许我会因为这些“玩具示例”而被一些人所诟病，但我更愿意看到我的读者们因此能保持饶有兴趣地学习。

3. 把我知道的以及我认为对于你学习语言很重要的东西都告诉你。我认为信息的重要性是分层次结构的。绝大多数情况下，我们没必要弄清问题的所有本质。好比编程语言中的某些特性和实现细节，95%的程序员都不需要取知道。这些细节除了会加重你的学习成本，还让你更觉得这门语言好复杂。如果你非要考虑这些细节，那么它还会迷惑该代码的阅读者/维护者，所以我主张选择简单的方法解决问题。

4. 希望本书能为你打下坚实的基础，方便你将来学习更难的课程和书籍。

![level_2_title](../images/level_2_title.png)

## 语言设计错误

每种语言都有设计错误。当新程序员必须涉足语言特性时并猜测应用场景和使用方式时，他们体验到极大的不确定性和挫折感。承认错误令人尴尬，但这种糟糕的初学者经历比认识到你错了什么还要糟糕。哎，每一种设语言/库的设计错误都会永久地嵌入在Java的发行版中。

诺贝尔经济学奖得主约瑟夫·斯蒂格利茨（Joseph Stiglitz）有一套适用于这里的人生哲学，叫做“承诺升级理论”：继续犯错误的成本由别人承担，而承认错误的成本由自己承担。

如果你有读过我过去的作品，那么你应该知道，我一般倾向于指出这些语言设计错误Java已经发展出了一批狂热的追随者。他们对待这门语言更像是阵营而不是编程工具。因为我已经写过有关Java的书，所以他们理所当然的认为我也是这个“阵营”的一份子。于是，当我指出Java的错误时，就会造成两种影响：

1. 最初，会有许多错误“阵营”的人成为了牺牲品。最终，时隔多年，大家都意识到这是个设计上的错误，然后错误就这样成为了Java历史的一部分。

2.更重要的是，新程序员并没有经历过“他们”为什么要采用这种实现方式的斗争过程。特别是那些隐隐约约感觉不对却依然说服自己“我必须要这么做”或者“我只是没学明白”从而继续错下去的人。更糟糕的是，教授这些编程知识的老师们没能深入的去研究这里是否有设计上的错误，而是继续错误的解读。通过了解语言设计上的错误，能让开发者们更好的理解和意识到错误的本质，从而更快地进步。

理解编程语言的设计错误至至关重要，甚至影响程序员的开发效率。一些公司在开发过程中会避免使用语言的某些功能特性。表面上看这些“功能特性”很高大上，但是弄不好却可能出现意料之外的错误，影响整个开发进程。

已知的语言设计错误也会给新的一门编程语言的发明提供参考意义。探索一门语言能做什么是很有趣的一件事，而语言设计错误能提醒你哪些“坑”是不能再趟的。多年以来，我一直感觉Java的设计者们有点脱离群众的。Java有些设计错误不免错的太明显，我都怀疑语言设计师们到底是为了用户服务还是出于其他的动机设计了这些功能。Java语言有许多臭名昭著的设计错误，很可能这也是诱惑所在。我感觉这是对程序员的不尊重。为此我很长时间不想于Java有任何瓜葛，很大程度上，这也是我为什么不想碰Java的原因吧。

现今当我再来看Java 8时，我发现与之前有许多不同的地方。Java语言的设计师们似乎对于语言和用户的态度发生了根本性上的改变。在多年忽视用户投诉之后，许多功能和库已经被语言搞砸了。

新功能的设计与以往有很大不同。掌舵者开始重视程序员的编程经验。新功能最终都在努力使语言变得更好，而不仅仅是停留在快速添加想法而不深入研究它们的含义。有一些新功能实现上非常优雅（至少在Java约束下尽可能优雅）。

我猜测可能是一些人离开设计组让他们意识到了这点。我没想到会有这些变化！因为这些原因吧，写这本书的体验要比以往的经历要好得多。Java 8包含了一系列基础和重要的改进。哎，不过Java有严格的“向后兼容”承诺。所以可能我们不大可能看到戏剧性的变化，当然我希望我是错的。尽管如此，我很赞赏那些敢于自我颠覆，并为Java设定更好路线的人。第一次，对于自己所写的部分Java 8代码我终于可以说“我喜欢这个！”

最后，本书所著时似乎也很不错，因为Java 8引入的新功能已经强烈的影响了今后Java的编码方式。截止我在写这本书时，Java 9似乎更专注于对语言底层的基础结构功能的重要更新，但是这些并不会影响本书所关注的编码类型。话说回来，得益于电子书出版形式的便捷，如果我发现本书有需要更新或添加的内容，我可以很快将新版本推送给现有读者。

![level_2_title](../images/level_2_title.png)

## 测试用例


