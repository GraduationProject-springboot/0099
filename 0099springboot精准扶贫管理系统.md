# 0099springboot精准扶贫管理系统

### 点击播放视频 ▼
[![Watch the video](https://i.sstatic.net/Vp2cE.png)](https://player.bilibili.com/player.html?isOutside=true&aid=BV16ia6epENY&bvid=BV16ia6epENY&cid=500001610579795&p=100)

### [所有项目](https://github.com/GraduationProject-springboot/allSpringbootProjects) 包安装运行












精准扶贫管理系统

摘要

随着信息技术在管理上越来越深入而广泛的应用，管理信息系统的实施在技术上已逐步成熟。本文介绍了精准扶贫管理系统的开发全过程。通过分析精准扶贫管理系统管理的不足，创建了一个计算机管理精准扶贫管理系统的方案。文章介绍了精准扶贫管理系统的系统分析部分，包括可行性分析等，系统设计部分主要介绍了系统功能设计和数据库设计。

本精准扶贫管理系统管理员和用户。管理员功能有个人中心，用户管理，贫困户管理，热门新闻管理，新闻类型管理，志愿者招聘管理，用户招聘管理，留言板管理，系统管理等。用户功能有个人中心，贫困户管理，用户应聘管理，我的收藏管理。因而具有一定的实用性。

本站是一个B/S模式系统，采用Spring
Boot框架，MYSQL数据库设计开发，充分保证系统的稳定性。系统具有界面清晰、操作简单，功能齐全的特点，使得精准扶贫管理系统管理工作系统化、规范化。本系统的使用使管理人员从繁重的工作中解脱出来，实现无纸化办公，能够有效的提高精准扶贫管理系统管理效率。

**关键词：**精准扶贫管理系统；Spring Boot框架；MYSQL数据库

**Abstract**

With the deepening and extensive application of information technology
in management, the implementation of management information systems has
gradually matured in technology. This article introduces the whole
process of the development of the precision poverty alleviation
management system. By analyzing the management deficiencies of the
precision poverty alleviation management system, a computer-managed
precision poverty alleviation management system was created. The article
introduces the system analysis part of the precision poverty alleviation
management system, including feasibility analysis, etc. The system
design part mainly introduces the system function design and database
design.

Administrators and users of this precision poverty alleviation
management system. Administrator functions include personal center, user
management, poor household management, hot news management, news type
management, volunteer recruitment management, user recruitment
management, message board management, system management, etc. User
functions include personal center, poor household management, user
application management, and my collection management. So it has a
certain practicability.

This site is a B/S model system, using Spring Boot framework, MYSQL
database design and development, fully guarantee the stability of the
system. The system has the characteristics of clear interface, simple
operation and complete functions, which makes the management of the
precision poverty alleviation management system systematized and
standardized. The use of this system frees managers from heavy work,
realizes paperless office, and can effectively improve the management
efficiency of the precision poverty alleviation management system.

**Keywords:** Precision poverty alleviation management system; Spring
Boot framework; MYSQL database

目录

[1系统概述 1](#系统概述)

[1.1 研究背景 1](#__RefHeading___Toc19234)

[1.2研究目的 1](#__RefHeading___Toc4125)

[1.3系统设计思想 1](#系统设计思想)

[2相关技术 2](#相关技术)

[2.1 MYSQL数据库 2](#mysql数据库)

[2.2 B/S结构 3](#bs结构)

[2.3 Spring Boot框架简介 4](#spring-boot框架简介)

[3系统分析 4](#系统分析)

[3.1可行性分析 4](#可行性分析)

[3.1.1技术可行性 4](#技术可行性)

[3.1.2经济可行性 5](#经济可行性)

[3.1.3操作可行性 5](#操作可行性)

[3.2系统性能分析 5](#系统性能分析)

[3.2.1 系统安全性 5](#系统安全性)

[3.2.2 数据完整性 6](#数据完整性)

[3.3系统界面分析 6](#__RefHeading___Toc19903)

[3.4系统流程和逻辑 7](#系统流程和逻辑)

[4系统概要设计 8](#系统概要设计)

[4.1概述 8](#概述)

[4.2系统结构 9](#系统结构)

[4.3.数据库设计 9](#数据库设计)

[4.3.1数据库实体 9](#数据库实体)

[4.3.2数据库设计表 11](#数据库设计表)

[5系统详细实现 14](#系统详细实现)

[5.1 管理员模块的实现 14](#管理员模块的实现)

[5.1.1 用户信息管理 14](#用户信息管理)

[5.1.2 贫困户信息管理 15](#贫困户信息管理)

[5.1.3 新闻类型管理 15](#新闻类型管理)

[5.1.4 志愿者招聘管理 16](#志愿者招聘管理)

[5.2 用户模块的实现 17](#用户模块的实现)

[5.2.2 志愿者招聘 17](#志愿者招聘)

[5.2.3 留言反馈管理 17](#留言反馈管理)

[5.2.3 贫困户 18](#贫困户)

[6系统测试 19](#系统测试)

[6.1概念和意义 19](#概念和意义)

[6.2特性 20](#特性)

[6.3重要性 20](#重要性)

[6.4测试方法 20](#测试方法)

[6.5 功能测试 21](#功能测试)

[6.6可用性测试 21](#可用性测试)

[6.7性能测试 22](#性能测试)

[6.8测试分析 22](#测试分析)

[6.9测试结果分析 23](#测试结果分析)

[结论 23](#结论)

[致谢语 23](#致谢语)

[参考文献 24](#参考文献)

# 

# 1系统概述

[]{#__RefHeading___Toc19234 .anchor}1.1 研究背景

随着计算机技术的发展以及计算机网络的逐渐普及，互联网成为人们查找信息的重要场所，二十一世纪是信息的时代，所以信息的管理显得特别重要。因此，使用计算机来管理精准扶贫管理系统的相关信息成为必然。开发合适的精准扶贫管理系统，可以方便管理人员对精准扶贫管理系统的管理，提高信息管理工作效率及查询效率，有利于更好的为人们服务。

[]{#__RefHeading___Toc4125 .anchor}1.2研究目的

随着互联网技术的快速发展，网络时代的到来，网络信息也将会改变当今社会。各行各业在日常企业经营管理等方面也在慢慢的向规范化和网络化趋势汇合。精准扶贫管理系统的信息化程度体现在将互联网与信息技术应用于经营与管理，以现代化工具代替传统手工作业。无疑，使用网络信息化管理使信息管理更先进、更高效、更科学，信息交流更迅速。

对于之前精准扶贫管理系统的管理，大部分都是使用传统的人工方式去管理，这样导致了管理效率低下、出错频率高。而且，时间一长的话，积累下来的数据信息不容易保存，对于查询、更新还有维护会带来不少问题。对于数据交接也存在很大的隐患。如果采用电子化的存储方式就会带来很大的改善，而且给用户的查询带来了很大便利，因此设计一个精准扶贫管理系统刻不容缓，能够提高信息的管理水平。

## 1.3系统设计思想

一个成功的网站应明确建设网站的目的，确定网站的功能，确定网站规模、投入费用，进行必要的市场分析等。只有详细的策划，才能避免在网站建设中出现的很多问题，使网站建设能顺利进行。同时，一个大型的计算机网站系统，必须有一个正确的设计指导思想，通过合理选择数据结构、网络结构、操作系统以及开发环境，构成一个完善的网络体系结构，才能充分发挥计算机信息管理的优势。根据现实生活中网民的实际需求，本系统的设计按照下述原则进行。

1.  有效性：实际上这里的有效性包括两个方面的意思：有用性和可用性。有用性是指站点潜在的能满足用户需求的功能，而可用性是指能够通过站点的操作实现特定的目标。可以看出一个站点如果不能恰当运行或设计得非常槽糕就不是一个好站点。可用站点的效益应该非常高，并易于学习，在实现用户目标时令人满意而不出错。

2.  高可靠性：一个实用的网站同时必须是可靠的，本设计通过合理而先进的网络设计以及软、硬件的优化选型，可保证网站的可靠性与容错性。

3.  高安全性：在设计中，将充分利用网络软、硬件提供的各种安全措施，既可以保证用户共享资源，充分考虑系统及数据资源的容灾、备份、恢复的要求。为系统提供强大的数据库备份工具。可以保证关键数据的安全性。操作权限级，设置不同的角色确保每一步的操作权限，可以由管理员进行设置。

4.  先进性：采用目前国际上最先进的开发技术，使用JSP开发技术，MYSQL作为网站后台数据库。采用这些技术降低了以后的系统运营成本，提高了系统的稳定性和易维护性。

5.  采用标准技术：本网站的所有设计遵循国际上现行的标准进行，以提高系统的开放性。

6.  外观和技术平衡：系统采用Web风格的界面设计，界面友好、美观，使用方便，易学易用。网站设计的关键问题是外观和技术的平衡。外现不好的网站令人厌烦，站点可以运行很好，但却不能带动用户积极性，相反，如果外观非常有表现力，但技术有限，用户则会感到非常失望。在外观与技术之间需要确定一个清晰而连续的关系，即外观与站点的意图相关，对不同类型的网站处理方法不同。

# 2相关技术

## 2.1 MYSQL数据库

MySQL是一个真正的多用户、多线程SQL数据库服务器。
是基于SQL的客户/服务器模式的关系数据库管理系统，它的有点有有功能强大、使用简单、管理方便、安全可靠性高、运行速度快、多线程、跨平台性、完全网络化、稳定性等，非常适用于Web站点或者其他应用软件的数据库后端的开发工作。此外，用户可利用许多语言编写访问MySQL数据库的程序。作为开放源代码运动的产物之一，MySQL关系数据库管理系统越来越受到人们的青睐，应用范围也越来越广。速度和易用性使MySQL特别适用于Web站点或应用软件的数据库后端的开发工作。

MYSQL数据库具有以下特点：

1、C和C ++中使用和测试，以确保源代码的编译器的便携性和灵活性。

2、支持多种操作系统AIX的，FreeBSD下，HP-UX，Linux和Mac
OS中，Novell公司的Netware，OpenBSD系统，OS/2裹时，Solaris，Windows等。

3、提供了用于不同的编程语言的API。编程语言，如C,, C
++，Python和Java的，的Perl，PHP，埃菲尔铁塔，Ruby和Tcl的。

4、以及使用的CPU资源来支持多线程。

5、算法优化查询SQL，切实提高搜索速度。

6、网络上的客户端和服务器可以用来编程任何独立的编程环境，也有中国，GB2312，BIG5，日文写作，一般基金，用于支持多国语言，并且可以嵌入在数据表和其他软件shift_jis访问柱可以用作的名称。

7、TCP / IP，ODBC和JDBC数据库，并提供连接到其他。

8、管理工具的管理，控制和优化数据库的操作。

9、可以数以千万计的记录在一个大的数据库。

## 2.2 B/S结构

B/S架构是一种基于互联网系统的软件系统开发架构，是现如今在软件系统开发中采用非常大量的一种软件系统结构。现如今B/S架构已经被大量使用，打破了C/S结构的结构，给基于网络结构的软件系统提供了良好的支持。B/S架构伴随着计算机网络技术发展而逐步的发展和更新。伴随着互联网的进一步发展，就要求大多数的管理系统要求不仅仅可以在一台电脑上使用，同时可以在接入互联网的其他电脑也可以使用对系统进行操作和使用。在这样的背景下基于B/S架构的软件系统设计方法得到了越来越大量的使用，基础部分也在不断的更新。

B/S架构是利用操作系统中的浏览器来进行使用的，不是一种窗体软件系统，不需要在使用系统的电脑上进行安装。B/S架构的运行方式是在远程的服务器上把开发的软件系统部署在远程的服务器上，在部署好软件系统之后就可以实现在任何接入互联网的电脑上访问部署好的软件系统。B/S架构给使用管理系统的用户带来极大的便利。

在三层体系结构的B/S（Browser/Server，浏览器/服务器结构）系统中，用户可以通过浏览器向分布在网络上的众多服务器发出请求。B/S系统极大地简化了客户机的工作量，客户机上只需要安装、配置少量的客户端运行软件即可，服务器将担负大量的工作，对数据库的访问以及应用程序的执行都将由服务器来完成。

B/S架构的不断成熟，主要使用WWW浏览器技术，结合多种浏览器脚本语言，用通用浏览器需要实现原本复杂的专有软件来实现的强大功能，并节约了开发成本，是一种新的软件架构。B/S系统包括：表示逻辑层，控制逻辑层，数据展现层，三层是相对独立又相互关联。

## 2.3 Spring Boot框架简介

Spring
Boot是由Pivotal团队提供的全新[框架](https://baike.baidu.com/item/框架/1212667)，其设计目的是用来[简化](https://baike.baidu.com/item/简化/3374416)新[Spring](https://baike.baidu.com/item/Spring/85061)应用的初始搭建以及开发过程。该框架使用了特定的方式来进行配置，从而使开发人员不再需要定义样板化的配置。通过这种方式，Spring
Boot致力于在蓬勃发展的快速应用开发领域(rapid application
development)成为领导者。

SpringBoot可以与经典的Java开发工具一起使用或者作为命令行工具安装。无论如何，需要JavaSDK1.6或者更高版本，本项目用到的是JDK1.8版本。

# 3系统分析

## 3.1可行性分析

通过对本精准扶贫管理系统实行的目的初步调查和分析，提出可行性方案并对其一一进行论证。我们在这里主要从技术可行性、经济可行性、操作可行性等方面进行分析。

### 3.1.1技术可行性

本精准扶贫管理系统采用SSM框架，JAVA作为开发语言，是基于WEB平台的B/S架构系统。

（1）Java提供了稳定的性能、优秀的升级性、更快速的开发、更简便的管理、全新的语言以及服务。整个系统帮用户做了大部分不重要的琐碎的工作。

（2）基于B/S模式的系统的开发已发展日趋成熟。

（3）众所周知，Java是面向对象的开发语言。程序开发员可以在Eclipse平台上面方便的使用一些已知的解决方案。
  

因此，精准扶贫管理系统在开发技术上具有很高可行性，且开发人员掌握了一定的开发技术，所以此系统的开发技术具有可行性。

### 3.1.2经济可行性

本精准扶贫管理系统采用的软件都是开源的，这样能够削减很多的精力和资源，降低开发成本。同时对计算机的配置要求也极低，即使是淘汰下来的计算机也能够满足需要，因此，本系统在经济上是完全具有可行性的，所以在经济上是十分可行的。

### 3.1.3操作可行性

本精准扶贫管理系统的界面简单易操作，用户只要平时有在用过电脑，都能进行访问和操作。本系统具有易操作、易管理、交互性好的特点，在操作上是非常简单的，因此在操作上具有很高的可行性。

综上所述，此系统开发目标已明确，在技术、经济和操作方面都具有很高的可行性，并且投入少、功能完善、管理方便，因此系统的开发是完全可行的。

## 3.2系统性能分析

### 3.2.1 系统安全性

此精准扶贫管理系统要严格控制管理权限，具体要求如下：

（1）要想对精准扶贫管理系统进行管理，首先要依靠用户名和密码在系统中登陆，无权限的用户不可以通过任何方式登录系统和对系统的任何信息和数据进行查看，这样可以保证系统的安全可靠性和准确性。

（2）在具体实现中对不同的权限进行设定，不同权限的用户在系统中登陆后，不可以越级操作。

### 3.2.2 数据完整性

（1）所有记录信息要保持全面，信息记录内容不可以是空。

（2）各种数据间相互联系要保持正确。

（3）相同数据在不同记录中要保持一致。

[]{#__RefHeading___Toc19903 .anchor}3.3系统界面分析

目前，界面设计已经成为对软件质量进行评价的一条关键指标，一个好的用户界面可以使用户使用系统的信心和兴趣增加，从而使工作效率提高，Spring
Boot框架是将JAVA语言作为脚本语言的，JSP网页给整个服务器端的JAVA库单元提供了一个接口用来服务HTTP的应用程序。创建动态页面比较方便。客户界面是指软件系统与用户交互的接口，往往涵盖输出、输入、人机对话的界面格式等。

1.输出设计

输出是由电脑对输入的基本信息进行解决，生成高质量的有效信息，并使之具有一定的格式，提供给管理者使用，这是输出设计的主要责任和目标。

系统开发的过程与实施过程相反，并不是从输入设计到输出设计，而是从输出设计到输入设计。这是由于输出表格与使用者直接相联系，设计的目的应当是确保使用者可以很方便的使用输出表格，并且可以将各部门的有用信息及时的反映出来。输出设计的准绳是既要整体琢磨不同管理层的所有需要，又要简洁，不要提供给用户不需要的信息。

2.输入设计

输入数据的收集和录入是比较麻烦的，需要非常多的人力和一定设备，而且经常出错。一旦输入系统的数据不正确，那么处理后的输出就会扩大这些错误，因此输入的数据的准确性对整个系统的性能起着决定性意义。

输入设计有以下几点原则：

1）输入量应尽量保持在能够满足处理要求的最低限度。输入量越少，错误率就会越少，数据的准备时间也越少。

2）应尽可能的使输入的准备以及输入的过程进行时比较方便，这样使错误的发生率降低。

3）应尽量早检查输入数据（尽量接近原数据发生点）,以便使错误更正比较及时。

4）输入数据尽早地记录成其处理所需的形式，以防止数据由一种介质转移到另一种介质时需要转录而可能发生的错误。

## 3.4系统流程和逻辑

![](media/image1.wmf)

图3-3登录流程图

![](media/image2.wmf)

图3-4修改密码流程图

# 4系统概要设计

## 4.1概述

本系统采用B/S结构(Browser/Server,浏览器/服务器结构)和基于Web服务两种模式，是一个适用于Internet环境下的模型结构。只要用户能连上Internet,便可以在任何时间、任何地点使用。系统工作原理图如图4-1所示：

![](media/image3.wmf)

图4-1系统工作原理图

## 4.2系统结构

本系统是基于B/S架构的网站系统，设计的功能结构图如下图所示：

![](media/image4.wmf)

图4-2功能结构图

## 4.3.数据库设计

### 4.3.1数据库实体

概念设计的目标是设计出反映某个组织部门信息需求的数据库系统概念模式，数据库系统的概念模式独立于数据库系统的逻辑结构、独立于数据库管理系统（DBMS）、独立于计算机系统。

概念模式的设计方法是在需求分析的基础上，用概念数据模型（例如E-R模型）表示数据及数据之间的相互联系，设计出反映用户信息需求和处理需求的数据库系统概念模式。概念设计的目标是准确描述应用领域的信息模式，支持用户的各种应用，这样既容易转换为数据库系统逻辑模式，又容易为用户理解。数据库系统概念模式是面向现实世界的数据模型，不能直接用于数据库系统的实现。在此阶段，用户可以参与和评价数据库系统的设计，从而有利于保证数据库系统的设计与用户的需求相吻合。在概念模式的设计中，E-R模型法是最常见的设计方法。本系统的E-R图如下图所示：

（1）管理员信息的实体属性图如下：

![](media/image5.wmf)

图4.12 管理员信息实体属性图

（2）新闻类型信息实体属性图如图4.13所示：

![](media/image6.wmf)

图4.13 新闻类型信息实体属性图

（3）留言板信息实体属性图如图4.14所示：

![](media/image7.wmf)

图4.14 留言板信息实体属性图

### 4.3.2数据库设计表

精准扶贫管理系统需要后台数据库，下面介绍数据库中的各个表的详细信息：

表4.1 留言板

  ----------- -------------- ---- ------------------- ----------------------------------
     字段          类型       空         默认                        注释

   id (主键)    bigint(20)    否                                     主键

    addtime     timestamp     否   CURRENT_TIMESTAMP               创建时间

    userid      bigint(20)    否                                   留言人id

   username    varchar(200)   是         NULL                       用户名

    content      longtext     否                                   留言内容

     reply       longtext     是         NULL                      回复内容
  ----------- -------------- ---- ------------------- ----------------------------------

表4.2 贫困户

  -------------------- -------------- ---- ------------------- ----------------------------
          字段              类型       空         默认                     注释

       id (主键)         bigint(20)    否                                  主键

        addtime          timestamp     否   CURRENT_TIMESTAMP            创建时间

        bianhao         varchar(200)   是         NULL                     编号

    jiatingchengyuan    varchar(200)   是         NULL                   家庭成员

    chengyuanrenshu       int(11)      是         NULL                   成员人数

     jiatingzhuzhi      varchar(200)   是         NULL                   家庭住址

   jiatingzhuangkuang     longtext     是         NULL                   家庭状况

        fengmian        varchar(200)   是         NULL                     封面

      renjunshouru        int(11)      是         NULL                   人均收入

     xiangxijieshao       longtext     是         NULL                   详细介绍

        zhanghao        varchar(200)   是         NULL                     账号

        xingming        varchar(200)   是         NULL                     姓名

          sfsh          varchar(200)   是          否                    是否审核

          shhf            longtext     是         NULL                   审核回复

       clicktime          datetime     是         NULL                 最近点击时间

        clicknum          int(11)      是           0                    点击次数
  -------------------- -------------- ---- ------------------- ----------------------------

表4.3 热门新闻

  --------------- -------------- ---- ------------------- --------------------------------
       字段            类型       空         默认                       注释

     id (主键)      bigint(20)    否                                    主键

      addtime       timestamp     否   CURRENT_TIMESTAMP              创建时间

      biaoti       varchar(200)   是         NULL                       标题

   xinwenleixing   varchar(200)   是         NULL                     新闻类型

      neirong        longtext     是         NULL                       内容

    fabushijian        date       是         NULL                     发布时间

     fengmian      varchar(200)   是         NULL                       封面

     clicktime       datetime     是         NULL                   最近点击时间

     clicknum        int(11)      是           0                      点击次数
  --------------- -------------- ---- ------------------- --------------------------------

表4.4 收藏表

  ----------- -------------- ---- ------------------- ----------------------------------
     字段          类型       空         默认                        注释

   id (主键)    bigint(20)    否                                     主键

    addtime     timestamp     否   CURRENT_TIMESTAMP               创建时间

    userid      bigint(20)    否                                    用户id

     refid      bigint(20)    是         NULL                       收藏id

   tablename   varchar(200)   是         NULL                        表名

     name      varchar(200)   否                                   收藏名称

    picture    varchar(200)   否                                   收藏图片
  ----------- -------------- ---- ------------------- ----------------------------------

表4.5 管理员表

  ----------- -------------- ---- ------------------- ----------------------------------
     字段          类型       空         默认                        注释

   id (主键)    bigint(20)    否                                     主键

   username    varchar(100)   否                                    用户名

   password    varchar(100)   否                                     密码

     role      varchar(100)   是        管理员                       角色

    addtime     timestamp     否   CURRENT_TIMESTAMP               新增时间
  ----------- -------------- ---- ------------------- ----------------------------------

表4. 6新闻类型

  --------------- -------------- ---- ------------------- --------------------------------
       字段            类型       空         默认                       注释

     id (主键)      bigint(20)    否                                    主键

      addtime       timestamp     否   CURRENT_TIMESTAMP              创建时间

   xinwenleixing   varchar(200)   是         NULL                     新闻类型
  --------------- -------------- ---- ------------------- --------------------------------

表4.7 用户

  ----------- -------------- ---- ------------------- ----------------------------------
     字段          类型       空         默认                        注释

   id (主键)    bigint(20)    否                                     主键

    addtime     timestamp     否   CURRENT_TIMESTAMP               创建时间

   zhanghao    varchar(200)   否                                     账号

     mima      varchar(200)   否                                     密码

   xingming    varchar(200)   否                                     姓名

   nianling    varchar(200)   否                                     年龄

    xingbie    varchar(200)   是         NULL                        性别

    shouji     varchar(200)   否                                     手机

   youxiang    varchar(200)   是         NULL                        邮箱

   zhaopian    varchar(200)   是         NULL                        照片
  ----------- -------------- ---- ------------------- ----------------------------------

表4.8 用户应聘

  ---------------- -------------- ---- ------------------- -------------------------------
        字段            类型       空         默认                      注释

     id (主键)       bigint(20)    否                                   主键

      addtime        timestamp     否   CURRENT_TIMESTAMP             创建时间

   zhaopinbiaoti    varchar(200)   是         NULL                    招聘标题

       zhiwei       varchar(200)   是         NULL                      职位

   shifouyingpin    varchar(200)   是         NULL                    是否应聘

   yingpinyuanyin     longtext     是         NULL                    应聘原因

   yingpinshijian       date       是         NULL                    应聘时间

      zhanghao      varchar(200)   是         NULL                      账号

      xingming      varchar(200)   是         NULL                      姓名

       shouji       varchar(200)   是         NULL                      手机

        sfsh        varchar(200)   是          否                     是否审核

        shhf          longtext     是         NULL                    审核回复
  ---------------- -------------- ---- ------------------- -------------------------------

表4.9 志愿者招聘

  ---------------- -------------- ---- ------------------- -------------------------------
        字段            类型       空         默认                      注释

     id (主键)       bigint(20)    否                                   主键

      addtime        timestamp     否   CURRENT_TIMESTAMP             创建时间

   zhaopinbiaoti    varchar(200)   是         NULL                    招聘标题

       zhiwei       varchar(200)   是         NULL                      职位

   zhaopinyaoqiu      longtext     是         NULL                    招聘要求

    gongzidaiyu     varchar(200)   是         NULL                    工资待遇

   gongzuodidian    varchar(200)   是         NULL                    工作地点

   gongzuoshijian   varchar(200)   是         NULL                    工作时间

   zhaopinrenshu      int(11)      是         NULL                    招聘人数

   zhaopinshijian       date       是         NULL                    招聘时间

   jiezhishijian        date       是         NULL                    截止时间

      fuzeren       varchar(200)   是         NULL                     负责人

   lianxifangshi    varchar(200)   是         NULL                    联系方式

       tupian       varchar(200)   是         NULL                      图片

      faburiqi          date       是         NULL                    发布日期

     clicktime        datetime     是         NULL                  最近点击时间

      clicknum        int(11)      是           0                     点击次数
  ---------------- -------------- ---- ------------------- -------------------------------

![](media/image8.gif){width="9.722222222222222e-3in"
height="9.722222222222222e-3in"}

![](media/image8.gif){width="9.722222222222222e-3in"
height="9.722222222222222e-3in"}

# 5系统详细实现

## 5.1 管理员模块的实现

### 5.1.1 用户信息管理

精准扶贫管理系统的系统管理员可以管理用户，可以对用户信息修改删除以及查询操作。具体界面的展示如图5.1所示。

![](media/image9.png){width="6.364583333333333in"
height="2.738888888888889in"}

图5.1 用户信息管理界面

### 5.1.2 贫困户信息管理

系统管理员可以对贫困户信息进行审核操作。具体界面如图5.2所示。

![](media/image10.png){width="6.377083333333333in"
height="2.8361111111111112in"}

图5.2 贫困户信息管理界面

### 5.1.3 新闻类型管理

系统管理员可以对新闻类型进行添加，修改，删除以及查询操作。界面如下图所示：

![](media/image11.png){width="6.374305555555556in"
height="4.043055555555555in"}

图5.3 新闻类型管理界面

### 5.1.4 志愿者招聘管理

系统管理员可以对志愿者招聘进行添加修改删除操作。界面如下图所示：

![](media/image12.png){width="6.375in" height="2.7645833333333334in"}

图5.4 志愿者招聘管理界面

## 5.2 用户模块的实现

### 5.2.2 志愿者招聘

用户可以在志愿者招聘进行收藏和应聘。界面如下图所示：

![](media/image13.png){width="6.372222222222222in"
height="3.7680555555555557in"}

图5.5 志愿者招聘界面

### 5.2.3 留言反馈管理

用户可以进行留言反馈。界面如下图所示：

![](media/image14.png){width="6.377083333333333in"
height="4.039583333333334in"}

图5.6 留言反馈界面

### 5.2.3 贫困户

用户可以查看贫困户信息。界面如下图所示：

![](media/image15.png){width="6.36875in" height="3.779861111111111in"}

图5.7 贫困户界面

# 6系统测试

## 6.1概念和意义

测试的定义：程序测试是为了发现错误而执行程序的过程。测试(Testing)的任务与目的可以描述为：

目的：发现程序的错误；

任务：通过在计算机上执行程序，暴露程序中潜在的错误。

另一个预测是相关的术语叫纠错(Debugging)。它的目的与任务可以规定为：

目的：定位和纠正错误；

任务：消除软件故障，保证程序的可靠运行。测试与纠错的关系，可以用图6-1的数据流图来说明。图中表明，每一次测试都要准备好若干必要的测试数据，与被测试程序一道送入计算机执行。通常把一次程序执行需要的测试数据，称为一个"测试用例(Test
Case)。每一个测试用例产生一个相应的"测试结果"。如果它与"期望结果"不想符合，便说明程序中存在错误，需要用纠错来改正。

![](media/image16.png){width="5.759722222222222in" height="1.78125in"}

图6.1测试与纠错信息流程

## 6.2特性

（1）挑剔性

测试是为了证明程序有错，而不是证明程序无错。因此，对于被测程序就是要"纯毛求疵"，就是要"鸡蛋里挑骨头"。

（2）复杂性

测试仪程序则比较容易，这其实是一个误区。设计测试用力是一项需要细致和高度技巧的高能工作，稍有不慎就会顾此失彼，发生不应用得数楼。

（3）不彻底性

实际测试都是不彻底的，当然不能够保证测试后的程序不存在遗漏的错误。

（4）经济性

通场这种测试称为"选择测试（Selective
Testing）"。为了降低测试成本，选择测试用力是应注意遵守"经济性"的原则。

## 6.3重要性

软件测试在软件生命周期中占据重要的地位，在传统的瀑布模型中，软件测试学仅处于运行维护阶段之前，是软件产品交付用户使用之前保证软件质量的重要手段。近来，软件工程界趋向于一种新的观点，即认为软件生命周期每一阶段中都应包含测试，从而检验本阶段的成果是否接近预期的目标，尽可能早的发现错误并加以修正，如果不在早期阶段进行测试，错误的延时扩散常常会导致最后成品测试的巨大困难。

## 6.4测试方法

首先我们来说界面测试，界面测试是为了使程序在不同的的操作平台上能够运行界面，并且能够保持原来的风格。我把完整程序拷贝到Windows
7环境下，似的程序运行正常，运行界面上的字体图片等设置都能够保持得非常好。不出现字体变形等情况！

其次进行功能测试。该系统测试采用的是单元测试，集成测试，完善性测试等多种方式进行测试。

经过测试，所有功能都能得以实现，没有任何变形。至此，在功能的测试上也已经比较圆满的完成了。

由于经验不足，写代码时出现了一些考虑不周的系统缺陷，写代码的时候会出现与设想不一致，比如说代码不规范导致接口与接口之间出现问题，功能与客户的要求不符合，这样导致产品不能过关，无法交付。所以产品在上线前必须反复测试，经过反复测试，修改，再测试，再修改，产品才能够不断完善。在整个系统测试中，根据需求文档和设计文档，逐一对功能进行检测并写好测试用例，有效避免残片缺陷，因为产品出现缺陷不仅影响功能，而且可以导致数据的不准确，导致产品质量的降低，经过测试，才能使得产品的稳定性和成熟度得到极大的提升，产品质量也才有保证。

## 6.5 功能测试

功能测试主要包括五项内容：适用性、准确性、可操作性、依从性、安全性。

本系统功能测试如表6.1所示：

表6.1 系统功能测试

  ----------------------------------- -----------------------------------
               测试内容                            测试结果

                适用性                                好

                准确性                                好

               可操作性                               好

                依从性                                好

                安全性                                好
  ----------------------------------- -----------------------------------

## 6.6可用性测试

可用性测试用于检测系统的可操作性、可理解性、可学习性等方面内容。具体测试方面如表6.2所示。

表6.2 系统可用性测试

  ---------------------------------------------------- ------------------
                         测试项                        测试人员的评价

         窗口移动、大小改变、关闭等操作是否正常        是

                    操作模块是否友好                   是

            模块、提示内容等文字描述是否正确           是

                 模块布局是否协调、合理                是

     模块的状态是否正确（对选中项能否发生对应切换）    是

                 鼠标、键盘操作是否支持                是

                 所需数据项是否正确显示                是

                    操作流程是否合理                   是

                    是否提供帮助信息                   是
  ---------------------------------------------------- ------------------

## 6.7性能测试

性能测试主要通过模拟系统运行环境，测试系统性能是否符合客户需求。性能测试的重要技术指标就是：系统运行速度、网络响应时间和支持并发节点数。

1）系统运行速度：通过在不同计算机上试运行本系统，没有发现有任何迟滞、停顿现象。

2）网络响应时间：网络响应时间主要包括网络最小响应时间、平均响应时间、最大响应时间三个参数。经过测试，在网络运营良好状态下，NBA局域网内响应时间三参数为：1/2/6s，NBA外网响应时间三参数为3/7/12s，符合客户需求，属于用户心理可承受范围。

3）支持并发节点数：经过模拟环境测试，本系统在并发节点达46个时，网络运营速度会发生较大波动，延迟时间10秒左右，符合客户需求。

## 6.8测试分析

本网站设计时借鉴了国内外优秀网站的优点，从界面到系统设计都保证了用户能够方便操作。系统的主要特点和优点归纳如下：

（1）本系统用的移置性和针对性都比较高，因为针对性高可以提供更好的服务而移置性可以在多个系统上运行，更给客户带来了极大的方便。

（2）该完整内容全面，管理方便可以及时的全面的处理各种错误，异常，这样避免了很多因用户的马虎操作而出现的失误，其操作方便，用户界面友好，能够上网的人都可以很好的进行操作。

## 6.9测试结果分析

经过对上述测试结果分析，本系统符合用户需求。所有基本功能点实现，操作简单，操作流程简单合理，产品运行性能良好，是一款值得推广的精准扶贫管理系统。

# 结论

在这次毕业设计中遇到的最困难的方面就是在数据库方面的知识，在刚开始进行毕业设计的时候感觉十分困难，根本不知道该从何处下手，但不断的坚持，设计最终被完成。无论多么的困难，只要能够坚持下来，善于去找到好的材料来研究，在研究中充分利用资源，没有困难是不会被成功解决的。

在开发系统的过程中，本人运用到了Spring
Boot框架和平时学习中所了解的一些技术，通过实现这些技术，大大提高了整个系统的性能。在论文中这些技术都做了比较详细的介绍。本系统还存在很多缺点和不完善的地方，例如有些细节上做的还不够完善，有些功能模块还需要加强。在今后的日子里，能够对这些不足进行改善。

通过这次最终的毕业设计，平时所学到的知识不仅融合了，而且获得了许多计算机知识。在整个设计过程中明白了许多东西，也培养独立工作能力，树立信心，对自己能力的工作能力，我相信以后会学习和工作生活中有至关重要的作用。同时也大大提高了手的能力，使其难以充分体会探索的乐趣和成功的创作过程，设计过程中汲取的东西，是一笔宝贵的财富。

回顾过去做毕业设计的整个过程，充满了付出和收获，但是当你看到成果的时候的感觉，是一种难以用言语表达的喜悦之感这些在毕业设计过程中学习到的东西将会使我终身受益！

最后，感谢指导老师的关心和指导，在我毕业设计的整个过程中，他给与了我很多的帮助和讲解，在导师的帮助下我的毕业设计才能如此顺利的完成。

# 致谢语

经过几个多月的不断学习，我的毕业设计终于如期完成。此次毕业设计是对我们日常所学计算机理论知识的一次综合性评测，也是将理论应用到实践的一项考察。

首先我要感谢此次指导我的老师，是他的及时纠正我在设计当中出现的问题，使得我的设计高质量完成。指导老师在我本次精准扶贫管理系统的开发过程中，为程序、框架的设计、代码等方面以及论文设计提供了很多宝贵的意见，并且为我推荐了许多相关的资料，他的指导和建议使我受益匪浅，通过老师的耐心辅导和指点，我的论文顺利完成，在此，我表示深刻的感谢。

我也要感谢帮助过我的同学们，和我一起探讨论文的不足，给我的设计提出宝贵的建议，在这次设计中他们的帮助使得我的设计更加完善更加具体。

最后，我也要感谢学校为我们提供了一个良好的学校环境。祝愿学校的领导教师以及和我一起奋斗的同学们工作顺利，事业有成，也要祝愿学校的前景更加辉煌。

# 参考文献

\[1\]付昕.
基于B/S模式仓库管理系统的实现\[J\].山东省农业管理干部学院学报, 2010,
27(4):166-168

\[2\] 雷文华, 薛小文. MATLAB和Servlet在网络数据处理中的应用\[J\].
电子测试, 2010, (11):81-86.

\[3\] 黄艳峰. 在Java语言中实施"案例教学"的研究与探索\[J\].
电脑知识与技术, 2010, 6(5):1148-1149

\[4\] 王玉英. 基于JSP的MySQL数据库访问技术\[J\]. 现代计算机：专业版,
2010, 19(14):63-66

\[5\] 赵钢. JSP Servlet+EJB的Web模式应用研究\[J\]. 电子设计工程, 2013,
21(13):47-49

\[6\] David L.Anderson.Managing Information
Systems.清华大学出版社，2002：16

\[7\] 王家华．软件工程\[M\]，沈阳：东北大学出版社，2011：46

\[8\] 张孝祥,徐明华.软件开发课堂.清华大学出版社，2009：55

\[9\] 崔洋.MySQL数据库应用从入门到精通.中国铁道出版社，2013：27

\[10\] 王珊,萨师煊.数据库系统概论.高等教育出版社, 2006：16

\[11\] 崔洋.MySQL数据库应用从入门到精通.中国铁道出版社，2013：27

\[12\] 王珊,萨师煊.数据库系统概论.高等教育出版社, 2006：16

\[13\] 张海潘.软件工程导论.清华大学出版社，2008：86

\[14\] 黄艳峰. 在Java语言中实施"案例教学"的研究与探索\[J\].
电脑知识与技术, 2010, 6(5):1148-1149

\[15\] 王玉英. 基于JSP的MySQL数据库访问技术\[J\]. 现代计算机：专业版,
2010, 19(14):63-66
