## Spring源码阅读

#### spring的设计理念

Spring是面向Bean的编程(BOP,Bean Oriented Programming),Bean在Spring中才是真正的主角。**Spring解决了一个非常关键的问题他可以让你把对象之间的依赖关系转而用配置文件来管理，也就是他的依赖注入机制。**这个注入关系在一个叫IoC容器中管理，Spring正是通过把对象包装在Bean中而达到对这些对象管理以及一些额外操作的目的。

Spring Context 就是要发现每个Bean之间的关系，为它们建立这种关系并且要维护好这种关系。所以**Context就是一个Bean关系的集合，这个关系集合又叫IoC容器**，一旦建立起这个IoC容器后Spring就可以为你工作了。

其实Core就是发现、建立和维护每个Bean之间的关系所需要的一系列的工具。

Beans组建包主要解决三件事：Bean的定义、Bean的创建以及对Bean的解析。对Spring的使用者来说唯一要关心的就是Bean的创建，

ApplicationContext继承了BeanFactory,这也说明了Spring容器中运行的主体对象是Bean，另外ApplicationContext继承了ResourceLoader接口，使得ApplicationContext可以访问到任何外部资源，这将在Core中详细说明。

总体来说ApplicationContext必须要完成一下几件事：

- 标识一个应用环境
- 利用BeanFactory创建Bean对象
- 保存对象关系表
- 能够捕获各种事件











































