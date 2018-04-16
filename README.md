# Learning_Laravel_Kernel

Laravel核心代码学习

## 前言

我16年才开始接触Laravel框架, 算是比较晚的。之前几年一直都是在用ZendFramework和Codeigniter，尤其Codeigniter这个小巧但是功能强大的框架在前几年很流行，当时我也非常喜欢Codeigniter的轻量级和灵活，写了很多Codeigniter的libraries，甚至为了能更好的在Codeigniter核心的基础上扩展出自己想要的功能通读了它的源码。Codeigniter的源码相对Laravel来说还是很容易读懂的，因为它是上一个时代的PHP框架并没有用到后来PHP才有的命名空间、性状这些特性，所以当时在学习源码时也没有刻意觉得要把这些东西梳理到文档里来帮助自己理解。 后来随着项目越做越成熟由于在Codeigniter里扩展了太多的自已写的libraries明显感觉代码维护难度较项目早期高了很多，也觉得老用一种思路进行软件开发慢慢会限制自己的进步，所以在16年下半年才开始接触Laravel, 试着用laravel重构公司里的一个管理后台。当时学习的方法就是在照着文档里写，一边开发一边看文档慢慢的把文档看了几遍使用起来就顺手多了，也从Google上找到了很多问题在Laravel里的最佳实践。在使用的过程中慢慢地也就对“依赖注入”、“控制反转”、“服务容器”、“服务提供者”和“中间件”这些东西有了些概念。后来17年换工作后部门主要应用的就是Laravel, 应用场景一多起来之后自然使用的就越发熟练。由于我一直以来都坚信做开发的不光要知其然还要知其所以然，所以一直对laravel里面的依赖注入、服务绑定、服务解析等等这些东西很好奇，再一个我觉得只有理解了一个框架的核心代码才能真正把一个框架用好才能写出最佳实践。之前在开发的时候已经零敲碎打的看了很多Laravel核心部分的源码了也看了不少相关的文章对Laravel的这些核心组件是怎么实现的有了一定的印象，但时间久了很多东西就忘了遇到不知道怎么解决的问题后还是得去一遍遍的看源码。所以进入18年后给自己的目标就是好好梳理一下Laravel核心的代码把他们用文字记录起来慢慢地梳理成体系，这样以后遇到问题可以节省不少看源码的时间，梳理成体系后也更有利于把这些知识分享给其他人共同进步。

## 面向的人群

要想很好地理解文章的内容你需要具备一定的PHP基础和Laravel的知识，为了文章的可读性我会尽量从Laravel每个模块典型用法开始逐步深入到底层的代码，我并不会解释核心里的每一行代码，更多的是会解释每一部分代码块的功能。所以你可以将文章作为导读跟随文章自己逐步去看一遍Laravel每个核心组件的代码，如果有哪里不理解的就去补齐那里用到的知识，相信看完Laravel底层的代码后你不仅能更熟练的使用Laravel也能在其它基础知识方面有所提高。

## 涉及的内容

文章主要专注于Laravel核心的学习，包括:服务容器、服务提供器、中间件、路由、Facades、事件驱动系统以及作为核心服务的Database、Request、Cookie和Session。其它的部分也都是作为服务注册到服务容器里提供给应用使用的，当你理解了上面那些东西后再去看其它的这些服务也就会很容易理解了。



## 文章目录

- [类的反射和依赖注入](https://github.com/kevinyan815/Learning_Laravel_Kernel/blob/master/aritcles/reflection.md)
- [服务容器(IocContainer)](https://github.com/kevinyan815/Learning_Laravel_Kernel/blob/master/aritcles/IocContainer.md)
- [服务提供器(ServiceProvider)](https://github.com/kevinyan815/Learning_Laravel_Kernel/blob/master/aritcles/ServiceProvider.md)
- [Facades](https://github.com/kevinyan815/Learning_Laravel_Kernel/blob/master/aritcles/Facades.md)
- [路由](https://github.com/kevinyan815/Learning_Laravel_Kernel/blob/master/aritcles/Route.md)
- [中间件](https://github.com/kevinyan815/Learning_Laravel_Kernel/blob/master/aritcles/Middleware.md)
- [Database 基础介绍](https://github.com/kevinyan815/Learning_Laravel_Kernel/blob/master/aritcles/Database1.md)
- [Database 查询构建器](https://github.com/kevinyan815/Learning_Laravel_Kernel/blob/master/aritcles/Database2.md)
