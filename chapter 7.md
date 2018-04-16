# Designing Computer Games
* Overview
* The Spec
* User Documentation
* Quality Control
* Artificial Intelligence (AI)
* The Computer Wargame Development Team
* Hardware for Computer Wargames
* Victory at Sea
* Notes on Game Components
* Hundred Years War
* Computer Wargame Design Tips for the Military Designer

# 设计电脑兵棋
* 概览
* 说明
* 用户文档
* 质量控制
* 人工智能（AI）
* 电脑兵棋开发团队
* 电脑兵棋的硬件
* 海上雄风（Victory at Sea）
* 关于游戏组件的注释
* 百年战争
* 对军事向设计者而言的电脑兵棋设计技巧

## Overview
Wargames on computer have had a mixed record. The "media" (the computer) is substantially
different than the paper and cardboard used in manual games. What works on paper does not
always work so well on the computer. The computer has capabilities that are often not exploited
in computerized wargames. Those wargames that do tend to emphasize the computers strengths
tend also to be situations like vehicle simulations. This makes sense, as a computer can handily
deal with the numerous calculations needed to simulate aircraft, ship or AFV (Armored Fighting
Vehicle, tanks and the like) activity. Manual games have a lot of problems with vehicle
simulation, so computerized vehicle simulations have done very well while their manual
counterparts languish unplayed by gamers with increasingly less time for games. 

## 概览

计算机上的兵棋上目前可以说是毁誉参半。计算机所用的“介质”，与手工游戏中所用的纸和纸板（cardboard）
有着本质的不同。在桌面上运行的很好的东西在计算机上运行的好。计算机的能力通常没有被相关的计算机化
的兵棋所充分挖掘。而那些聚焦计算机优势的则通常变成车辆模拟器那样的东西。这是有意义的，因为计算机
可以轻松解决模拟飞机，舰船和AFV（Armored Fighting Vehicle(装甲战斗车辆)，坦克之类的）所需海量计算。
手工游戏在车辆模拟上有着很多问题，所以计算机化的车辆模拟在此解决了这些问题，特别是考虑到它们的手工
对应产品正被越发少空闲时间的玩家所抛弃的情况下。

Computerized versions of non-simulator military situations is still an evolving area.
Programmers have been designing computer wargames for over twenty years. Game designers
have not been working on computer wargames for nearly as long. This has always been a major
problem with a lot of computer wargames that were (and largely still are) designed by
programmers who are often new to game design. Game design and programming are two
different skills that do have some
conceptual overlap. A lot of manual wargamers are programmers. But few programmers start out
as game designers and few who began as game designers were programmers. This has led to
most computer wargames designed by people who are better programmers than game designers.
This has produced some awful computer wargames. While the cost to the player of these
wretched games has been high (more in terms of aggravation than money), the experience has
enabled those programmers with a talent for game design to rise above the pack. Chris Crawford
and Gary Grigsby are two of the most notable of this new generation of designers. There are a
dozen or so who are nearly as good as these two (I won't name names, lest I inadvertently forget
someone who deserves to be mentioned. You know who you are, including the foreigners.) But
there are still a lot of neophyte game designers who may be great (or sometimes dreadful)
programmers turning out painfully inadequate games. 

计算机化的非模拟军事的市场情况仍然是个发展中的领域。程序员在二十年间正在不断的设计计算机兵棋。
游戏设计师在同样的时间则没怎么为计算机兵棋出力。大量的计算机兵棋曾是（很大程度上现在也是）
被对游戏设计并不了解的程序员所设计，这已经变成了一个大问题。游戏设计和编程时两种不同的技能，
尽管有一些概念的重叠。很多手工兵棋玩家是程序员。但是很少有程序员一开始是游戏设计师，且很少有
开始是游戏设计师的过去是程序员。这已经导致多数计算机兵棋是被更精通编程而不是游戏设计的人所设计的。
这已经导致了很多诡异的计算机兵棋的产生。尽管玩家既已为这些蹩脚的游戏付出了很多成本
（主要指对游戏蹩脚的恼火而不是费用），这些经验也帮助那些在游戏设计有着天赋的程序员脱颖而出。
Chris Crawford 与 Gary Grigsby 是这些新生代设计师里最值得提到的两位。有很多人和他们有着和这两位
水平接近的人（我不会列举出他们的名字，以免我没留神忘记其中一些值得提到的人。你知道你是谁，
包括外国人。）。尽管存在这些人，但依然存在大量的新手游戏设计者，他们的编程技术也许很强（有时糟透了）
，但他们还是被证明在生产恼人的，不合适的游戏。

Thus the first thing you must consider when creating a computer wargame is are you going to do
the designing and programming or only one of these chores. This is not a trivial decision. A
superb programmer many be a mediocre (or simply lackadaisical) game designer and will
produce, at best, a good looking game that has little useful play (or historical) value. A good
game designer who is an inadequate programmer won't get very far. The third solution, to have a
good game designer work with one or more good programmers usually produces good results
once the communications problems can be overcome. This team approach is becoming
increasingly common, particularly since current computer wargames are so elaborate that many
different specialists must be called in (for programming, graphics, interface, sound and
documentation) that adding a game designer to the list is no burden and is usually a decided plus.
The last solution, having a someone that combines the talents of a programmer and game
designer is rare because that combination is extraordinary. 

当你想要创造一个计算机兵棋时，首要要考虑的事情就是你将同时做设计和编程还是两者之一。
这不是一个平凡的问题。一个超级程序员也许只是一个平庸（或惰怠）的游戏设计者，然后他就会造出，
在最好的情况下，一个界面看起来很漂亮但是在游戏性和历史性上价值有限的游戏。一个好的游戏设计者，
即使他是个不那么称职的程序员，也不会跑那么偏。第三个解决方案，即有一个好的游戏设计者与一个或多个
好的程序员合作通常会得到的产品，只要沟通问题能被解决。这种团队组织方式正在变得普遍，特别是考虑到
当前的计算机兵棋变得越发复杂，使得越来越多的专家被招进服务
（对于编程来说，图像，界面，声音和文档）的情况，增加一个游戏设计师到团队来说并不是一个负担而显然是一个
增益。最后一个解决方案，有一个人兼有程序员和游戏设计师的天赋，考虑到这种兼具如此的非凡，所以十分罕见。

Before we get into the nuts and bolts of this, I ought to present my own credentials. This will put
what I say here in perspective. 

在我们开始具体细节之前，我将谈谈自己的经验，这将帮助形成对后面内容的正确认识。

I've designed five computer wargames. For three of them, I did the design, someone else did the
programming. The first one I programmed myself. It was an experiment, which was just as well.
It didn't turn out that badly, but it was far from publishable. It was called "Rus" and was
programmed in Microsoft BASIC (on a TRS80 Mod I) in 1981 so that I could get an idea what
programming computer wargames was all about. I had some background in programming,
having learned the rudiments of COBOL and RPG II in the 1970s, in addition to the primitive
language of HPs first series of programmable calculators. COBOL and RPG II were dreadful
languages and, although I had access to a minicomputer running those two languages, I did little
with my programming knowledge beyond reading 
the program listings of the programmers that worked for me. I had done several business
applications in BASIC, a language I learned in 1978. The Rus game was about the Viking
invasion of Russia in the ninth and tenth centuries. 

我已经设计了5个计算机兵棋。对于它们中的3个，我做了设计工作，其他的则做了编程工作。其中第一个是我自己编程的。
作为一个实验，它并不是那么糟，但是离可出版的水平还有差距。它被称为 “Rus” ，是用 Microsoft Basic（在
一个TRS80 Mod I 机器上）于1981年编写的，从而我能够对编写计算机兵棋是怎么回事有个概念。我在编程上
有一些背景知识——我曾经在1970年左右学过COBOL和RPG II的基本内容，还学过HP第一代可编程计算器的
原生语言（primitive language）。COBOL与RPG II 都是糟糕的语言，尽管我可以使用运行这两个语言的微型计算机，
我的编程知识止步于阅读程序员们给我写的程序清单。在我在1978年学过BASIC语言后，我已经做过一些的商业应用
使用这个种语言。Rus游戏是关于在9和10世纪维京人对俄罗斯的入侵的。

The Rus (as the Russians called the Vikings) advanced down Russian rivers, plundering and
settling as they went. So in my game you proceeded down one of the Russian rivers,
encountering (and dealing with) all sorts of situations as you went. It was a revealing experience.
I quickly learned that my game design ideas rapidly outstripped my programming skills. I was
comfortable in BASIC, and I knew what peeks and pokes could do within the operating system.
After finishing the game, I decided to leave programming to those with a knack with it. 

Rus（俄罗人对维京人的称呼）沿俄罗斯河向下，抢掠和定居它们一路经过的地方。所以在我的游戏中，你也沿其中
一条俄罗斯河向下，遭遇和处理各种你遇到的情况。编写这个游戏是我的一个揭示性的经验。我很快认识到我迸发的
游戏设计想法超越了我的编程技术。我乐于使用BASIC，也知道怎么用peek，poke（译注：BASIC语言类似C指针的命令）
与操作系统交互。在完成这个游戏后，我决定把变成工作留给那些对此有经验的人做。