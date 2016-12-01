## 搜集一些关键词，用于学习
* 前端实时可视化开发工具体验 [liveStyle liveReload CodeKit]
* [Aaron艾伦慕课网专题](http://www.imooc.com/u/290139/courses?sort=publish)
* [前端数据调试抓包工具fiddler](http://www.imooc.com/video/388)
* localStorage sessionStorage cookie 实现前端存储的用法与思路
* 前后端耦合性--前后端完全解耦(开发，代码，部署，纯页面改版)
* 数据传输协议 -文本协议(json,xml)  二进制
* mock.js 前后端分离开发数据模拟，假数据
* 前端脚手架工具
* 需求分析-脚手架工具-数据Mock-架构设计-代码编写-自动化测试-编译打包
* 前端路由-单页面应用SPA
* js动画实质(逐渐的改变dom的某个属性值)  js帧动画函数 requestAnimationFrame 1000/60 1秒60帧，掉帧现象
* CSS3动画，关键帧技术，逐帧动画
* 如果当前style="left:190.5px;"表示当前left是190.5px，但是offsetLeft读取的只是整数部分，所以运动到这个时候，就会停止下来，只能通过，速度为正时，向上取证，速度为负时向下取证。
* [优化页面响应时间](http://www.imooc.com/video/6321)  (动态页面静态化，优化数据库，使用负载均衡，使用缓存等)
* php文件执行顺序--语法分析--编译--运行--展示结果
* html文件执行顺序：运行
* js无缝滚动最佳实现方式 [慕课网](http://www.imooc.com/video/179)
* css3动画贝塞尔曲线
* js--生命周期函数
* [基于slideout.js实现的移动端侧边栏滑动特效]
* [Web前端从入门菜鸟到实践老司机所需要的资料与指南合集](https://segmentfault.com/a/1190000007611188)
* 私有作用域 函数作用域 全局作用域 
* [前端面经](http://gold.xitu.io/entry/583d301d61ff4b007ed9998f)
   1. 最近在看哪些前端方面得书？
   2. js的基本数据（简单）类型有哪些？复杂数据类型是？
   3. 解释一下什么是闭包？
   4. css3常用得样式有哪些？了解css3吗？
   5. 知道哪些HTML5的新特性？
   6. 了解AJAX吗？如何实现跨域？
   7. 对jQuery了解多少，看过源码吗？DOM篇？事件篇？动画篇？异步？
   8. 在浏览器中输入域名到显示，其背后是怎样的一系列流程？
   9. 如何优化页面的显示速度？
   10. 了解数据结构么？常用的数据结构有哪些？
   11. 讲述一下域名到页面的过程。
   12. HTTP方法除了GET和POST还有哪些？
   13. GET请求和POST请求有长度限制么？
   14. CSS中的position属性有哪些值？
   15. 哪些操作会造成内存泄漏？
   16. 前端的安全性问题有哪些？
   17. JS实现继承有哪几种方法？
   18. display有哪些属性值？
   
* [EventUtil--跨浏览器的事件对象](http://www.cnblogs.com/hykun/p/EventUtil.html)
* 什么是DOM2级方法，IE方法，DOM0级方法？
* js事件机制？内存泄漏？js的垃圾回收机制？生命周期函数？
* XSS跨站脚本攻击，HTML注入？
* js事件冒泡？事件捕获？
* [DOM2级事件](http://blog.csdn.net/zhu1988renhui/article/details/7945025)规定了事件流得三个阶段：事件捕获阶段，处于目标阶段，事件冒泡阶段。
* 事件处理程序：响应某个事件的函数就叫做事件处理程序，或称为事件侦听器。事件处理程序都是以"on"开头的。例如onclick、onload事件。
* try{}catch(e){}事件异常处理
* [HTML事件处理程序](http://blog.csdn.net/zhu1988renhui/article/details/7945025)：（直接在标签内添加事件）（缺点：时差问题,HTML与JS代码紧密耦合）
* DOM0级事件处理程序-DOM2级事件处理程序-IE事件处理程序 ---- 总结封装为一个**跨浏览的事件处理程序-EventUtil**
* 类：封装，继承，多态。
* [JavaScript中实现继承得几种方式](http://lib.csdn.net/snippet/18/47126)
* js继承：用一个空函数来作为中转完成原型链的继承 [JavaScript的9种继承实现方式归纳](http://www.jb51.net/article/66266.htm)
* 把原型指向一个实例对象就能完成继承吗？
```js
//http://blog.csdn.net/ladycode/article/details/51282407
function Person(){  
  this.name="bob";    
}  
Person.prototype.eat=function(){  
  return "food";  
}  
function Student(){}  
Student.prototype=new Person();//将Person实例赋给Student的原型对象  Person的实例对象拥有一个指向它得原型对象得指针 [[prototype]]，在chrome中是可见得，`__proto__`，但在大多数浏览器中是不可见得。这个指针也指向了一个内存地址，把拥有这个指针得实例对象赋值给子类得原型对象后，自然子类得原型对象也获取了这个`__proto__`指针，指向了父类得原型对象。
var one=new Student();  
one.name//bob  
one.eat()//food,Student的实例能访问到Person对象的实例方法，也能访问到其原型属性中的方法
```
* 子类如果和父类共用一个原型对象，那么子类就无法扩展自己的属性了，因为子类和父类都指向了一个原型对象，其实就是一个内存地址，那么改变子类，父类也会改变，这样式很危险得。
* 总结下构造函数、原型和实例的关系：每个构造函数都有一个原型对象，原型对象拥有一个指向构造函数的指针，而实例拥有一个指向原型对象的内部指针（这就是前面所提到的[[Prototype]]，即__proto__，要注意的是这个__proto__属性在chrome浏览器中是可以看到的，而在大部分浏览器是隐藏的！）
* [原型对象的用途是为每个实例对象存储共享的方法和属性，它仅仅是一个普通对象而已。并且所有的实例是共享同一个原型对象，因此有别于实例方法或属性，原型对象仅有一份](http://www.2cto.com/kf/201506/407981.html)
* [js私有作用域(function(){})(); 模仿块级作用域](http://blog.csdn.net/u013474104/article/details/44197513)
* JavaScript中的事件委托


































































