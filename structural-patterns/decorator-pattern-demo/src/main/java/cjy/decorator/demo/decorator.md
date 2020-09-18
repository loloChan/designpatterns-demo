## 装饰器模式
装饰器的核⼼就是在不改变原有类的基础上给类新增功能。而要实现这种功能，
除了使用装饰器模式以为，还可以使用继续、AOP等方法途径。但是继承会导致
子类过多，而AOP又会带来额外的复杂度。使用装饰器模式则更灵活且简单。

### 作用(应用场景)
- 主要解决的是直接继承下因功能的不断横向扩展导致子类膨胀的问题。

### jdk中的应用
- I/O流中的BufferReader。new BufferedReader(new FileReader(""))。
BufferedReader就是FileReader的装饰器。

### 案例
模拟一个sso单点登录系统的验证，一开始仅仅对用户的账户进行校验，随着业务的发展
需要增加对用户访问资源的权限进行校验，也就是不同的用户可以访问的系统资源限制不
一样。