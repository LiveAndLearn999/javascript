# javascript
## books
#### javascript高级编程
##### 一，javascript简介
  1. JavaScript组成
  ---
      + 核心（ECMAScript）
      + 文档对象模型（DOM）
      + 浏览器对象模型（BOM）
  2.  ECMAScript 
  ---
    + 由ECMA-262定义的ECMAScript与web浏览器没有依赖关系。实际上这门语言本身不包含输入输出的定义。ECMA-262定义的只是这门语言的基础，而在此基础
      之上可以构建更完善的脚本语言。我们常见的web浏览器只是ECMAScript实现可能的宿主环境之一。宿主环境不仅提供基本的ECMAScript实现，同时也提供
      该语言的扩展，以便语言与环境之间对接交互。而这些扩展——如DOM，则利用ECMAScript的核心类型和语法提供更多更具体的功能，以便实现针对环境的
      操作。其他宿主环境包括node和Adobe Flash。ECMA-262包含内容
    + 语法
    + 类型
    + 语句
    + 关键字
    + 保留字
    + 操作符
    + 对象
    + ECMAScript就是对实现该标准规定的各个方面内容的语言描述。javascript实现了ECMAScript，Adobe ActionScript同样也实现了ECMAScript
  3. ECMAScript兼容
  ---
    + 支持ECMA-262描述的所有“类型，值，对象，属性，函数以及程序句法和语义”
    + 支持Unicode字符标准
    + 添加ECMA-262没有描述的“更多类型，值，对象，属性和函数”。ECMA-262所说的这些新增特性，主要是该标准中没有规定新的对象和对象的新属性。
    + 支持ECMA-262没有定义的“程序和正则表达式语法”（也就是说，可以修改和扩展内置的正则表达式语法）
  4. 文档对象模型（DOM）
  ---
    + 文档对象模型（DOM，document object model）是针对XML但经过扩展用于HTML的应用程序编程接口（API，application Programming InterFace）。DOM把整个页面映射为一个多层节点的结构。HTML或XML页面中的每个组成部分都是某种类型的节点，这些节点又包含着不同类型的数据。
    + 使用DOM的原因： Internet Explorer 4 ֖ Netscape Navigator 4 分别支持不同形式的 DHTML ，没有统一标准。此时，w3c开始着手规划DOM。
    + DOM级别  DOM1级--1998.10---DOM核心 和 DOM HTML；DOM核心：规定的是如何映射基于XML的文档结构，以便简化对文档中任意部分的访问和操作。DOM HTML模块则在DOM核心的基础上加以扩展，添加了针对HTML的对象和方法。
    + 注意： DOM并不是只是针对javascript的，很多语言也都实现了DOM。不过，在web浏览器中，基于ECMAScript实现的DOM的确已经成为了javascript这门语言的一个重要组成部分。
    + DOM2级：  在DOM1的基础上又扩展了（DHTML一直都支持的）鼠标和用户界面事件，范围，遍历，（迭代DOM文档的方法）等细节模块，而且同构对象接口增加了对css的支持。DOM1级中的DOM核心模块也经过扩展开始支持XML命名空间。DOM2级引入了下列新模块，也给出了众多新类型和新接口定义：
      * DOM视图（DOM views）：定义了跟踪不同文档（例如，应用css之前和之后的文档），视图的接口
      * DOM事件（DOM Events）：定义了基于css为元素应用样式的接口
      * DOM遍历和范围（DOM Traversal and Rangle）：定义了遍历和操作文档树的接口
    + DOM3 级则进一步扩展了DOM，引入了统一方法加载和保存文档的方法-在DOM加载和保存（DOM Load and Save）模块中定义；新增了验证文档方法-在DOM验证（DOM Validation） 模块中定义。DOM3级也对DOM核心进行了扩展。开始支持XML1.0规范，涉及XML Infoset，XPath和XML Base。
    + 注意了： 在阅读DOM标准的时候，读者可能会看到DOM0级（DOM Level 0）的字眼。实际上，DOM0级标准是是不存在的；所谓DOM0级只是DOM历史坐标中的一个参照点而已。具体说来，DOM0级指的是Internet Explorer 4.0和Netscape Navigator 4.0 最初支持的DHTML；
    + 其他DOM标准： 除了DOM核心和DOM HTML接口之外，另外几种语言还发布了只针对自己的DOM标准。下面列出的语言都是基于XML的，每种语言的DOM标准都添加了与特定语言相关的新方法和新接口。
      * SVG（Scalable Vector Graphic可伸缩矢量图）1.0；
      * MatnML（Mathematical Markup Language，数学标记语言）1.0；
      * SMIL（Synchronized Multimedia Integration Lanuage，同步多媒体集成语言）
      * 还有一些语言也开发了自己的DOM实现，例如Mozilla 的XUL（XML User Interface Lanuage ，XML用户界面语言）但是，只有上面列出的几种语言是W3C推荐的标准。
    + web浏览器对DOM的支持
      * 再DOM标准出现了一段时间之后，Web浏览器才开始实现它。
   5. 浏览器对象模型（BOM）
   ---
    + 从根本上讲，BOM只处理浏览器窗口和框架；但人们习惯上也把所有针对浏览器得javascript扩展算作BOM得一部分，
      * 弹出新浏览器窗口得功能
      * 移动，缩放和关闭浏览器窗口得功能
      * 提供浏览器详细信息得navigator
      * 提供浏览器所加载页面得详细信息得location对象
      * 提供用户显示器分辨率详细信息得screen对象
      * 对cookies得支持
      * 像XMLHttpRequest 和IE的ActiveXObject这样的自定义对象
      * 注意： 由于没有BOM标准可以遵循，因此每个浏览器都有自己的实现虽然也存在一些事实标准。例如：要有window对象和navigation对象等，但每个浏览器都会以这两个对象乃至其他对象定义属于自己的属性和方法。现在有了HTML5，BOM实现的细节有望朝着兼容性越来越高的方向发展。
    6. JavaScript版本
    ---
      
    7.  小结
    ---
      + JavaScript是一门专门与网页交互而设计的脚本语言，由三部分组成
        * ECMAScript 由ECMA-262 定义提供核心语言功能
        * 文档对象模型（DOM），提供访问和操作网页内容的方法和接口
        * 浏览器对象模型（BOM），提供与浏览器交互的方法和接口你
 
 
##### 二，在HTML中使用JavaScript
    1. 《script》元素
    ---
      + 向HTML页面中插入JavaScript的主要方法，就是使用《script》元素。这个元素由Netscape创造并在Netscape Navigator 2 中首先实现。后来，这个元素被加入到正式的HTML规范中。
        * async： 可选。表示应该立即下载脚本，但不应妨碍页面中的其他操作，比如下载其他资源或等待加载其他脚本。只对外部脚本文件有效
        * charset： 可选，表示通过src属性指定代码的字符集。由于大多浏览器会忽略它的值，因此这个属性很少有人用
        * defer 可选。表示脚本可以延迟到文档完全被解析和显示之后再执行。只对外部脚本文件有效。IE7及更早版本对嵌入脚本也支持这个属性
        * language 已废弃。原来你用于表示编写代码使用脚本语言（如JavaScript，JavaScript1.2或VBScript ）大多数浏览器会忽略这个属性。因此也没有必要再用了
        * src： 可选 表示包含要执行代码的外部文件。
        * type ： 可选。可以看成是language 的替代属性。表示编写代码使用脚本语言的内容类型（也称为MIME类型），
    
    
    

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
