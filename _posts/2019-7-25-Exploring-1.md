---
layout:     post
title:      "探索历史大数据"
subtitle:   "Exploring Big Historical Data: The Historian's Macroscope"
date:       2019-7-25 9:00:00
author:     "弦望晦朔"
header-img: "img/post/post-digitalhistory-1.jpg"
tags:
    - Digital History
    - 历史学
    - 探索历史大数据系列
---

# 1.前言

当我看完《探索历史大数据：历史学家的宏观视角》（原书名：**Exploring Big Historical Data : The Historian's Macroscope**）的第一章的时候，我就想着要给这本书里的内容做一个索引和整理了。如今距我开始阅读这本书已过去了很久的时间，我还是未能很好的掌握书中所介绍的所有方法和工具，这一方面，是因为我时间和精力的有限，另外一方面，也是因为这本书所带来的方法和工具太过于繁多以至于无法在短期内完全消化。

 

因此，我决定把这本书单独拆出来，以6~8次推文的形式，将它全书所介绍的方法和工具做一个系统性的描述和说明。



这一次推文的主要目的是对**Digital History**领域进行一个简要的介绍并对整书整体的架构进行一个简要的梳理，在简要介绍的阶段，我将会援引一些有关于此领域的有趣的项目进行介绍。



# **2.Digital History是什么**

那么迅速进入我们的正题，**Digital History**是什么？维基百科给出的解释是：

>  *Digital history is the use of digital media to further historical analysis, presentation, and research. It is a branch of the Digital humanities and an extension of quantitative history, cliometrics, and computing. Digital history is commonly digital public history, concerned primarily with engaging online audiences with historical content, or, digital research methods, that further academic research. Digital history outputs include: digital archives, online presentations, data visualizations, interactive maps, time-lines, audio files, and virtual worlds to make history more accessible to the user. A researcher can interact with, explore and visualise, the output more easily than with conventional historiographical material. Recent digital history projects focus on creativity, collaboration, and technical innovation, text mining, corpus linguistics, network analysis, 3D Modeling, and big data analysis. Utilising these resources the user can rapidly develop new analyses that can link to, extend, and bring to life existing histories.*][1]

 

经过这段非常官方的阐述以后，我想你大概对**Digital History**有一个初步的认识了，当然，如果你不愿意看这么一大串官方而又干巴巴的介绍的话，我想我可以推荐你打开浏览器，使用任意的搜索引擎，然后在搜索框内键入“What is Digital Humanities[2]”，点击进入搜索到的有此URL的网站，看完一条，就刷新一次，直到你觉得你已经充分了解到什么是**Digital Humanities**以后，就可以关闭它了，因为每一次刷新，它都会给出你一个新的解释。

![/img/post/digitalhistory-1/1.png](/img/post/digitalhistory-1/1.png)

*图1 "What Is Digital Humanities?"*



相比起维基百科的长篇大论，"Broadly"这个解释真是简单易懂了。事实上，这个网站本身也是**Digital Humanities**的一部分，一个可视化展示自己成果的网页。



有关于**Digital History**和**Digital Humanities**的区别，现在你可以把它们视作等价，或是把**Digital History**视作**Digital Humanities**的一个下属分支，他们具体的区别，我们将在之后的章节进行讨论。

 

那么就让我们开始介绍一些**Digital History**领域有趣的项目。



哈佛和北大有一个合作项目——中國歷代人物傳記資料庫（CBDB）[3]，它最近一次的更新在2019年4月，这个数据库中收录了从唐到清约42万名人物的传记资料，它将一个一个历史人物的生平模式化，其中囊括了一个人的出生地，求学地，仕宦地址，任官，父母，配偶，著作等等社会行动。它的一个很大的用处是作为群体传记学的的分析工具。当然，倘若把它与CHGIS（中国历史地理信息系统）[4]进行搭配，又可进行许多有趣的分析，比如朝代人口的地理流动。



倘若不把眼光立足于中国，而是立足于世界呢？

ORBIS（*The Stanford Geospatial Network Model of the Roman World*）[5]是一个很有趣的GIS项目，简要的介绍一下的话，就是它复原了罗马世界的交通运输路线，相应的根据季节变换，交通路线也会有新的变动，以便于进行相应时代的事件的分析。



![/img/post/digitalhistory-1/5.png](/img/post/digitalhistory-1/5.png)

*图2 " The Stanford Geospatial Network Model of the Roman World "*

 

如上部分介绍的**Digital History**的项目都倾向于宏观层面，微观层面也有很多有意思的项目，比如说*Trading Consequences*[6],它收集了19世纪诸多的贸易数据，你可以通过地点或者商品进行检索，以帮助你了解19世纪的贸易情况。

我们都知道英美法系还有一个名字叫做"判例法系"，*Old Bailey*[7]记录了伦敦从1674年到1913年的诸多案例，以供社会各界人士进行查阅。

 

# **3.《探索历史大数据》框架**

这本书共7章，大致说来，可分为三个部分。

前两章是本书的第一个部分，作为对该领域的总体性概括，从**Digital History**的各类项目，援引到**Digital History**的起源与发展历史，并对如何获取想要的历史数据做了简要的描述。

第二部分的重点在于文本分析与主题建模上，这一部分我认为实际上是入门者最痛苦的一个部分，虽然都是基于现有的工具，但是使用工具的能力强弱依据于你的技能技巧是否纯熟，我在图3中将我个人认为需要熟练运用这些工具的技能技巧做了一个简单的总结和概括，需要说明的是，这些工具是作者在本书中给出的，但我个人认为可以用来替代的工具还有许多，如进行文本分析的词频分析时，许多工具不支持中文，这时候可以利用Python的中文分词包（如Jieba、THULAC等），在Python中自写一个词频统计小工具，又比如可视化阶段，本书没有给出任何工具，但你可以使用SPSS，或R语言，Python的matplotlib进行绘图，在最后进行网络运用的阶段，Neo4j也是一个不错的可以选择使用的工具。总的来说，我觉得在选取工具的使用方面，不必拘泥于工具，而更应该关注工具使用的意义。

第三部分内容主要是网络分析，在这一部分，你将面临着与上述部分完全不同的困难，即，信息论，图论等相关内容的学习和思考，这一部分更倾向于计科，目前我正在恶补这方面的知识，以期在做到这方面的相关介绍的时候，能够提交一个自己满意的文本。

![/img/post/digitalhistory-1/3.png](/img/post/digitalhistory-1/3.png)

*图3 探索历史大数据简略思维导图*

 

# **4.小结**

原书中序言对本书三个作者的成长经历都做了一段大概的梳理，序言的最后一段有这么一句话，我非常喜欢：“**将我们的个人经历联系在一起就会发现一个关键的共同点，即尽管走了一些弯路，但我们都渴望通过现象看到本质。**”

**Digital History**目前仍然是一个尚未成熟的领域，它可能仅仅是提供了一种方法而非一种视野和观点，但是在我们还囿于固有的视野和观点中的时候，方法的革新或许会带来视野的革新，这也是我对**Digital History**满怀希望的一个重要的原因，毕竟我们都希望透过现象，看到本质。

有关于**Digital History**领域这本书实质上还只是一个入门，在阅读完本书以后，**Programing Historian**[8]提供了诸多**Digital History**领域的实用技巧，《**Digital History : A Guide to Gathering,Preserving and Presenting the Past on the Web**》[9]同样也是一本非常好的入门教材，在接下来这一系列的推文中，我会综合在这个领域中我看到的各种书籍，以期做一个相对完善的介绍。

 

# 5.参考文献

[1]    [Digital history[J]. Wikipedia, 2019.](<https://en.wikipedia.org/wiki/Digital_history>)

[2]    [HEPPLER J A. What Is Digital Humanities?](<https://whatisdigitalhumanities.com/>)

[3]   [中國歷代人物傳記資料庫（CBDB）[EB/OL]. [2019-07-04].](https://projects.iq.harvard.edu/chinesecbdb.) 

[4]    [CHGIS[EB/OL]. [2019-07-04].]( http://www.people.fas.harvard.edu/~chgis/.)

[5]    [ORBIS: The Stanford Geospatial Network Model of the Roman World[EB/OL]. [2019-07-04].]( http://orbis.stanford.edu/.)

[6]  [Access the Data:Trading Consequences[EB/OL]. [2019-07-05]](http://tradingconsequences.blogs.edina.ac.uk/access-the-data/.)

[7]    [Old Bailey Online - The Proceedings of the Old Bailey, 1674-1913 - Central Criminal Court[EB/OL]. [2019-07-04].](https://www.oldbaileyonline.org/index.jsp.)

[8]    [The Programming Historian[J]. Programming Historian, .](https://programminghistorian.org)

[9]    [Digital History: A Guide to Gathering, Preserving, and Presenting the Past on the Web[EB/OL]. [2019-07-04].](http://chnm.gmu.edu/digitalhistory/.)