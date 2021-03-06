# C++设计模式

## 什么是设计模式
“每一个模式描述了一个在我们周围不断重复发生的问题，以及该问题的解决方案的核心。这样，你就能一次又一次地使用该方案而不必做重复劳动”。
——Christopher Alexander
+ 好的面向对象设计是面对变化，提高软件的**复用性**。
+ 先寻找变化点，然后在变化点上应用设计模式，而不是任何时间任何地方都用。
+ 先写代码，而后采用设计模式进行重构。

## 如何解决复杂性？
+ 分解
  + 人们面对复杂性有一个常见的做法：即分而治之，将大问题分解为多个小问题，将复杂问题分解为多个简单问题。
  + 分析问题的思路。
+ 抽象
  + 更高层次来讲，人们处理复杂性有一个通用的技术，即抽象。由于不能掌握全部的复杂对象，我们选择忽视它的非本质细节，而去处理泛化和理想化了的对象模型。
  + 编写代码的思路。
  
  
## 面向对象设计原则
1. 依赖倒置原则（DIP）
  + 高层模块(稳定)不应该依赖于低层模块(变化)，二者都应该依赖于抽象(稳定) 。
  + 抽象(稳定)不应该依赖于实现细节(变化) ，实现细节应该依赖于抽象(稳定)。
  
        MainForm -> Line\Rect  =>  MainFrom - > Shape
                                                  ↑ 
                                              Line\Rect
2. 开放封闭原则（OCP）
  + 对扩展开放，对更改封闭。
  + 类模块应该是可扩展的，但是不可修改。
    > 对于改变应该尽量采用增加的方式对应，而不是修改的方式。
3. 单一职责原则（SRP）
  + 一个类应该仅有一个引起它变化的原因。
  + 变化的方向隐含着类的责任。
4. Liskov 替换原则（LSP）
  + 子类必须能够替换它们的基类(IS-A)。
  + 继承表达类型抽象。
5. 接口隔离原则（ISP）
  + 不应该强迫客户程序依赖它们不用的方法。
  + 接口应该小而完备。
6. 优先使用对象组合，而不是类继承
  + 类继承通常为“白箱复用”，对象组合通常为“黑箱复用” 。
    > 小明的父类是人类，而不是小明的父亲，通过理解的继承关系有误。
  + 继承在某种程度上破坏了封装性，子类父类耦合度高。
  + 而对象组合则只要求被组合的对象具有良好定义的接口，耦合度低。
7. 封装变化点
  + 使用封装来创建对象之间的分界层，让设计者可以在分界层的一侧进行修改，而不会对另一侧产生不良的影响，从而实现层次间的松耦合。
8. 针对接口编程，而不是针对实现编程
  + 不将变量类型声明为某个特定的具体类，而是声明为某个接口。
  + 客户程序无需获知对象的具体类型，只需要知道对象所具有的接口。
  + 减少系统中各部分的依赖关系，从而实现“高内聚、松耦合”的类型设计方案。

## 重构技巧
1. 静态 -> 动态
2. 早绑定 -> 晚绑定
3. 继承 -> 组合
4. 编译时依赖 -> 运行时依赖
5. 紧耦合 -> 松耦合

## 从封装变化角度对模式分类
### 组件协作：
+ [Template Method](https://github.com/lichangqing2611/Cpp-Design-Patterns/tree/master/Template%20Method)
+ [Observer/Event](https://github.com/lichangqing2611/Cpp-Design-Patterns/tree/master/Observer)
+ [Observer(Head-First版)](https://github.com/lichangqing2611/Cpp-Design-Patterns/tree/master/Observer-Pattern)
+ [Strategy](https://github.com/lichangqing2611/Cpp-Design-Patterns/tree/master/Strategy)
+ [Strategy(Head-First版)](https://github.com/lichangqing2611/Cpp-Design-Patterns/tree/master/Strategy-Pattern)
### 单一职责：
+ [Decorator](https://github.com/lichangqing2611/Cpp-Design-Patterns/tree/master/Decorator)
+ [Bridge](https://github.com/lichangqing2611/Cpp-Design-Patterns/tree/master/Bridge)
### 对象创建:
+ [Factory Method](https://github.com/lichangqing2611/Cpp-Design-Patterns/tree/master/Factory%20Method)
+ [Abstract Factory](https://github.com/lichangqing2611/Cpp-Design-Patterns/tree/master/Abstract%20Factory)
+ [Prototype](https://github.com/lichangqing2611/Cpp-Design-Patterns/tree/master/Prototype)
+ [Builder](https://github.com/lichangqing2611/Cpp-Design-Patterns/tree/master/Builder)
### 对象性能：
+ [Singleton](https://github.com/lichangqing2611/Cpp-Design-Patterns/tree/master/Singleton)
+ [Flyweight(享元模式)](https://github.com/lichangqing2611/Cpp-Design-Patterns/tree/master/Flyweight)
### 接口隔离:
+ [Façade(门面模式)](https://github.com/lilichangqing2611/Cpp-Design-Patterns/tree/master/Facade)
+ [Proxy](https://github.com/lichangqing2611/Cpp-Design-Patterns/tree/master/Proxy)
+ [Mediator(中介者)](https://github.com/lichangqing2611/Cpp-Design-Patterns/tree/master/Mediator)
+ [Adapter](https://github.com/lichangqing2611/Cpp-Design-Patterns/tree/master/Adapter)
### 状态变化：
+ [Memento(备忘录)](https://github.com/lichangqing2611/Cpp-Design-Patterns/tree/master/Memento)
+ [State](https://github.com/lichangqing2611/Cpp-Design-Patterns/tree/master/State)
### 数据结构：
+ [Composite(组合模式)](https://github.com/lichangqing2611/Cpp-Design-Patterns/tree/master/Composite)
+ [Iterator](https://github.com/lichangqing2611/Cpp-Design-Patterns/tree/master/Iterator)
+ [Chain of Resposibility(职责链)](https://github.com/lichangqing2611/Cpp-Design-Patterns/tree/master/Chain%20of%20Resposibility)
### 行为变化：
+ [Command](https://github.com/lichangqing2611/Cpp-Design-Patterns/tree/master/Command)
+ [Visitor](https://github.com/lichangqing2611/Cpp-Design-Patterns/tree/master/Visitor)
### 领域问题：
+ [Interpreter](https://github.com/lichangqing2611/Cpp-Design-Patterns/tree/master/Interpreter)

### 现代较少用的模式
+ Builder
+ Mediator
+ Memento
+ Iterator
+ Chain of Resposibility
+ Command
+ Visitor
+ Interpreter

## 什么时候不用设计模式
1. 代码可读性很差时
2. 需要理解还很浅时
3. 变化没有显现时
4. 不是系统的关键依赖点
5. 项目没有复用价值时
6. 项目将要发布时
