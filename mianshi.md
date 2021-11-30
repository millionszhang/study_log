java 集合 list 和set 



集合 排序

集合 遍历删除

arraylist 去重



hashcode 和equals 方法有什么作用 区别

hashmap 的put 过程

转换红黑树过程

hashmap负载因子是多少 

0.75

java中的反射
[反射机制](https://so.csdn.net/so/search?from=pc_blog_highlight&q=反射机制)就是在程序的运行过程中被允许对程序本身进行操作，比如自我检查，进行装载，还可以获取类本身，类的所有成员变量和方法，类的对象，还可以在运行过程中动态的创建类的实例，通过实例来调用类的方法，这就是反射机制一个比较重要的功能了

那些设计模式

#### beanfactory 和 applicationcontext两个容器的区别

如果 Bean 的某一个属性没有注入，使用 BeanFacotry 加载后，第一次调用 getBean() 方法时会抛出异常，而 ApplicationContext 则会在初始化时自检，这样有利于检查所依赖的属性是否注入。
因此，在实际开发中，通常都选择使用 ApplicationContext，只有在系统资源较少时，才考虑使用 BeanFactory。本教程中使用的是 ApplicationContext 容器。



### springmvc拦截器

Spring MVC中的拦截器（Interceptor）类似于Servlet中的过滤器（Filter），它主要用于拦截用户请求并作相应的处理。例如通过拦截器可以进行权限验证、记录请求信息的日志、判断用户是否登录等。
要使用Spring MVC中的拦截器，就需要对拦截器类进行定义和配置。通常拦截器类可以通过两种方式来定义。
1.通过实现HandlerInterceptor接口，或继承HandlerInterceptor接口的实现类（如HandlerInterceptorAdapter）来定义。

2.通过实现WebRequestInterceptor接口，或继承WebRequestInterceptor接口的实现类来定义。

#### mybatis动态sql 其中一个线程为什么是start方法而不是run方法呢

start 方法会调用start0方法，start0是native方法，会启动一个线程，由虚拟机去调用线程的run方法，这里由于重写了父类的run方法，所以调用子类的run方法

####  hashcode作用

1、HashCode的存在主要是为了查找的快捷性，HashCode是用来在散列存储结构中确定对象的存储地址的

2、如果两个对象equals相等，那么这两个对象的HashCode一定也相同

3、如果对象的equals方法被重写，那么对象的HashCode方法也尽量重写

4、如果两个对象的HashCode相同，不代表两个对象就相同，只能说明这两个对象在散列存储结构中，存放于同一个位置Java中的hashCode方法就是根据一定的规则将与对象相关的信息（比如对象的存储地址，对象的字段等）映射成一个数值，这个数值称作为散列值



error和exception有什么区别

springaop 

 





### [1、什么是存储过程？用什么来调用？](https://gitee.com/souyunku/DevBooks/blob/master/docs/MySQL/MySQL最新2021年面试题及答案，汇总版.md#1什么是存储过程用什么来调用)

存储过程是一个预编译的SQL语句，优点是允许模块化的设计，就是说只需创建一次，以后在该程序中就可以调用多次。如果某次操作需要执行多次SQL，使用存储过程比单纯SQL语句执行要快。可以用一个命令对象来调用存储过程。

### [2、优化数据库的方法](https://gitee.com/souyunku/DevBooks/blob/master/docs/MySQL/MySQL最新2021年面试题及答案，汇总版.md#2优化数据库的方法)

**1、** 选取最适用的字段属性，尽可能减少定义字段宽度，尽量把字段设置NOTNULL，例如’省份’、’性别’最好适用ENUM

**2、** 使用连接(JOIN)来代替子查询

**3、** 适用联合(UNION)来代替手动创建的临时表

**4、** 事务处理

**5、** 锁定表、优化事务处理

**6、** 适用外键，优化锁定表

**7、** 建立索引

**8、** 优化查询语句

### [3、完整性约束包括哪些？](https://gitee.com/souyunku/DevBooks/blob/master/docs/MySQL/MySQL最新2021年面试题及答案，汇总版.md#3完整性约束包括哪些)

数据完整性(Data Integrity)是指数据的精确(Accuracy)和可靠性(Reliability)。

**分为以下四类：**

**1、** 实体完整性：规定表的每一行在表中是惟一的实体。

**2、** 域完整性：是指表中的列必须满足某种特定的数据类型约束，其中约束又包括取值范围、精度等规定。

**3、** 参照完整性：是指两个表的主关键字和外关键字的数据应一致，保证了表之间的数据的一致性，防止了数据丢失或无意义的数据在数据库中扩散。

**4、** 用户定义的完整性：不同的关系数据库系统根据其应用环境的不同，往往还需要一些特殊的约束条件。用户定义的完整性即是针对某个特定关系数据库的约束条件，它反映某一具体应用必须满足的语义要求。

与表有关的约束：包括列约束(NOT NULL（非空约束）)和表约束(PRIMARY KEY、foreign key、check、UNIQUE) 。

### [4、使用B树的好处](https://gitee.com/souyunku/DevBooks/blob/master/docs/MySQL/MySQL最新2021年面试题及答案，汇总版.md#4使用b树的好处)

B树可以在内部节点同时存储键和值，因此，把频繁访问的数据放在靠近根节点的地方将会大大提高热点数据的查询效率。这种特性使得B树在特定数据重复多次查询的场景中更加高效。

### [5、视图有哪些特点？哪些使用场景？](https://gitee.com/souyunku/DevBooks/blob/master/docs/MySQL/MySQL最新2021年面试题及答案，汇总版.md#5视图有哪些特点哪些使用场景)

**「视图特点：」**

**1、** 视图的列可以来自不同的表，是表的抽象和在逻辑意义上建立的新关系。

**2、** 视图是由基本表(实表)产生的表(虚表)。

**3、** 视图的建立和删除不影响基本表。

**4、** 对视图内容的更新(添加，删除和修改)直接影响基本表。

**5、** 当视图来自多个基本表时，不允许添加和删除数据。

「视图用途：」 简化sql查询，提高开发效率，兼容老的表结构。

**6「视图的常见使用场景：」**

**1、** 重用SQL语句；

**2、** 简化复杂的SQL操作。

**3、** 使用表的组成部分而不是整个表；

**4、** 保护数据

**5、** 更改数据格式和表示。视图可返回与底层表的表示和格式不同的数据。

### [7、事务是如何通过日志来实现的](https://gitee.com/souyunku/DevBooks/blob/master/docs/MySQL/MySQL最新2021年面试题及答案，汇总版.md#6事务是如何通过日志来实现的)

因为事务在修改页时，要先记 undo，在记 undo 之前要记 undo 的 redo， 然后修改数据页，再记数据页修改的 redo。 Redo（里面包括 undo 的修改） 一定要比数据页先持久化到磁盘。

当事务需要回滚时，因为有 undo，可以把数据页回滚到前镜像的 状态，崩溃恢复时，如果 redo log 中事务没有对应的 commit 记录，那么需要用 undo把该事务的修改回滚到事务开始之前。

如果有 commit 记录，就用 redo 前滚到该事务完成时并提交掉。

### [8、索引有哪几种类型？](https://gitee.com/souyunku/DevBooks/blob/master/docs/MySQL/MySQL最新2021年面试题及答案，汇总版.md#7索引有哪几种类型)

**1、** 主键索引: 数据列不允许重复，不允许为NULL，一个表只能有一个主键。

**2、** 唯一索引: 数据列不允许重复，允许为NULL值，一个表允许多个列创建唯一索引。

**3、** 普通索引: 基本的索引类型，没有唯一性的限制，允许为NULL值。

**4、** 全文索引：是目前搜索引擎使用的一种关键技术，对文本的内容进行分词、搜索。

**5、** 覆盖索引：查询列要被所建的索引覆盖，不必读取数据行

**6、** 组合索引：多列值组成一个索引，用于组合搜索，效率大于索引合并

### [9、谈谈六种关联查询，使用场景。](https://gitee.com/souyunku/DevBooks/blob/master/docs/MySQL/MySQL最新2021年面试题及答案，汇总版.md#8谈谈六种关联查询使用场景。)

**1、** 交叉连接

**2、** 内连接

**3、** 外连接

**4、** 联合查询

**5、** 全连接

**6、** 交叉连接

### [10、试述视图的优点？](https://gitee.com/souyunku/DevBooks/blob/master/docs/MySQL/MySQL最新2021年面试题及答案，汇总版.md#9试述视图的优点)

(1) 视图能够简化用户的操作 (2) 视图使用户能以多种角度看待同一数据； (3) 视图为数据库提供了一定程度的逻辑独立性； (4) 视图能够对机密数据提供安全保护。

### [11、MySQL自增主键用完了怎么办？](https://gitee.com/souyunku/DevBooks/blob/master/docs/MySQL/MySQL最新2021年面试题及答案，汇总版.md#10mysql自增主键用完了怎么办)

自增主键一般用int类型，一般达不到最大值，可以考虑提前分库分表的。

## 12. Vue.js 的特点

- 易用： 简单，易学，上手快
- 灵活： （渐进式）不断繁荣的生态系统，可以在一个库和一套完整框架之间自如伸缩。
- 高效： 20kB min+gzip 运行大小；超快虚拟 DOM；最省心的优化
- 双向绑定：开发效率高
- 基于组件的代码共享
- Web项目工程化，增加可读性、可维护性

## 13 Vue.js 双向绑定的原理

Vue.js 2.0 采用数据劫持（Proxy 模式）结合发布者-订阅者模式（PubSub 模式）的方式，通过 Object.defineProperty()来劫持各个属性的 setter，getter，在数据变动时发布消息给订阅者，触发相应的监听回调。

每个组件实例都有相应的watcher程序实例，它会在组件渲染的过程中把属性记录为依赖，之后当依赖项的setter被调用时，会通知watcher重新计算，从而致使它关联的组件得以更新。

> Vue.js 3.0, 放弃了Object.defineProperty ，使用更快的ES6原生 Proxy (访问对象拦截器, 也称代理器)

步骤：

1. 需要observe的数据对象进行递归遍历，包括子属性对象的属性，都加上setter和getter这样的话，给这个对象的某个值赋值，就会触发setter，那么就能监听到了数据变化
2. compile解析模板指令，将模板中的变量替换成数据，然后初始化渲染页面视图，并将每个指令对应的节点绑定更新函数，添加监听数据的订阅者，一旦数据有变动，收到通知，更新视图
3. Watcher订阅者是Observer和Compile之间通信的桥梁，主要做的事情是: ①在自身实例化时往属性订阅器(dep)里面添加自己 ②自身必须有一个update()方法 ③待属性变动dep.notice()通知时，能调用自身的update()方法，并触发Compile中绑定的回调，则功成身退。
4. MVVM作为数据绑定的入口，整合Observer、Compile和Watcher三者，通过Observer来监听自己的model数据变化，通过Compile来解析编译模板指令，最终利用Watcher搭起Observer和Compile之间的通信桥梁，达到数据变化 -> 视图更新；视图交互变化(input) -> 数据model变更的双向绑定效果。

## 14 Vue.js 3.0 放弃defineProperty, 使用Proxy的原因

Object.defineProperty缺陷

1. 监控到数组下标的变化时，开销很大。所以Vue.js放弃了下标变化的检测；
2. Object.defineProperty只能劫持对象的属性，而Proxy是直接代理对象。Object.defineProperty需要遍历对象的每个属性，如果属性值也是对象，则需要深度遍历。而 Proxy 直接代理对象，不需要遍历操作。
3. Object.defineProperty对新增属性需要手动进行Observe。vue2时需要使用 vm.$set 才能保证新增的属性也是响应式
4. Proxy支持13种拦截操作，这是defineProperty所不具有的
5. Proxy 作为新标准，长远来看，JS引擎会继续优化 Proxy，但 getter 和 setter 基本不会再有针对性优化

## 15 Vue 2 中给 data 中的对象属性添加一个新的属性时会发生什么？如何解决？

视图并未刷新。这是因为在Vue实例创建时，新属性并未声明，因此就没有被Vue转换为响应式的属性，自然就不会触发视图的更新，这时就需要使用Vue的全局 api $set()：`this.$set(this.obj, 'new_property', 'new_value')`

## 16 Computed和Watch的区别

1. computed 计算属性 : 依赖其它属性值,并且 computed 的值有缓存,只有它依赖的 属性值发生改变,下一次获取 computed 的值时才会重新计算 computed 的值。
2. watch 侦听器 : 更多的是观察的作用,无缓存性,类似于某些数据的监听回调,每 当监听的数据变化时都会执行回调进行后续操作。

> 运用场景：

1. 当我们需要进行数值计算,并且依赖于其它数据时,应该使用 computed,因为可以利用 computed 的缓存特性,避免每次获取值时,都要重新计算。
2. 当我们需要在数据变化时执行异步或开销较大的操作时,应该使用 watch,使用 watch 选项允许我们执行异步操作 ( 访问一个 API ),限制我们执行该操作的频率, 并在我们得到最终结果前,设置中间状态。这些都是计算属性无法做到的。
3. 多个因素影响一个显示，用Computed；一个因素的变化影响多个其他因素、显示，用Watch;

## 17 Computed 和 Methods 的区别

1. computed: 计算属性是基于它们的依赖进行缓存的,只有在它的相关依赖发生改变时才会重新求值对于 method ，只要发生重新渲染，
2. method 调用总会执行该函数
3. 

## 18 虚拟DOM，diff算法

（1）让我们不用直接操作DOM元素，只操作数据便可以重新渲染页面
（2）虚拟dom是为了解决浏览器性能问题而被设计出来的
当操作数据时，将改变的dom元素缓存起来，都计算完后再通过比较映射到真实的dom树上
（3）diff算法比较新旧虚拟dom。如果节点类型相同，则比较数据，修改数据；如果节点不同，直接干掉节点及所有子节点，插入新的节点；如果给每个节点都设置了唯一的key，就可以准确的找到需要改变的内容，否则就会出现修改一个地方导致其他地方都改变的情况。比如A-B-C-D, 我要插入新节点A-B-M-C-D,实际上改变的了C和D。但是设置了key，就可以准确的找到B C并插入

## 19 为何需要Virtual DOM？

1. 具备跨平台的优势
2. 操作 DOM 慢，js运行效率高。我们可以将DOM对比操作放在JS层，提高效率。
3. 提升渲染性能

## 20 过滤器 (Filter)

在Vue中使用filters来过滤(格式化)数据，filters不会修改数据，而是过滤(格式化)数据，改变用户看到的输出（计算属性 computed ，方法 methods 都是通过修改数据来处理数据格式的输出显示。
使用场景： 比如需要处理时间、数字等的的显示格式；

## 21 常见的事件修饰符及其作用

1. `.stop`：等同于 JavaScript 中的 event.stopPropagation() ，防止事件冒泡；
2. `.prevent` ：等同于 JavaScript 中的 event.preventDefault() ，防止执行预设的行为（如果事件可取消，则取消该事件，而不停止事件的进一步传播）；
3. `.capture` ：当元素发生冒泡时，先触发带有该修饰符的元素。若有多个该修饰符，则由外而内触发。如 div1中嵌套div2中嵌套div3.capture中嵌套div4，那么执行顺序为：div3=》div4=》div2=》div1
4. `.self` ：只会触发自己范围内的事件，不包含子元素；
5. `.once` ：只会触发一次。

## 22 v-show指令和v-if指令的区别是什么？

v-show 仅仅控制元素的显示方式，将 display 属性在 block 和 none 来回切换；而v-if会控制这个 DOM 节点的存在与否。当我们需要经常切换某个元素的显示/隐藏时，使用v-show会更加节省性能上的开销；当只需要一次显示或隐藏时，使用v-if更加合理。

## 23 v-model 是如何实现的，语法糖实际是什么

1. 作用在表单元素上`v-model="message"`等同于`v-bind:value="message" v-on:input="message=$event.target.value"`
2. 作用在组件上, 本质是一个父子组件通信的语法糖，通过prop和$.emit实现, 等同于`:value="message" @input=" $emit('input', $event.target.value)"`

## 24 data为什么是一个函数而不是对象

JavaScript中的对象是引用类型的数据，当多个实例引用同一个对象时，只要一个实例对这个对象进行操作，其他实例中的数据也会发生变化。

而在Vue中，我们更多的是想要复用组件，那就需要每个组件都有自己的数据，这样组件之间才不会相互干扰。

所以组件的数据不能写成对象的形式，而是要写成函数的形式。数据以函数返回值的形式定义，这样当我们每次复用组件的时候，就会返回一个新的data，也就是说每个组件都有自己的私有数据空间，它们各自维护自己的数据，不会干扰其他组件的正常运行。

## 25 Vue template 到 render 的过程

1. 调用parse方法将template转化为ast（抽象语法树, abstract syntax tree）
2. 对静态节点做优化。如果为静态节点，他们生成的DOM永远不会改变，这对运行时模板更新起到了极大的优化作用。
3. 生成渲染函数. 渲染的返回值是VNode，VNode是Vue的虚拟DOM节点，里面有（标签名，子节点，文本等等）

## 26 Vue data 中某一个属性的值发生改变后，视图会立即同步执行重新渲染吗？

不会立即同步执行重新渲染。
Vue 实现响应式并不是数据发生变化之后 DOM 立即变化，而是按一定的策略进行 DOM 的更新。
Vue 在更新 DOM 时是异步执行的。只要侦听到数据变化， Vue 将开启一个队列，并缓冲在同一事件循环中发生的所有数据变更。

如果同一个watcher被多次触发，只会被推入到队列中一次。这种在缓冲时去除重复数据对于避免不必要的计算和 DOM 操作是非常重要的。
然后，在下一个的事件循环"tick"中，Vue 刷新队列并执行实际（已去重的）工作。

## 27 axios是什么

易用、简洁且高效的http库， 支持node端和浏览器端，支持Promise，支持拦截器等高级配置。

## 28 sass是什么？如何在vue中安装和使用？

Sass 是一个将脚本解析成 CSS 的脚本语言（SassScript），也是一款 CSS 预处理器，它减少了 CSS 的重复，也因此节省了时间。Sass 是最早的 CSS 预处理语言，有比 Less 更强大的功能。Sass 扩展了 CSS3，增加了规则、变量、混入选择器、继承等特性。

1. 用npm安装加载程序（ sass-loader、 css-loader等加载程序)。
2. 在 webpack.config.js中配置sass加载程序。

## 29 Vue.js页面闪烁

Vue. js提供了一个v-cloak指令，该指令一直保持在元素上，直到关联实例结束编译。当和CSS一起使用时，这个指令可以隐藏未编译的标签，直到实例编译结束。用法如下。

```html
[v-cloak]{ 
 display:none; 
} 
<div v-cloak>{{ title }}</div>
```

## 30 如何解决数据层级结构太深的问题

在开发业务时，经常会岀现异步获取数据的情况，有时数据层次比较深，如以下代码: `span 'v-text="a.b.c.d"></span>`, 可以使用vm.$set手动定义一层数据: `vm.$set("demo"，a.b.c.d)`

## 31 在 Vue. js开发环境下调用API接口，如何避免跨域

config/ index.js内对 proxyTable项配置代理。

## 32 批量异步更新策略

Vue 在修改数据后，视图不会立刻更新，而是等同一事件循环中的所有数据变化完成之后，再统一进行视图更新。
换句话说，只要观察到数据变化，就会自动开启一个队列，并缓冲在同一个事件循环中发生的所以数据改变。在缓冲时会去除重复数据，从而避免不必要的计算和 DOM 操作。

## 33 vue 的 nextTick 方法的实现原理

1. vue 用异步队列的方式来控制 DOM 更新和 nextTick 回调先后执行
2. microtask 因为其高优先级特性，能确保队列中的微任务在一次事件循环前被执行完毕

## 34 Vue 组件 data 为什么必须是函数 ?

因为组件是可以复用的,JS 里对象是引用关系,如果组件 data 是一个对象,那么子组件中的 data 属性值会互相污染。
所以一个组件的 data 选项必须是一个函数,因此每个实例可以维护一份被返回对象的独立的拷贝。

## 35 v-if和v-for一起使用的弊端及解决办法

由于v-for的优先级比v-if高，所以导致每循环一次就会去v-if一次，而v-if是通过创建和销毁dom元素来控制元素的显示与隐藏，所以就会不停的去创建和销毁元素，造成页面卡顿，性能下降。

解决办法：

1. 在v-for的外层或内层包裹一个元素来使用v-if
2. 用computed处理

## 36 vue常用指令

1. v-model 多用于表单元素实现双向数据绑定（同angular中的ng-model）
2. v-bind 动态绑定 作用： 及时对页面的数据进行更改
3. v-on:click 给标签绑定函数，可以缩写为@，例如绑定一个点击函数 函数必须写在methods里面
4. v-for 格式： v-for="字段名 in(of) 数组json" 循环数组或json(同angular中的ng-repeat)
5. v-show 显示内容 （同angular中的ng-show）
6. v-hide 隐藏内容（同angular中的ng-hide）
7. v-if 显示与隐藏 （dom元素的删除添加 同angular中的ng-if 默认值为false）
8. v-else-if 必须和v-if连用
9. v-else 必须和v-if连用 不能单独使用 否则报错 模板编译错误
10. v-text 解析文本
11. v-html 解析html标签
12. v-bind:class 三种绑定方法 1、对象型 '{red:isred}' 2、三元型 'isred?"red":"blue"' 3、数组型 '[{red:"isred"},{blue:"isblue"}]'
13. v-once 进入页面时 只渲染一次 不在进行渲染
14. v-cloak 防止闪烁
15. v-pre 把标签内部的元素原位输出

## 37 组件传值方式有哪些

1. 父传子：子组件通过props['xx'] 来接收父组件传递的属性 xx 的值
2. 子传父：子组件通过 this.$emit('fnName',value) 来传递,父组件通过接收 fnName 事件方法来接收回调
3. 其他方式：通过创建一个bus，进行传值
4. 使用Vuex

## 38 vue中如何编写可复用的组件 （编写组件的原则）

1. 以组件功能命名
2. 只负责ui的展示和交互动画，不要在组件里与服务器打交道（获取异步数据等）
3. 可复用组件不会因组件使用的位置、场景而变化。尽量减少对外部条件的依赖。

## 39 如何让CSS只在当前组件中起作用？

在每一个Vue.js组件中都可以定义各自的CSS、 JavaScript代码。如果希望组件内写的CSS只对当前组件起作用，只需要在Style标签添加Scoped属性，即。

## 40 keep-alive是什么？

如果需要在组件切换的时候，保存一些组件的状态防止多次渲染，就可以使用 keep-alive 组件包裹需要保存的组件。

两个重要属性，include 缓存组件名称，exclude 不需要缓存的组件名称。

## 41如何在 Vue. js动态插入图片

对“src”属性插值将导致404请求错误。应使用 v-bind:src （简写`:src`）格式代替。

## 42 父子组件的生命周期顺序

1. 加载渲染过程：
   父beforeCreate->父created->父beforeMount->子beforeCreate->子created->子beforeMount->子mounted->父mounted
2. 子组件更新过程：父beforeUpdate->子beforeUpdate->子updated->父updated
3. 父组件更新过程：父beforeUpdate->父updated
4. 销毁过程：父beforeDestroy->子beforeDestroy->子destroyed->父destroyed

## 43 vuex的核心概念

1. state => 基本数据
2. getters => 从基本数据派生的数据
3. mutations => 修改数据，同步
4. actions => 修改数据，异步 (Action 提交的是 mutation，而不是直接变更状态)
5. modules => 模块化Vuex

## 44 vuex是什么？怎么使用？哪种功能场景使用它？

Vuex 是一个专为 Vue.js 应用程序开发的状态管理器，采用集中式存储管理应用的所有组件的状态，主要是为了多页面、多组件之间的通信。
Vuex有5个重要的属性，分别是 State、Getter、Mutation、Action、Module，由 view 层发起一个 Action 给 Mutation，在 Mutation 中修改状态，返回新的状态，通过 Getter暴露给 view层的组件或者页面，页面监测到状态改变于是更新页面。如果你的项目很简单，最好不要使用 Vuex，对于大型项目，Vuex 能够更好的帮助我们管理组件外部的状态，一般可以运用在购物车、登录状态、播放等场景中。

## 45 多个组件之间如何拆分各自的state，每块小的组件有自己的状态，它们之间还有一些公共的状态需要维护，如何思考这块

1. 公共的数据部分可以提升至和他们最近的父组件，由父组件派发
2. 公共数据可以放到vuex中统一管理，各组件分别获取

## 46  vue-router路由的两种模式

vue-router中默认使用的是hash模式

1. hash模式, 带#。如：http://localhost:8080/#/pageA。改变hash，浏览器本身不会有任何请求服务器动作的，但是页面状态和url已经关联起来了。
2. history模式，不带#， 如：http://localhost:8080/ 正常的而路径，并没有#。基于HTML5的 pushState、replaceState实现

## 47 vue-router如何定义嵌套路由

通过children 数组：

```js
const router = new VueRouter({
  routes: [
    {
      path: "/parentPage",
      component: testPage,
      children: [
        {
          path: "/childrenA",
          component: childrenComponentA,
        },
        {
          path: "/childrenB",
          component: childrenComponentB,
        },
      ],
    },
    {
      // 其他和parentPage平级的路由
    },
  ],
});
```

## 48  vue-router有哪几种导航钩子？

1. 全局导航钩子：router.beforeEach(to,from,next)
2. 组件内的钩子beforeRouteEnter (to, from, next) beforeRouteUpdate (to, from, next) beforeRouteLeave (to, from, next)
3. 单独路由独享组件 beforeEnter: (to, from, next)

## 49 $route和$router的区别

1. $route是“路由信息对象”，包括path，params，hash，query，fullPath，matched，name等路由信息参数。
2. $router是“路由实例”对象包括了路由的跳转方法，钩子函数等

## 50 路由之间跳转的方式

1. 声明式（标签跳转）
2. 编程式（ js跳转）

## 51 active-class是哪个组件的属性

vue-router 模块 的router-link**组件**

ElementUI是怎么做表单验证的？在循环里对每个input验证怎么做呢？
model绑定表单数据,通过prop取表单数值，根据rule取form-item rules 或则rules[prop]校验

你有二次封装过ElementUI组件吗？
ElementUI怎么修改组件的默认样式？
方法一：/deep/
方法二：>>>
方法三：在外层添加一层div，设置自定义类名，再修改里边的样式, 格式.自定义类名 .需要修改的样式 {}。

ElementUI的穿梭组件如果数据量大会变卡怎么解决不卡的问题呢？
在 left-footer 的 slot 里面加个翻页组件，
并修改 filter-method 方法重绘穿梭机组件，
大概保持每页 50 条这样子。

ElementUI表格组件如何实现动态表头？
使用自定义表头，即 中传入自定义 slot。表头整体结构变化则得自己 v-for 表头配置拼

<el-table-column> 重绘
<template v-for="item in tableColownms"> 
	<el-table-column v-if="item.type!='hidden'" :key="item.id" :prop="item.field" sortable :label="item.label"> 
</template>
1
2
3
4
ElementUI使用表格组件时有遇到过问题吗？
遇到表格的横向滚动条被固定列挡住的问题，在有合计的情况下（1：表格有横向滚动条，2：有固定列，3：底部有合计）满足这三个条件，
固定列的的宽度会把横向滚动条挡住，导致固定列下面滚动条不能拖动。

Object.freeze
这算是一个性能优化的小技巧吧。在我们遇到一些 big data的业务场景，它就很有用了。尤其是做管理后台的时候，经常会有一些超大数据量的 table，或者一个含有 n 多数据的图表，这种数据量很大的东西使用起来最明显的感受就是卡。但其实很多时候其实这些数据其实并不需要响应式变化，这时候你就可以使用 Object.freeze 方法了，它可以冻结一个对象(注意它不并是 vue 特有的 api)。
当你把一个普通的 JavaScript 对象传给 Vue 实例的 data 选项，Vue 将遍历此对象所有的属性，并使用 Object.defineProperty 把这些属性全部转为 getter/setter，它们让 Vue 能进行追踪依赖，在属性被访问和修改时通知变化。
使用了 Object.freeze 之后，不仅可以减少 observer 的开销，还能减少不少内存开销。相关 issue。
使用方式：this.item = Object.freeze(Object.assign({}, this.item))

有用过哪些vue的ui？说说它们的优缺点？
个人认为iview比elementUI好看，elementUI在多级联动菜单有一个bug（父子value一样的时候不显示） ？

mint-ui使用过程中有没有遇到什么坑？怎么解决的？
1，样式不容易被修改，可以用/deep/或者》》》进行复写；
2，Field组件在ios上，输入框的提示信息太靠后，由label引起的，所以不要用它自带的label做提示名
3，无限滚动



#### 52 **spring 中都用到了哪些设计模式?**

- **「1.工厂设计模式」**: 比如通过 BeanFactory 和 ApplicationContext 来生产 Bean 对象
- **「2.代理设计模式」**: AOP 的实现方式就是通过代理来实现，Spring主要是使用 JDK 动态代理和 CGLIB 代理
- **「3.单例设计模式」**: Spring 中的 Bean 默认都是单例的
- **「4.模板方法模式」**: Spring 中 jdbcTemplate 等以 Template 结尾的对数据库操作的类，都会使用到模板方法设计模式，一些通用的功能
- **「5.包装器设计模式」**: 我们的项目需要连接多个数据库，而且不同的客户在每次访问中根据需要会去访问不同的数据库。这种模式让我们可以根据客户的需求能够动态切换不同的数据源
- **「6.观察者模式」**: Spring 事件驱动模型观察者模式的
- **「7.适配器模式」**:Spring AOP 的增强或通知(Advice)使用到了适配器模式



#### **53.spring 中有哪些核心模块?**

- 1.**「Spring Core」**：Spring核心，它是框架最基础的部分，提供IOC和依赖注入DI特性
- 2.**「Spring Context」**：Spring上下文容器，它是 BeanFactory 功能加强的一个子接口
- 3.**「Spring Web」**：它提供Web应用开发的支持
- 4.**「Spring MVC」**：它针对Web应用中MVC思想的实现
- 5.**「Spring DAO」**：提供对JDBC抽象层，简化了JDBC编码，同时，编码更具有健壮性
- 6.**「Spring ORM」**：它支持用于流行的ORM框架的整合，比如：Spring + Hibernate、Spring + iBatis、Spring + JDO的整合等
- 7.**「Spring AOP」**：即面向切面编程，它提供了与AOP联盟兼容的编程实现
- 





#### **54 .说一下你理解的 IOC 是什么?**

首先 IOC 是一个**「容器」**，是用来装载对象的，它的核心思想就是**「控制反转」**那么究竟**「什么是控制反转」**?

控制反转就是说，**「把对象的控制权交给了 spring，由 spring 容器进行管理」**，我们不进行任何操作那么为**「什么需要控制反转」**?

我们想象一下，没有控制反转的时候，我们需要**「自己去创建对象，配置对象」**，还要**「人工去处理对象与对象之间的各种复杂的依赖关系」**，当一个工程的量起来之后，这种关系的维护是非常令人头痛的，所以就有了控制反转这个概念，将对象的创建、配置等一系列操作交给 spring 去管理，我们在使用的时候只要去取就好了



#### **55.spring 中的 IOC 容器有哪些?有什么区别?**

spring 主要提供了**「两种 IOC 容器」**，一种是 **「BeanFactory」**，还有一种是 **「ApplicationContext」**

它们的区别就在于，BeanFactory **「只提供了最基本的实例化对象和拿对象的功能」**，而 ApplicationContext 是继承了 BeanFactory 所派生出来的产物，是其子类，它的作用更加的强大，比如支持注解注入、国际化等功能

#### 56、Spring AOP 底层原理

aop 底层是采用动态代理机制实现的：接口+实现类 
 如果要代理的对象，实现了某个接口，那么 Spring AOP 会使用 JDK Proxy，去创建代 理对象。 
 没有实现接口的对象，就无法使用 JDK Proxy 去进行代理了，这时候 Spring AOP 会 使用 Cglib 生成一个被代理对象的子类来作为代理。 



就是由代理创建出一个和 impl 实现类平级的一个对象，但是这个对象不是一个真正的对象， 只是一个代理对象，但它可以实现和 impl 相同的功能，这个就是 aop 的横向机制原理，这 样就不需要修改源代码

#### 57、HashMap 的底层数据结构是怎样的

当链表长度大于阈值（默认为 8）时，会首先调用 treeifyBin()方法。这个方法会根据 HashMap 数组来决定是否转换为红黑树。只有当数组长度大于或者等于 64 的情况下，才会 执行转换红黑树操作，以减少搜索时间。否则，就是只是执行 resize() 方法对数组扩容

#### 58、HashMap 的扩容机制是怎样的

 空参数的构造函数：实例化的 HashMap 默认内部数组是 null，即没有实例化。第一次 调用 put 方法时，则会开始第一次初始化扩容，长度为 16。 
 有参构造函数：用于指定容量。会根据指定的正整数找到不小于指定容量的 2 的幂数， 将这个数设置赋值给阈值（threshold）。第一次调用 put 方法时，会将阈值赋值给容量， 然后让 阈值 = 容量 x 负载因子。
  如果不是第一次扩容，则容量变为原来的 2 倍，阈值也变为原来的 2 倍。（容量和阈值 都变为原来的 2 倍时，负载因子还是不变）。 
此外还有几个细节需要注意： 
 首次 put 时，先会触发扩容（算是初始化），然后存入数据，然后判断是否需要扩容； 
 不是首次 put，则不再初始化，直接存入数据，然后判断是否需要扩容

#### 59、请你谈谈 MySQL 事务隔离级别，MySQL 的默认隔离级别是什么？ 

为了达到事务的四大特性，数据库定义了 4 种不同的事务隔离级别：  READ-UNCOMMITTED（读取未提交）：最低的隔离级别，允许脏读，也就是可能读取 到其他会话中未提交事务修改的数据，可能会导致脏读、幻读或不可重复读。 
 READ-COMMITTED（读取已提交）： 只能读取到已经提交的数据。Oracle 等多数数 据库默认都是该级别 （不重复读），可以阻止脏读，但是幻读或不可重复读仍有可能发 生。 
 REPEATABLE-READ（可重复读）：对同一字段的多次读取结果都是一致的，除非数据 是被本身事务自己所修改，可以阻止脏读和不可重复读，但幻读仍有可能发生。  SERIALIZABLE（可串行化）：最高的隔离级别，完全服从 ACID 的隔离级别。所有的 事务依次逐个执行，这样事务之间就完全不可能产生干扰，也就是说，该级别可以防止脏 读、不可重复读以及幻读。 
 MySQL 默认采用的 REPEATABLE_READ 隔离级别。 

#### 60、可重复读解决了哪些问题？ 

 可重复读的核心就是一致性读(consistent read);保证多次读取同一个数据时，其值都和事 务开始时候的内容是一致，禁止读取到别的事务未提交的数据，会造成幻读。 
 而事务更新数据的时候，只能用当前读。如果当前的记录的行锁被其他事务占用的话，就 需要进入锁等待。
 查询只承认在事务启动前就已经提交完成的数据。 
 可重复读解决的是重复读的问题，可重复读在快照读的情况下是不会有幻读，但当前读的 时候会有幻读。 

#### 61、对 SQL 慢查询会考虑哪些优化 ？

 分析语句，是否加载了不必要的字段/数据。 
 分析 SQL 执行计划（explain extended），思考可能的优化点，是否命中索引等。 
 查看 SQL 涉及的表结构和索引信息。 
 如果 SQL 很复杂，优化 SQL 结构。 
 按照可能的优化点执行表结构变更、增加索引、SQL 改写等操作。 
 查看优化后的执行时间和执行计划
 如果表数据量太大，考虑分表。
  利用缓存，减少查询次数。

#### 62、谈一谈缓存穿透、缓存击穿和缓存雪崩，以及解决办法？ 

##### 缓存穿透 

 问题：大量并发查询不存在的 KEY，在缓存和数据库中都不存在，同时给缓存和数据库 带来压力。 
 原因：一般而言，缓存穿透有 2 种可能性：业务数据被误删，导致缓存和数据库中都没 有数据。恶意进行 ddos 攻击。 
 分析：为什么会多次透传呢？不存在 一直为空，需要注意让缓存能够区分 KEY 不存在和 查询到一个空值。 
 解决办法：缓存空值的 KEY，这样第一次不存在也会被加载会记录，下次拿到有这个 KEY。Bloom 过滤或 RoaingBitmap 判断 KEY 是否存在，如果布隆过滤器中没有查到 这个数据，就不去数据库中查。在处理请求前增加恶意请求检查，如果检测到是恶意攻击， 则拒绝进行服务。完全以缓存为准，使用延迟异步加载的策略（异步线程负责维护缓存的 数据，定期或根据条件触发更新），这样就不会触发更新。 

#####  缓存击穿 

 问题：某个 KEY 失效的时候，正好有大量并发请求访问这个 KEY。 
 分析：跟穿透其实很像，属于比较偶然的。 
 解决办法：KEY 的更新操作添加全局互斥锁。完全以缓存为准，使用延迟异步加载的策 略（异步线程负责维护缓存的数据，定期或根据条件触发更新），这样就不会触发更新。 

##### 缓存雪崩 

 问题：当某一时刻发生大规模的缓存失效的情况，导致大量的请求无法获取数据，从而将 流量压力传导到数据库上，导致数据库压力过大甚至宕机。 
 原因：一般而言，缓存雪崩有 2 种可能性：大量的数据同一个时间失效：比如业务关系 强相关的数据要求同时失效 Redis 宕机 
 分析：一般来说，由于更新策略、或者数据热点、缓存服务宕机等原因，可能会导致缓存 数据同一个时间点大规模不可用，或者都更新。所以，需要我们的更新策略要在时间上合 适，数据要均匀分享，缓存服务器要多台高可用。 
 解决办法：更新策略在时间上做到比较平均。如果数据需要同一时间失效，可以给这批数 据加上一些随机值，使得这批数据不要在同一个时间过期，降低数据库的压力。使用的热 数据尽量分散到不同的机器上。多台机器做主从复制或者多副本，实现高可用。做好主从 的部署，当主节点挂掉后，能快速的使用从结点顶上。实现熔断限流机制，对系统进行负 载能力控制。对于非核心功能的业务，拒绝其请求，只允许核心功能业务访问数据库获取 数据。服务降价：提供默认返回值，或简单的提示信息

#### 63、一个 Redis 实例最多能存放多少的 keys？List、Set、Sorted Set 他们最 多能存放多少元素？ 

理论上 Redis 可以处理多达 232 的 keys，并且在实际中进行了测试，每个实例至少存放 了 2 亿 5 千万的 keys。我们正在测试一些较大的值。任何 list、set、和 sorted set 都可 以放 232 个元素。换句话说，Redis 的存储极限是系统中的可用内存值。 

#### 64、Redis 数据结构 压缩列表和跳跃表的区别 

 压缩列表（ziplist）本质上就是一个字节数组，是 Redis 为了节约内存而设计的一种线性 数据结构，可以包含多个元素，每个元素可以是一个字节数组或一个整数。 30 
 跳跃表（skiplist）是一种有序数据结构，它通过在每个节点中维持多个指向其他节点的指 针，从而达到快速访问节点的目的。跳跃表支持平均 O（logN）、最坏 O（N）复杂度 的节点查找，还可以通过顺序性操作来批量处理节点

#### 65、谈谈自己对于 Spring AOP 的了解？ 

AOP(Aspect-Oriented Programming:面向切面编程)能够将那些与业务无关，却为业务模块 所共同调用的逻辑或责任（例如事务处理、日志管理、权限控制等）封装起来，便于减少系统 的重复代码，降低模块间的耦合度，并有利于未来的可拓展性和可维护性。 

#### 66、 Spring Bean 容器的生命周期是什么样的？ 

 Bean 容器找到配置文件中 Spring Bean 的定义。 
 Bean 容器利用 Java Reflection API 创建一个 Bean 的实例。 
 如果涉及到一些属性值 利用 set()方法设置一些属性值。 
 如果 Bean 实现了 BeanNameAware 接口，调用 setBeanName()方法，传入 Bean 的 名字。 
 如果 Bean 实现了 BeanClassLoaderAware 接口，调用 setBeanClassLoader()方法， 传入 ClassLoader 对象的实例。 
 如果 Bean 实现了 BeanFactoryAware 接口，调用 setBeanFactory()方法，传入 BeanFactory 对象的实例。 
 与上面的类似，如果实现了其他 *.Aware 接口，就调用相应的方法。  如果有和加载这个 Bean 的 Spring 容器相关的 BeanPostProcessor 对象，执行 postProcessBeforeInitialization() 方法 
 如果 Bean 实现了 InitializingBean 接口，执行 afterPropertiesSet()方法。  如果 Bean 在配置文件中的定义包含 init-method 属性，执行指定的方法。  如果有和加载这个 Bean 的 Spring 容器相关的 BeanPostProcessor 对象，执行 postProcessAfterInitialization() 方法 
 当要销毁 Bean 的时候，如果 Bean 实现了 DisposableBean 接口，执行 destroy() 方 法。 
 当要销毁 Bean 的时候，如果 Bean 在配置文件中的定义包含 destroy-method 属性， 执行指定的方法

#### 67、Lambda 表达式是啥？优缺点？ 

lambda 表达式，也被称为闭包，它是推动 Java 8 发布的最重要新特性。lambda 允许把函 数作为一个方法的参数（函数作为参数传递进方法中），使用 Lambda 表达式可以使代码变 的更加简洁紧凑。 
优点： 
 代码更加简洁  减少匿名内部类的创建，节省资源 
 使用时不用去记忆所使用的接口和抽象函数
 缺点：
  不易于后期维护，必须熟悉 lambda 表达式和抽象函数中参数的类型  可读性差 
 若不用并行计算，很多时候计算速度没有比传统的 for 循环快。（并行计算有时需要预热 才显示出效率优势） 
 不容易调试。 
 若其他程序员没有学过 lambda 表达式，代码不容易让其他语言的程序员看懂

#### 68、MySQL 事务的特性有什么，说一下分别是什么意思？ 

 原子性：即不可分割性，事务要么全部被执行，要么就全部不被执行。  一致性或可串性。事务的执行使得数据库从一种正确状态转换成另一种正确状态。 
 隔离性。在事务正确提交之前，不允许把该事务对数据的任何改变提供给任何其他事务。 持久性。事务正确提交后，其结果将永久保存在数据库中，即使在事务提交后有了其他故 障，事务的处理结果也会得到保存

#### 69、Redis 常见的几种数据结构说一下？各自的使用场景？ 

string 介绍：string 数据结构是简单的 key-value 类型。 
使用场景： 一般常用在需要计数的场景，比如用户的访问次数、热点文章的点赞转发数量等 等。 
list 介绍：list 即是 链表 使用场景：发布与订阅或者说消息队列、慢查询。 hash 介绍：hash 类似于 JDK1.8 前的 HashMap，内部实现也差不多(数组 + 链表)。 使用场景：系统中对象数据的存储。 
set 介绍：set 类似于 Java 中的 HashSet 。Redis 中的 set 类型是一种无序集合，集合中的元 素没有先后顺序。当你需要存储一个列表数据，又不希望出现重复数据时，set 是一个很好的 选择，并且 set 提供了判断某个成员是否在一个 set 集合内的重要接口，这个也是 list 所不 能提供的。可以基于 set 轻易实现交集、并集、差集的操作 47 使用场景： 需要存放的数据不能重复以及需要获取多个数据源交集和并集等场景。 
sorted set 介绍：和 set 相比，sorted set 增加了一个权重参数 score，使得集合中的元素能够按 score 进行有序排列，还可以通过 score 的范围来获取元素的列表。有点像是 Java 中 HashMap 和 TreeSet 的结合体。 使用场景：需要对数据根据某个权重进行排序的场景。比如在直播系统中，实时排行信息包含 直播间在线用户列表，各种礼物排行榜，弹幕消息（可以理解为按消息维度的消息排行榜）等 信息。 
bitmap 介绍：bitmap 存储的是连续的二进制数字（0 和 1），通过 bitmap, 只需要一个 bit 位来表 示某个元素对应的值或者状态，key 就是对应元素本身 。我们知道 8 个 bit 可以组成一个 byte，所以 bitmap 本身会极大的节省储存空间。。 使用场景：适合需要保存状态信息（比如是否签到、是否登录...）并需要进一步对这些信息进 行分析的场景。比如用户签到情况、活跃用户情况、用户行为统计（比如是否点赞过某个视 频）。

#### 70、Java 多线程有哪几种实现方式？ 

 通过继承 Thread 类创建线程类 
 实现 Runnable 接口创建线程类 
 通过 Callable 和 Future 接口创建线程

#### 71、MySQL 索引分类? 单列索引 

 普通索引：MySQL 中基本索引类型，没有什么限制，允许在定义索引的列中插入重复值 和空值，纯粹为了查询数据更快一点。 
 唯一索引：索引列中的值必须是唯一的，但是允许为空值，
 主键索引：是一种特殊的唯一索引，不允许有空值。 
组合索引： 多个字段组合上创建的索引，只有在查询条件中使用了这些字段的左边字段时，索引才会被使 用，使用组合索引时遵循最左前缀集合。 
全文索引： 只有在 MyISAM 引擎上才能使用，只能在 CHAR,VARCHAR,TEXT 类型字段上使用全文 索引，介绍了要求，说说什么是全文索引，就是在一堆文字中，通过其中的某个关键字等，就 能找到该字段所属的记录行，比如有"你是个靓仔，靓女 ..." 通过靓仔，可能就可以找到该条 记录 
空间索引： 空间索引是对空间数据类型的字段建立的索引，MySQL 中的空间数据类型有四种，geometry、point、LineString、polygon。在创建空间索引时，使用 SPATIAL 关 键字。要求，引擎为 MyISAM，创建空间索引的列，必须将其声明为 NOT NULL。 

#### 72、了解线程 & 进程的区别吗？  

操作系统中可以拥有多个进程，一个进程里可以拥有多个线程，线程在进程内执行 进程和线程的区别 
 容易创建新线程。创建新进程需要重复父进程 
 线程可以控制同一进程的其他线程。进程无法控制兄弟进程，只能控制其子进程 
 进程拥有自己的内存空间。线程使用进程的内存空间，且要和该进程的其他线程共享这个 空间；而不是在进程中给每个线程单独划分一点空间。 
 （同一进程中的）线程在共享内存空间中运行，而进程在不同的内存空间中运行 
 线程可以使用 wait（），notify（），notifyAll（）等方法直接与其他线程（同一进程） 通信；而，进程需要使用“进程间通信”（IPC）来与操作系统中的其他进程通信

#### 73、据库三大范式是什么 

 第一范式：每个列都不可以再拆分。 
 第二范式：在第一范式的基础上，非主键列完全依赖于主键，而不能是依赖于主键的一部 分。 
 第三范式：在第二范式的基础上，非主键列只依赖于主键，不依赖于其他非主键。 在设计数据库结构的时候，要尽量遵守三范式，如果不遵守，必须有足够的理由。比如性 能。事实上我们经常会为了性能而妥协数据库的设计。

#### **74：HashMap 的数据结构？**

A：哈希表结构（链表散列：数组+链表）实现，结合数组和链表的优点。当链表长度超过 8 时，链表转换为红黑树。
 **`数组的优点`**随机访问性强，查找速度快，时间复杂度为O(1)

**`链表的优点`**1.任意位置插入元素和删除元素的速度快，时间复杂度为O(1) 2.内存利用率高，不会浪费内存3.链表的空间大小不固定，可以动态拓展

#### **75：HashMap 的工作原理？** 

HashMap 底层是 hash 数组和单向链表实现，数组中的每个元素都是链表，由 Node 内部类（实现 Map.Entry接口）实现，HashMap 通过 put & get 方法存储和获取。

存储对象时，将 K/V 键值传给 put() 方法：

①、调用 hash(K) 方法计算 K 的 hash 值，然后结合数组长度，计算得数组下标；

②、调整数组大小（当容器中的元素个数大于 capacity * loadfactor 时，容器会进行扩容resize 为 2n）；

③、i.如果 K 的 hash 值在 HashMap 中不存在，则执行插入，若存在，则发生碰撞；

ii.如果 K 的 hash 值在 HashMap 中存在，且它们两者 equals 返回 true，则更新键值对；

iii. 如果 K 的 hash 值在 HashMap 中存在，且它们两者 equals 返回 false，则插入链表的尾部（尾插法）或者红黑树中（树的添加方式）。（JDK 1.7 之前使用头插法、JDK 1.8 使用尾插法）（注意：当碰撞导致链表大于 TREEIFY_THRESHOLD = 8 时，就把链表转换成红黑树）

获取对象时，将 K 传给 get() 方法：①、调用 hash(K) 方法（计算 K 的 hash 值）从而获取该键值所在链表的数组下标；②、顺序遍历链表，equals()方法查找相同 Node 链表中 K 值对应的 V 值。

hashCode 是定位的，存储位置；equals是定性的，比较两者是否相等。

#### **76.当两个对象的 hashCode 相同会发生什么？**

因为 hashCode 相同，不一定就是相等的（equals方法比较），所以两个对象所在数组的下标相同，"碰撞"就此发生。又因为 HashMap 使用链表存储对象，这个 Node 会存储到链表中。

#### 7**7.HashMap中put方法的过程？**

答：“调用哈希函数获取Key对应的hash值，再计算其数组下标；

如果没有出现哈希冲突，则直接放入数组；如果出现哈希冲突，则以链表的方式放在链表后面；

如果链表长度超过阀值( TREEIFY THRESHOLD==8)，就把链表转成红黑树，链表长度低于6，就把红黑树转回链表;

如果结点的key已经存在，则替换其value即可；

如果集合中的键值对大于12，调用resize方法进行数组扩容。”

#### 7**8.数组扩容的过程？**

创建一个新的数组，其容量为旧数组的两倍，并重新计算旧数组中结点的存储位置。结点在新数组中的位置只有两种，原下标位置或原下标+旧数组的大小。

#### **79.说说你对红黑树的见解？**

- 每个节点非红即黑
- 根节点总是黑色的
- 如果节点是红色的，则它的子节点必须是黑色的（反之不一定）
- 每个叶子节点都是黑色的空节点（NIL节点）
- 从根节点到叶节点或空子节点的每条路径，必须包含相同数目的黑色节点（即相同的黑色高度）

#### 80. Linedlist和ArrayList的区别

ArrayList是基于动态数组的数据结构，LinkedList基于链表的数据结构。
ArrayList查询操作快，LinedList增删操作快。

（4） 结合项目中使用
对于需要快速插入，删除元素，应该使用LinkedList。
对于需要快速随机访问元素，应该使用ArrayList。
对于“单线程环境” 或者 “多线程环境，但List仅仅只会被单个线程操作”，此时应该使用非同步的类(如ArrayList)。
对于“多线程环境，且List可能同时被多个线程操作”，此时，应该使用同步的类(如Vector)。

#### 81. 如何预防死锁

## 造成死锁的⼏个原因： 

1. ⼀个资源每次只能被⼀个线程使⽤ 

2. ⼀个线程在阻塞等待某个资源时，不释放已占有资源 

\3. ⼀个线程已经获得的资源，在未使⽤完之前，不能被强⾏剥夺 

\4. 若⼲线程形成头尾相接的循环等待资源关系

这是造成死锁必须要达到的4个条件，如果要避免死锁，只需要不满⾜其中某⼀个条件即可。⽽其中前3个条件是作为锁要符合的条件，所以要避免死锁就需要打破第4个条件，不出现循环等待锁的关系。 

在开发过程中： 

\1. 要注意加锁顺序，保证每个线程按同样的顺序进⾏加锁 

\2. 要注意加锁时限，可以针对所设置⼀个超时时间 

\3. 要注意死锁检查，这是⼀种预防机制，确保在第⼀时间发现死锁并进⾏解决

#### 82. Java基础数据类型

 **一、Java四大数据类型分类**

**1、整型**

byte 、short 、int 、long

**2、浮点型**

float 、 double

**3、字符型**

char

**4、布尔型**

boolean

#### 83面向对象的三大特征

封装
因为对象都对自己负责，所以，对象的很多东西都不需要或不可以暴露给其他对象。封装解决了数据的安全性，内在也体现了‘每个对象都对自己负责’。

继承
主要是实现了代码的复用。

多态
说白了，就是一个相同的指令发出，不同的对象会对这个指令有不同的反应，所以称为多态。

1、SpringBoot自动配置的原理是什么？
SpringBoot启动的时候通过@EnableAutoConfiguration注解找到META-INF/spring.factories配置文件中所有的自动配置类，并对其进行加载，而这些自动配置类的类名都是以AutoConfiguration结尾来命名的，它实际上就是一个javaConfig形式的Spring容器配置类，它们都有一个@EnableConfigurationPerperties的注解，通过这个注解启动XXXProperties命名的类去加载全局配置中的属性，如server.port,而XXXProperties通过@ConfigurationProperties注解将全局配置文件中的属性与自己的属性进行绑定。

2、SpringBoot 配置加载顺序?
1、 properties文件 2、YAML文件 3、系统环境变量 4、命令行参数

3、spring boot初始化环境变量流程?
1、 调用prepareEnvironment方法去设置环境变量

2、 接下来有三个方法getOrCreateEnvironment，configureEnvironment，environmentPrepared

3、 getOrCreateEnvironment去初始化系统环境变量

4、 configureEnvironment去初始化命令行参数

5、 environmentPrepared当广播到来的时候调用onApplicationEnvironmentPreparedEvent方法去使用postProcessEnvironment方法load yml和properties变量

4、运行 SpringBoot 有哪几种方式？
1、 打包用命令或者者放到容器中运行

2、 用 Maven/ Gradle 插件运行

3、 直接执行 main 方法运行

#### **问题五：Spring Boot 还提供了其它的哪些 Starter Project Options？**

Spring Boot 也提供了其它的启动器项目包括，包括用于开发特定类型应用程序的典型依赖项。

spring-boot-starter-web-services - SOAP Web Services

spring-boot-starter-web - Web 和 RESTful 应用程序

spring-boot-starter-test - 单元测试和集成测试

spring-boot-starter-jdbc - 传统的 JDBC

spring-boot-starter-hateoas - 为服务添加 HATEOAS 功能

spring-boot-starter-security - 使用 SpringSecurity 进行身份验证和授权

spring-boot-starter-data-jpa - 带有 Hibeernate 的 Spring Data JPA

spring-boot-starter-data-rest - 使用 Spring Data REST 公布简单的 REST 服务

#### 问题十二 什么是 Spring Date？

来自：//projects.spring.io/spring- data/

> Spring Data 的使命是在保证底层数据存储特殊性的前提下，为数据访问提供一个熟悉的，一致性的，基于 Spring 的编程模型。这使得使用数据访问技术，关系数据库和非关系数据库，map-reduce 框架以及基于云的数据服务变得很容易。

为了让它更简单一些，Spring Data 提供了不受底层数据源限制的 Abstractions 接口。

下面来举一个例子

![img](https://ask.qcloudimg.com/http-save/3421842/5cbuxgvbxw.jpeg?imageView2/2/w/1620)

你可以定义一简单的库，用来插入，更新，删除和检索代办事项，而不需要编写大量的代码。

#### 问题十九 RequestMapping 和 GetMapping 的不同之处在哪里？

- RequestMapping 具有类属性的，可以进行 GET,POST,PUT 或者其它的注释中具有的请求方法。
- GetMapping 是 GET 请求方法中的一个特例。它只是 ResquestMapping 的一个延伸，目的是为了提高清晰度。

#### 问题二十 为什么我们不建议在实际的应用程序中使用 Spring Data Rest?

我们认为 Spring Data Rest 很适合快速原型制造！在大型应用程序中使用需要谨慎。

通过 Spring Data REST 你可以把你的数据实体作为 RESTful 服务直接发布。

当你设计 RESTful 服务器的时候，最佳实践表明，你的接口应该考虑到两件重要的事情：

- 你的模型范围。
- 你的客户。

通过 With Spring Data REST，你不需要再考虑这两个方面，只需要作为 TEST 服务发布实体。

这就是为什么我们建议使用 Spring Data Rest 在快速原型构造上面，或者作为项目的初始解决方法。对于完整演变项目来说，这并不是一个好的注意。



**5、Spring Boot 的核心注解是哪个？它主要由哪几个注解组成的？**

启动类上面的注解是@SpringBootApplication，它也是 Spring Boot 的核心注解，主要组合包含了以下 3 个注解：

@SpringBootConfiguration：组合了 @Configuration 注解，实现配置文件的功能。

@EnableAutoConfiguration：打开自动配置的功能，也可以关闭某个自动配置的选项，如关闭数据源自动配置功能： @SpringBootApplication(exclude = { DataSourceAutoConfiguration.class })。

@ComponentScan：Spring组件扫描。

### 1.10 SpringBoot、Spring MVC和Spring有什么区别？

- **Spring**
  Spring最重要的特征是依赖注入。所有Spring Modules不是依赖注入就是IOC控制反转。
  当我们恰当的使用DI或者是IOC的时候，可以开发松耦合应用。
- **Spring MVC**
  Spring MVC提供了一种分离式的方法来开发Web应用。通过运用像DispatcherServelet，MoudlAndView 和 ViewResolver 等一些简单的概念，开发 Web 应用将会变的非常简单。
- **SpringBoot**
  Spring和Spring MVC的问题在于需要配置大量的参数。
  SpringBoot通过一个自动配置和启动的项来解决这个问题。

### 3.2 比较一下Spring Security 和Shiro各自的优缺点 ?

由于SpringBoot官方提供了大量的非常方便的开箱即用的Starter，包括Spring Security的Starter ，使得在 SpringBoot中使用Spring Security变得更加容易，甚至只需要添加一个依赖就可以保护所有的接口，所以，如果是SpringBoot 项目，一般选择 Spring Security 。当然这只是一个建议的组合，单纯从技术上来说，无论怎么组合，都是没有问题的。Shiro和Spring Security相比，主要有如下一些特点：

1. Spring Security 是一个重量级的安全管理框架；Shiro 则是一个轻量级的安全管理框架
2. Spring Security 概念复杂，配置繁琐；Shiro 概念简单、配置简单
3. Spring Security 功能强大；Shiro 功能简单







####  前后端分离，如何维护接口文档 ?

前后端分离开发日益流行，大部分情况下，我们都是通过 Spring Boot 做前后端分离开发，前后端分离一定会有接口文档，不然会前后端会深深陷入到扯皮中。一个比较笨的方法就是使用 word 或者 md 来维护接口文档，但是效率太低，接口一变，所有人手上的文档都得变。在 Spring Boot 中，这个问题常见的解决方案是 Swagger ，使用 Swagger 我们可以快速生成一个接口文档网站，接口一旦发生变化，文档就会自动更新，所有开发工程师访问这一个在线网站就可以获取到最新的接口文档，非常方便。

### 4.12 如何使用SpringBoot实现异常处理？

Spring 提供了一种使用 ControllerAdvice 处理异常的非常有用的方法。 我们通过实现一个 ControlerAdvice 类，来处理控制器类抛出的所有异常。

### [11、什么是WebSockets？](https://link.zhihu.com/?target=https%3A//gitee.com/souyunku/DevBooks/blob/master/docs/SpringBoot/SpringBoot%E6%9C%80%E6%96%B0%E9%9D%A2%E8%AF%95%E9%A2%98%E5%8F%8A%E7%AD%94%E6%A1%88%E9%99%84%E7%AD%94%E6%A1%88%E6%B1%87%E6%80%BB.md%231%E4%BB%80%E4%B9%88%E6%98%AFwebsockets)

WebSocket是一种计算机通信协议，通过单个TCP连接提供全双工通信信道。

![img_2.png][img_0826_04_2.png]

**1、** WebSocket是双向的 -使用WebSocket客户端或服务器可以发起消息发送。

**2、** WebSocket是全双工的 -客户端和服务器通信是相互独立的。

**3、** 单个TCP连接 -初始连接使用HTTP，然后将此连接升级到基于套接字的连接。然后这个单一连接用于所有未来的通信

**4、** Light -与http相比，WebSocket消息数据交换要轻得多。



[进程](https://zh.wikipedia.org/zh-cn/进程)（process）和[线程](https://zh.wikipedia.org/zh-cn/线程)（thread）是操作系统的基本概念，但是它们比较抽象，不容易掌握。

最近，我读到一篇[材料](http://www.qnx.com/developers/docs/6.4.1/neutrino/getting_started/s1_procs.html)，发现有一个很好的类比，可以把它们解释地清晰易懂。

1.

![img](http://www.ruanyifeng.com/blogimg/asset/201304/bg2013042401.jpg)

计算机的核心是CPU，它承担了所有的计算任务。它就像一座工厂，时刻在运行。

2.

![img](http://www.ruanyifeng.com/blogimg/asset/201304/bg2013042402.png)

假定工厂的电力有限，一次只能供给一个车间使用。也就是说，一个车间开工的时候，其他车间都必须停工。背后的含义就是，单个CPU一次只能运行一个任务。

3.

![img](http://www.ruanyifeng.com/blogimg/asset/201304/bg2013042403.jpg)

进程就好比工厂的车间，它代表CPU所能处理的单个任务。任一时刻，CPU总是运行一个进程，其他进程处于非运行状态。

4.

![img](http://www.ruanyifeng.com/blogimg/asset/201304/bg2013042404.jpg)

一个车间里，可以有很多工人。他们协同完成一个任务。

5.

![img](http://www.ruanyifeng.com/blogimg/asset/201304/bg2013042405.jpg)

线程就好比车间里的工人。一个进程可以包括多个线程。

6.

![img](http://www.ruanyifeng.com/blogimg/asset/201304/bg2013042406.png)

车间的空间是工人们共享的，比如许多房间是每个工人都可以进出的。这象征一个进程的内存空间是共享的，每个线程都可以使用这些共享内存。

7.

![img](http://www.ruanyifeng.com/blogimg/asset/201304/bg2013042407.jpg)

可是，每间房间的大小不同，有些房间最多只能容纳一个人，比如厕所。里面有人的时候，其他人就不能进去了。这代表一个线程使用某些共享内存时，其他线程必须等它结束，才能使用这一块内存。

8.

![img](http://www.ruanyifeng.com/blogimg/asset/201304/bg2013042408.jpg)

一个防止他人进入的简单方法，就是门口加一把锁。先到的人锁上门，后到的人看到上锁，就在门口排队，等锁打开再进去。这就叫["互斥锁"](https://zh.wikipedia.org/wiki/互斥锁)（Mutual exclusion，缩写 Mutex），防止多个线程同时读写某一块内存区域。

9.

![img](http://www.ruanyifeng.com/blogimg/asset/201304/bg2013042409.jpg)

还有些房间，可以同时容纳n个人，比如厨房。也就是说，如果人数大于n，多出来的人只能在外面等着。这好比某些内存区域，只能供给固定数目的线程使用。

10.

![img](http://www.ruanyifeng.com/blogimg/asset/201304/bg2013042410.jpg)

这时的解决方法，就是在门口挂n把钥匙。进去的人就取一把钥匙，出来时再把钥匙挂回原处。后到的人发现钥匙架空了，就知道必须在门口排队等着了。这种做法叫做["信号量"](https://en.wikipedia.org/wiki/Semaphore_(programming))（Semaphore），用来保证多个线程不会互相冲突。

不难看出，mutex是semaphore的一种特殊情况（n=1时）。也就是说，完全可以用后者替代前者。但是，因为mutex较为简单，且效率高，所以在必须保证资源独占的情况下，还是采用这种设计。

11.

![img](http://www.ruanyifeng.com/blogimg/asset/201304/bg2013042411.png)

操作系统的设计，因此可以归结为三点：

（1）以多进程形式，允许多个任务同时运行；

（2）以多线程形式，允许单个任务分成不同的部分运行；

（3）提供协调机制，一方面防止进程之间和线程之间产生冲突，另一方面允许进程之间和线程之间共享资源。

