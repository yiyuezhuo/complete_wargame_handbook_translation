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

The second game I programmed was done on a dare. What brought that about was the
appearance of the 123 spreadsheet program in 1983. I had been using the earlier VisiCalc
spreadsheet to great effect since late 1980, but 123 was a supercharged VisiCalc with a macro
language. The macro language was, in essence, brain damaged BASIC. I did a lot with macros,
and still do. On a dare, I created a wargame on a spreadsheet. Actually, the first spreadsheet
wargame was done on the CP/M version of Microsoft’s MultiPlan spreadsheet. I ended up doing
versions of this wargame on SuperCalc, Symphony and Quattro. Someone else got it going on
the Excel spreadsheet program. I began giving it away in 1983 and that "wargame" played a
major role in getting the military to use spreadsheets for combat modeling. This type of computer
wargame is not slick enough to be a commercial product, but it gets a lot of real wargaming work
done. 

我编写的第二个游戏的激励来源于123电子表格（spreadsheet）程序的出现。我之前重度使用过早期的VisiCalc
电子表格，但123甚至是一个全面强化过的VisiCalc，包括一个宏语言。这个宏语言基本上是一个脑残
（brain damaged）版的BASIC。我曾经和宏经常打交道，并仍然和它们打交道。在一时的冲动下，我在
一个电子表格程序上创造了一个兵棋。实际上，第一个电子表格兵棋被实现在
Microsoft's MultiPlan 电子表格的 CP/M版上。最终我把这个版本的兵棋到SuperCalc，Symphony与Quattro上。
还有人把它移植到了Excel上。我从1983年开始赠送它，这个“兵棋”在将电子表格引入军事建模中
扮演了一种重要的角色。这种类型的电脑兵棋没有规整（slick）到可以作为商业产品，但是它使得一些实际的
兵棋工作得以完成。

My third computer wargame was more polished, and recognizable. In 1985 I was asked by an old
Army friend (Ray Macedonia, recently retired from running the Wargames Department of the
Army War College) to create a manual wargame on tactical armored warfare. He needed it for
the work he was doing with his new employer (AVCO, later part of Textron) on anti-tank
weapons. So I created the manual game in a few months. They liked it so much that AVCO
asked to have it turned into a computer wargame. They gave me a Symbolics workstation, two
programmers and a lot of money and three months later we had it up and running. Neat game,
full color graphics, AI and everything. 

我的第三个计算机兵棋更加优雅，且富有知名度。在1985年，一个陆军的老朋友（Ray Macedonia，最近从
管理陆军战学院兵棋部分（Wargames Department of the Army War College）的职位上退休）请求我
做一个战术级装甲战手工兵棋。这是他的新雇主（AVCO，之后成为Textron的一部分）在反坦克武器上
的工作上所需要的。所以我在几个月中做了一个手工兵棋。他们很喜欢它，不但如此，AVCO还请求将它
实现为计算机兵棋。他们给了我一个Symbolics工作站，两个程序员和很多经费。三个月后，我们完成了
它，这是一个完备的游戏，有着全彩的图像显示，AI和所有应有的东西。

While I had never done a computer wargame like that before, I already knew how to spec
(writing out the specifications for the programmer) out a project for programmers, as I had been
doing that since the early 1970s and through the 1980s was usually supervising one or more
teams of programmers doing financial modeling programs. In 1989 I got involved with the
GEnie computer network and ended up agreeing to design a multi-player (over 300 players)
game of the Hundred Years War. The programming was done on a mainframe computer and all
the players got together via their PC and a telephone call (through a modem). 

尽管我在之前从没有以这样的方式完成过一个电脑兵棋，但那时我已有在项目中对程序员说明要求
（写面向程序员的详细说明书）的经验，因为我在1970年代早期和整个80年代通常都在监督一个或多个
程序员团队编写金融建模程序。在1989年，GEnie电脑网络与我沟通，并决定设计一个多人在线（超过300个玩家）
的百年战争游戏。编程在一个大型计算机上进行，而所有玩家通过他们的PC和拨号上网聚合起来。

That game went into alpha testing in 1991 and went online for paying customers in 1992. In
1991 I was approached by 360 Pacific (publisher of many computer wargames, including the
best seller Harpoon) about doing a computer wargame on the naval war in the Pacific. I agreed,
and the spec was done by October, 1991 with programming to continue through 1992. 

这游戏在1991年进入alpha测试，并最终上线于1992年。在1991年，360 Pacific（很多电脑兵棋的出版商，
包括畅销的Harpoon）联系我做一个太平洋上的水面战的电脑兵棋。我同意，它的说明在1991年10月被完成，
而它的编程工作则持续了整个1992年。

It is from the above perspective that I will describe how one should go about designing a
computer wargame. Some of the material presented here is from the lectures I have been giving
to military wargame designers for the past dozen years. That will just broaden your knowledge of
designing computer wargames a bit more. 

我将依据上面谈的内容描述如何设计一个电脑兵棋。在这里出现的一些内容是从我过去十几年间
给军事兵棋设计师课程中拿来的。你将从中学到更大设计电脑兵棋知识。

Note that we are talking about designing, not programming, a computer wargame. Actually
writing the program code for a computer wargame is a whole different matter. The programming
techniques are not only very arcane (and largely understandable only by programmers) but
change substantially from year to year as computers and programming tools become more
powerful and, well, different. Designing computer wargames consists of principles and
techniques that are less subject to change. 

注意我们正在谈论如何设计而不是如何编程一个计算机兵棋。实际上编写一个计算机兵棋的代码几乎是
一件完全不同的事。编程技术不只是晦涩的（通常只能被程序员所理解），而且在随时间不断发生
巨大的改变，同时计算机和编程工具也变得更加强大与面目陌生。设计一个电脑兵棋所需的原理和技术
却并没有发生多大的变化。

##The Spec
Keep in mind that a computer does what you tell it to do not what you want it to do. Unlike
people (some people, anyway) you can't just tell a computer what you want done and expect your
request to be carried out. Computers require explicit instructions. These are called computer
programs, or computer software. The terms program and software are often used
interchangeably. 

## 说明
讲这句话记住：电脑只做你叫它去做的事，而不能做你想让它做得事。不像人（一些人，大概），
你不能只是告诉电脑你想要什么然后期待你的请求会被贯彻。电脑要求明确的指示，它们被称为
计算机程序，或者计算机软件。术语“程序”（program）和“软件”（software）经常被混用。

Programmers make their living by turning someone else’s need for a computer to do something
into a program that will make a computer do what is requested. The programmer, however,
requires precise (or at least unambiguous) directions from the user of the program. In this case
the user giving direction is the game designer. These directions are delivered in the form of a
"specification" or "spec." 

程序员所干的事基本就是将其他人让电脑做什么事的需求转化为一个可以让电脑这么做的程序。程序员，
无论如何，至少需要用户提供精确的（或至少没有歧义）对程序的描述。在这里，给出描述的用户就是
游戏设计师。这些描述以“说明”（"specification" or "spec" ）的形式给出。

Specs come in many different forms. On one extreme you have many pages of flow charts
(boxes of different shape connected by solid and dotted lines) showing which data goes where
and does what. These flow charts are accompanied by equally voluminous instructions on how to
set up data files (lists of information), what formulas to use and how the processed data should
look when it is presented to the user (on the computer screen or printer). On the other extreme
you have some verbal instructions accompanied by a few notes scribbled on a piece of paper. My
approach to a spec is somewhere in the middle, as I have found that the flow chart approach gets
ignored (at least a lot of detail gets ignored) by the programmers while the other extreme leaves
the programmer confused and inclined to invent whatever he needs and hope that it's what the
user meant. 

说明有很多形式。在一个极端，你给出大量的流程图（一些被实虚线连接的框），它们展示了数据如何流动与用于做什么。
与流程图有同样规模的还有关于如何初始化数据文件（一些信息的列表），用什么公式，被处理过的数据如何
被显示给用户（在电脑屏幕或者打印机）的指示。在另一个极端，你给出一些口头的说明，以及几张草稿纸上的
潦草注释。我个人的的说明方式介于两者之间。我注意到流程图方式经常被程序员忽略（至少是很多细节被忽略），
而另一个方式中，程序员被含糊的指示所迷惑和带偏，只得搞出他自认为适合用户的东西。

Naturally, I'm going to push my own personal version of what I think a spec should be, if only
because it's a system I have used successfully for many years with dozens of different
programmers. I count my approach a success because most of the programs worked well and
most of the programmers are either still working for me or at least return my phone calls. What
we are describing here is a spec for a computer wargame, any computer wargame.

自然地，我将会论述我个人认为的说明应当有的样子，
只不过因为这是一套我在那么多年间与很多程序员成功合作的系统。
我觉得这个方法还是成功的，因为那些程序仍然运行的很好，而参与的程序员要么还在为我工作，
要么至少会接我打的电话。我们在这里将描述的说明可以用于所有计算机兵棋。

The spec is divided into three parts. 

说明被分为三个部分。

### Input/Output

### 输入/输出

