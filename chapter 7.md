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

作为玩家，你的目标是保证你家族的成长，繁荣和生存（现实世界一天对应游戏时间三个月）。你可以以一个
贫穷的Gascon贵族或者强大的英格兰伯爵开始游戏。你的胜利程度取决于在这个世纪中你从你的初始地位提升了多少，
或者造成了英格兰和法兰西多大的王朝，军事和经济差异。游戏允许玩家在两个层面上行动，作为一个到处游荡
的冒险家，只为战斗，竞技赛和狩猎而生（在这个时代中很多人采用的行为方式），或者作为一个野心勃勃而
富有能力的管理者，管理他的资产，并参与国家事务。后一种行为方式在长期来看受到的奖励更多，但前者
也许更加有趣。我们中两类人都有一点。

In this game the computer is used in areas where it does the most good. The medieval economic
system is run by the computer. Medieval economies were fairly complex. Although most of the
population was farming, about ten percent was not and was instead trading and producing a
variety of manufactured goods that could be bought and sold over wide areas. There was money
about, a bureaucracy and a heavily armed nobility. At any given time, at least 1-2 percent of the
population was in arms. Most of these troops were mercenaries and they were either paid or you
suffered their depredations as brigands. Many mercenaries turned to brigandage once large
armies were demobilized, 

[[vas illos]]

creating a constant state of conflict during several periods. As the game goes on, brigand bands
(run by the computer) will become an increasing threat to your fiscal, and physical, well being. 

在这个游戏中，电脑被用在被适合它的地方。中世纪经济系统被计算机运营。中世纪经济非常复杂，尽管
大多数人口都在务农但越有10%的人口在贸易，生产手工艺品，并将这些产品带到世界的各个区域。很多钱
流向了官僚和武装贵族。在任何时间，至少有1%-2%的人口处于武装状态。这些军事势力中的很多
是雇佣兵，他们要么被你雇佣要么你将会被他们掠夺。大多数雇佣兵会在大军被解散时成为这样的盗匪。

[[vas illos]]

造成了一个长期的冲突和动乱的时代在这个时间。当游戏进程推进时，盗匪（电脑控制）将变成对你的钱袋，
幸福和性命的越来越大的威胁。

Taxes were raised, somewhat inefficiently and often with such vigor that rebellion resulted. The
brigand depredations also get the common folk riled up. It's bad enough when they refuse to pay
their taxes, but if you're a real bad actor, they'll come after your head. 

If you decide to spend all your time fighting in wars and tournaments, your fiefs will "run
themselves," although less efficiently. In other words, without your personal attention, your
bailiffs will be less rigorous and honest. Your wife and children may develop excessive spending
habits and, in general, your assets will waste away. 

税收以比较低效的方式收集，而且经常伴随着叛乱带来的影响。盗匪的掠夺也会让普通群众烦躁不安。
当他们拒绝交税时，情况已经变得足够糟糕，但如果你是个真正差劲的演员，他们会来取你项上人头。

如果你决定将你全部的时间用在战斗和骑士竞技上，你的领地将以较低的效率“自行运行”。换句话说，
脱离了你个人的关注，你的总管的严格和诚实将有所下降，你的妻子和孩子将养成花销过高的生活习惯，
一般来说，这将造成你财产的浪费。

You can borrow and lend money, or buy and sell fiefs. Fiefs are the basic economic unit of the
game and there are about 800 of them. The "fief file" is itself an interesting historical document,
containing data dredged up from numerous sources and containing traditional "fiefs"
(agricultural areas) as well as towns and religious facilities (church owned fiefs with
monasteries, etc.). There is, for example, a fief in France called Condom, run by a player who
will be known as the Sire de Condom. There's also another Welch fief called something worse,
but it's in Gaelic. Hey, we just call them as we see them. But you can see where the French got
some of their historical traits from. 

Play the game and you'll quickly discovered that even the largest cities had fewer than 100,000
citizens within its walls. Less than five percent of the population lived in walled towns and cities,
most of the remainder lived in small villages surrounded by farmland and pastures. 

你可以借入，贷出资金或者购买或出售领地。“领地”是游戏中的基本经济单位，一共差不多有800个。
“领地文件”本身就是一种令人感兴趣的历史文件，其包含了大量混淆来源扒出来的数据。传统的领地是
农业区域，但也包含城镇和宗教设施（教堂中教士们控制的封地）。作为例子，法兰西有一个领地叫做
Condom（避孕套），它的玩家控制者也许应该被称为Sire de Condom(避孕套爵士)。还有个在Gaelic的
叫Welch（赖皮）的封地也许更糟。唉，我们这么叫它只是因为它们确实叫这个名字。也许你可以从这里看出
法国人是从哪获得他们的一些历史传统的。

玩这个游戏后你也许马上回发现甚至最大的城市都只有少于100000的市民。少于10%的人口生活在有墙的城镇，城市中。
大多数其他人生活在被农田和牧场包围的小镇中。

About two percent of the population belonged to the nobility or a nobles household. This group
included many of the troops. Thus of the thirty million (pre-plague) population in the area
covered by the game, only a few hundred thousand men were fighters. The three hundred players
occupy one of three ranks. Every player is at least a "lesser noble" controlling one or more fiefs.
Three dozen players are "magnates," or overlords of several lesser nobles and themselves the
holders of more fiefs than a lesser noble. One player is the king of England and one really
unfortunate wretch is the king of France. 

To start the game off in the proper spirit, the English players (about one third the total) are
allowed a week to discuss things among themselves and elect those of their number deemed most
suitable to be magnates and the king. This represents the superior cohesiveness of the English
government, even though they did not have elections as such. Those players who chose to be
French (or were forced to be French if all the English slots were taken) are randomly assigned as
lesser nobles, magnates and king. This maximizes the chances of the wrong person getting into a
key position. 

大约有2%的人口属于贵族阶级或者贵族家庭。这个群体包含了很多团体。游戏涉及的区域有大概三千万人口（瘟疫前）
，只有几十万男人是战斗人员。三百个玩家占据着三个等级。每个玩家至少是一个“小贵族”（“lesser noble”），
其控制了一个或多个空地。36个玩家是“大贵族”（magnates），它们是一些小贵族的领主，本身也控制着
比小贵族更多的领地。一个玩家是英格兰国王而另一个不幸的卑鄙之人则为法兰西国王。

为了使得游戏以合适的精神开始，英国玩家（占总量中的三分之一）被允许在一周之内讨论并选举出他们认为最合适
的大贵族和国王的人选。这表明了英国政府更高的凝聚力，尽管历史上并没有这样的选举。选择加入法国一方
（或因为英国人选占满而被迫选择法国）的玩家则被随机指派其作为小贵族，大贵族和国王。这最大化了
错误的人占据关键位置的概率。

While combat is the final arbiter of events, there are other ways to get things done. After all,
battles are only a forceful way of obtaining a treaty. The English king wants to become the
French king and to do so he must control enough French territory to make his coronation as
French king convincing. There is a legal system built into the game, covering both civil and
church matters. You can be declared an outlaw or excommunicated. You can even be tried and
executed. There's a Pope (actually, more than one during this period), heresy and the ever
popular Black Death (which will ultimately destroy half the population over several outbreaks). 

尽管战斗是很多事情的最终裁决者，也存在着一些其他的方式解决它们。基本上，战斗只是一种得到条约
的强制手段。英国国王想要成为法国国王，所以他必须控制足够的发过领土来使得他对法国王位的宣称
令人信服。游戏中有一个法律系统，包含民法和宗教法。有一个教皇（当然，在整段时间有不止一位），
异端与黑死病（它最终在数次爆发中消灭了一半的人口）。

Money plays a large role in the game. Although several currencies were used in this period, we
invented a new one, the ducat (which was actually the name of an Italian currency) so that you
wouldn't have to deal with all the different exchange rates. By way of example, 600 ducats
equals one English Pound and 135 ducats equals one French Livre, and so on. One ducat also
equals one US dollar (1992 vintage). Money is important in this period. Troops were the biggest 
expense. The feudal levy could still be called out, but only for local defense and only for a
limited period of time. On average, a mercenary soldier cost about 2,000 ducats per turn (a
season of three months). Most armies in this period contained 5-10,000 men, which meant 10-20
million ducats per turn just for the troops. The king of England only had that much income per
turn (in the best of times) and there were other expenses (household, maintenance of
fortifications, bribes and payments to officials, etc.). The king had several thousand people on his
payroll and even a magnate had several hundred servants and soldiers to support (and an income
of up to several million ducats per turn). You can borrow money, but basically the English kept
the war going for so long because they were better soldiers, their ships controlled the English
Channel (most of the time) and they were able to constantly plunder French fiefs. Thus the object
of taking your army into the field was not battle, but plunder. Sort of like a game of Monopoly
with edged weapons. 

钱在这个游戏中扮演了重要角色，尽管当时有多种不同的货币在被使用。我们炮制了一个新的，
所谓的达克特（ducat，它曾经是意大利货币的名字），从而你不用去烦恼不同的换算率。作为例子，600达克特
等于1英镑，135达克特等于1法国里弗（Livre）。1达克特也等于1美元（1992出产（vintage）
（译：vintage这个词指葡萄酒的出产时间，如82年拉菲之类的））。钱在这个时间段很重要，军队开销是重要部分。
封建征召兵（levy）仍然可以被召集，但只能用于地区局部防御且只能使用有限的时间。平均来说，
一个雇佣军士兵每回合（一个季度）要消耗2000达克特。大多数这个时候的军团包含5000-10000人，这意味着
1-2千万达克特每回合的支出。英格兰王每个回合也只有这个数目的收入（在他最好的时候），而同时他又有其他
的开销（家庭支付，要塞维护，腐败与给官员的工资等）。国王亲自支付数千人的工资，而大贵族也要维护数百人的
从者和士兵（他们每回合有数百万的收入）。你可以借钱。英国可以在战争中坚持那么长时间，因为他们拥有
更强的战士，他们的船控制着英吉利海峡（大多数时间），他们还能持续的掠夺法国的领地。
从而将你的军队开到战场的目标不是战斗，而是掠夺，看上去像是在玩流血版大富翁游戏（game of Monopoly）。

Using a remote computer does not waste the capabilities of your PC. For players with IBM
compatible machines and Macintoshes there is a program you can download from GEnie. This
program, (a Graphic Front End or GFE) will incorporate a datacomm program to connect with
GEnie (more specifically, the Hundred Years War game) and have an editor for writing
messages to other players and the graphics capability to display game activities in more detail.
Players with other PC types can still play just by connecting with GEnie, but will not have access
to all the amenities in the GFE. The GFE costs nothing (except the connect time to download it, a
few bucks). 

使用远程计算机并不会浪费你的PC的配置。对于使用与IBM兼容的机器与Macintoshes电脑的玩家，
你可以从GEnie下载一个程序，该程序（一个图形前端（Graphic Front End,GFE））可以使用一个datacomm
程序去连接GEnie（更清楚地说，百年战争游戏），并且可以拥有一个对其他玩家写消息的编辑器，
而图形方面则可以显示游戏种更多的细节。使用其他PC类型的玩家仍然可以通过连接GEnie来游玩，但是
不能使用GFE的全部功能。GFE是免费的（除了连接并下载它的费用，几块钱吧）

When you first connect with this game via GEnie you immediately know you're not in Kansas
any more. If it's you first time, you're asked if you want to join the game. If you answer yes you
receive a screen full of information on who your character is ("you are William de Clinton, the
Baron of Huntington in Cambridgeshire, England, etc.," or "You are the Captal de Buch, lord of
the fortifications guarding the port of Buch on the Gascon coast and the owner of three fiefs,
etc.") and what your resources are (other fiefs owned, annual income, etc.) as well as personal
information (age, state of health, wife, kids, state of your fortifications, troops under your
control, claims on other players fiefs, etc.). 

当你首次通过GEnie连接游戏时，你就会理解知道你并不在Kansas之类的地方。如果这是你第一次进入，
你会被询问是否想要加入游戏，如果回答是，你就会接到一屏幕信息，它告诉你你的角色是什么（“你是
William de Clinton，Huntington in Cambridgeshire，England的男爵”，或者“你是Captal de Buch，
守备Buch on Gascon海岸港口的要塞的领主，并拥有三块领地。”）以及你的资源有什么（“其他拥有的领地，
年收入等”），以及个人信息（年龄，健康数值，妻子，孩子，你的要塞的状态，你控制的军队，对
其他玩家领地的宣称等）。

You can sign on and do nothing and your character's life will go on. In this case you would be
the medieval equivalent of a couch potato. Taxes are collected and spent in your estate, dishonest
officials will embezzle most of the surplus and life will go on with you doing little more than
observing. Note that you play through the current eldest male of the family your character
belongs to. When the eldest male dies, the next eldest male descendent takes over. If none is
available, the line dies and you're out of the game. Among other things, you have to look after
the wife and kiddies (which involves some interesting and obvious activities not normally found
in wargames, but essential to medieval military affairs). 

你可以在注册后什么都不干，而你的角色依然会继续生活下去。在这个情况中，你的角色基本等价于现代的
沙发土豆（couch potato，即除了躺在沙发上看电视什么都不干的人）。税收被征收上来并用在你的资产中，
不诚实的执事将偷掉其中的大部分剩余而生活将继续，而你除了观察外什么都不干。注意你会扮演你家族中
最年长者，当这位长者去世时，下一个长者将接替其位置。如果没有合适的长者连任，则家族系谱断绝，游戏结束。
除此之外，你还必须关注你的妻子和孩子（这涉及一些在一般兵棋中很难见到的有趣而且重要的事情，但是
在中世纪军事事务却是很重要的。）

However, there is much to do and this is the virtue of an online computer game. The key here is
the multiple players and the ease of communication and interaction. Multiplayer games are
usually more enjoyable than two player encounters, yet solitaire play is the most common
because of the difficulty in getting the players together. Online games eliminate these problems.
Whenever you get on you can send and receive messages. You can also talk with other players
who are on at the same time and join together for tournaments (jousting, duels, etc.), hunting or
conspiracies or affairs of state (there was often little difference between the two). This form of
real time of communication, in a time when it took three weeks to ride from one end of France to
another, is justified by the three month length of the game "turns" (one day of real time). Players
may allocate their 90 days more productively, performing such drudgery as managing their fiefs
or training with arms. But true to the period, they may spend most (or all) of their time out
hunting and fighting. Naturally, the more ambitious (and probably the older) players will more
readily adapt to building their power through management and diplomacy. The important thing is
that up to three hundred individuals in one historically based game will make for an interesting
experience. Should some bloody minded sixteen year old find him (or her) self king of France,
surrounded by a few equally rapacious nobles and faced with a thirty-five year old tax
accountant, management consultant or college professor playing the king of England. 

网上电脑游戏的优点之一就是易于玩家的交流和交互。多人游戏通常比双人游戏更有意思，但是在大多数情况下
难以实现，因为很难集齐各个玩家。网上游戏解决了这个困难，无论你在哪，都可以接到和发送消息。
你也可以与其他在线的玩家对话，并一同参与竞赛（骑马长枪比武，决斗之类的），狩猎，阴谋或者国家事务
（这两者之间并没有很大的差别）。在一个从法兰西一端到另一端要花三周时间的时代，之所以存在这种即时沟通能力，
可以被实际上一回合的时间长达三个月（对应一天真实时间）来解释。玩家也许会更有效的分配他的90天，
如卖力地管理他的领地或者练习武艺。但实际上在这段时间，他们很可能花了大多数（如果不是全部）时间
去用于狩猎和打仗。自然地，越有野心的玩家（也许同样越老的玩家）将倾向于构建他们的权势，通过管理和
外交。重要的是300个在基于历史的游戏的玩家将创造一个有趣的体验。想想一个嗜血的十六岁少年（或少女）
也许会发现它作为法王，报一群同样贪婪的贵族所包围，同时还要面对扮演英王的三十五岁的税务顾问，
管理咨询或者大学教授的情景。

Well, this game will be fun just to watch. And you will be able to watch. For example, we can
have play by play descriptions.

Battles during the period were infrequent (perhaps one or two a month of real time, or one or two
every seven years of game time). However, you could usually see them coming (money and
mercenaries had to be collected, negotiations conducted, etc.), so we will announce them and
enable any interested GEnie users to view the action in terminal mode. "Hundred Years War:
Witness the Battle of Rouen at 9 PM, February 3rd, 1993." The "Heralds" (sysops) will give play
by play commentary, battle maps (o's and x's) plus participant interviews, pre and post battle
commentary and the like. Everything but tailgate parties. Sort of like a football game with edged
weapons, no timeouts and no referees (and very few rules). 

当然，这个游戏仅仅是看上去就很有趣的样子。你也的确可以看看，通过以下口头描述当一会云玩家。

战役在这个时间段并不是很频繁（也许一个现实月里有一两次，或者说每7个游戏年中有1,2次）。
尽管你可以看到它们发生的进程（经费被收集，雇佣兵被召集，谈判等），所以我们将公告它们并且
让感兴趣的GEnie用户可以在终端模式里看到他们的行动。“百年战争：见证Rouen战役，
发生于1993年2月3日下午9点”。“传令官”（管理员）会给出详细的报告和评论，包括战斗地图（XO来表示），
加上参与者的采访，战斗前和战斗后的评论之类的。有所有东西除了车尾聚会（taillgate parties）
（译：指看外出看体育比赛的一种聚会）。有点像流血的足球比赛，只是没有时间限制和裁判（以及很少一点规则）。

"Here we are folks, outside the French city of Rouen in the year of our Lord 1376, where the
Duke of Normandy and the Count of Artois have marshalled their forces to settle a dispute over
who shall be the Duke of Brittany. The Normans have a contingent of English troops under the
Earl of Bedford and are the current favorites. The six thousand Norman troops and eleven
thousand French troops are arrayed and combat is expected to commence in about fifteen
minutes at 9:40 PM EST. First, however, we have a live interview with his lordship, the
Constable of France, the Count of Artois. Tell us, Count, how do you expect to overcome those
English longbowmen?" And so on... 

“这里是吃瓜群众，正在法兰西城市Rouen外，现在是自我们的主诞生以来的1376年。在这里，
诺曼底公爵和Artois公爵统领着他们的军队准备解决一场关于谁将成为布列塔尼公爵的争端。
诺曼人拥有一支由Bedford伯爵指挥的英格兰分遣队，是当前的种子选手。六千诺曼人和一万一千
法兰西军队的战斗准备即将十五分钟后的东部时间下午9:40开始。我们将直播采访这位大人，
法兰西治安官（Constable，译：法兰西五大官员头衔之一），Artois伯爵。告诉我们，伯爵大人，
你将打算如何对付英国人的长弓兵？”之类的。。。

More frequently, there will be tournaments. These involve all sorts of individual combat,
including jousting. The joust will be handled like the familiar vehicle simulators computer games
are famous for. Our version will have dozens of players from all over the country lining up
electronically to come thundering down the lists in real time for fame, glory and (game) money.
We're also working on a system whereby other players can watch the action, and perhaps even
make bets (with ducats only) on the action (another bit of historical realism). Note that jousts
were also a popular way to settle sieges. Real (not blunted) weapons were used and the fight was
to the death. 

出现的更多的是竞技赛。这包含各种类型的个体战斗，如骑马长枪比武（jousting）。这种决斗类似
赛车模拟游戏。我们的版本将包含来自各地的十二个玩家，他们排在一排，为名声，荣誉，（游戏中的）金钱
对对方发起冲锋。我们也在做一个系统，该系统可以为为其他玩家观看他们的装具，并提供一个赌博机制
（仅能使用杜卡特），赌比武的结果（又成功了反映了中世纪历史的一个方面）。注意骑马长枪比武
也是解决城堡围攻的一个流行的方式。不过这里使用真正的长枪而非钝器，并战至一方战死为止。

Naturally, new technology costs more. Connect time for online games via the GEnie network is
$6.00 an hour (as of 1992, billed to the nearest minute). The game is being designed so that, if
you use the GFE, you can actively participate using only 2-3 hours a month. If the game goes a
full century (400 days), it's going to cost you something like $200 to play the entire game. That's
fifty cents a day. Not cheap, but not all that outrageous either. How else could you participate in
the Hundred Years War? One of the big problems with on line games is their expense. Many 
players find themselves spending hundreds of dollars a month on these addictive games and
many have to drop out because they can't afford it. The Hundred Years War will be unique in
that it will be one of the first on line games to confront this problem. The way the game is
designed, there is no real advantage to spending hundreds of dollars a month on the game (unless
you want to be really good at jousting, which is actually a relatively minor aspect of the period).
Players can have a major impact while only incurring costs of no more than $20-$30 a month.
This way, we hope to get a lot more players involved. Online gaming looks to be one of the more
interesting new areas for historical simulations in quite some time. 

自然地，使用新技术将带来更高的花费。使用GEnie网络连接游戏的费用是每小时6美元（1992年物价，按分钟计费）。
游戏被设计为，如果你使用GFE，你每个月只需用上线2-3小时。如果这个游戏运营了整个游戏百年（现实400天），它将会
花掉你大约200美元以玩过整场游戏。这相当于每天50年美元。不算很便宜，不过也没有那么贵。你还能怎么参与
这个游戏呢。线上游戏的一个问题就是它的话费。有些成瘾网上游戏玩家发现他们在游戏上每月花了数百美元，
从而其中很多人因为负担不起而被迫中途退出。百年战争的独特之处在于它将成为第一个试图解决这个
问题的线上游戏。游戏的设计方式使得每月在游戏中花掉数百美元并不会使你获得太大优势（除非你
花费很多去试图精通骑马长枪比武，中世纪中倒也的确经常发生类似的事），玩家仅需花费20-30美元美元就可
造成很大的影响。通过这个方式，我们希望使得更多玩家参与。网络游戏看起来是历史模拟游戏可以大展身手
的崭新领域。

But why just talk about it when we can walk you through a few activities of the actual game
(alpha version) in late 1991. I was playing Louis II, Count of Flanders. What follows is what
actually appeared on my computer screen as I connected to GEnie and entered the Hundred
Years War game. Brief notes explaining what I'm doing will appear interspersed with the game
related material. 

[[production note: my comments appear in brackets. Computer material should appear in
different type face, I suggest sans serif]] 


但是为什么我们要仅仅是抽象地谈论他们，当我们可以的确带你见识这个游戏在1991末的alpha版本的样子呢？
下面的内容将是我连接到GEnie并在我屏幕上显示的游戏内容，我将扮演Louis II，Flanders伯爵。
游戏中的一些内容将被以注释的形式解释。

[[我的注释将标在方括号中。电脑显示的东西应该不同的样式出现，我建议使用无衬线字体（译：即每个字母
单独显示，衬线字体的显示会考虑上下文）]]

```
** Thank you for choosing GEnie **

The Consumer Information Service from General Electric
Copyright (C), 1992

GEnie Logon at: 05:46 EST on: 921107
Last Access at: 21:47 EST on: 921107

No letters waiting.

GEnie Announcements (FREE)

1. NEW FCC COST INCREASE THREATENS COMPUTER SERVICES......*FCC
2. NEW NEW NEW The 1992 Version GEnie Satin Jacket.......*ORDER
3. New Area Codes in California and Maryland.............. 
4. If you love Soap Operas, check out the >free< RTCin....SHOWBIZ
5. Subscribe now to DUNGEONS & DRAGONS(tm) games..........TSR
6. November issue the Caribbean Travel Roundup is here....TIS
7. Win MICROSOFT SOLUTION software at FREE RTC............HOSB
8. RTCs, Mickey's Birthday................................FLORIDA
9. RECHARGER Magazine RTC on the..........................PSRT
10. Computer Football League opens.........................SCORPIA
11. Speak with a Technical Support Supervisor..............CHIPSOFT
12. LIVE from LEIPZIG......................................GERMANY
13. Mid-Week football fun. Call the plays for Texas A&M....QB1
14. Play the weekly Fantasy Football Pool and win $$.......FF
15. Upload contest wins FREE time, Usenet news in..........UNIX

Enter #, <H>elp, or <CR> to continue?Move 945
```


```
** 感谢您使用GEnie **

信息服务有通用电气提供
Copyright (C), 1992

GEnie登入: 05:46 EST on: 921107
最后访问: 21:47 EST on: 921107

没有邮件

GEnie公告 (免费)

1. 新的联邦通信委员会（FCC）支出威胁计算机服务......*FCC
2. 最新出品,GEnie 1992年版缎纹夹克（Satin Jacket）.......*ORDER
3. 加利福尼亚与马里兰州的新区号（Area Code）.............. 
4. 如果你喜欢肥皂剧, 请看>免费的< RTCin....SHOWBIZ
5. 现在订购龙与地下城(tm)游戏..........TSR
6. 这里看11月加勒比海旅游概览....TIS
7. 免费赢取微软解决方案软件 RTC............HOSB
8. 米奇的生日的RTC ................................FLORIDA
9. 充电（RECHARGER）杂志RTC在这儿 ..........................PSRT
10. 计算机足球联盟成立.........................SCORPIA
11. 与技术支持主管谈笑风生..............CHIPSOFT
12. 来自莱比锡的LIVE......................................GERMANY
13. 周中足球粉丝们，去德克萨斯A&M玩吧....QB1
14. 参加幻想足球赛发大财.......FF
15. 上传竞赛获取免费时间,Usenet大新闻..........UNIX


输入 #, <H>elp, 或 <CR> 继续?Move 945
```

[The first thing you see is GEnie ID and promotional material. You are not charged for looking
at that. I entered the command "Move 945" and that took me to the Hundred Years War (HYW)
game. The GFE would take you there automatically.]

[首先你会看到的东西是GEnie ID和这些广告内容。你不是必须看这些东西，我输入命令“Move 945”进入
百年战争（HYM）游戏。GFE程序则会自动进入游戏。]

```
The game and its RT are a GEnie VALUE ($6 an hour) Service

WELCOME TO THE HUNDRED YEARS WAR MULTIPLAYER ONLINE GAME

The game is on page 945, the HYW RT is on page 946. Weekly Real Time
Conferences on Saturday, 4 PM Eastern Time in the games Interactive Court.
Plenty of files on the game in the file library (page 946). Plenty of good
advice and companionship in the HYW RT (page 946). Plenty of mayhem and
adventure in the game (page 945).

HYW Staff, and their GEnie email IDs

Designed by Jim Dunnigan: HYW$
System development by Dan Masterson: HYW$
Research by Al Nofi: HYW$
Player assistance provided by the Heralds:
Herald of England- Darrell L. Killpack: FROTZ
Herald of England- Mark O. Kinkead: M.KINKEAD
Herald of France- Barbara Byro: BYRO
Herald of France- Robert B. Kasten: R.KASTEN1
Herald of the Others- Daniel H. Scheltema: D.SCHELTEMA
Master of the Archives- Charles R. Townsley: C.TOWNSLEY
Master of the Peerage- Richard A. Edwards: R.EDWARDS26
Master of the Scrivners- Dave Zincavage: JDZ3

Help is always available in the HYW RT (page 946)

GEnie Page 945

Hundred Years War (tm) by DENO

1. Personal Affairs
2. Travel
3. Hunting, Combat and Dirty Deeds
4. Official Acts
5. The Herald
6. Scoreboard
7. Instructions
8. Join Hundred Years War
9. HYW RoundTable
10. Send FEEDBACK to DENO

Enter #, <P>revious, or <H>elp?1

```

```
这个游戏和它的RT（译：类似论坛）由GEnie VALUE(每小时6美元)服务提供

欢迎来到百年战争多人在线游戏

这个游戏在945页，HYW RT在946页。周实时会议在东部时间星期六下午4点于游戏交互法庭召开。
大量关于游戏的文件可见于文件图书馆（946页），大量关于在HYW RT的沟通建议见于946页。
大量的混乱和冒险见于游戏（945页）。

HYW工作人员，和他们的GEnie邮箱地址与ID

设计师 邓尼根: HYW$
系统开发 Dan Masterson：HYW$
研究 Al Nofi: HYW$
玩家协助 Heralds:
英格兰传令官- Darrell L. Killpack: FROTZ
英格兰传令官- Mark O. Kinkead: M.KINKEAD
法兰西传令官- Barbara Byro: BYRO
法兰西传令官- Robert B. Kasten: R.KASTEN1
其他区域传令官- Daniel H. Scheltema: D.SCHELTEMA
档案管理者- Charles R. Townsley: C.TOWNSLEY
贵族管理者- Richard A. Edwards: R.EDWARDS26
公证管理者- Dave Zincavage: JDZ3



你总可以在HYW RT（946页）上得到游戏帮助

GEnie 945页

百年战争（tm）DEMO版


1. 个人事务
2. 旅行
3. 收敛，战斗与肮脏的勾当
4. 官方行为
5. 传令官
6. 分数榜
7. 介绍
8. 加入百年战争
9. HYW圆桌会议
10. 给DEMO反馈

输入 #, <P>revious, 或 <H>elp?1

```

[This is the main HYW menu. The first thing I want to do is go to the personal affairs menu (1) to
see how I'm doing.]

[这是HYW的主要菜单。我首先想转到个人事务菜单（1）中看看我正在干什么。]

```
1. <Fie>f Management
2. <P>ersonal Characteristics
3. <H>ousehold Affairs
4. <Fa>mily Matters
5. <Fin>ancial Activity
6. <C>ourt
7. <A>larum Menu
8. <G>amble
9. <O>nline Messages
10. Dump Vital Financial Information
11. Dump Vital Family Information
12. <I>nteractive Court
Enter #, or <ENTER> To Exit: 2
```

```
1. <Fie>(e)文件管理
2. <P>(ersonal) 个人特征
3. <H>(ousehold) 家族事务
4. <Fa>(mily) 家庭事务
5. <Fin>(ancial)财务事务
6. <C>(ourt) 宫廷
7. <A>(larum)警告菜单
8. <G>(amble)赌博
9. <O>(nline)在线消息
10. 删除(Dump)重要财务信息 
11. 删除重要家庭信息
12. <I>(nteractive)与宫廷交互
Enter #, 或 回车 以 退出: 2
```

[Personal affairs has numerous submenus. But first I'll show you "who I am." by choosing menu
option 2.]

[个人事务有很多子菜单，但是首先我先选择菜单选项2来向你展示“我是谁”]

```
Personal Purse 877.00
Current Location is AFC01 Luxeil
Current Health 3 Maximum Health 3
```

<table border="1" cellpadding="2" width="695">
  <tbody><tr>
    <td width="140"><small><code>Management</code></small></td>
    <td width="19"><small><code>3</code></small></td>
    <td width="126"><small><code>Guile</code></small></td>
    <td width="19"><small><code>1</code></small></td>
    <td width="166"><small><code>Leadership</code></small></td>
    <td width="45"><small><code>8</code></small></td>
    <td width="98"><small><code>Stature</code></small></td>
    <td width="18"><small><code>7</code></small></td>
  </tr>
  <tr>
    <td width="140"><small><code>Protection</code></small></td>
    <td width="19"><small><code>2</code></small></td>
    <td width="126"><small><code>Endurance</code></small></td>
    <td width="19"><small><code>8</code></small></td>
    <td width="166"><small><code>Attack Value</code></small></td>
    <td width="45">1</td>
    <td width="98">&nbsp;</td>
  </tr>
  <tr>
    <td width="140"><small><code>Tournament</code></small></td>
    <td width="19"><small><code>3</code></small></td>
    <td width="126"><small><code>Sire ID</code></small></td>
    <td width="19"><small><code>0</code></small></td>
    <td width="166"><small><code>Org ID</code></small></td>
    <td width="45"><small><code>285</code></small></td>
  </tr>
</tbody></table>

```
You are Heinrich V de Limbourg Your ID is 285 Your age is 46
You are married to Alais de Limbourg.
Sex m You Speak F1
Wife is not Pregnant
Court Persona Is 285
```

_______________________

```
Athlete 4
Command 7
Insightful of people 8
Insightful of situations 4
Superstitious 5
See Titles (Y or N)? y
 Fief ID Fief Name Rank
1. HLG01 Limbourg 11 Graf
Press <ENTER> to continue.
```
____________________




```
个人钱包 877.00
当前位置为 AFC01 Luxeil
当前健康值 3 最大健康值 3
```

<table border="1" cellpadding="2" width="695">
  <tbody><tr>
    <td width="140"><small><code>管理</code></small></td>
    <td width="19"><small><code>3</code></small></td>
    <td width="126"><small><code>狡诈</code></small></td>
    <td width="19"><small><code>1</code></small></td>
    <td width="166"><small><code>领导力</code></small></td>
    <td width="45"><small><code>8</code></small></td>
    <td width="98"><small><code>声望</code></small></td>
    <td width="18"><small><code>7</code></small></td>
  </tr>
  <tr>
    <td width="140"><small><code>保护</code></small></td>
    <td width="19"><small><code>2</code></small></td>
    <td width="126"><small><code>忍耐（Endurance）</code></small></td>
    <td width="19"><small><code>8</code></small></td>
    <td width="166"><small><code>攻击值</code></small></td>
    <td width="45">1</td>
    <td width="98">&nbsp;</td>
  </tr>
  <tr>
    <td width="140"><small><code>竞技赛</code></small></td>
    <td width="19"><small><code>3</code></small></td>
    <td width="126"><small><code>Sire ID</code></small></td>
    <td width="19"><small><code>0</code></small></td>
    <td width="166"><small><code>Org ID</code></small></td>
    <td width="45"><small><code>285</code></small></td>
  </tr>
</tbody></table>

```
你是Limbourg的Heinrich V,你的ID是285。你的年龄是46岁。
你娶了Limbourg的Alais
性别 男 你说F1语
妻子没有怀孕
宫廷角色（Court Persona）为285
```

_______________________

```
运动能力 4
战斗能力 7
对人类的洞察力 8
对形势的洞察力 4
迷信 5
看头衔 (Y or N)? y
 领地ID  领地名  等级
1. HLG01  Limbourg  11 伯爵
按 回合 以 继续.
```
____________________


[If it looks like something out of out of a Role Playing Game (RPG), it is, as HYW is a RPG,
albeit one played on a vast scale and historically accurate. I describe my character as a dirty old
man, but more on that later.]

[Back at the Personal Affairs Menu, I go to check out my financial situation. As in real life,
money drives this game.]

[如果这个游戏看上去像角色扮演游戏（RPG），其实吧，百年战争就是个RPG，不过是在一个广阔的历史尺度
与精度的世界中。我将我的角色描述为一个肮脏的老男人，之后会介绍更多。]

[回到个人事务菜单中，我转而检查自己的财务情况。就像在现实生活中一样，钱驱动着整个游戏。]

```
Financial Activity

1. <S>ummary of all Holdings
2. <I>ndividual Fief Status
3. <F>iefs Owned List
4. <C>urrent Finances
5. <P>ayments to Other Players
6. <B>uy and Sell Fiefs
7. Hire and Fire <N>PCs
8. Hire <T>roops
9. <E>xit

Enter # 3
```
[Lets check out my fiefs, the source of a feudal lords wealth.]

```
Fief ID Fief Name Trsry Kp Lvl Surp Llty Bail Mngr AT Status
1. HLG01 Limbourg 6 5.79 -35 9.0 392 0 N Calm


Choose Fief 1 to 1, <E> Followed by Fief # to Examine, <P>revious Page,
or <ENTER> TO Quit: 1

Fall Of 1340 90.0 Days Left

Current Fief HLG01 Limbourg
Loyalty 9.00 Surplus -35.00 Treasury Balance 6.23 Status Calm
Bailiff ID 392
Auto Transfer Flag Is Off, Surplus Will Not Be Transfered To Purse

Personal Purse 877.00
```

```
财务事务

1. <S>(ummary)私有资产汇总
2. <I>(ndividual)个人体领地状况
3. <F>(iefs)所拥有领地列表
4. <C>(urrent)当前财务
5. <P>(ayments)给其他玩家的支付
6. <B>(uy)买卖领地
7. 雇佣与解雇<N>PCs
8. 征召<T>武装
9. <E>xit

输入 # 3
```
[让我们看看我的领地，封建领主财务的来源]

```
   领地ID 领地名称 价值 城堡等级 结余 Llty Bail Mngr AT 状态
1. HLG01  Limbourg 6    5.79   -35  9.0  392  0    N  安宁的

输入 1跳转到领地1, <E>后跟领地序号对该领地检查, <P>以调回上一页,
或 回车退出: 1

1340 秋季 剩余90.0天

当前领地： HLG01 Limbourg
忠诚 9.00 总结余 -35.00 收入 6.23 状态 安宁的
Bailiff ID 392
自动转移标记为关闭状态，从而结余不会自动结转到钱包中

个人钱包 877.0
```

[The Graf de Limbourg controls one fief, with a name, and location, that still exist in modern
Germany. This was one of the many peripheral areas included in the game. Most of the fiefs are
in France and England.]

[Limbourg伯爵控制着的这个领地，它的名字和位置在当今德国仍然存在。这个区域在游戏涉及范围的边界，
游戏中的主要的领地还是分布在法兰西和英格兰]

```
Enter # 1
Individual Fief Summary
Limbourg (HLG01 ) Liege HRE:Germany Population 20.3
Language F1 Freedom 1 Status Calm
Your Overlord is Guy Baudet (290) Bailiff ID 392
Fields 5.22 Industry 2.08 Weather 0.99 Trsy Bal 6.23
Knights 28 MAA 10 Lt Cav 0 Yeomen 0 Foot 406 Rabble 8932
```

<table border="1" cellpadding="2" width="80%">
  <tbody><tr>
    <td><small><code>&nbsp;&nbsp; </code></small></td>
    <td><small><code>Last Season&nbsp;&nbsp; </code></small></td>
    <td><small><code>Crnt Season&nbsp;&nbsp; </code></small></td>
    <td><small><code>Next Season</code></small></td>
  </tr>
  <tr>
    <td><small><code>Loyalty&nbsp;&nbsp; </code></small></td>
    <td><small><code>8.73&nbsp;&nbsp; </code></small></td>
    <td><small><code>9.00</code></small></td>
  </tr>
  <tr>
    <td><small><code>GDP&nbsp;&nbsp; </code></small></td>
    <td><small><code>3117&nbsp;&nbsp; </code></small></td>
    <td><small><code>3121&nbsp;&nbsp; </code></small></td>
    <td><small><code>3138</code></small></td>
  </tr>
  <tr>
    <td><small><code>1-Tax Rate&nbsp;&nbsp; </code></small></td>
    <td><small><code>14.0%&nbsp;&nbsp; </code></small></td>
    <td><small><code>14.0%&nbsp;&nbsp; </code></small></td>
    <td><small><code>14.0%</code></small></td>
  </tr>
  <tr>
    <td><small><code>Income&nbsp;&nbsp; </code></small></td>
    <td><small><code>436&nbsp;&nbsp; </code></small></td>
    <td><small><code>436&nbsp;&nbsp; </code></small></td>
    <td><small><code>439</code></small></td>
  </tr>
  <tr>
    <td><small><code>2-Officials&nbsp;&nbsp; </code></small></td>
    <td><small><code>80&nbsp;&nbsp; </code></small></td>
    <td><small><code>66&nbsp;&nbsp; </code></small></td>
    <td><small><code>60</code></small></td>
  </tr>
  <tr>
    <td><small><code>3-Garrison&nbsp;&nbsp; </code></small></td>
    <td><small><code>222&nbsp;&nbsp; </code></small></td>
    <td><small><code>182&nbsp;&nbsp; </code></small></td>
    <td><small><code>165</code></small></td>
  </tr>
  <tr>
    <td><small><code>4-Infrastructure&nbsp;&nbsp; </code></small></td>
    <td><small><code>122&nbsp;&nbsp; </code></small></td>
    <td><small><code>100&nbsp;&nbsp; </code></small></td>
    <td><small><code>90</code></small></td>
  </tr>
  <tr>
    <td><small><code>5-Keep (Level)&nbsp;&nbsp; </code></small></td>
    <td><small><code>160 ( 5.64)&nbsp;&nbsp; </code></small></td>
    <td><small><code>131 ( 5.79)&nbsp;&nbsp; </code></small></td>
    <td><small><code>119</code></small></td>
  </tr>
  <tr>
    <td><small><code>Extra Expenses&nbsp;&nbsp; </code></small></td>
    <td><small><code>-24&nbsp;&nbsp; </code></small></td>
    <td><small><code>-7</code></small></td>
  </tr>
  <tr>
    <td><small><code>Total Expenses&nbsp;&nbsp; </code></small></td>
    <td><small><code>560&nbsp;&nbsp; </code></small></td>
    <td><small><code>471</code></small></td>
  </tr>
  <tr>
    <td><small><code>Graft&nbsp;&nbsp; </code></small></td>
    <td><small><code>0&nbsp;&nbsp; </code></small></td>
    <td><small><code>0</code></small></td>
  </tr>
  <tr>
    <td><small><code>Overlord Taxes&nbsp;&nbsp; </code></small></td>
    <td><small><code>0&nbsp;&nbsp; </code></small></td>
    <td><small><code>0</code></small></td>
  </tr>
  <tr>
    <td><small><code>Surplus/Deficit&nbsp;&nbsp; </code></small></td>
    <td><small><code>-124&nbsp;&nbsp; </code></small></td>
    <td><small><code>-35</code></small></td>
  </tr>
</tbody></table>

```
Enter 1-5 to change, or <ENTER> to Quit:
```

```
输入 # 1
个人领地汇总
Limbourg (HLG01 ) 封君（Liege） HRE:德意志人口 20.3
语言 F1 自由度 1 状态 安宁的
你的领主是 Guy Baudet (290) Bailiff ID 392
农田 5.22 手工业 2.08 天气 0.99 盈余 6.23
骑士 28 武装人员（MAA） 10 轻骑兵（Lt Cav） 0 自由民（Yeomen） 0 步兵 406 暴民（Rabble） 8932
```

<table border="1" cellpadding="2" width="80%">
  <tbody><tr>
    <td><small><code>&nbsp;&nbsp; </code></small></td>
    <td><small><code>上一季度&nbsp;&nbsp; </code></small></td>
    <td><small><code>当前季度&nbsp;&nbsp; </code></small></td>
    <td><small><code>下一季度</code></small></td>
  </tr>
  <tr>
    <td><small><code>忠诚&nbsp;&nbsp; </code></small></td>
    <td><small><code>8.73&nbsp;&nbsp; </code></small></td>
    <td><small><code>9.00</code></small></td>
  </tr>
  <tr>
    <td><small><code>GDP&nbsp;&nbsp; </code></small></td>
    <td><small><code>3117&nbsp;&nbsp; </code></small></td>
    <td><small><code>3121&nbsp;&nbsp; </code></small></td>
    <td><small><code>3138</code></small></td>
  </tr>
  <tr>
    <td><small><code>1-税率&nbsp;&nbsp; </code></small></td>
    <td><small><code>14.0%&nbsp;&nbsp; </code></small></td>
    <td><small><code>14.0%&nbsp;&nbsp; </code></small></td>
    <td><small><code>14.0%</code></small></td>
  </tr>
  <tr>
    <td><small><code>收入&nbsp;&nbsp; </code></small></td>
    <td><small><code>436&nbsp;&nbsp; </code></small></td>
    <td><small><code>436&nbsp;&nbsp; </code></small></td>
    <td><small><code>439</code></small></td>
  </tr>
  <tr>
    <td><small><code>2-官员&nbsp;&nbsp; </code></small></td>
    <td><small><code>80&nbsp;&nbsp; </code></small></td>
    <td><small><code>66&nbsp;&nbsp; </code></small></td>
    <td><small><code>60</code></small></td>
  </tr>
  <tr>
    <td><small><code>3-守备队&nbsp;&nbsp; </code></small></td>
    <td><small><code>222&nbsp;&nbsp; </code></small></td>
    <td><small><code>182&nbsp;&nbsp; </code></small></td>
    <td><small><code>165</code></small></td>
  </tr>
  <tr>
    <td><small><code>4-基础设施&nbsp;&nbsp; </code></small></td>
    <td><small><code>122&nbsp;&nbsp; </code></small></td>
    <td><small><code>100&nbsp;&nbsp; </code></small></td>
    <td><small><code>90</code></small></td>
  </tr>
  <tr>
    <td><small><code>5-城堡(等级)&nbsp;&nbsp; </code></small></td>
    <td><small><code>160 ( 5.64)&nbsp;&nbsp; </code></small></td>
    <td><small><code>131 ( 5.79)&nbsp;&nbsp; </code></small></td>
    <td><small><code>119</code></small></td>
  </tr>
  <tr>
    <td><small><code>额外开支&nbsp;&nbsp; </code></small></td>
    <td><small><code>-24&nbsp;&nbsp; </code></small></td>
    <td><small><code>-7</code></small></td>
  </tr>
  <tr>
    <td><small><code>总开支&nbsp;&nbsp; </code></small></td>
    <td><small><code>560&nbsp;&nbsp; </code></small></td>
    <td><small><code>471</code></small></td>
  </tr>
  <tr>
    <td><small><code>贿赂&nbsp;&nbsp; </code></small></td>
    <td><small><code>0&nbsp;&nbsp; </code></small></td>
    <td><small><code>0</code></small></td>
  </tr>
  <tr>
    <td><small><code>领主税&nbsp;&nbsp; </code></small></td>
    <td><small><code>0&nbsp;&nbsp; </code></small></td>
    <td><small><code>0</code></small></td>
  </tr>
  <tr>
    <td><small><code>结余/负债&nbsp;&nbsp; </code></small></td>
    <td><small><code>-124&nbsp;&nbsp; </code></small></td>
    <td><small><code>-35</code></small></td>
  </tr>
</tbody></table>

```
输入 1-5 修改, 或 回车 以 退出:
```

[I'm currently taxing this fief at a high level, but I'm also investing a lot in Infrastructure (roads,
public buildings and the like) and payments to the Garrison (the local knights and men at arms),
which will enable me to raise taxes even higher.]

[Back at the main menu, I go to the Alarum menu, to find out that has been happening in the
game recently. Each day of real time represents 90 days (one season) of game time.]

[我正在在这个领地征收较高的税收，不过我也同样在其基础设施（道路，公共建筑之类的）投入了很多。
我在守备队（地方骑士和武装人员）维护上也投入了很多，这使得我可以高枕无忧的征收高税。]

[回到主菜单，我回到警告菜单去查看最近游戏世界中发生了什么。真实世界每一天对应游戏世界90天。]

```
Alarum Menu

1. <R>ead Personal History File
2. Read <H>erald
3. <A>ctive Player List
4. <S>cores

999. Move To Main HYW Menu

Enter #, or <ENTER> To Exit: h

Enter Season Of History You Want To Read

1. Last Season (Summer 1340)
2. Two Seasons Ago (Spring 1340)
3. Three Seasons Ago (Winter 1339)

Enter #, or <ENTER> To Exit: 1
```

```
警告菜单

1. <R>(ead) 阅读个人历史档案
2. 阅读<H>(erald)传令官消息
3. <A>(ctive)上线玩家列表
4. <S>(cores)分数

999. 移到HYM主菜单

输入 #, or 回车 以 退出: h

输入你想要阅读的档案所处的季度

1. 上一季度 (1340夏季)
2. 上两季度 (1340春季)
3. 上三季度 (1339冬季)

输入 #, 或 回车 以 退出: 1
```

[I look at the most recent season (yesterday in real time) and find out who was born, who died,
who is at war, what battles were fought, keeps besieged and fiefs pillaged. Never a dull moment
in the 14th century.]

[我查看上一个季度（即真实时间的昨天）的记录看看都有谁出生，死亡，处于战争中，发生了哪些战斗，
那些领地被围攻和劫掠。在14世纪永远不会有无趣的一天。]

```
History For Summer 1340

The Freville Family (18) has had a baby boy.
The Burys Family (46) has had a baby boy.
The de Bohun Family (101) has had a baby boy.
The de Camus Family (119) has had a baby girl.
778 Catherine Berkeley died in child birth.
The Glyn Dwr Family (195) has had a baby girl.
658 Marie de Preaux died in child birth.
The de Rohan Family (205) has had a baby girl.
The du Barril Family (206) has had a baby boy.
The Holland Family (226) has had a baby girl.
The Douglas Family (282) has had a baby boy.
The de Loraille Family (297) has had a baby girl.
The de Namur Family (305) has had a baby girl.
The Grovesner Family (239) has had a grandson.
```

```
1340夏季纪事

Freville家族(18)生了个男孩.
Burys家族(46)生了个男孩.
de Bohun家族(101)生了个男孩.
de Camus 家族 (119)生了个女孩.
778 Catherine Berkeley难产身亡.
The Glyn Dwr 家族 (195)生了个女孩.
658 Marie de Preaux难产身亡.
de Rohan 家族 (205)生了个女孩.
du Barril 家族 (206)生了个男孩.
Holland 家族 (226)生了个女孩.
Douglas 家族 (282)生了个男孩.
de Loraille Family (297)生了个男孩.
de Namur 家族 (305)生了个男孩.
The Grovesner Family (239)生了个孙子.
```

[Because you only can stay in the game if you have an heir to replace your current character
when it dies, marriage and children are important. Childbirth was, however, more dangerous
then than it is today and even the wives of aristocrats were at risk.]

[由于当你当前角色死亡时你必须有一个继承人替换当前角色才能继续游戏。所以结婚和生育是很重要的，
生育在中世纪比起今天要危险的多，即使是贵族家庭的女性也常常处于难产身亡的风险中。]

```
Eudes de Burgundy (53) has died at Dijon.
Isabelle Richemont (103) has died at Limoges.
John de Cobham (163) has died at Maidstone.
Simone Boccanera (287) has died at Genoa.
Andrea Orsini (407) has died at Venice.
Louise de Craon (687) has died at Rochefort.
Jeanne de Laval (705) has died at La Fert.
Margaret ap Gwain (715) has died at Montbard.
Press <ENTER> to continue.
Jeanne de Clare (716) has died at Llandovery.
Annette de Gonzolles (760) has died at Llanbyther.
Thomas de Floques (950) has died at Portsmouth.
Alexandre de Corvino (1235) has died at Evreaux.
Eudes du Barril (6274) has died at Perigord.
Alain de Lyon (6315) has died at Laon.
```

```
Eudes de Burgundy (53) 在Dijon去世.
Isabelle Richemont (103) 在Limoges去世.
John de Cobham (163) 在Maidstone去世.
Simone Boccanera (287) 在Genoa去世.
Andrea Orsini (407) 在Venice去世.
Louise de Craon (687) 在Rochefort去世.
Jeanne de Laval (705) 在La Fert去世.
Margaret ap Gwain (715) 在Montbard去世.
按 回车 以 继续.
Jeanne de Clare (716) 在Llandovery去世.
Annette de Gonzolles (760) 在Llanbyther去世.
Thomas de Floques (950) 在Portsmouth去世.
Alexandre de Corvino (1235) 在Evreaux去世.
Eudes du Barril (6274) 在Perigord去世.
Alain de Lyon (6315) 在Laon去世.
```

[Warfare was common, and often the forces were commanded, if only in name, by women. These
female warriors were almost always widows who were forced to send out troops to defend their 
interests. The women would usually hire a noted freelance commander to actually lead the
troops in battle. Unlike most wargames, this one actually attracts a large number of female
players.]

[冲突是常见的，而且这些军队常常是被女人所统领，虽然一般是名义上的。这些女性战士通常是一些寡妇，
她们被迫派出军队去包围她们的利益。这些女人通常雇佣一个著名的雇佣兵头领去实际指挥军队。不像大多数
兵棋，这个游戏的确吸引了很多女性玩家。]

```
FPO03 La Roche de Poitiers 正在被 Anne Aubert (112)围攻 .
FPO03 La Roche de Poitiers 被 Anne Aubert (112)所夺取.
APR01 Barcelonette 正在被 Jean de Clermont (121)围攻.
APR01 Barcelonette 被 Jean de Clermont (121) 劫掠
APR01 Barcelonette 被 Jean de Clermont (121) 袭击
APR01 Barcelonette 被 Jean de Clermont (121) 夺取.
ANC02 Puget 正在被 Jean de Clermont (121) 围攻.
Mary Elizabeth Clifford (230) 与 Robert de Nesles (764) 成婚.
Anne Glyn Dwr (6303) 与 Roger Mowbry (1079) 成婚.
Jean de Clermont (121) 已被绝罚.
Blanche de Ponthieve (632) 与 Charles de Chabannes (1127) 成婚.
Guy de Sully (82) 开始召集军队.
Bodo Badarieux (1583) 在试图刺杀 Gautier le Roy (60) 时被捕.
Herve Gex (3689) 在试图绑架 Jeanne le Roy (799) 时被捕.
```

[Assassination and kidnapping were considered perfectly reasonable ways to achive your goals
in this period. They were a lot cheaper than hiring an army.]

[刺杀和绑架在这个时代被认为是完全合理的达成目的的手段。它们比使用正式的武力要便宜得多。]

```
APR01 Barcelonette is being besieged by Clare Paleologo (231).
Press <ENTER> to continue.
Jean de Clermont (121) Has Been Outlawed
By Philippe VI de Valois (200).
```

```
APR01 Barcelonette 正在被 by Clare Paleologo (231) 围攻.
按 回车 以 继续.
Jean de Clermont (121) 被 Philippe VI de Valois (200) 宣布为不法之徒
```

[At this point in the game, the player with the Jean de Clermont decided to wage a private war.
The French king (Philippe VI de Valois) told him to stop, as did the player playing the Pope. De
Clermont ignored both, and in this season he was outlawed by the king and excommunicated by
the Pope. The king and his loyal vassals raised armys and marched on de Clermonts lands in the
south central French Forez region. Doesn't pay to mess with the king.]

[在游戏的这个时间点，操纵Jean de Clearmont的玩家决定发起一场私人战争，
另一个同时扮演法王（Philippe VI de Valois）和教皇的玩家要求他停战。De Clermont同时无视这两个要求，
于是他同时被法王宣布为非法，被教皇绝罚。同时法王和他重视的附庸召集军队赶往Clermont的在法兰西中南部的
Fores领地。所以不要试图激怒你的王。]

```
FCE05 Mantes was pillaged by Ame de St-Vollier (10)
FCE05 Mantes is being besieged by Ame de St-Vollier (10).
FCE05 Mantes was raided by Ame de St-Vollier (10)
Eleanor de Grailly (1043) and John d'Urtino (531) were married.
Roger de Clermont (789) was captured during a successful siege.
Elizabeth de Clermont (6228) was captured during a successful siege.
FCE05 Mantes was taken by Ame de St-Vollier (10).
FCE03 Pontoise is being besieged by Ame de St-Vollier (10).
FCE01 Clermont was raided by Thierry III de Grand Pre (252)
FCE01 Clermont is being besieged by Philippe VI de Valois (200).
Jean de Clermont (121)'s Garrison Defeated
Thierry III de Grand Pre (252) During A Pillage/Raid Attempt At Clermont.
FCE01 Clermont surrendered to Philippe VI de Valois (200)
FCE03 Pontoise was pillaged by Philippe VI de Valois (200)
APR01 Barcelonette is being besieged by Louise de Gonzolles (173).
FCE03 Pontoise is being besieged by Philippe VI de Valois (200).
FCE01 Clermont is being besieged by Thierry III de Grand Pre (252).
Thierry III de Grand Pre (252) Defeated
Philippe VI de Valois (200)'s Garrison During A Siege Attempt At Clermont.
FGU12 Graves is being besieged by Jean de Grailly (126).
Press <ENTER> to continue.
Jean de Grailly (126) Defeated
Foucaud de Rouchechourt (3)'s Garrison During A Siege Attempt At Graves.
Jean de Grailly (126) Defeated
Foucaud de Rouchechourt (3)'s Garrison During A Siege Attempt At Graves.
Foucaud de Rouchechourt (3) was captured during a successful siege.
Bodo Digne (3257) was captured during a successful siege.
FGU12 Graves was taken by Jean de Grailly (126).
FCE01 Clermont paid extortion to Thierry III de Grand Pre (252)
Thierry III de Grand Pre (252) Defeated
Philippe VI de Valois (200)'s Garrison During A Siege Attempt At Clermont.
Thierry III de Grand Pre (252) Defeated
Philippe VI de Valois (200)'s Garrison During A Siege Attempt At Clermont.
Anne de Breche (1120) and Nicholas de Breche (186) were married.
APR01 Barcelonette was pillaged by Alfonso XI de Castilla y Leon (8)
APR01 Barcelonette was raided by Alfonso XI de Castilla y Leon (8)
APR01 Barcelonette is being besieged by Alfonso XI de Castilla y Leon (8).
APR01 Barcelonette was taken by Alfonso XI de Castilla y Leon (8).
Elizabeth de Bertrand was caught seducing
Bertrand du Guesclin.
Elizabeth de Bertrand (193) and Bodo de Mauny (794) were married.
Henry Percy was caught seducing
Annette de Stafford.
Press <ENTER> to continue.
```

```
FCE05 Mantes 被Ame de St-Vollier (10) 劫掠
FCE05 Mantes 正在被Ame de St-Vollier (10) 围攻.
FCE05 Mantes 被Ame de St-Vollier (10)袭击
Eleanor de Grailly (1043) 与 John d'Urtino (531) 成婚.
Roger de Clermont (789) 在城陷后被捕.
Elizabeth de Clermont (6228) 在城陷后被捕.
FCE05 Mantes 被 Ame de St-Vollier (10) 所夺取.
FCE03 Pontoise 正被 Ame de St-Vollier (10) 围攻.
FCE01 Clermont 被 Thierry III de Grand Pre (252) 袭击
FCE01 Clermont 正被 Philippe VI de Valois (200) 围攻.
Jean de Clermont (121) 的守备队被击败了
Thierry III de Grand Pre (252) 在 Clermont 对抗掠夺企图.
FCE01 Clermont 向 Philippe VI de Valois (200) 投降
FCE03 Pontoise 被 Philippe VI de Valois (200) 劫掠
APR01 Barcelonette 正被 Louise de Gonzolles (173) 围攻.
FCE03 Pontoise 正被 Philippe VI de Valois (200) 围攻.
FCE01 Clermont 正被 Thierry III de Grand Pre (252) 围攻.
Thierry III de Grand Pre (252) 被击败了
Philippe VI de Valois (200)的守备队 Clermont 在对抗围攻.
FGU12 Graves 正在被 Jean de Grailly (126) 围攻.
按 回车 以 继续.
Jean de Grailly (126) 被击败了
Foucaud de Rouchechourt (3)的守备队在 Graves 对抗围攻.
Jean de Grailly (126) 被击败了
Foucaud de Rouchechourt (3)的守备队在 Graves 对抗围攻.
Foucaud de Rouchechourt (3) 在城陷后被捕.
Bodo Digne (3257) 在城陷后被捕.
FGU12 Graves 被Jean de Grailly (126) 所夺取.
FCE01 Clermont 支付勒索金给 Thierry III de Grand Pre (252)
Thierry III de Grand Pre (252) 被击败
Philippe VI de Valois (200)的守备队在 Clermont 对抗围攻.
Thierry III de Grand Pre (252) 被击败了
Philippe VI de Valois (200)的守备队在 Clermont 对抗围攻.
Anne de Breche (1120) 与 Nicholas de Breche (186) 成婚.
APR01 Barcelonette 被 Alfonso XI de Castilla y Leon (8) 劫掠
APR01 Barcelonette 被 Alfonso XI de Castilla y Leon (8) 袭击
APR01 Barcelonette 正在被 Alfonso XI de Castilla y Leon (8) 围攻.
APR01 Barcelonette 被 Alfonso XI de Castilla y Leon (8) 所夺取.
Elizabeth de Bertrand 在对 Bertrand du Guesclin 的勾引中被捕.
Elizabeth de Bertrand (193) 与 Bodo de Mauny (794) 成婚.
Henry Percy 在对 Annette de Stafford 的勾引中被捕.
按 回车 以 继续.
```

[Back at the Alarum menu, I can also see who the other players are. In this game there were
over a hundred at this time. Below is one screen full.]

[回到警告菜单， 我可以看到有哪些其他玩家。在此时的游戏中有超过一百个玩家。下面是一屏内容]

<table border="1" cellpadding="2" width="80%">
  <tbody><tr>
    <td><small><code>ID</code></small></td>
    <td><small><code>Name</code></small></td>
    <td>&nbsp;</td>
    <td><small><code>E-Mail</code></small></td>
  </tr>
  <tr>
    <td><small><code>1. 22</code></small></td>
    <td><small><code>Benedict XII</code></small></td>
    <td><small><code>Pontifex Maximus</code></small></td>
    <td><small><code>GM</code></small></td>
  </tr>
  <tr>
    <td><small><code>2. 83</code></small></td>
    <td><small><code>Guy</code></small></td>
    <td><small><code>Baveux</code></small></td>
    <td><small><code>SIMUTRONICS</code></small></td>
  </tr>
  <tr>
    <td><small><code>3. 222</code></small></td>
    <td><small><code>Renard VI</code></small></td>
    <td><small><code>de Pons</code></small></td>
    <td><small><code>FDITIZIO</code></small></td>
  </tr>
  <tr>
    <td><small><code>4. 109</code></small></td>
    <td><small><code>Guy</code></small></td>
    <td><small><code>d'Albon</code></small></td>
    <td><small><code>J.JIMENEZ</code></small></td>
  </tr>
  <tr>
    <td><small><code>5. 58</code></small></td>
    <td><small><code>Gaston II</code></small></td>
    <td><small><code>de Carcassone</code></small></td>
    <td><small><code>CGW</code></small></td>
  </tr>
  <tr>
    <td><small><code>6. 47</code></small></td>
    <td><small><code>Edward III</code></small></td>
    <td><small><code>Plantagenet</code></small></td>
    <td><small><code>DIPLOMACY-1</code></small></td>
  </tr>
  <tr>
    <td><small><code>7. 60</code></small></td>
    <td><small><code>Gautier</code></small></td>
    <td><small><code>le Roy</code></small></td>
    <td><small><code>DIPLOMACY-3</code></small></td>
  </tr>
  <tr>
    <td><small><code>8. 176</code></small></td>
    <td><small><code>Louis</code></small></td>
    <td><small><code>de Bourbon-LaMarche</code></small></td>
    <td><small><code>AUSI-SUPPORT</code></small></td>
  </tr>
  <tr>
    <td><small><code>9. 364</code></small></td>
    <td><small><code>Connor</code></small></td>
    <td><small><code>McKinnon</code></small></td>
    <td><small><code>A</code></small></td>
  </tr>
  <tr>
    <td><small><code>10. 97</code></small></td>
    <td><small><code>Hugh</code></small></td>
    <td><small><code>de Audley</code></small></td>
    <td><small><code>FROTZ</code></small></td>
  </tr>
  <tr>
    <td><small><code>11. 288</code></small></td>
    <td><small><code>Personne I</code></small></td>
    <td><small><code>Inconnu</code></small></td>
    <td><small><code>M.WIELENGA2</code></small></td>
  </tr>
  <tr>
    <td><small><code>12. 46</code></small></td>
    <td><small><code>Edward</code></small></td>
    <td><small><code>Burys</code></small></td>
    <td><small><code>J.BRANDT7</code></small></td>
  </tr>
  <tr>
    <td><small><code>13. 157</code></small></td>
    <td><small><code>Juana II</code></small></td>
    <td><small><code>de Navarra</code></small></td>
    <td><small><code>B.HUNTER7</code></small></td>
  </tr>
  <tr>
    <td><small><code>14. 12</code></small></td>
    <td><small><code>Anger</code></small></td>
    <td><small><code>de Montault</code></small></td>
    <td><small><code>J.CUMMINS</code></small></td>
  </tr>
  <tr>
    <td><small><code>15. 164</code></small></td>
    <td><small><code>John</code></small></td>
    <td><small><code>Mowbry</code></small></td>
    <td><small><code>W.HART9</code></small></td>
  </tr>
</tbody></table>

```
Choose Character 1 to 15, <N>ext Page, or <ENTER> TO Quit: 
```

<table border="1" cellpadding="2" width="80%">
  <tbody><tr>
    <td><small><code>ID</code></small></td>
    <td><small><code>Name</code></small></td>
    <td>&nbsp;</td>
    <td><small><code>E-Mail</code></small></td>
  </tr>
  <tr>
    <td><small><code>1. 22</code></small></td>
    <td><small><code>Benedict XII</code></small></td>
    <td><small><code>Pontifex Maximus</code></small></td>
    <td><small><code>GM</code></small></td>
  </tr>
  <tr>
    <td><small><code>2. 83</code></small></td>
    <td><small><code>Guy</code></small></td>
    <td><small><code>Baveux</code></small></td>
    <td><small><code>SIMUTRONICS</code></small></td>
  </tr>
  <tr>
    <td><small><code>3. 222</code></small></td>
    <td><small><code>Renard VI</code></small></td>
    <td><small><code>de Pons</code></small></td>
    <td><small><code>FDITIZIO</code></small></td>
  </tr>
  <tr>
    <td><small><code>4. 109</code></small></td>
    <td><small><code>Guy</code></small></td>
    <td><small><code>d'Albon</code></small></td>
    <td><small><code>J.JIMENEZ</code></small></td>
  </tr>
  <tr>
    <td><small><code>5. 58</code></small></td>
    <td><small><code>Gaston II</code></small></td>
    <td><small><code>de Carcassone</code></small></td>
    <td><small><code>CGW</code></small></td>
  </tr>
  <tr>
    <td><small><code>6. 47</code></small></td>
    <td><small><code>Edward III</code></small></td>
    <td><small><code>Plantagenet</code></small></td>
    <td><small><code>DIPLOMACY-1</code></small></td>
  </tr>
  <tr>
    <td><small><code>7. 60</code></small></td>
    <td><small><code>Gautier</code></small></td>
    <td><small><code>le Roy</code></small></td>
    <td><small><code>DIPLOMACY-3</code></small></td>
  </tr>
  <tr>
    <td><small><code>8. 176</code></small></td>
    <td><small><code>Louis</code></small></td>
    <td><small><code>de Bourbon-LaMarche</code></small></td>
    <td><small><code>AUSI-SUPPORT</code></small></td>
  </tr>
  <tr>
    <td><small><code>9. 364</code></small></td>
    <td><small><code>Connor</code></small></td>
    <td><small><code>McKinnon</code></small></td>
    <td><small><code>A</code></small></td>
  </tr>
  <tr>
    <td><small><code>10. 97</code></small></td>
    <td><small><code>Hugh</code></small></td>
    <td><small><code>de Audley</code></small></td>
    <td><small><code>FROTZ</code></small></td>
  </tr>
  <tr>
    <td><small><code>11. 288</code></small></td>
    <td><small><code>Personne I</code></small></td>
    <td><small><code>Inconnu</code></small></td>
    <td><small><code>M.WIELENGA2</code></small></td>
  </tr>
  <tr>
    <td><small><code>12. 46</code></small></td>
    <td><small><code>Edward</code></small></td>
    <td><small><code>Burys</code></small></td>
    <td><small><code>J.BRANDT7</code></small></td>
  </tr>
  <tr>
    <td><small><code>13. 157</code></small></td>
    <td><small><code>Juana II</code></small></td>
    <td><small><code>de Navarra</code></small></td>
    <td><small><code>B.HUNTER7</code></small></td>
  </tr>
  <tr>
    <td><small><code>14. 12</code></small></td>
    <td><small><code>Anger</code></small></td>
    <td><small><code>de Montault</code></small></td>
    <td><small><code>J.CUMMINS</code></small></td>
  </tr>
  <tr>
    <td><small><code>15. 164</code></small></td>
    <td><small><code>John</code></small></td>
    <td><small><code>Mowbry</code></small></td>
    <td><small><code>W.HART9</code></small></td>
  </tr>
</tbody></table>

```
Choose Character 1 to 15, <N>ext Page, or <ENTER> TO Quit: 
使用字符1-15进行选择， <N>下一页 或者 回车 以 退出:
```

[Back at the main menu, I go to the Travel Menu.]

[回到主菜单, 进入旅行菜单.]

```
TRAVEL MENU

Fall Of 1340 86.0 Days Left

       -------7-Northwest--------   -------9-Northeast--------
       - AFC02 Vesoul 1.0-          - AFC01 Luxeil 1.0-
----------4-West----------   Current Fief     ----------6-East------
AFC05 Pesmes 1.0-            AFC04 Besancon   AFC03 Clerval 1.0-
       -------1-Southwest--------   -------3-Southeast--------
       - AFC07 Salins 1.0-          - AFC06 Pontarlie 1.0-

You Are Outside The Keep No Army Present In Fief

Choose Number Of Direction You Wish To Move, or

2. <Exa>mine Fief             5. <V>isit Court and Enter Keep
8. <Po>rt Movement            10. <A>rmies in Fief
11. <Ent>er Keep              12. <Exi>t Keep
13. <L>ist Those Outside Keep 14. <C>ombat\Dirty Deeds Menu
15. <F>ief Management         16. <Pe>rsonal Affairs Menu
17. Army <M>anagement         18. <O>nline Messages

Enter #, or <ENTER> To Exit: v
```

```
旅行菜单

1340秋季  剩余86.0天

       -------7-西北--------   -------9-东北--------
       - AFC02 Vesoul 1.0-     - AFC01 Luxeil 1.0-
----------4-西----------   当前领地         ----------6-东------
AFC05 Pesmes 1.0-          AFC04 Besancon   AFC03 Clerval 1.0-
       -------1-西南--------   -------3-东南--------
       - AFC07 Salins 1.0-     - AFC06 Pontarlie 1.0-

你正在城堡外面。这个领地当前没有军队。

选择一个数字前往你想去的方向，或者

2. <Exa>mine Fief             5. <V>isit Court and Enter Keep
8. <Po>rt Movement            10. <A>rmies in Fief
11. <Ent>er Keep              12. <Exi>t Keep
13. <L>ist Those Outside Keep 14. <C>ombat\Dirty Deeds Menu
15. <F>ief Management         16. <Pe>rsonal Affairs Menu
17. Army <M>anagement         18. <O>nline Messages

2. <Exa>(mine)检查领地        5. <V>(isit)进入城堡并访问宫廷
8. <Po>(rt) 港口移动          10. <A>(rmies)领地里的军团
11. <Ent>(er) Keep 进入城堡   14. <Exi>(t) 离开城堡
13. <L>ist 列出城堡外的人     14. <C>(ombat)战斗/肮脏勾当菜单
15. <F>(ief) 领地管理         16. <Pe>(rsonal) 个人事务菜单
17. 军团 <M>(nagement)管理    18. <O>(nline)在线消息

输入 #, 或 回车 以 退出: v
```

[The travel menu is an easy way to move around Europe. Note the use of the six sided "hexagon"
technique to regulate movement. Just like many manual games, and many computer wargames
also. The Travel Menu also allows access to nearly all the other features of the game. I decide to
visit the court of the fief I am already in.]

[I choose to "attend court" To see who is hanging around the local lords chateau. Most of the
characters here are NPCs (Non Player Characters). ]

[旅行菜单让你可以在欧洲轻松移动。注意这里使用了六角格来进行移动，像很多手工,电脑兵棋一样。在旅行菜单
也可以直接调用游戏提供的其他选项。我选择进入我正待着的领地的宫廷中。]

[我选择“进入宫廷”来看看地方领主的城堡。大多数在这的角色都是NPC（即不是玩家控制的角色）]。

```
Court

Fall Of 1340 86.0 Days Left

Fief AFC04 Besancon
The Owner Is Jeanne II de Bourgogne (156) Who Is Active.
Province Franche-Comte Kingdom HRE:Arles
The Overlord is Jeanne II de Bourgogne (156)
```

<table border="1" cellpadding="2" width="80%">
  <tbody><tr>
    <td><strong><small><code>ID</code></small></strong></td>
    <td><strong><small><code>Name</code></small></strong></td>
    <td><strong><small><code>Org</code></small></strong></td>
    <td><strong><small><code>Sex</code></small></strong></td>
    <td><strong><small><code>Type</code></small></strong></td>
    <td><strong><small><code>Comp</code></small></strong></td>
  </tr>
  <tr>
    <td><small><code>1. 156</code></small></td>
    <td><small><code>Jeanne II de Bourgogne</code></small></td>
    <td><small><code>156</code></small></td>
    <td><small><code>F</code></small></td>
    <td><small><code>PLYR*</code></small></td>
  </tr>
  <tr>
    <td><small><code>2. 465</code></small></td>
    <td><small><code>Thomas de Beauchamp</code></small></td>
    <td><small><code>156</code></small></td>
    <td><small><code>M</code></small></td>
    <td><small><code>FMLY</code></small></td>
  </tr>
  <tr>
    <td><small><code>3. 475</code></small></td>
    <td><small><code>Alais de Limbourg</code></small></td>
    <td><small><code>285</code></small></td>
    <td><small><code>F</code></small></td>
    <td><small><code>FMLY</code></small></td>
    <td><small><code>YES</code></small></td>
  </tr>
  <tr>
    <td><small><code>4. 499</code></small></td>
    <td><small><code>Philippe de Bourgogne</code></small></td>
    <td><small><code>156</code></small></td>
    <td><small><code>M</code></small></td>
    <td><small><code>FMLY</code></small></td>
  </tr>
  <tr>
    <td><small><code>5. 915</code></small></td>
    <td><small><code>Robert de Savoy</code></small></td>
    <td><small><code>156</code></small></td>
    <td><small><code>M</code></small></td>
    <td><small><code>FMLY</code></small></td>
  </tr>
  <tr>
    <td><small><code>6. 939</code></small></td>
    <td><small><code>Clare de Savoy</code></small></td>
    <td><small><code>156</code></small></td>
    <td><small><code>F</code></small></td>
    <td><small><code>FMLY</code></small></td>
  </tr>
  <tr>
    <td><small><code>7. 1015</code></small></td>
    <td><small><code>Ame de Savoy</code></small></td>
    <td><small><code>156</code></small></td>
    <td><small><code>F</code></small></td>
    <td><small><code>FMLY</code></small></td>
  </tr>
  <tr>
    <td><small><code>8. 1611</code></small></td>
    <td><small><code>Roger Baiona</code></small></td>
    <td><small><code>156</code></small></td>
    <td><small><code>M</code></small></td>
    <td><small><code>NPC</code></small></td>
  </tr>
  <tr>
    <td><small><code>9. 2038</code></small></td>
    <td><small><code>Bernard Bourg</code></small></td>
    <td><small><code>156</code></small></td>
    <td><small><code>M</code></small></td>
    <td><small><code>NPC</code></small></td>
  </tr>
  <tr>
    <td><small><code>10. 2719</code></small></td>
    <td><small><code>Sean Chateau-Renault</code></small></td>
    <td><small><code>156</code></small></td>
    <td><small><code>M</code></small></td>
    <td><small><code>NPC</code></small></td>
  </tr>
  <tr>
    <td><small><code>11. 2753</code></small></td>
    <td><small><code>Bernard Chaumont</code></small></td>
    <td><small><code>156</code></small></td>
    <td><small><code>M</code></small></td>
    <td><small><code>NPC</code></small></td>
  </tr>
</tbody></table>

```
Choose Character 1 to 11, <E> Followed By # To Examine, <N>ext Page,
or <Q>uit: 6
```

```
宫廷

1340秋季  剩余86.0天

Fief AFC04 Besancon
主人是 Jeanne II de Bourgogne (156) 他正在线.
Province Franche-Comte Kingdom HRE:Arles
领主是 Jeanne II de Bourgogne (156)
```

<table border="1" cellpadding="2" width="80%">
  <tbody><tr>
    <td><strong><small><code>ID</code></small></strong></td>
    <td><strong><small><code>名字</code></small></strong></td>
    <td><strong><small><code>组织</code></small></strong></td>
    <td><strong><small><code>性别</code></small></strong></td>
    <td><strong><small><code>类型</code></small></strong></td>
    <td><strong><small><code>Comp</code></small></strong></td>
  </tr>
  <tr>
    <td><small><code>1. 156</code></small></td>
    <td><small><code>Jeanne II de Bourgogne</code></small></td>
    <td><small><code>156</code></small></td>
    <td><small><code>F</code></small></td>
    <td><small><code>PLYR*</code></small></td>
  </tr>
  <tr>
    <td><small><code>2. 465</code></small></td>
    <td><small><code>Thomas de Beauchamp</code></small></td>
    <td><small><code>156</code></small></td>
    <td><small><code>M</code></small></td>
    <td><small><code>FMLY</code></small></td>
  </tr>
  <tr>
    <td><small><code>3. 475</code></small></td>
    <td><small><code>Alais de Limbourg</code></small></td>
    <td><small><code>285</code></small></td>
    <td><small><code>F</code></small></td>
    <td><small><code>FMLY</code></small></td>
    <td><small><code>YES</code></small></td>
  </tr>
  <tr>
    <td><small><code>4. 499</code></small></td>
    <td><small><code>Philippe de Bourgogne</code></small></td>
    <td><small><code>156</code></small></td>
    <td><small><code>M</code></small></td>
    <td><small><code>FMLY</code></small></td>
  </tr>
  <tr>
    <td><small><code>5. 915</code></small></td>
    <td><small><code>Robert de Savoy</code></small></td>
    <td><small><code>156</code></small></td>
    <td><small><code>M</code></small></td>
    <td><small><code>FMLY</code></small></td>
  </tr>
  <tr>
    <td><small><code>6. 939</code></small></td>
    <td><small><code>Clare de Savoy</code></small></td>
    <td><small><code>156</code></small></td>
    <td><small><code>F</code></small></td>
    <td><small><code>FMLY</code></small></td>
  </tr>
  <tr>
    <td><small><code>7. 1015</code></small></td>
    <td><small><code>Ame de Savoy</code></small></td>
    <td><small><code>156</code></small></td>
    <td><small><code>F</code></small></td>
    <td><small><code>FMLY</code></small></td>
  </tr>
  <tr>
    <td><small><code>8. 1611</code></small></td>
    <td><small><code>Roger Baiona</code></small></td>
    <td><small><code>156</code></small></td>
    <td><small><code>M</code></small></td>
    <td><small><code>NPC</code></small></td>
  </tr>
  <tr>
    <td><small><code>9. 2038</code></small></td>
    <td><small><code>Bernard Bourg</code></small></td>
    <td><small><code>156</code></small></td>
    <td><small><code>M</code></small></td>
    <td><small><code>NPC</code></small></td>
  </tr>
  <tr>
    <td><small><code>10. 2719</code></small></td>
    <td><small><code>Sean Chateau-Renault</code></small></td>
    <td><small><code>156</code></small></td>
    <td><small><code>M</code></small></td>
    <td><small><code>NPC</code></small></td>
  </tr>
  <tr>
    <td><small><code>11. 2753</code></small></td>
    <td><small><code>Bernard Chaumont</code></small></td>
    <td><small><code>156</code></small></td>
    <td><small><code>M</code></small></td>
    <td><small><code>NPC</code></small></td>
  </tr>
</tbody></table>

```
输入 1-11 选择角色, <E> 后接 # 以进行检查, <N>(ext) 跳转下一页,
或 <Q>(uit)退出: 6
```

[Well, well, it seems I have come upon the family of the owner. There is Jeanne II de Bourgogne,
obviously the widow who now runs the place. The others belonging to "Org(anization)" 156 are
her children and Thomas de Beauchamp must be the husband of one of her daughters. I think I'll
get to know one of the daughters.]

[吼啊，看起来我跑到主人家里了。这位Jeanne II de Bourgogne显然作为寡妇统治着这里。其他属于“组织”156
的是她的孩子，而Thomas de Beauchamp则为她一个女儿的丈夫，我想我要去了解一下她几个女儿中的一个。]

```
This is Clare de Savoy (939) who is Married.
She is Not Pregnant
Current Health 5 Maximum Health 5
Age 21 Sex f Language F2 Loyalty 3
Management 8 Guile 4 Leadership 1 Stature 1.0
Protection 1 Endurance 3 Attack Value 2
Tournament 3 Sire ID 177 Org Id 156
 Berserker 1
 Collector 4
 Evil Eye 7
 Insightful of people 9
 Insightful of Self 2
 Keepmaster 1
 Siegecraft 6
 Sorcery 6
Press <ENTER> to continue.
```

```
这位是 Clare de Savoy (939) 她已经结婚了.
她没有怀孕
当前健康值 5 最大健康值 5
年龄 21 性别 f 语言 F2 忠诚 3
管理 8 狡诈 4 领导力 1 声望 1.0
保护 1 忍耐 3 攻击值 2
竞技 3 Sire ID 177 Org Id 156
 狂战士 1
 收集者 4
 邪眼 7
 对人类的洞察力 9
 对自我的洞察力 2
 城堡管理 1
 攻城 6
 巫术 6
按 回车 以 继续.
```

[Hmmm, young Clare is certainly a piece of work, Great manager, lousy leader and a taste for
the occult. A married witch, let's see if we can get acquainted....]

[Emmm, 年轻的Clare是一个这样的人。她是很好的管理者，恶心（lousy）的领导者，以及喜爱超自然的东西。
一个已婚的女巫，让我们看看我们能不能进一步了解她。。]

```
Current Character: 939 Clare de Savoy

1. <E>xamine Character
2. <H>ire NPC
3. <S>educe
4. <A>dd To Traveling Companions
5. <R>emove As Traveling Companion
6. <ENTER> To Quit

 Enter # 3
 
Sire, what type of lady do you take me for!
Press <ENTER> to continue.
Seduction Takes One Day.
Year: 1340 Season: Fall Days Left: 85.0
Press <ENTER> to continue.
```

```
当前选定角色: 939 Clare de Savoy

1. <E>(xamine) 检视该角色
2. <H>(ire) 雇佣NPC
3. <S>(educe) 勾引
4. <A>(dd) 将其加入旅行同伴
5. <R>(emove) 将其移除出旅行同伴
6. 回车 以 退出

 输入 # 3
 
大人，你给我找了个怎样的小姐啊！
输入 回车 以继续
勾引花掉一天
1340年 秋季 剩余85天
输入 回车 以 继续
```

[Hmmm, these young wives can be unpredictable. But let's try again.]

[Emmmm, 这些年轻的有妇之夫的态度啊，就是不可预料，让我们再试一次。]

```
Enter # 3
Let us steal away to a place of peace and quiet...
Press <ENTER> to continue.
Seduction Takes One Day.
Year: 1340 Season: Fall Days Left: 81.0
Press <ENTER> to continue.
```

```
输入 # 3
让我们偷偷找一个僻静的地方...
输入 回车 以 继续.
勾引花掉了一天.
1340年秋季 剩余81.0
输入 回车 以 继续.
```

[Ahhh, much better. Chivalry lives, in the shadows. Hanky panky was included as a game
function because it was quite common in the 14th century. In fact, you can't have a realistic
game of the Hundred Years War without adultery. It seems that a major problem the French had
was the ruling family, the Valois. At this point in time the Valois were "genetically challenged."
As the game simulates the passing of characteristics by both parents to their children, it would
have taken several generations of outstanding Valois wives to breed all the bad characteristics
out of the line. France could not wait that long. One of the French kings half way through the
game was totally loopy and his wife was receptive to the attentions of other nobles. This resulted
in a Valois heir that was not a Valois (the queen publicly admitted as much.) France noted that
the illegitimate Valois was a much smoother article than the genuine Valois and accepted the
bastard heir. This did much to turn things around for the French.]

[吼啊。骑士精神总是活在如此的阴影之下。游戏中包括做这样的苟且之事的功能因为这种事在14世纪的确常见。
事实上，你不能在一个号称真实的百年战争游戏中不包含通奸内容。似乎法兰西最大的问题就是它的通知家族，
Valois。这个时间点Valois是“基因上出现了偏差”，正如游戏设计使得父母的特性会遗传给子女，
Valois家族也将会需要几代优秀的夫人来把劣等基因移除出去。法兰西不能等待那么久，
一位法王在游戏时间的一半都处于精神错乱中，从而他的妻子就引起了各个贵族的注意。这导致了Valois的继承人
其实并不是Valois的种（王后公开承认这一点），法兰西觉得这个非法的Valois比真正的Valois更合适，
并接受这个野种作为继承人。这个跟法兰西的命运有很大的关系。]

[Back at the Travel Menu, I go to the Army Management Menu, I proceed to hire some troops by
Recruiting in the Current Fief. This I can do immediately by offering local troops money to
follow my banner. This cannot gather many troops, but when you need some soldiers in a hurry,
this is the way to go. Gathering a large army, the "Call to Arms," takes several months and
everyone knows about it.]

[回到旅行菜单，进入军队管理菜单，我通过在当前领地征兵来组建军队。我可以通过给当地军事团体一些钱
来让它们立即追随我的旗帜。这个方法并不能招到很多军队，但是当你需要迅速招到一些战士时是有用的。
召集大军需要使用“战斗动员”（Call to Arms）]，这将消耗几个月并且被所有人知道。

```
Army Management

1. <C>all To Arms
2. <R>ecruit In Current Fief
3. <A>rmy Status
4. <D>isband Army
5. <M>uster Out
6. <S>tanding Order
7. <T>ransfer Troops
8. <P>ick Up Troops Responding To Call To Arms
9. Assemble <F>leet
999. Move To Main HYW Menu

Enter #, or <ENTER> To Exit: r

Purse: 877.00 Kducats

Soldiers cost 1 Kducats Per Soldier Per Season.
You must, also, pay a 1 Kducat recruiting fee.
How many soldiers do you wish to hire: 200
You recruited:
 16 Knights
 7 Men At Arms
 0 Yeomen
177 Foot
Your recruiting took 3 days.

Year: 1340 Season: Fall Days Left: 76.0

Press <ENTER> to continue.
```