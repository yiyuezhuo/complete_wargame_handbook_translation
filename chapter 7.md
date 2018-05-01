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

# 设计电脑游戏
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
考虑到所有的“演员”都是电子的，该怎么实施“潜规则”（casting couch）？
 
## Appropriate, and Other, Hardware for Computer Wargames

* IBM PC (and clones). First introduced in 1981, this machine does not have the best
combination of features, but it can do the job. Uses the Intel 16 bit 8088 or 8086
processor. Wide array of add-on components make the IBM PC series the most flexible
machine available. Widely available, there are over sixty million installed world wide.
Standard machine in most organizations. Widest selection of software. Most major new
software first comes out in an IBM PC version. Large number of different games. The
original (1981) IBM PC had twice the throughput of older 8 bit machines (Apple, CP/M,
Commodore 64, etc.) Now considered a low end machine. Can be boosted much higher
with add-ons. About half the PCs in the world are of this type. I still have a 1983 Compaq
(a portable clone of the original IBM PC) which I keep as a spare. I've added a hard disk
and a high density disk drive. Nine years old and still going. Gets turned on four or five
times a year and still works. 

## 开发计算机兵棋的适用和不适用的硬件

* IBM PC（与仿制机）。在1981年发布，这个机器没有提供最佳的功能，但倒也能用来干活。
它使用Intel 16 bit 8088或8086处理器。大量的附加组件使得IBM PC系列得以成为使用最灵活的机器。
它使用广泛，在全世界上已有高达六千万台。它是大多数公司和组织的标准机器，也是软件的目标市场，
主流软件首先会发布IBM PC版，其中包括大量的游戏。原版（1981）IBM 速度两倍于
老式八位机（Apple，CP/M，Commodore 64等）。这些现在被认为是低端机器的东西仍然可以被附加组件所
加速。世界上近半数量的PC都属于此类。我现在仍有一台1983的Compaq（一种原版IBM PC的便携仿制机）
作为备用机。我自己给它加上一个一个硬盘和一个高密度磁盘驱动器（high density disk drive）。
过了九年时间仍然可以运行，事实上它一年会被开四到五次。

* IBM AT type- Introduced in 1984. Also known as the ISA (Industry Standard
Architecture) type. Three to ten times the throughput of the original PC. Can be boosted
even higher with add-ons. Based on the Intel 16 bit 80286 microprocessor. In 1991, the
baseline machine for many new computer wargames.
* 386 machines- Introduced in 1986. Fifteen to thirty times the speed of an original PC.
Based on the Intel i386 32 bit microprocessor. Standard machine of the early 1990s.
* 486 machines- Introduced in 1989. Thirty to seventy times the speed of an original PC.
Based on the Intel i486 32 bit microprocessor. Standard machine of the mid 1990s.
* 586 machines- Introduced in 1993. Sixty to over a hundred times the speed of an original
PC. Plus this machine will have much more powerful video capabilities, enabling it to
create movies ("full action video") on the computer screen. Based on the Intel i586 32 bit
microprocessor. Standard machine of the mid to late 1990s.
* The Clones-Offer same capabilities as IBM models at lower prices. Some clone models
also out perform IBM machines at lower price. Compaq was the first major clone, in
1983. Others followed, pushing prices lower and performance higher each year. Major
clone maker PCs considered as reliable (if not more so) than IBM. 

* IBM AT型- 1984年发布。也被称为ISA（Industry Standard Architecture，工业标准结构）。
 比原版PC快三到五倍。并可以被附加组件加速的更快。基于Intel 16位80286微处理器。是
 在1991年的大多数新电脑兵棋的基准配置。
* 386机- 1986年发布。比原版PC快十五到三十倍。基于Intel i386 32位微处理器。在90年代早期的标准机器。
* 486机- 1989年发布。比原版PC快三十到七十倍。是90年代中期的标准机器。
* 586机- 1993年发布。比原版PC快60到100倍。而且这个机子有更强的图形能力，从而可以进行过场
的实时演算。基于Intel i586 32位微处理器，是90年代中后期的标准机器。
* 仿制机提供了比IBM的型号相差无几的性能，同时价格更低。1983年的Compad是第一个流行的仿制机。
这些仿制机在竞争中拉低了价格，提高了性能。大型的仿制机厂商所生产的PC被认为比IBM生产的还可靠。

* Macintosh- The Mac II series is equal to the 386 and high end AT machines, but costs a
third more. Graphics about the same as IBM EGA and VGA modes. Original MAC and
MAC SE a cut above XT in speed, but more expensive and not numerous enough to
support widely distributed software. Later Mac models matched Intel microprocessor
machines (IBM and clones). Many games running on IBM machines are not available for
the MAC.
* Low Cost Machines- Apple II and Commodore 64/128 have limited power, but still
widely available. No longer any new games for Apple II, some for the Commodore.
Amiga- Excellent hardware capabilities, but not a major factor in the US market (most
sales are in Europe). Good selection of software, but increasingly distant third after the 
IBM and Mac. Atari ST- Similar to the Amiga, but not as technically advanced. Also sold
widely in Europe, but less and less in the US. The ST may survive not survive long in the
US market. 

Life at the Front

To give you some more insight on how computer wargames are designed, I include here some
material on the two computer wargames I was working on as this book was being written. 

* Macintosh- Mac II 系列可等同于386和更高的AT机器，但要贵三分之一。图形能力类似于IBM EGA和VGA模式。
原版MAC和MAC SE在速度上远高于XT，但更昂贵，且不支持很多流行的软件。后来的Mac与Intel微处理器机器
（IBM与仿制机）兼容（match）。很多运行在IBM机上的游戏不能运行在MAC上。
* 低价机- Apple II与 Commodore 64/128性能较差，但仍然广泛存在。不再有新的游戏面向Apple II，而有
一小部分面向Commodore。Amiga- 有着很好的硬件，但是其在美国市场并不是主要部分（其多数销售在欧洲），
在软件上有很多选项，但是在IBM和MAC后位居第三。Atari ST-类似于Amiga，但是技术上比其落后。
同样在欧洲上销售很多，但在美国却卖的很差。ST也许不能在美国市场生存多久了。

实战经验

为了给你一些电脑兵棋是怎么被设计的一些直觉，我将我参与的两个电脑兵棋的材料放进这了。

## Victory at Sea
This is a game on naval warfare in the Pacific during World War II. In effect, it's a strategic
game of the entire war in the Pacific with the option to drop down at any time and fight it out
ship to ship (or, more likely, aircraft to ship). It's the first of a series of games. Additional disks
will be published later to cover other theaters of the World War II naval war.

Below is an extract from the introduction to the Victory at Sea spec, delivered on October 15th,
1991. 

## 海上雄风
这是个关于二战太平洋海战的游戏。在这个游戏中，你可以在整场太平洋战争的任何时点进入打海空战。
这是这个系列的第一个游戏，增补内容将在之后出版以覆盖二战的其他海战情况。

下面是从海上雄风说明的介绍部分选出的一部分内容，其在1991年10月15日写成。

### Notes on Game Components

####The Map Displays

At the moment you have a list of ports and instructions to scan any Pacific region map into your
paint program. Then implement latitude and longitude coordinates to overlay the posts list onto
this map. Because a degree of longitude varies as the cosine of latitude, the length of a degree of
latitude varies from 69 miles at the equator to zero at the poles. We don't go quite that far, but do
reach two thirds of the way to the north pole (60 degrees north), meaning the degree of latitude
in under 50 miles that far up. The map will have to be adjusted. That should be no problem as
you will have the 140 principal location listed in terms of latitude and longitude. We can supply
more as needed, although we don't want to crowd the map. We counted over 500 atolls and
islands capable of supporting some kind of garrison (many at great expense in shipping, as even
water would have to be brought in to some of the drier ones). Some of these were actually
garrisoned by the Japanese (Tarawa). Once you have the map sorted out electronically, send it to
me and we'll indicate the "atoll clusters." I thought it better to leave that complication for last. It
will make some programmers life easier. 

### 关于游戏要素的注释

#### 地图显示

当前，你有一个港口的列表，以及一些关于如何把太平洋区域扫描进你的绘图程序部分的指导文件。
接下来你应该实现纬度坐标系以将港口映射到地图上。纬线的一度经度长度随着纬度的余弦而变化，如从
赤道的69英里到南北极的0英里。我们的地图并不会覆盖到极点，但是会覆盖北半球的三分之二（到北纬60度处），
这意味着在那里的一度长度将小于50英里(meaning the degree of latitude in under 50 miles that far up).。地图必须被修正。
你将要把140个以经纬度表示的地点布置在地图上，如果有必要还会有更多，尽管我们并不像地图显得太拥挤。
我们还统计了500个珊瑚岛（atolls），它们能够放置一些守备队（其中大多数在运输上都很昂贵，
甚至水都要专门运输上去）。它们中一些被日军（Tarawa）守备。一旦你电子化地图完成，请把它发给我，
我们将标出“珊瑚岛群”（atoll clusters）。我觉得把这种麻烦事放到最后再做最好。
这可以减轻程序员的工作量。

###Interface

The interface Gordon and I worked out was earlier keyed to routines in the game. This has to be
updated and I will do this in the next week. There's more than enough stuff for each existing
screen mockup.

### 接口

Gordon和我设计的接口在之前已经被写入了游戏。我将在下一周更新它。目前关于界面原型的资料已经足够了。


### Databases
The databases are complete, although we'll update them right down to the wire as we uncover
new stuff. Nothing radical, but there's always something. As all the databases are in spreadsheet
files, we can put them in any form you want for uploading into the source. I do that a lot. I don't
like it, but I've gotten pretty good at it. 

### 数据库
数据库已经做完了，尽管如果我们想要挖掘新的东西的话会立即更新它。总会有些虽不十分重要，但可以加进去的东西。
所有的数据库是以电子表格的方式存储，我们可以将它们转换成任何适合显示到屏幕上的形式。我经常做这个，
尽管我并不喜欢，但是我的确十分擅长此道。

### Algorithms
Over 95% of the needed algorithms are done. Some of the key ones have been tested and proofed
using a monte carlo system I've developed. However, it requires a bit of coding and screwing
around to get them into a format where the monte carlo testing will work. You know what monte
carlo is? If not, it's a model that tests an algorithm or, more often in my case, a series of
algorithms over thousands of iterations and gives a reliable picture of what the system will do
over many iterations. My system produces graphs as well as summary stats. I can then go back
and tweak it until I get it to do what needs to be done. I will continue to test the game algorithms
this way until they are cast in code, at which time we should monte carlo them again. The naval
surface combat routines have gone through over 6,000 iterations like that. But many of the
routines will not be fully testable until they are in code. The systems are set up so that I have a
lot of numbers I can change to bring the system into the proper balance. Once you start writing
code, give me initial executables with as much data in external tables so that I can tweak. I can
use a hex editor to change ASCII data in a binary executable or overlay. Changing binary
directly is a bitch. Could also use some monte carlo modeling capability, mainly the ability to
have x number of iterations of a situations with both sides on AI and loss stats sent to an ASCII
file in tabular format for analysis. 

### 算法
超过95%的算法已经被完成了。其中那些关键的部分已经被测试并以我开发的蒙特卡洛程序验证了其正确性。
运行这些蒙特卡洛检验需要写一些代码将一些东西转换成恰当的格式。你知道蒙特卡洛是什么吗？
如果不知道，在我经常处于的情况中，它是一个模型，其可以检验以数千次迭代来检验算法，并显出
系统在这些迭代中工作状态。看到这些反馈后我可以再去调整数据直到达到我想要的效果。
我将继续以这个方式调试游戏算法直到它们被编码为止，在那之前我们也需要最后蒙特卡洛验证一次。
海战模块已经被以这样的方式迭代了6000次。但是大多数弄快并不能被这些测试直到它们被编码完成。
我这有很多可以调整的参数，这些参数会被调成使得游戏处于恰当的平衡状态。一旦你开始编码，
给我一个可执行程序以及外部表格保存的数据，以便让我可以调试。尽管我可以使用十六进制编辑器
直接修改二进制可执行文件中的ASCII数据，但这么直接改二进制数据是令人恶心的。你也应当使用一些
蒙特卡洛建模技术，其中特别有用的是对一个情景进行x次迭代，并将AI和损失数据存到一个表格形式的ASCII
文件以便分析。

### Artificial Intelligence
The keys to realistic combat AI are hidden information and randomness. If you have that, you
can employ quite simple routines. As Clauswitz and Sun Tzu point out, even simple plans are
difficult to execute in combat. The Artificial Intelligence data is presented in narrative form with
the probabilities imbedded in the description of the routines. I'm still having some problem with
the strategic AI, but nothing that a little more application won't solve. 

### 人工智能
实现看起来真实的战斗AI的关键是信息隐藏和随机性。如果你实现了这些，那么你就可以比较简单的实现AI。
正如克劳塞维茨和孙子指出的，在战斗中，即使是非常简单的计划也难以执行。AI的数据以一些操作的概率
所表示。在策略AI上我仍然有一些问题没有解决，但没有什么特别难对付的部分。

### General Advisory
This is the first time in nearly 20 years that I've had to deliver a spec to programmers I've never
met. I usually do the programmer hiring, so I know what they are capable of and what they prefer
to get in the form of a spec. It also helps that my programmers know I sign the payroll and bonus
checks. In any event, I'm delivering the AI stuff in a pretty generic format so that the
programmers can get a good sense of what it is going to do and then get back to me with
whatever alternate format they might prefer. It won't take long to reformat it once I know the
preferred format.

### 全面咨询
这是我二十多年第一次向从来没有见过的程序员写说明。一般来说我会亲自选择雇佣的程序员人选，所以我
知道他们想要什么格式的说明。另一方面，程序员知道是由我亲自来发工资将近也是有帮助的。无论如何，
我在传达AI相关的事宜时会使用一种相当宽泛的方式，从而程序员可以了解到他们大致上要做什么，然后
向我要求以他们更喜欢的格式编写的说明。一旦我知道他们更喜欢什么格式，将现有说明改写成那个格式并不困难。

### Footnote feature
We can cobble those together from notes, but for a full blown version we'll need a codicil on the
contract to clarify the book contract Al and I are now negotiating with my publisher. The big
version would, in effect, be a book on a disk and would be a great selling point that would add
little to the production costs (an extra disk) and nothing to development (the bits that are already
going into the FootNote feature would simply be larger). Tom says he's amenable to signing the
agreement needed to protect the book copyright. 

### 笔记作为卖点
我们可以把设计笔记汇总起来编本书，不过这需要在合约上加上关于这本书的条款，对此Al和我正在和出版商讨论此事。
这个书将存在一个磁盘上，它将成为一个有意义的卖点而并不会太过增加生产成本（一个额外的磁盘），也不会
增加开发成本（已经实现了这些笔记的要求）。Tom说他已经同意签署保护这个书的版权的协议。

### Communication

Until you figure out exactly how you're going to code this thing, you'll have a lot of queries.
Since financial and military models don't mix, you won't be able to get a hold of me when I'm
downtown (material here deleted as I don't want too many people to have an easy time tracking
me down when I'm trying to get work done). Otherwise, leave a message on the answering
machine. I will email confirmations on all phone discussions of spec changes, but do it via email
as much as possible. Normally, I check email twice a day: between 4-8 AM and 4-7 PM Eastern
time (1-5 AM and 1-4 PM Western time). If you alert me that you will be throwing a lot of
queries at me, I can usually arrange to check mail between 11 AM-2 PM Eastern time (8-11 AM
Western time). In most cases, I take care of email queries immediately (especially when I'm at
home, where all the computer records and printed research material is available). This in over 80
percent of the cases you will have an answer in under six hours. On those I can't answer
immediately, I usually pass on to Al Nofi (ANOFI on GEnie) and he usually gets back in 24
hours. I keep copies of all incoming and outgoing email and keep it indexed, so I can find
anything within seconds. One helluva organized sumbitch, ain't I?

### 沟通

在你完全搞明白到底怎么编码这些东西之前，你必须进行大量的询问。由于商业和军事模型不应该混合起来，
你不应当在我在（划掉）的地方（这里的内容被删掉了，以免当我想用这些时间办公时，太多人追踪我，）
的时候联系我。其他时候，在电话应答机（answering machine）上留一条信息。我会发电子邮件确认
所有关于说明内容改变的电话讨论，说明本身也应当尽可能以电子邮件的方式进行。通常一天中我会检查两次
电子邮件：在东部时间上午4-8点与在下午4-7点（西部时间上午1-5点，下午1-4点）。如果你提示我你将会向我
提很多问题，我可以在东部时间上午11点到下午2点（西部时间上午8-11点）也检查邮件。在大多数情况下，
我会立即回复电子邮件询问（特别是当我在家里的时候，我家里有着全部的数据资料和研究资料）。
在80%的情况中你可以在六小时内获得一个答复。在我不能立即回答的情况下，我会传给Al Nofi(ANOFI on GEnie)
，他通常会在24小时内回来。我备份了所有发出和收到的邮件并进行了索引，所谓我可以立即找到我想找到的邮件。
看起来我真是个一个热衷于整理的怪物。

### Spec Files

Files (with one exception, two versions of each, .WK1 is 123 spreadsheet version and .ASC is
IBM ASCII version with CR/LF at the end of each 72 character line):
* VASSPEC.NN- This note.
* VASGAME- Game procedures. The game rules. Has a functioning menu system if you
have a spreadsheet compatible with 123 macros (I used Quattro Pro in 123 mode).
* VASSHIPS- The ship stats. This was larger until we took out the German, Italian and
most of the French and British ships (the latter two nations did have some ships in the
Pacific). The game information is on the left hand side. To the right is historical
information, some of which is used to calculate game values so has to stay in place.
* VASDIV- The ground and air units.
* VASPORTS- The map information as well as capabilities of ports and bases.
* VASAIR- Not really needed by the codemakers, just us showing off. We had to compile
this one in order to come up with a dozen or so numbers for "average" aircraft stats by
year for each side.
* VASGUYS- The leaders, and all their stats.

### 说明的各个文件

每个文件，除了一个例外外都有两个格式，一个是`.WK1`为123电子表格格式而`.ASC`为IBM ASCII格式，其
每72个字符有一个回车。文件列表如下：

* `VASSPEC.NN`- 这个注释。
* `VASGAME`- 游戏程序。游戏规则。如果你的电子表格软件兼容123宏还可有一个菜单系统
（我使用123模式的Quattro pro）。
* `VASSHIPS`- 舰艇数值。这个文件现在还有点太大了，之后我会拿掉德国，意大利和大多数发过和英国
的舰艇（后两个国家还是有一些舰艇在太平洋）。游戏信息存在左边，右边是历史信息，有些信息会被用来
计算游戏数值，所以不要修改它。
* `VASDIV`- 地面和空中单位。
* `VASPORTS`- 地图信息与港口与基地承载能力。
* `VASAIR`- 程序员并不真的需要这个文翰，它只是我们用来展示的。我们编辑了这个文件来讨论
双方空军在各年的“平均”数值。
* `VASGUYS`- 双方的将领与它们的数值。

* Implementation Sequence (as I see it)
...Strategic Display
...Unit List
...Strategic Movement
...Tactical Display
...Tactical Movement and Combat
...Strategic Combat
...Strategic AI
...Tactical AI
...Leadership 
...Other

* 实现顺序（在我看来）
...战略展示
...单位列表
...战略移动
...战术显示
...战术移动和战斗
...战略战斗
...战略AI
...战术AI
...指挥能力
...其他


* Program Sequence
...Load main executable
...Player chooses scenario option
...Program initializes scenario and begins play
...Player input
...Change production
...Reroute supply
...Movement orders

* 程序执行顺序
...载入主程序
...玩家选择剧本
...程序初始化剧本
...玩家输入
...生产变化
...补给线变动
...移动命令

* Computer Procedures
...Strategic Search
...Tactical Search
...Strategic Move
...Tactical Move
...Strategic (Aggregated) Combat
...Tactical (detailed) Combat
...Logistics
...Strategy Selection
...Tactics Selection
...Etc 

I used the above to guide my priorities in conditioning the enclosed material for delivery. Let me
know how it's supposed to be so I can shift gears accordingly.

* 电脑程序
...战略搜索
...战术搜索
...战略移动
...战术移动
...战略（集成）战斗
...战术（细节）战斗
...后勤
...战略选择
...战术选择
...等等

我使用上面的列表来指导我在资料传递上的优先级。让我知道你想要什么从而我可以做对应的调整。

* Resolution
...One day Strategic
...One Hour Operational
...30 Sec tactical

A footnote on this project. While the official start date was July 15th, it was largely delayed for
six weeks because a few days after signing the contract my co-pilot, Al Nofi, had to have
emergency eye surgery. His eyesight survived, but it was not until early September that he could
get into the research big time. You always have to make allowances for disasters. 

* 战斗尺度
...天级别战略
...小时级别行动
...30秒战术

关于这个项目的脚注。尽管官方的开始时间之前是7月15日，但是它已经被大幅延误了六周因为之前，在签署合约后
我的合作伙伴，Al Nofi突然要做一个眼部手术。他的视力最终得以保留，但是在在九月前他不能再投入到
大规模研究中。人的命运啊就是不可意料，你总要考虑到灾难的行程提前做好余量准备。


## 百年战争

As this book was being written, the Hundred Years War game is in alpha test. This game is one
aspect of computerized wargames that is just now coming into its own and this is the use of
modems for multiplayer games via telephone linked computers. For nearly ten years, computer
networks such as Compuserve and GEnie there have offered multiplayer games, but none of
these have been history based (or, at best, only vaguely so). To remedy this situation, I signed a
contract with GE to design a multiplayer (300 players) game of the Hundred Years War to be
played on their GEnie system. Al Nofi (research) and Dan Masterson (programming) will
comprise the rest of the team that will recreate 14th and 15th century England and France (plus
Italy, Spain, parts of Germany, Scotland, Ireland and sundry other adjacent areas). The game will
cover economics, religion and politics in addition to the purely military aspects. 

在这本书正在写的时候，百年战争游戏正在进行alpha测试中。这个新式电脑兵棋使用了调制解调机来连结
各个电脑以实现多人游戏。在近十年中，电脑网络，如Compuserve何GEnoie已经搞出了很多多人游戏，
但是它们中没有一个是基于历史的（或者说，用好话讲，只有空洞的背景）。为了缓解这个形势，
我与GE签订了合同去设计一个关于百年战争的多人（300玩家）游戏，基于GEnie系统。Al Nofi(研究)与
Dan Masterson(编程)将构成团队的剩余部分。这个团队致力于重现14和15世纪的英格兰和法兰西（加上意大利，
西班牙，一部分德国，苏格兰，爱尔兰以及其他近邻的区域）。除了主要的军事部分以外，这个游戏还覆盖了
经济，宗教和政治部分。

As a player, your objective is to insure the growth, prosperity and survival of your family line
(each day of real time equals three months of game time). You may start out the game as
anything from an impoverished Gascon noble to a mighty earl of England. Your degree of
victory is rated on how much you increase what you started with during the century or so it takes
England and France to settle their dynastic, military and economic differences. The game allows
players to operate on two levels, either as a free wheeling adventurer, living only for battle,
tournaments or the hunt (a rather common attitude in those times), and/or as an ambitious and
able administrator of his estates and participant in the affairs of state. The latter course is more
rewarding in the long run, but the former can be more fun for the mash and bash set. There's a
little of that it all of us. 