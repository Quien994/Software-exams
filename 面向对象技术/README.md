# 面向对象技术  

## 目录  
- [面向对象基础](#面向对象基础)  
  - [面向对象的基本概念](#1-面向对象的基本概念)
  - [面向对象设计的原则](#2-面向对象设计的原则)
- [UML](#UML)  
- [设计模式](#设计模式)  

## 内容  
### 面向对象基础  
> 把数据及对数据的操作方法放在一起，作为一个相互依存的整体——对象。对同类对象抽象出其共性，形成类。类中的大多数数据，只能用本类的方法进行处理。类通过一个简单的外部接口与外界发生关系，对象与对象之间通过消息进行通信。程序流程由用户在使用中决定。对象即为人对各种具体物体抽象后的一个概念，人们每天都要接触各种各样的对象，如手机就是一个对象。  

#### 1. 面向对象的基本概念
1. 对象  
  在面向对象的系统中，对象是基本的运行时的实体，它既包括数据（属性），也包括作用于数据的操作（行为）。从程序设计者来看，对象是一个程序模块；从用户来看，对象为他们提供了所希望的行为。  
  一个对象通常可由`对象名、属性`和`方法`3个部分组成。  
  一个对象把属性和行为封装成一个整体。  
  封装是一种信息隐蔽技术，它的目的是使对象的使用者和生产者分离，使对象的定义与实现分开。  

2. 消息  
  对象之间进行通信的一种构造叫做消息  
  当一个消息发送给某个对象时，包含要求接收对象取执行某些活动的消息。接收到信息的对象经过解释，然后予以响应。这种通信机制称为消息传递。发消息的对象不需要知道接收消息的对象如何请求予以响应。  

3. 类  
  一个类定义了一组大体上相似的对象。`一个类所包含的方法和数据描述一组对象的共同行为和属性`。把一组对象的共用特征加以抽象并存储在一个类中是面向对象技术最重要的一点。是否建立了一个丰富的类库，是衡量一个面向对象程序设计语言成熟与否的重要标志。  
  类可以分成三种：`实体类、接口类（边界类）和控制类`。  

4. 继承  
  继承是`父类`和`子类`之间`共享数据和方法`的机制。这是类之间的一种关系，在定义和实现一个类的时候，可以在一个已经存在的类的基础上进行，把这个已经存在的类所定义的内容作为自己的内容，并加入新的内容。

5. 多态  
  在收到消息时，对象要予以响应。`不同的对象收到同一消息可以产生完全不同的结果`，这一现象称为多态。  
  多态的实现受到继承的支持，利用类的继承的层次关系，把具有通用功能的消息存放在高层次，而不同的实现这一功能的行为放在低层次，在这些低层次上生成的对象能够给通用消息以不同的响应。  

#### 2. 面向对象设计的原则  
1. 单一责任原则  
  就一个类而言，应该仅有一个引起它变化的原因  
  
2. 开放-封闭原则  
  软件实体应该是可以扩展的，及开放的；但是不可修改的，及封闭的  
  
3. 里氏替换原则  
  子类型必须能够替换掉他们的基类型  
  
4. 依赖倒置原则  
  抽象不应该依赖于细节，细节应该依赖于抽象  
  
5. 接口分离原则  
  不应该强迫客户依赖于它们不用的方法  
  
<div align=center >
<a href=#目录>返回目录</a>
</div>

### UML  
> UML词汇表包含3种构造块：事务、关系和图。事务是对模型中最具有代表性的抽象；关系把事务结合在一起；图聚集了相关的事物。  

#### 1. 事务  
> UML中有4种事务：结构事务、行为事务、分组事务和注释事务。  

1. 结构事务  
  结构事务是UML模型中的名词。   
  结构事务包括类、接口、协作、用例、主动类、构件、制品和结点  
  
2. 行为事务  
  行为事务是UML模型的动态部分  
  行为事务包括交互、状态机和活动  
  
3. 分组事务  
  分组事务是UML模型的组织部分，最主要的分组事务是包  
  包是把元素组织成组的机制，这种机制具有多种用途  
  结构事务、行为事务甚至是其他分组事务都可以放进包内  
  
4. 注释事务  
  注释事务是UML模型的解释部分  
  
#### 2. 关系  
> UML有4种关系：依赖、关联、泛化和实现  

1. 依赖  
  依赖是两个事务间的语义关系，其中一个事务发生变化会影响另一个事务的语义。 
  
  <div align=center >
  <img src="https://github.com/gong2xi/Software-exams/blob/main/%E9%9D%A2%E5%90%91%E5%AF%B9%E8%B1%A1%E6%8A%80%E6%9C%AF/images/dependency.jpg">
  </div>
  
2. 关联  
  描述了一组链，链是对象之间的连接。  
  聚集是一种特殊类型的关联，它描述了整体和部分间的结构关系  
  
  <div align=center>
  <img src="https://github.com/gong2xi/Software-exams/blob/main/%E9%9D%A2%E5%90%91%E5%AF%B9%E8%B1%A1%E6%8A%80%E6%9C%AF/images/association.jpg">
  </div>  
  
  <div align=center>
  <img src="https://github.com/gong2xi/Software-exams/blob/main/%E9%9D%A2%E5%90%91%E5%AF%B9%E8%B1%A1%E6%8A%80%E6%9C%AF/images/aggregation.jpg">
  </div>
  
3. 泛化  
  泛化是一种特殊/一般的关系：特殊元素（子元素）的对象可替代一般元素（父元素）的对象  
  
  <div align=center>
  <img src="https://github.com/gong2xi/Software-exams/blob/main/%E9%9D%A2%E5%90%91%E5%AF%B9%E8%B1%A1%E6%8A%80%E6%9C%AF/images/generalization.jpg">
  </div>
  
4. 实现  
  实现是类元之间的语义关系，其中一个类元指定了由另一个类元保证执行的契约  
  
  <div align=center>
  <img src="https://github.com/gong2xi/Software-exams/blob/main/%E9%9D%A2%E5%90%91%E5%AF%B9%E8%B1%A1%E6%8A%80%E6%9C%AF/images/realization.jpg">
  </div>

#### 3. UML图  
1. 类图  
  类图展现了一组对象、接口、协作和它们之间的关系  
  类图中也包含注解和约束。类图还可以含有包和子系统，而二者都用于把模型元素聚集成更大的组块  
  
  <div align=center>
  <img src="https://github.com/gong2xi/Software-exams/blob/main/%E9%9D%A2%E5%90%91%E5%AF%B9%E8%B1%A1%E6%8A%80%E6%9C%AF/images/class_diagram.png">
  </div>
  
2. 对象图  
  对象图展现了某一时刻一组对象以及它们之间的关系，描述了在类图中所建立的事物的实例的静态快照  
  
   <div align=center>
  <img src="https://github.com/gong2xi/Software-exams/blob/main/%E9%9D%A2%E5%90%91%E5%AF%B9%E8%B1%A1%E6%8A%80%E6%9C%AF/images/object_diagram.png">
  </div>
  
3. 用例图  
  用例图展现了一组用例、参与者以及它们之间的关系  
  
   <div align=center>
  <img src="https://github.com/gong2xi/Software-exams/blob/main/%E9%9D%A2%E5%90%91%E5%AF%B9%E8%B1%A1%E6%8A%80%E6%9C%AF/images/use_case_diagram.png">
  </div>
  
4. 序列图  
  序列图是场景的图形化表示，描述了以时间顺序组织的对象之间的交互活动  
  
   <div align=center>
  <img src="https://github.com/gong2xi/Software-exams/blob/main/%E9%9D%A2%E5%90%91%E5%AF%B9%E8%B1%A1%E6%8A%80%E6%9C%AF/images/sequence_diagram.png">
  </div>
  
5. 状态图  
  状态图展现了一个状态机，它由状态、转换、事件和活动组成  
  状态图关注系统的动态视图，对于接口、类和协作的行为建模尤为重要，强调对象行为的事件顺序  
  
   <div align=center>
  <img src="https://github.com/gong2xi/Software-exams/blob/main/%E9%9D%A2%E5%90%91%E5%AF%B9%E8%B1%A1%E6%8A%80%E6%9C%AF/images/state_diagram.png">
  </div>
  
6. 活动图  
  活动图是一种特殊的状态图，它展现了在系统内从一个活动到另一个活动的流程  
  
   <div align=center>
  <img src="https://github.com/gong2xi/Software-exams/blob/main/%E9%9D%A2%E5%90%91%E5%AF%B9%E8%B1%A1%E6%8A%80%E6%9C%AF/images/activity_diagram.png">
  </div>
  
<div align=center >
<a href=#目录>返回目录</a>
</div>
    
    







