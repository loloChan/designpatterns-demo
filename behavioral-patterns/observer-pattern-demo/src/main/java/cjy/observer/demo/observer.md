## 观察者模式
定义对象间一种一对多的依赖关系，使得每 当一个对象改变状态，
则所有依赖于它的对象都会得到通知并被自动更新。简单说，就是当一个
行为发生时，传递信息给另一个用户接收并做出相应处理。

### 作用
- 主要解决一个对象状态改变给其他对象通知的问题。

### 应用实例
- java.util.EventListener
- zookeeper的watchdog机制

### 案例
- 模拟小客车摇号结果通知

### 优点
- 观察者和被观察者是抽象耦合的。 
- 建立一套触发机制。

### 缺点
- 如果一个被观察者对象有很多的直接和间接的观察者的话，将所有的观察者都通知到会花费很多时间。 
- 如果在观察者和观察目标之间有循环依赖的话，观察目标会触发它们之间进行循环调用，可能导致系统崩溃。 
- 观察者模式没有相应的机制让观察者知道所观察的目标对象是怎么发生变化的，而仅仅只是知道观察目标发生了变化。