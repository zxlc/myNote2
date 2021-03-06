
# UML

## 类图（Class Diagrams）

- 类图是使用频率最高的 UML 图之一。类图是描述类之间的关系的静态视图，能够让我们在编写代码之前对系统有一个全面的认识。
- 类图表示类、接口和它们之间的协作关系，用于系统设计阶段。

### 类

类使用包含类名、属性和操作且带有分隔线的矩形来表示

1. 类名：类名（Name）是一个字符串
2. 属性：类的成员变量，表示格式：
  ```
  [可见性]属性名:类型[=默认值]
  ```
  > “可见性”表示该属性对类外的元素是否可见，包括公有（Public）、私有（Private）、受保护（Protected）和朋友（Friendly）4 种，在类图中分别用符号+、-、#、~表示

3. 操作：类的成员方法，表示格式：
  ```
  [可见性]名称(参数列表)[:返回类型]
  ```

类图中需注意以下几点：
- 字段和方法返回值的数据类型非必需
- 抽象类或抽象方法用斜体表示
- 如果是接口，则在类名上方加 <<Interface>>
- 静态类或静态方法加下划线

### 接口

接口使用一个带有名称的小圆圈来进行表示

![类图示例](http://c.biancheng.net/uploads/allimg/181112/3-1Q1121P6195T.gif)

### 类之间的关系

UML 将事物之间的联系归纳为 6 种，并用对应的图形类表示。将类与类之间的关系根据耦合度从弱到强排列：依赖关系、一般关联关系、聚合关系、组合关系、泛化关系和实现关系。

#### 依赖关系

依赖关系是一种使用关系，它是对象之间耦合度最弱的一种关联方式，是临时性的关联。在代码中，某个类的方法通过局部变量、方法的参数或者对静态方法的调用来访问另一个类（被依赖类）中的某些方法来完成一些职责。

**依赖关系使用带箭头的虚线来表示，箭头从使用类指向被依赖的类**。

如下是人与手机的关系图，人通过手机的语音传送方法打电话。
![依赖关系](http://c.biancheng.net/uploads/allimg/181112/3-1Q1121PA2Y5.gif)

#### 关联关系

关联关系是对象之间的一种引用关系，用于表示一类对象与另一类对象之间的联系

关联关系是类与类之间最常用的一种关系，分为一般关联关系、聚合关系和组合关系

1. 一般关联
   - 一般关联可以是双向的，也可以是单向的，在代码中通常将一个类的对象作为另一个类的成员变量来实现一般关联
   - **双向的关联可以用带两个箭头或者没有箭头的实线来表示，单向的关联用带一个箭头的实线来表示，箭头从使用类指向被关联的类**，也可以在关联线的两端标注角色名，代表两种不同的角色
   ![一般关联](http://c.biancheng.net/uploads/allimg/181112/3-1Q1121Q5115Q.gif)

2. 聚合关系（Aggregation）
   - 整体和部分之间的关系，是 has-a 的关系，其中成员对象是整体对象的一部分，但是成员对象可以脱离整体对象而独立存在
   - **聚合关系可以用带空心菱形的实线来表示，菱形指向整体**
   ![聚合关系](http://c.biancheng.net/uploads/allimg/181112/3-1Q1121Q541410.gif)

3. 组合关系
   - 也表示类之间的整体与部分的关系，但它表示构成关系，整体对象可以控制部分对象的生命周期，一旦整体对象不存在，部分对象也将不存在
   - **组合关系用带实心菱形的实线来表示，菱形指向整体**
   ![组合关系](http://c.biancheng.net/uploads/allimg/181112/3-1Q1121QFD27.gif)

#### 泛化关系

泛化关系是父类与子类之间的关系，是一种继承关系，是 is-a 的关系

**泛化关系用带空心三角箭头的实线来表示，箭头从子类指向父类**

![泛化关系](http://c.biancheng.net/uploads/allimg/181112/3-1Q1121Q62C57.gif)

#### 实现关系

实现关系是接口与实现类之间的关系

**实现关系使用带空心三角箭头的虚线来表示，箭头从实现类指向接口**

![实现关系](http://c.biancheng.net/uploads/allimg/181112/3-1Q1121QI4317.gif)
