<center><span style="color:green;font-size:25px;font-weight:bolder;">Spring Framework 5源码研读分析</span> </center>


- [IDEA](https://www.cnblogs.com/gqzdev/p/idea.html)

- [JDK9以上](https://www.oracle.com/technetwork/java/javase/overview/index.html)

- [Gradle-5.6.4](https://services.gradle.org/distributions/)

[Spring官方文档中文版](https://www.springcloud.cc/spring-reference.html)

[Spring Framework](https://spring.io/projects/spring-framework)

简单来说Bean的生命周期：

![Bean](https://github.com/MoreThanICanSay/image/blob/master/bean.jpg)

AbstractRefreshableApplicationContext 继承关系

![AbstractRefreshableApplicationContext](https://github.com/MoreThanICanSay/image/blob/master/AbstractRefreshableApplicationContext.jpg)

DefaultListableBeanFactory 继承关系

![DefaultListableBeanFactory](https://github.com/MoreThanICanSay/image/blob/master/DefaultListableBeanFactory.jpg)

>BeanFactory有三个子类：
>* ListableBeanFactory
>* HierarchicalBeanFactory
>* AutowireCapableBeanFactory

>ListableBeanFactory接口表示这些Bean是可列表的，而HierarchicalBeanFactory表示的是这些Bean是有继承关系的，也就是每个Bean有可能有父Bean。AutowireCapableBeanFactory接口定义Bean的自动装配规则。这四个接口共同定义了Bean的集合、Bean之间的关系、以及Bean行为。