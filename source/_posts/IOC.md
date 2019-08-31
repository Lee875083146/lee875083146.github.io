---
title: IOC——控制反转
tags: [IOC,DI,Spring]
categories:
- Spring
- IOC
date: 2019-08-30 22:59:16
entitle: Spring-IOC
---

分离关注（Separation of Concerns）是IOC模式和AOP产生的最原始动力，通过功能分解可得到关注点，这些关注可以是Components，Aspects和Services。
本文将介绍IOC即控制反转。

<!--more-->
## IOC

在面向对象理念的指导下，我们已经习惯了面向接口编程，即抽象不应该依赖于具体，具体依赖于抽象，面向接口编程有很多的好处，例如可以提供不同子类的实现，在有新的实现时只需要新增新的类实现目标接口即可，增加代码的稳定性和健壮性。

但接口的实现是必须要执行的，即代码在执行的时候必须是有具体实现的，那么我们接口的实现类必须在执行前的某一时刻注入到依赖它的类中。

IOC——Inversion of Control，即控制反转，就是解决类与接口依赖关系的一种方式，面向对象的思想中，为了降低耦合，常常引入第三方去协调，新的IOC模式DI（Dependency Injection）依赖注入，就是将类之间的关系通过第三方进行注入，不需要类自己去解决调用关系。高层次模块不应该依赖低层次模块，他们应该依赖于一种抽象，且这种抽象不应该依赖细节，细节应该依赖于抽象。

DI将实现调用者和被调用者解耦，将依赖先剥离，在适当的时候进行注入。即开发者只需要关心接口的交互，不需要关心调用者如何获取被调用者的具体实例。

在DI中，对象只依赖于IOC/DI容器，不再相互依赖，实现了松耦合，在对象创建的时候，容器将其所依赖的具体实例自动匹配并注入，在Spring 中结合Java的垃圾回收机制，开发这不需要关注Bean的创建或者销毁，只需要使用即可，大大提升了开发效率。

IOC的三种类型：
类型|解释|例子
-|-|-
一|从JNDI或ServiceManager等获取被调用者|EJB/J2EE
二|使用JavaBean的setter方法|SpringFramework
三|构造方法中实现依赖|PicoContainer

## Spring IOC实现原理








## Spring-IOC与DDD聚合根之间调用的逻辑相悖










## 参考资料
[Jdon-IOC](https://www.jdon.com/AOPdesign/Ioc.htm)
我非常喜欢[解道](https://www.jdon.com)这个网站，面向对象、领域驱动都是我非常感兴趣的方向，我从这个网站学到了很多，也推荐大家去交流学习。
