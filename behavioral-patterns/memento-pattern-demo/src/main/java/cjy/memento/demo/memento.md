## 备忘录模式
在不破坏封装性的前提下，捕获一个对象的内部状态(成员变量)，并在该对象之外保存这个状态。
这样以后就可将该对象恢复到原先保存的状态。

### 作用
- 捕获一个对象的内部状态，并在该对象之外保存这个状态，这样可以在以后将对象恢复到原先保存的状态。

### 应用实例
- windows的ctrl + z
- 浏览器里的后退
- 数据库事务管理(回滚)

### 案例


### 优点
- 给用户提供了一种可以恢复状态的机制，可以使用户能够比较方便地回到某个历史的状态。 
- 实现了信息的封装，使得用户不需要关心状态的保存细节。

### 缺点
- 消耗资源。如果类的成员变量过多，势必会占用比较大的资源，而且每一次保存都会消耗一定的内存。