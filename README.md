# javascript
## books
#### javascript高级编程
##### 一，javascript简介
  1. JavaScript组成
      + 核心（ECMAScript）
      + 文档对象模型（DOM）
      + 浏览器对象模型（BOM）
  2.  ECMAScript 
    > 由ECMA-262定义的ECMAScript与web浏览器没有依赖关系。实际上这门语言本身不包含输入输出的定义。ECMA-262定义的只是这门语言的基础，而在此基础
         之上可以构建更完善的脚本语言。我们常见的web浏览器只是ECMAScript实现可能的宿主环境之一。宿主环境不仅提供基本的ECMAScript实现，同时也提供
         该语言的扩展，以便语言与环境之间对接交互。而这些扩展——如DOM，则利用ECMAScript的核心类型和语法提供更多更具体的功能，以便实现针对环境的
         操作。其他宿主环境包括node和Adobe Flash。ECMA-262包含内容
    > 语法
    > 类型
    > 语句
    > 关键字
    > 保留字
    > 操作符
    > 对象
    > ECMAScript就是对实现该标准规定的各个方面内容的语言描述。javascript实现了ECMAScript，Adobe ActionScript同样也实现了ECMAScript
  3. ECMAScript兼容
    +    支持ECMA-262描述的所有“类型，值，对象，属性，函数以及程序句法和语义”
    +    支持Unicode字符标准
    +    添加ECMA-262没有描述的“更多类型，值，对象，属性和函数”。ECMA-262所说的这些新增特性，主要是该标准中没有规定新的对象和对象的新属性。
    +    支持ECMA-262没有定义的“程序和正则表达式语法”（也就是说，可以修改和扩展内置的正则表达式语法）
  4. 文档对象模型（DOM）
    +    文档对象模型（DOM，document object model）是针对XML但经过扩展用于HTML的应用程序编程接口（API，application Programming InterFace）。DOM把整个页面映射为一个多层节点的结构。HTML或XML页面中的每个组成部分都是某种类型的节点，这些节点又包含着不同类型的数据。
    
    

## 深入知识点
#### js数据类型隐式转换的原则-- https://blog.csdn.net/siboogi/article/details/53669567
  1. js数据类型转化主要分三种情况
    * 转换为boolean类型
    * 转换为number类型
    * 转换为string类型
  2. 转换为boolean类型
    * 数据在 逻辑判断 和 逻辑运算 之中会隐式转换为boolean类型
    * 规则： 数字0 》 false NaN 》 false 空字符 》 false null 》 false undefined 》 false 非0数字 》 true 非空字符串 》 true 非null对象类型 》 true
    * 注意：如果使用new操作符创建的对象隐式转换为boolean类型都是true，哪怕是new String（） 连续两个非操作符（！！）可以将一个数强制转换为boolean类型。
  3. 转换为string类型和转换为number类型
    * 我们将两个放在一起讨论是因为一个数到底转换成为string还是number受到运行环境和操作符的影响，而不是上面转换为boolean类型这么固定
    * 运行环境对数据类型隐式转换的影响
      * 很多内置函数期望传入的参数的数据类型是固定的，如：alert（value），它期望传入的value值是一个string类型，但是如果我们引入的是number类型或者object
      非string类型的数据的时候，就会发生数据类型的隐式转换。
    * 操作符也会影响数据的类型转换
      * 1当+号作为一元操作符操作单操作数的时候，他就会将这个数转换为数字类型
      * 当+号作为二元操作符时，如果两个操作数中存在一个字符类型的话，那么另外一个操作数也会无条件地转换为字符串
      * 当+号作为二元操作符时，如果两个操作数一个都不是字符串的话，两个操作数会隐式转换成数字类型(如果无法成功转换成数字，则变成NaN，再往下操作)，再进行加法算数操作
      * 当算数运算的操作符是+号以外的其他操作数时，两个操作数都会转成数字类型进行数字运算。
    * 所以我们应该这样来判断
      * 
