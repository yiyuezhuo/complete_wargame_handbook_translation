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

First comes the I/O (input/output). In plain English, this means what the user sees on the screen
(output) and what commands the user can give to the program to obtain a desired result (input).
This is often called the "look and feel" of a program. The easiest way to prepare this is to do a
mock up on the computer screen. These days, one of the many "paint" programs are used to,
literally, draw ("paint") the various proposed screens. Some years ago I used a program called
Demo (clever name, eh?) to build screens. The advantage the Demo program had was that you
could make the controls on the screen active, to bring up additional screens and similar things. I 
stopped using Demo when I realized that for my purposes (my programmers didn't need THAT
much direction), a much simpler method would suffice. So I just typed up what the input and
output screens would look like. Games use more complex screens, often with lifelike terrain,
vehicles or people on them. These don't have to be shown realistically, a simple notation will do.
The important thing is to let the programmer know what will generally go where on the screen. 

首先让我们讨论 I/O (input/output(输入/输出))。简单的来说，这意味着用户在屏幕上看到的东西（输出）
与用户为获取想要的结果给程序的指令（输入）。这经常被称为程序的“界面外观”。规划它的最简单的方法
就是在电脑屏幕上笔画。最近，有很多绘图程序被用来画出所想要的界面。几年前我用过一个叫做Demo
（不是一个很聪明的名字吗？）的程序来构建界面。Demo程序的主要好处在于你可以控制窗口活动，以构造
更丰富的界面和类似的东西。当我意识到我的程序员其实并不需要那么细致的指导时，我停止了使用Demo并
转而使用更简单的方法——我只是在电脑打出界面看起来应该是什么样子的描述。游戏使用更复杂的界面，
通常有着栩栩如生的地形，车辆和人。它们不是必须以现实主义的风格显示出来，一个简单的符号也行。
重要的事是让我们的程序员知道在屏幕上的什么东西将会到什么地方去。

When you think about it (it's a good idea to think while specing a program), there are not that
many screens involved in most games. There might be a lot of different graphics put on the
screen, but this is just popping a new picture on to the same screen. Yes, that's one of the secrets
of computer wargame design, move and vary a small number of items to make it look like a
whole lot. Just like real life. 

当你考虑I/O的时候，你必须意识到在大多数兵棋中并不需要看上去需要的那么多数量的界面。
大多数界面都是由一个界面为基础加上一些图像生成的。使得，这是计算机兵棋设计的一个奥秘，
移动和变化类型数量很有限的东西让它看起来很多样，就像现实生活一样。

## Databases

## 数据库

The foundation of any automated model are its databases. There are several database types which
must be used in a computer wargame. Their use is similar to the use of this data in a manual
wargame. 

大多数自动化模型的最基础部分是它的数据库。电脑兵棋中有很多必须的数据库类型。它们的使用类似于
手动兵棋中对这些数据的使用：

* Terrain- The terrain database can safely follow the conventions used in the manual
model, even to the extent of using the same cell structure and terrain information used in
each cell. There is rarely any justification for the extreme detail found in many digitized
terrain systems.
* Order of Battle- List of units to be used in the model and the capabilities they need for
interaction with the other elements of the model. Unlike a manual wargame, you can
safely use a lot more data because the computer has a lot of capacity to crunch numbers
without even breathing hard.
* Attrition Tables- What happens to weapons and targets when weapons are used. This is
the combat results tables (CRTs). Computer games can use more complex and multiple
CRTs.
* Terrain Effects Tables- Effects of terrain on units. Effects can be more complex and
detailed than in manual games.
* Victory Conditions Tables- Goals of units or groups of units.
* Supply Tables- Supply holdings and consumption for various units.
* Doctrine (AI) Tables- Artificial Intelligence Capability. Rules for unit behavior. SOP's
for combat and movement. Tables for command control and panic for various units.
Leadership behavior, etc.
* Other items- Any other items that the user feels are needed for the model.
* Scenario Tables- Specify which of the above items are to be combined into a particular
battle situation. Preferably kept in a library (on the computers hard disk) that the user has
easy access to with an editor and report generator. 

* 地形- 地形数据库完全可以按照手工兵棋的传统来写，
甚至维持使用相同的格子结构和相同地形对这些格子的效果。并没有什么理由给地形系统引入过多的细节。
* 战斗序列（OOB）-模型中将用到的单位的列表，应当写出它们的与模型中其他要素交互的方式。
并不像手工兵棋，你可以放心的使用更多的数据因为电脑很容易处理海量数据而不至其使人面对这些数据一样头痛。
* 损耗表-当装备使用时，装备和攻击目标将发生什么。这主要是战斗结果表（CRT），
电脑兵棋使用更复杂和更多的战斗结果表相比于手工兵棋。
* 地形效果表-地形对单位的效果。地形可以比在手工兵棋的更复杂和富有细节。
* 胜利条件表-控制单位所要达成的目标。
* 补给表-各种单位所持有和消耗的补给量。
* 教条（Doctrine）(AI)表-人工智能功能。单位行为规则。关于移动和战斗的标准操作程序（SOP）。
描述命令控制和各种单位恐慌的表格。指挥行为等。
* 其他东西-任何用户觉得对于模型需要的东西。
* 剧本表-将上面的东西与所要表示的战斗局势所粘合起来。最后在用户容易找到的地方放上剧本编辑器和
战斗报告生成器。

## Internal Model Procedures

## 内部模型过程

Otherwise known as algorithms in computerspeak. The manual model does not translate directly
to an automated version. Some adjustments and design modifications must be used. 

* Positioning on terrain- Generally use x,y coordinates system. This is easier to
implement on a computer and will give you roughly the same accuracy as the hex based
manual models.


不同于计算机语境下的算法，手工模型不能直接被转化为自动化版本。一些修改和设计上的修改是必须的。

* 区域定位方式-通常使用x,y坐标系。这个在计算机上容易实现，且拥有与手工模型的六角格系统类似的精确性。



* Combat activity- Follow a sequence of play very similar to that used in the manual
model. Higher speed and automatic operation of a computerized wargame combine to
give appearance of simultaneous activity. Operations generally take place in alternating
fractions of a second (for each phase in the sequence of play). 

1. Detect- Use sensors to determine if enemy forces are present and/or within range of
weapons.

2. Check for Damage- Can be enemy caused or from operational causes. If Damaged,
Physical Effects- Degradation of system performance. Psychological Effects- Modify
troops will to continue operations.

3. Fire or Flee- System analyzes situation. If logic, or psychological effects, dictate, system
withdraws from combat. Otherwise, continue.

4. Record actions in "Diary" Database for report generation.

5. Repeat Above- Continue until end of time period allotted for operations, or victory
conditions specify ending operations. 

* 战斗操作- 遵循一个与手工模型中十分类似的顺序操作过程，
但由于计算机的操作速度很快所以使得它像是同时完成的一样。每个阶段的操作通常使用一秒的几分之一。

1. 侦查- 使用传感器判定是否敌方出现，以及是否在武器射程中。

2. 检查损伤-可以是被敌人造成的或者操作造成的。如果损伤了，物理效果- 系统效能的下降。
精神损伤- 影响单位继续战斗的意愿。

3. 射击或逃跑- 系统分析战况。 单位将会撤退，如果被命令/受到精神打击或自行判断应当撤退。
否则将继续战斗。

4. 记录各种行动到 “日志”数据库中以便之后生成报告。

5. 报告上面的内容- 循环执行上面的过程直到结束时间或者胜利条件被满足。

* Victory calculation- Done continuously and with great accuracy, although user may
want to see probability of victory at certain points in the run.
* Scenario Deployment- Much more rapid than in the manual model. A good user
interface allows the player to rapidly explore many aspects of the game with great ease of
use and accuracy.
* Scenario Generation- Using an electronic library of scenario building blocks (maps, unit
organizations, doctrinal SOP's, etc.) the user can quickly build new scenarios or edit
existing ones. The edit function also allows building blocks to be created or edited.

* 胜利情况结算- 被连续而精确的结算，尽管用户可能想要看到在推演过程的特定时间点的胜利概率。

* 剧本布置- 计算机布置的比手工游戏快得多。一个好的用户接口使得用户可以
快速简单地探索游戏的各个层面。

* 剧本生成- 通过使用事先定义的剧本积木（地图，单位结构，AI等），用户可以快速的构建剧本或
修改剧本。同时积木本身也应该可以被穿件和修改。

* User Reports- These can also be edited as to format by the user. The principle items a
user would generally require would be,

1. OB Status- Starting and finishing status of units.

2. Terrain View- Which terrain configuration was used (Large/small scale via zoom.

3. Victory Status-What the player is allowed to know, given intelligence constraints and
other factors, about how close either side is to victory.

4. I/O Routines- How to handle interaction between model and user. The user must be able
to easily modify the following program instructions. This is done by setting up the
routines in table format and programmed to prevent the user from doing anything that
would crash the system. If the user does anything unintentionally silly, the system will
simply display these actions on the screen, allowing changes to be made and their results
observed until the user is satisfied.

* 用户报告- 它们也能被用户编辑和格式化。一个报告通常应有以下元素：

1. OB状态- 单位的初始和末尾的状态。

2. 地形视图- 使用了大比例尺还是小比例尺的地图放缩比。

3. 胜利状况- 在玩家所被允许知道的信息内，告之玩家接近胜利的程度。

4. I/O 程序- 如何处理模型和用户之间的交互。用户必须能控制程序接下来的走向。
我们应当用限制玩家去做破坏系统的事情。如果玩家做出预期之外的行为，系统将把他做得事展示出来，
让他可以改变他的行为并显示结果直到玩家满意。

5. Movement-A combination of, historical movement capabilities, based on field tests and
experience. SOP's (Standard Operating Procedure) for movement, right out of the book.
Limiting factors, primarily psychological factors that don't make it into the field manuals
or peace time soldiers knowledge.

6. Combat- Similar to movement. In this case applies to the servicing of weapons.

7. Intelligence- How much information of their own and enemy force

8. does each side have at start and during each intelligence cycle time period. This time
period is based on how long it historically took for new information to reach the
commander and be acted upon.

9. Other- As needed. 

5. 移动- 包含根据现场测试和经验得到的历史移动能力，移动的标准操作程序（right out of the book?本书内容外？）
限制因素，例如精神因素之类的不在战场手册或不为和平时期的战士所知的东西。

6. 战斗- 类似于移动。包含装备维修内容。

7. 智能- 知道多少关于它们自己和敌方的信息。

8. 在每个智能循环时间期报告相关信息。这个时间长度决定于在历史上新消息到达指挥官以及做出反应所要消耗的时间。

9. 其他所需要的。

## User Documentation
The Players Manual- The instructions for actually playing the game should be imbedded within
the game via a "help" system. Printed instructions should do little more than list which keys do
what or give an overview of the menu system. Help should be context sensitive (when you
invoke help, it first brings up a help screen relevant to where the player is in the game.)

## 用户文档

玩家手册- 玩这个游戏的指导应该被内嵌仅游戏的“帮助”系统中。指导的打印版应当不做超过列举哪些按键可以做什么
以及给出菜单的概览外的事。帮助应该是上下文敏感的（当你启动帮助，
它应该打开一个与玩家在游戏中的状态相关的帮助窗口）

Hypertext Historical System- It's increasingly popular to have a context sensitive historical
manual built into the system. When invoked, the system brings up historical data relevant to
where the player is in the game. The "hypertext" refers to a system whereby key words on the
screen are highlighted to serve as a command (when the cursor is placed over them and
activated) to pop up another screen relevant to that key word. 

超文本历史系统- 设置一个上下文敏感的内建历史手册是一个日益流行的做法。当启动时，系统显示一个历史数据
，其与玩家正在游戏的地方有关。“超文本”意指一个这样的系统——一些关键字被高亮，以表示其是一个命令（
当鼠标放到上面的并点击的时候），其可以打开另一个与这个关键字相关联的窗口。

## Quality Control

Testing- Keystroke emulators are useful to automatically run the system through an extensive
suite of hypothetical user operations. Some of these test programs will also capture the screens
and other results to a file where this test data will be compared to what should have happened
and flag error conditions.

Double Team- A system I often use, which is expensive, is to have two teams of programmers
overlapping (and even duplicating) each other on a project. This greatly reduces the chances of
the project being late, or sloppy. I doubt if game publishers can ever afford this, but I thought it
worth mention. It works.

Compile the Source Yourself- Learn to use a code analyzer, etc. This is a programmer function,
but if you are overseeing a project, it's a good way to keep on top of things. You can make
changes to data in the program (to correct something) recompile and see if that fixes it. Only
programmers should change code and sometimes even changing data will cause a program to
fail. 

## 质量控制

测试- 用按键模拟器去模拟假定的用户的按键操作是操作的。有些这种测试程序还能记录屏幕状态和其他数据
到一个文件中，然后这份测试数据可以与它被期望的样子所比较以发现错误。

两个团队- 我经常使用的一个昂贵的系统，那就是我有两队做几乎相同事情的程序员。这极大地减少了
项目被延误，程序员偷懒的现象。我怀疑游戏出版商是否能够负担的了这个成本。但是我想它值得被提到，
因为它是有用的。

自己编译源代码- 学习使用代码分析器之类的东西。这是一个程序员的工具，但是如果你正在监督一个项目，
你可以通过这个方法在顶层进行操作。你可以对程序的数据进行修改（以调整某些东西），重新编译它
并且看看这是否解决了问题。而只有程序员应当修改代码，甚至有时修改数据都会导致程序无法运行。

## Artificial Intelligence (AI)

These are the routines that enable the computer to operate as a worthy opponent for a human
player. These AI routines are not as complicated as they might appear.

AI routines need not take up a lot of space in the program. It is possible to get powerful AI
routines into as little as 2,000 bytes ("characters," or "2K" in computerspeak).

Doctrine is what drives AI, doctrine is the standard procedures that armed forces use when in
combat. Every armed force has a doctrine. Some doctrines are more efficient than others, but
that's something you have to dig up in your research.

## 人工智能（AI）

有一些方法可以让电脑成为可以与人类玩家匹敌的对手。这些方法并不一定十分复杂。

AI不需要占用程序的许多空间。以少于2kb的方式就可以得到一个强大的AI。

教条式驱动AI的东西，教条式一些武装单位在战斗中使用的东西，每个武装单位都有一个教条。一些
教条比其他的更有效，但是这是你必须在研究中去发现的东西。

There's also the problems of "Theory versus Practice" in doctrine. What the doctrine says is not
always what the troops do. You have to do more research to find out how the troops deviated
from their doctrine, to what extent and how often. 

For the commander, combat is a rather simple process: at least as far as decision making goes.
There is often imperfect information. That is, the commander is often not sure of the status of his
own troops and is even less well informed about the enemy. Thus the commander usually makes
simple decisions. To mix things up and keep the human player on his toes, you should also use a
random selection from two or more possible moves by the AI led side.

Where AI becomes complex is when you have AI measure its sides situation against the human
players. This routine is driven by the victory conditions. The measurement is a combination of
the combat strength of friendly and enemy units, the "value" of their current position and the
"value" of enemy positions. Normally, the AI would select the highest value enemy positions to
go after, but not always. By randomly selecting one of the most valuable enemy positions, the AI
player gives the human player the impression that some real thought is going on. If nothing else,
it makes the AI side unpredictable, and thus dangerous.

Creating the AI routines is a game in itself. You'll simply have to practice. It's not so hard. I did
many successful manual AI systems (for paper wargames) before I did my first computerized
systems. With the experience gained on the paper games, I had no trouble at all with the
computerized AI. Your mileage may differ 

教条也有一些“理论与实践”的矛盾。教条所所说的并不是军队所做的。你必须做更多的研究去搞明白
军队如何脱离教条，什么程度以及如何频繁。

对于指挥官，战斗倒是一个简单的过程：直到要做决定时。信息经常是不完全的，指挥官经常不确切知道他自己的
部队的状态，且更不清楚敌方的状态。故而指挥官通常做出愚蠢的决定。为了让人类玩家感觉自己在与人类对战，
你应当让AI在控制他的军队时在可能的几个行动中的决定中也引入随机要素。

当AI要估计它面对人类玩家的局面优劣状况时情况变得复杂起来。这个估计围绕胜利条件进行，
包括计算敌我双方单位的强度和它们所占据位置的“价值”。一般来说，AI会选择最高价值的敌方位置进攻，
但并不总是如此。通过随机选择一些最有价值的敌方目标，AI玩家会给人类玩家一种它的确在思考的感觉。
如果不是这样的话，AI会产生不可预料的行为，这不是人类玩家想要的。

设计一个AI本身就是一个游戏。你必须实践，这并不是很难。我做过很多成功的手工（桌面）兵棋系统的AI
在我做我的第一个计算机化AI之前。在有了从桌面游戏的经验后，做电脑AI毫无压力。你也不会差到哪里去。

##The Computer Wargame Development Team
First, there's the designer. Actually, before the designer there's the publisher, who has to agree to
put up the money and distribute the final product. The publisher generally gets no respect and
less recognition. While I've designed over a hundred games, I've published nearly four hundred.
Designing is generally fun, publishing is customarily hard. That said, once the designer has
delivered a spec that makes some kind of sense to the programmer, the programmer has to turn it
into a computer program, the software, the game you can play.

In my experience, it is best to use one programmer, plus support staff. The more programmers
are used the more programmer time is wasted in programmers keeping tabs on each other.
Modular programming is not practical as with this approach much of the system design is done
during code development. Programmer must be diligent, willing to work 6-7 days a week, leap
tall buildings at a single bound, etc. 

## 计算机兵棋开发团队

首先，有一个设计师。当然在设计师前更有出版商，其同意付钱和出版最终产品。出版商通常不会得到什么
尊重和知名度。我本人设计了100多个游戏的同时，还出版了将近400个。设计通常是快乐的，出版则通常是
困难的。一旦设计师写出一个说明给程序员，程序员则将其转化为一个电脑程序，即你玩的那个游戏。

在我的经验中，使用一个程序员加一个支持人员是坠吼的。越多的程序员被使用，则越多的程序员时间被浪费
在维持彼此的沟通上。模块化编程并不像这个方法一样具有实践意义，大多数设计设计是在代码实际开发过程中
被确定的。程序员必须勤奋，有一周工作6-7周的意愿，能够克服困难等。

### Support Staff
* Designer- Whoever designed the manual game, or drew up the spec without a full blown
manual game. The designers job is to insure that the programmer doesn't get lost while
implementing the spec. It's best that the designer be kept in the process as the
programming goes forward. There's always the chance that the programmer may try to
turn the game into his design (either on purpose or by accident), a development that
rarely works out very well.

* Development System Experts- To help programmer with quick solutions to technical
programming problems. These people give advice when asked, they don't write code. In
the Hundred Years War game this consisted of the folks who ran the GEnie mainframe
computers and the world wide communications system over which players would connect
with each other as they played the game. In Victory at Sea, the lead expert was Gordon
Walton, who led the earlier Harpoon project for the publisher, had designed and
programmed some wargames himself, and could solve a lot of problems by simply
pointing where they were and what the easiest solution was.

### 支持人员

* 设计师- 可以是设计手工游戏的，也可以是没有完整的手工游戏下编写说明的人。设计师的职责是
保证程序员不会在实现说明的过程中迷失方向。设计师应当在编程工作推进时紧跟进度。由于总是有可能
程序员会尝试将游戏转变为他的设计思路（不管是有意还是无意的），当这发生时，基本不会做出好产品。

* 系统开发专家- 给予程序员编程技术问题上的快速解答。这些人在被咨询时做出答复，但他们自己不写代码。
在百年战争中，这些人包括运行GEnie大型机和玩家互相通信用的联网系统的工作人员。在海上雄风中，
首席专家是Gordon Walton,他曾领导之前的Harpoon项目，他为自己设计和编程了很多兵棋，也可以轻松点出
问题所在和解决方法。

* Chief Testing User- Keeps everyone honest by testing system every step of the way.
Does nothing but test and make a general pest of himself. Sometimes the designer takes
on this task, sometimes it's someone working out of the publishers offices. Generally, this
person is in charge of testing and keeps track of bugs as they appear and checks to see
that they were taken care of. A currently popular title for this job is "Quality Control
Manager." Sounds better than "Chief Pest."

* Researcher- Digs up additional operational data not already present, but often implicit,
in the manual model. The computer wargame can handle more detail and it is often useful
for it to do so. In both Hundred Years War and Victory at Sea, Al Nofi was the principal
researcher. 

* Programmer Assistant- Handles routine tasks for programmer (common data entry
tasks, system maintenance, order the pizza and jolt cola, do the paperwork, etc.).

* 首席测试用户（Chief Testing User）- 通过测试系统的每个步骤确保每个人尽忠职守。
他专职测试和让自己变成团队里的讨厌鬼。有时设计师自己做这个工作，有时这个人来自出版商。
一般来说，这个人负责测试，追踪BUG并检查它们是否被妥善的解决。当前对这个职务的一个流行的称谓是
“质量控制经理”，这听上去比“首席讨厌鬼”（Chief Pest）强。

* 研究者- 挖掘在手工模型没有显示出现，但是隐含的数据。电脑兵棋可以处理更多的细节，从而利用上这些数据
是有用的。在百年战争和海上雄风中，Al Nofi 是首席研究者。

* 程序员助理- 处理程序员的日常事务（普通数据录入，系统维护，订购披萨和摇晃可乐，做文书工作等）。


*  Project Manager/Expediter- Keeps management at bay, solves project related problems
quickly. Hand holder, ass kicker, cheerleader, etc. This is usually a management
representative who reports directly to the publisher. Often has to yell at and argue with
publisher also. For some reason, I like this particular job.

In the commercial computer wargames industry it is currently fashionable to use job titles
borrowed from the movie business. Most of these companies are in California, although largely
northern California. Lifestyle envy? Anyway, the head of a computer game project is the
"producer," the chief programmer is the "director." I have not confirmed this, but the sound
specialists may now be called "Foley editor." Given that all the "actors" are electronic, where
does that leave the casting couch?

* 项目经理/稽查人- 确保管理正确的执行，快速解决项目相关问题。项目的协商者，督促者，鼓励者等。
他通常是直接向出版商汇报的管理代表。但也经常与出版商争论。由于某些原因，我喜欢这个工作。

在商业电脑兵棋工业，现在有一个时尚，即借用电影产业的术语。大多数公司都在加利福尼亚，尽管大多数在
北加利福尼亚。这是一种对其生活方式的向往吗？无论如何，电脑游戏项目的头头被称为“制片人”（producer），
而首席程序员被称为“导演”（director），我没有去验证这一点，但似乎音效专家被称作“Foley editor”(音效师)
考虑到所有的“演员”都是电子的，“潜规则”（casting couch）该到哪里进行？

