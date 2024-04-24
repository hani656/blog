---
title: 面试助手
recommend: true
---

# 前端基础

# html

## 1.1 html标签的类型（head， body，!Doctype） 他们的作用是什么

**!DOCTYPE 标签**

* 它是指示 web 浏览器关于页面使用哪个 HTML 版本进行编写的指令

head：

* 是所有头部元素的容器, 绝大多数头部标签的内容不会显示给读者
* 该标签下所包含的部分可加入的标签有 base, link, meta, script, style和title

body：

* 用于定义文档的主体, 包含了文档的所有内容
* 该标签支持 html 的全局属性和事件属性

## 1.2 h5新特性

* 新增选择器 document.querySelector、document.querySelectorAll
* 拖拽释放(Drag and drop) API
* 媒体播放的 video 和 audio
* 本地存储 localStorage 和 sessionStorage
* 离线应用 manifest
* 桌面通知 Notififications
* 语意化标签 article、footer、header、nav、section
* 增强表单控件 calendar、date、time、email、url、search
* 地理位置 Geolocation
* 多任务 webworker
* 全双工通信协议 websocket
* 历史管理 history
* 跨域资源共享(CORS) Access-Control-Allow-Origin
* 页面可见性改变事件 visibilitychange
* 跨窗口通信 PostMessage
* Form Data 对象
* 绘画 canvas

## 1.3 伪类和伪元素

伪类：用于已有元素处于某种状态时为其添加对应的样式，这个状态是根据用户行为而动态变化的

&#x9; 例如：当用户悬停在指定元素时，可以通过\:hover来描述这个元素的状态，虽然它和一般css相似，可以为 已有元素添加样式，但是它只有处于DOM树无法描述的状态下才能为元素添加样式，所以称为伪类

伪元素：用于创建一些不在DOM树中的元素，并为其添加样式

&#x9; 例如，我们可以通过\:before来在一个元素之前添加一些文本，并为这些文本添加样式，虽然用户可以看见 这些文本，但是它实际上并不在DOM文档中

## 1.4 html语义化

| title          | 页面主体内容                                                 |
| :------------- | :----------------------------------------------------------- |
| hn             | h1\~h6，分级标题，\<h1> 与 \<title> 协调有利于搜索引擎优化   |
| ul li          | 无序列表                                                     |
| ol li          | 有序列表                                                     |
| header         | 页眉通常包括网站标志、主导航、全站链接以及搜索框             |
| nav            | 标记导航，仅对文档中重要的链接群使用                         |
| main           | 页面主要内容，一个页面只能使用一次。如果是web应用，则包围其主要功能 |
| article        | 定义外部的内容，其中的内容独立于文档的其余部分               |
| section        | 定义文档中的节（section、区段）。比如章节、页眉、页脚或文档中的其他部分 |
| aside          | 定义其所处内容之外的内容。如侧栏、文章的一组链接、广告、友情链接、相关产品列表等 |
| footer         | 页脚，只有当父级是body时，才是整个页面的页脚                 |
| small          | 呈现小号字体效果，指定细则，输入免责声明、注解、署名、版权   |
| strong         | 和 em 标签一样，用于强调文本，但它强调的程度更强一些         |
| em             | 将其中的文本表示为强调的内容，表现为斜体                     |
| mark           | 使用黄色突出显示部分文本                                     |
| figure         | 规定独立的流内容（图像、图表、照片、代码等等）（默认有40px左右margin） |
| figcaption     | 定义 figure 元素的标题，应该被置于 figure 元素的第一个或最后一个子元素的位置 |
| cite           | 表示所包含的文本对某个参考文献的引用，比如书籍或者杂志的标题 |
| progress       | 定义运行中的进度（进程）                                     |
| address        | 作者、相关人士或组织的联系信息（电子邮件地址、指向联系信息页的链接） |
| blockquoto     | 定义块引用，块引用拥有它们自己的空间                         |
| del、ins、code | 移除的内容、添加的内容、标记代码                             |

**语义化优点**

* 易于用户阅读，样式丢失的时候能让页面呈现清晰的结构
* 有利于SEO，搜索引擎根据标签来确定上下文和各个关键字的权重
* 方便屏幕阅读器解析，如盲人阅读器根据语义渲染网页
* 有利于开发和维护，语义化更具可读性，代码更好维护，与CSS3关系更和谐

## 1.5 引入样式时，link和@import的区别？

* 链接样式时，link只能在HTML页面中引入外部样式
* 导入样式表时，@import 既可以在HTML页面中导入外部样式，也可以在css样式文件中导入外部css样式

## 1.6 介绍一下你对浏览器内核的理解

主要分成两部分：渲染引擎(Layout Engine或Rendering Engine)和js引擎

* 渲染引擎：负责取得网页的内容（HTML、XML、图像等等）、整理讯息（例如加入CSS等），以及计算网页的显示方式，然后会输出至显示器或打印机。浏览器的内核的不同对于网页的语法解释会有不同，所以渲染的效果也不相同。
* js引擎：解析和执行JavaScript来实现网页的动态效果

## 1.7 常见的浏览器内核有哪些

* Trident( MSHTML )：IE MaxThon TT The World 360 搜狗浏览器
* Geckos：Netscape6及以上版本 FireFox Mozilla Suite/SeaMonkey
* Presto：Opera7及以上(Opera内核原为：Presto，现为：Blink)
* Webkit：Safari Chrome

## 1.8 label标签的作用是什么? 是怎么用的?

* label标签用来定义表单控件间的关系
* 当用户选择该标签时，浏览器会自动将焦点转到和标签相关的表单控件上
* label 中有两个属性是非常有用的, FOR和ACCESSKEY
* FOR属性功能：表示label标签要绑定的HTML元素，你点击这个标签的时候，所绑定的元素将获取焦点

## 1.9 title与h1的区别、b与strong的区别、i与em的区别?

* title属性没有明确意义，只表示标题；h1表示层次明确的标题，对页面信息的抓取也有很大的影响
* strong标明重点内容，语气加强含义；b是无意义的视觉表示
* em表示强调文本；i是斜体，是无意义的视觉表示
* 视觉样式标签：b i u s
* 语义样式标签：strong em ins del code

## 1.10 元素的alt和title有什么不同？

* 在alt和title同时设置的时候，alt作为图片的替代文字出现，title是图片的解释文字

## 1.11 浏览器页面有哪三层构成，分别是什么，作用是什么?

* 浏览器页面构成：结构层、表示层、行为层
* 分别是：HTML、CSS、JavaScript
* 作用：HTML实现页面结构，CSS完成页面的表现与风格，JavaScript实现一些客户端的功能与业务。

## 1.12 网页制作会用到的图片格式有哪些？

* Webp：WebP格式，谷歌（google）开发的一种旨在加快图片加载速度的图片格式。并能节省大量的服务器带宽资源和数据空间。Facebook Ebay等知名网站已经开始测试并使用WebP格式。
* Apng：是PNG的位图动画扩展，可以实现png格式的动态图片效果，有望代替GIF成为下一代动态图标准

## 1.13 viewport 所有属性？

* width :设置layout viewport的宽度，为一个正整数，或字符串'device-width'
* initial-scale:设置页面的初始缩放值，为一个数字，可以带小数
* minimum-scale:允许用户的最小缩放值，为一个数字，可以带小数
* maximum-scale:允许用户的最大缩放值，为一个数字，可以带小数
* height:设置layout viewport的高度，这个属性对我们并不重要，很少使用
* user-scalable:是否允许用户进行缩放，值为‘no’或者‘yes’

安卓中还支持：target-densitydpi，表示目标设备的密度等级，作用是决定css中的1px 代表多少物理像素

## 1.14 meta标签的name属性值？

name 属性主要用于描述网页，与之对应的属性值为content，content中的内容主要是便于搜索引擎机器人查找信息和分类信息用的

> A 、Keywords(关键字)说明：keywords用来告诉搜索引擎你网页的关键字是什么。

> B 、description(网站内容描述) 说明：description用来告诉搜索引擎你的网站主要内容。

> C 、robots(机器人向导)说明：robots用来告诉搜索机器人哪些页面需要索引，哪些页面不需要索引。

## 1.15 a标签中 如何禁用href 跳转页面 或 定位链接?

e.preventDefault();

href="javascript\:void(0);

## 1.16 video标签的几个属性方法

* src：视频的URL
* poster：视频封面，没有播放时显示的图片
* preload：预加载
* autoplay：自动播放
* loop：循环播放
* controls：浏览器自带的控制条
* width：视频宽度
* height：视频高度

## 1.17 块级元素、行内元素、行内块元素

**块级元素：**

特点：可设置宽高边距，占满整行，会自动换行

示例：div、 p、 h1 、h6、ol、ul、dl、table、address、blockquote、form

**行内元素：**

特点：无法设置宽高边距，不会占满整行，不会自动换行

示例：a、strong、b、em、i、del、s、ins、u、span

**行内块元素：**

特点：可设置宽高，占满整行，但不会自动换行

示例：img、input

## 1.18 web标准和w3c标准

web标准：分为结构、表现和行为

W3C标准：提出了更规范的要求

1、结构方面：标签字母要小写，标签要闭合，标签要正确嵌套

2、css和js方面：尽量使用外链写法，少用行内样式，属性名要见名知意

## 1.19 前端需要注意哪些SEO

1、合理的title、description、keywords：搜素时对这三项的权重逐个减少，title强调重点，重要关键词不要超过两次，而且要靠前，不同页面title要有所不同，description高度概括页面内容，长度合适，不过分堆砌关键词，不同页面description有所不同，keywords列出重要关键词即可

2、语义化的html代码，符合W3C标准

3、提高网站速度

4、重要HTML代码放前面

5、重要内容不要用js输出：爬虫不会执行js获取内容

6、少用 iframe：搜索引擎不会抓取 iframe 中的内容

7、非装饰性图片必须加 alt

## 1.20 canvas和svg的区别

| canvas                                                         | svg                                              |
| :------------------------------------------------------------- | :----------------------------------------------- |
| 通过js绘制2D图形，按像素进行渲染，当位置发生改变会重新进行绘制 | 使用XML绘制的2D图形，可以为元素添加js处理器      |
| 依赖分辨率                                                     | 不依赖分辨率                                     |
| 不支持事件处理器                                               | 支持事件处理器                                   |
| 弱的文本渲染能力                                               | 最适合带有哦大型渲染区域的应用程序（如谷歌地图） |
| 能以.png或.jpg格式保存结果图像                                 | 复杂度高会减慢渲染速度                           |
| 最适合图像密集型游戏，其中的许多对象会被频繁重绘               | 不适合游戏应用                                   |

# CSS

## 1.1 标准盒模型和IE盒模型两者的区别是什么？

**概念**

CSS盒模型本质上是一个盒子，封装周围的HTML元素，它包括： 外边距`（margin）` 、 边框

`（border）` 、 `内边距（padding）` 、`实际内容（content）` 四个属性

**设置盒子模型**

* box-sizing\:content-box;(标准盒模型)
* box-sizing\:border-box;(IE怪异盒模型)

**区别**

* 标准的(W3C)盒模型：元素的实际宽度等于设置的宽高 + border + padding (默认方式)
* IE盒模型（怪异盒模型）： 元素的实际宽度就等于设置的宽高，即使定义有 border 和 padding 也不会改变元素的实际宽度，即 ( Element width = width )

## 1.2 盒子塌陷是什么？

**盒子塌陷**

本应该在父盒子内部的元素跑到了外部。

**为什么会出现盒子塌陷？**

当父元素没设置足够大小的时候，而子元素设置了浮动的属性，子元素就会跳出父元素的边界（脱离文

档流），尤其是当父元素的高度为auto时，而父元素中又没有其它非浮动的可见元素时，父盒子的高度

就会直接塌陷为零， 我们称这是**CSS**高度塌陷

**解决塌陷的方法**

1. 设置宽高
2. 设置BFC
3. 清除浮动
4. 给父盒子添加border
5. 给父盒子设置padding-top

## 1.3 继承相关

css的继承：就是给父级设置一些属性，子级继承了父级的该属性，这就是我们的css中的继承

**常用无继承性的属性**

1. display：规定元素应该生成的框的类型

2. 文本属性：

    vertical-align：垂直文本对齐

    text-decoration：规定添加到文本的装饰

    text-shadow：文本阴影效果

    white-space：空白符的处理

    unicode-bidi：设置文本的方向

3. 盒子模型的属性：width、height、margin、padding、border

4. 背景属性：background

5. 定位属性：float、clear、position、top、right、bottom、left、min-width、min-height、max

   width、max-height、overflow、clip、z-index

**有继承性的属性**

1. font：字体系列属性

2. 文本系列属性：

   text-indent：文本缩进

    text-align：文本水平对齐

    line-height：行高

    word-spacing：增加或减少单词间的空白（即字间隔）

    letter-spacing：增加或减少字符间的空白（字符间距）

    text-transform：控制文本大小写

    direction：规定文本的书写方向

    color：文本颜色 a元素除外

3. 元素可见性：visibility

4. 表格布局属性：caption-side、border-collapse、border-spacing、empty-cells、table-layout

5. 列表布局属性：list-style-type、list-style-image、list-style-position、list-style

6. 生成内容属性：quotes

7. 光标属性：cursor

## 1.4 行内元素可以设置padding，margin吗？

* 行内元素的margin左右有效，上下无效
* 行内元素的padding左右有效 ，但是由于设置padding上下不占页面空间，无法显示效果，所以无效

## 1.5 什么是边距重叠？什么情况下会发生边距重叠？如何解决边距重叠？

边距重叠：两个box如果都设置了边距，那么在垂直方向上，两个box的边距会发生重叠，以绝对值大的那个为最终结果显示在页面上

**边距重叠分为两种：**

同级关系的重叠：

同级元素在垂直方向上外边距会出现重叠情况，最后外边距的大小取两者绝对值大的那个

父子关系的边距重叠：

嵌套崩塌

父子关系，如果子元素设置了外边距，在没有把父元素变成BFC的情况下，父元素也会产生外边距。

给父元素添加overflow：hidden 这样父元素就变为 BFC，不会随子元素产生外边距。

## 1.6 BFC是什么？

**文档有几种流**

1. 定位流
   * 绝对定位方案，盒从常规流中被移除，不影响常规流的布局；
   * 它的定位相对于它的包含块，相关CSS属性：top、bottom、left、right；
   * 如果元素的属性position为absolute或fixed，它是绝对定位元素；
   * 对于position: absolute，元素定位将相对于上级元素中最近的一个relative、fixed、absolute，如果没有则相对于body；
2. 浮动流
   * 左浮动元素尽量靠左、靠上，右浮动同理
   * 这导致常规流环绕在它的周边，除非设置 clear 属性
   * 浮动元素不会影响块级元素的布局
   * 但浮动元素会影响行内元素的布局，让其围绕在自己周围，撑大父级元素，从而间接影响块级元素布局
   * 最高点不会超过当前行的最高点、它前面的浮动元素的最高点
   * 不超过它的包含块，除非元素本身已经比包含块更宽
   * 行内元素出现在左浮动元素的右边和右浮动元素的左边，左浮动元素的左边和右浮动元素的
   * 右边是不会摆放浮动元素的
3. 普通流
   * 在常规流中，盒一个接着一个排列;
   * 在块级格式化上下文里面， 它们竖着排列；
   * 在行内格式化上下文里面， 它们横着排列;
   * 当position为static或relative，并且float为none时会触发常规流；
   * 对于静态定位(static positioning)，position: static，盒的位置是常规流布局里的位置；
   * 对于相对定位(relative positioning)，position: relative，盒偏移位置由top、bottom、
   * left、right属性定义。即使有偏移，仍然保留原有的位置，其它常规流不能占用这个位置。

**定义**

BFC的基本概念–BFC就是“块级格式化上下文”的意思，也有译作“块级格式化范围”。

通俗的讲，就是一个特殊的块，内部有自己的布局方式，不受外边元素的影响。

**布局规则**

1. 内部的 Box 会在垂直方向，一个接一个地放置
2. 垂直方向上的距离由margin决定。（完整的说法是：属于同一个BFC的两个相邻Box的margin会发生重叠（塌陷），与方向无关。）
3. 每个元素的左外边距与包含块的左边界相接触（从左向右），即使浮动元素也是如此。（这说明BFC中子元素不会超出他的包含块，而position为absolute的元素可以超出他的包含块边界）
4. BFC的区域不会与float的元素区域重叠
5. 计算BFC的高度时，浮动子元素也参与计算
6. BFC就是页面上的一个隔离的独立容器，容器里面的子元素不会影响到外面元素，反之亦然

**哪些元素会创建 BFC**

1. 根元素
1. float 属性不为 none
1. position 为 absolute 或 fixed
1. display 为 inline-block， table-cell， table-caption， flex， inline-flex
1. overflow 不为 visible

**场景**

1. **清除元素内部浮动**

   只要把父元素设为BFC就可以清理子元素的浮动了，最常见的用法就是在父元素上设置overflow: hidden样式，对于IE6加上zoom:1就可以了。

   计算BFC的高度时，自然也会检测浮动或者定位的盒子高度。
2. **解决外边距合并问题(嵌套崩塌)**

   外边距合并的问题。

   盒子垂直方向的距离由margin决定。属于同一个BFC的两个相邻盒子的margin会发生重叠

   属于同一个BFC的两个相邻盒子的margin会发生重叠，那么我们创建不属于同一个BFC，就不会发生margin重叠了。
3. **制作右侧自适应的盒子问题**

   普通流体元素BFC后，为了和浮动元素不产生任何交集，顺着浮动边缘形成自己的封闭上下文

## 1.7 块元素居中

* 我们可以利用margin:0 auto来实现元素的水平居中。
* 利用绝对定位，设置四个方向的值都为0，并将margin设置为auto，由于宽高固定，因此对应方向实现平分，可以实现水

平和垂直方向上的居中。

* 利用绝对定位，先将元素的左上角通过top:50%和left:50%定位到页面的中心，然后再通过margin负值来调整元素

的中心点到页面的中心。

* 利用绝对定位，先将元素的左上角通过top:50%和left:50%定位到页面的中心，然后再通过translate来调整元素

的中心点到页面的中心。

* 使用flex布局，通过align-items\:center和justify-content\:center设置容器的垂直和水平方向上为居中对

齐，然后它的子元素也可以实现垂直和水平的居中。

对于宽高不定的元素，后面两种方法，可以实现元素的垂直和水平的居中。

## 1.8 CSS 优化、提高性能的方法有哪些？

**加载性能：**

* css压缩：将写好的css进行打包压缩，可以减小文件体积
* css单一样式：当需要下边距和左边距的时候，很多时候会选择使用margin-left:20px;margin-bottom:30px
* 减少使用@import，建议使用link，因为后者在页面加载时一起加载，前者是等待页面加载完成之后再进行加载

**选择器性能：**

* 关键选择器（key selector）。选择器的最后面的部分为关键选择器（即用来匹配目标元素的部分）。CSS选择符是从右到左进行匹配的。
* 当使用后代选择器的时候，浏览器会遍历所有子元素来确定是否是指定的元素等等
* 如果规则拥有ID选择器作为其关键选择器，则不要为规则增加标签。
* 过滤掉无关的规则（这样样式系统就不会浪费时间去匹配它们了）。
* 尽量少的去对标签进行选择，而是用class。
* 尽量少的去使用后代选择器，降低选择器的权重值。后
* 代选择器的开销是最高的，尽量将选择器的深度降到最低，最高不要超过三层，更多的使用类来关联每一个标签元素。
* 了解哪些属性是可以通过继承而来的，然后避免对这些属性重复指定规则。

**渲染性能：**

* 属性值为0时，不加单位。
* 可以省略小数点之前的0。
* 标准化各种浏览器前缀：带浏览器前缀的在前。标准属性在后。
* 选择器优化嵌套，尽量避免层级过深。
* css雪碧图，同一页面相近部分的小图标，方便使用，减少页面的请求次数，但是同时图片本身会变大，使用时，优劣考虑清楚，再使用。
* 不滥用web字体。对于中文网站来说WebFonts可能很陌生，国外却很流行。web fonts通常体积庞大，而且一些浏览器在下载web fonts时会阻塞页面渲染损伤性能。

**可维护性、健壮性：**

* 将具有相同属性的样式抽离出来，整合并通过class在页面中进行使用，提高css的可维护性。
* 样式与内容分离：将css代码定义到外部css中

## 1.9 行内元素和块级元素什么区别，然后怎么相互转换

**块级元素**

1. 总是从新的一行开始，即各个块级元素独占一行，默认垂直向下排列

2. 高度、宽度、margin及padding都是可控的，设置有效，有边距效果

3. 宽度没有设置时，默认为100%

4. 块级元素中可以包含块级元素和行内元素

**行内元素**

1. 和其他元素都在一行，即行内元素和其他行内元素都会在一条水平线上排列

2. 高度、宽度是不可控的，设置无效，由内容决定

3. 根据标签语义化的理念，行内元素最好只包含行内元素，不包含块级元素

**转换**

1. display:inline;转换为行内元素
2. display:block;转换为块状元素
3. display:inline-block;转换为行内块状元素

## 1.10 min-width/max-width **和** **min-height/max-height** 属性间的覆盖规则？

1. max-width 会覆盖 width，即使 width 是行内样式或者设置了 !important。
2. min-width 会覆盖 max-width，此规则发生在 min-width 和 max-width 冲突的时候；

## 1.11 浏览器是怎样解析CSS选择器的？

CSS选择器的解析是从右向左解析的

**原因：**

从右向左的匹配在第一步就筛选掉了大量的不符合条件的最右节点(叶子节点)，而从左向右的匹配规则的性能都浪

费在了失败的查找上面

## 1.12 width\:auto 和 width:100%的区别

* width:100%会使元素box的宽度等于父元素的contentbox的宽度
* width\:auto会使元素撑满整个父元素，margin、border、padding、content区域会自动分配水平空间。

## 1.13 display、position和float的相互关系？

* 首先我们判断display属性是否为none，如果为none，则position和float属性的值不影响元素最后的表现
* 然后判断position的值是否为absolute或者fixed，如果是，则float属性失效，并且display的值应该被 设置为table或者block，具体转换需要看初始转换值
* 如果position的值不为absolute或者fixed，则判断float属性的值是否为none，如果不是，则display 的值则按上面的规则转换。注意，如果position的值为relative并且float属性的值存在，则relative相对 于浮动后的最终位置定位
* 如果float的值为none，则判断元素是否为根元素，如果是根元素则display属性按照上面的规则转换，如果不是， 则保持指定的display属性值不变

总的来说，可以把它看作是一个类似优先级的机制，"position\:absolute"和"position\:fixed"优先级最高，有它存在 的时候，浮动不起作用，'display'的值也需要调整；其次，元素的'float'特性的值不是"none"的时候或者它是根元素 的时候，调整'display'的值；最后，非根元素，并且非浮动元素，并且非绝对定位的元素，'display'特性值同设置值。

## 1.14 IFC 是什么？

IFC指的是行级格式化上下文，它有这样的一些布局规则：

* 行级上下文内部的盒子会在水平方向，一个接一个地放置。
* 当一行不够的时候会自动切换到下一行。&#x20;
* 行级上下文的高度由内部最高的内联盒子的高度决定

## 1.15 为什么不建议使用统配符初始化 css 样式

* 采用\*{pading:0;margin:0;}这样的写法好处是写起来很简单，但是是通配符，需要把所有的标签都遍历一遍，当网站较大时， 样式比较多，这样写就大大的加强了网站运行的负载，会使网站加载的时候需要很长一段时间，因此一般大型的网站都有分层次的一 套初始化样式
* 出于性能的考虑，并不是所有标签都会有padding和margin，因此对常见的具有默认padding和margin的元素初始化即 可，并不需使用通配符\*来初始化

## 1.16 CSS3 新特新

1. 新增各种 CSS 选择器 `:not(p)` 选择每个非p的元素； `p:empty` 选择每个没有任何子级的p元素（包括文本节点）
2. 边框（Borders）
3. 背景 background-clip（规定背景图的绘制区域），background-origin，background-size
4. 线性渐变 （Linear Gradients） 向下/向上/向左/向右/对角方向
5. 文本效果 阴影text-shadow，textwrap，word-break，word-wrap
6. 2D 转换 transform\:scale(0.85,0.90) | translate(0px,-30px) | skew(-9deg,0deg) |rotate()  **3D转换** perspective()；transform是向元素应用 2D 或者 3D 转换
7. 过渡 transition
8. 动画
9. 多列布局 （multi-column layout）
10. 盒模型
11. flex 布局
12. 多媒体查询 \*\*定义两套css，当浏览器的尺寸变化时会采用不同的属性

##  1.17 position 跟 display、float 这些特性相互叠加后会怎么样？

* display 属性规定元素应该生成的框的类型；position属性规定元素的定位类型；float属性是一种布局方式，定义元素在哪个方向浮动。
* 类似于优先级机制：position：absolute/fixed优先级最高，有他们在时，float不起作用，display值需要调整。float 或者absolute定位的元素，只能是块元素或表格。

## 1.18 什么是CSS 预处理器？为什么使用？

* Less、Sass、Stylus，用来预编译Sass或less，增强了css代码的复用性，还有层级、mixin、变量、循环、函数等，具有很方便的UI组件模块化开发能力，极大的提高工作效率

**为什么要使用？**

* 可嵌套性
* 变量
* Mixins(混合@mixin)：可重用性高，可以注入任何东西
* @extend：允许一个选择器继承另一个选择器
* @function:函数功能，用户使用@function 可以去编写自己的函数
* 引用父元素&：在编译时，&将被替换成父选择符
* 计算功能
* 组合连接： #{} :变量连接字符串
* 循环语句：（很少用到）
* if 语句：（很少用到）

## 1.19 浏览器是怎样解析的？

1. HTML 被 HTML 解析器解析成 DOM 树；2. CSS 被 CSS 解析器解析成 CSSOM 树；
2. 结合 DOM 树和 CSSOM 树，生成一棵渲染树(Render Tree)，这一过程称为 Attachment；
3. 生成布局(flow)，浏览器在屏幕上“画”出渲染树中的所有节点；
4. 将布局绘制(paint)在屏幕上，显示出整个页面。

## 1.20 在网页中的应该使用奇数还是偶数的字体？为什么呢？

* 使用偶数字体
* Windows 自带的点阵宋体（中易宋体）从 Vista 开始只提供 12、14、16 px 这三个大小的点阵，而 13、15、17 px时用的是小一号的点。（即每个字占的空间大了 1 px，但点阵没变），于是略显稀疏

## 1.21 元素竖向的百分比设定是相对于容器的高度吗？

当按百分比设定一个元素的宽度时，它是相对于父容器的宽度计算的，但是，对于一些表示竖向距离的属性，例如 padding-top , padding-bottom , margin-top , margin-bottom 等，当按百分比设定它们时，依据的也是父容器的宽度，而不是高度

## 1.22 怎么让谷歌支持小于12px的文字？

使用 scale

## 1.23 li 与 li 之间有看不见的空白间隔是什么原因引起的？有什么解决办法？

行框的排列会受到中间空白（回车空格）等的影响，因为空格也属于字符,这些空白也会被应用样式，占据空间，所以会有间隔，把字符大小设为0，就没有空格了

**解决方法：**

1. 可以将代码全部写在一排
2. 浮动li中float：left
3. 在ul中用font-size：0（谷歌不支持）；
4. 可以将 ul{letter-spacing: -4px;};li{letter-spacing: normal;}

## 1.24 display\:inline-block 什么时候会显示间隙？

1. 有空格时候会有间隙 解决：s除空格
2. margin正值的时候 解决：margin使用负值
3. 使用font-size时候 解决：font-size:0、letter-spacing、word-spacing

## 1.25 png、jpg、gif 这些图片格式解释一下，分别什么时候用。有没有了解过webp？

* png是便携式网络图片（Portable Network Graphics）是一种无损数据压缩位图文件格式.优点是：压缩比高，色彩好。 大多数地方都可以用。
* jpg是一种针对相片使用的一种失真压缩方法，是一种破坏性的压缩，在色调及颜色平滑变化做的不错。在www上，被用来储存和传输照片的格式。
* gif是一种位图文件格式，以8位色重现真色彩的图像。可以实现动画效果.
* webp格式是谷歌在2010年推出的图片格式，压缩率只有jpg的2/3，大小比png小了45%。缺点是压缩的时间更久了，兼容性不好，目前谷歌和opera支持。

## 1.26 style 标签写在 body 后与 body前有什么区别？

页面加载自上而下 当然是先加载样式。
写在 body 标签后由于浏览器以逐行方式对HTML文档进行解析，当解析到写在尾部的样式表（外联或写在 style 标签）会导致浏览器停止之前的渲染，等待加载且解析样式表完成之后重新渲染，在windows的IE下可能会出现 FOUC 现象（即样式失效导致的页面闪烁问题）

## 1.27 ::before 和::after 中双冒号和单冒号有什么区别、作用？

**区别**

在css中伪类一直用:表示，如 `:hover`，`:active`等

伪元素在CSS1中已存在，当时语法使用 : 表示 ，如：`:before`和`:after`

后来在CSS3中修订，伪元素用 ::表示，如 `::before` 和 `::after`，以此区分伪元素和伪类

由于低版本 IE 对双冒号不兼容，开发者为了兼容性各浏览器，继续使使用 :after 这种老语法表示伪元素

单冒号`:` CSS3表示伪类；双冒号`::`CSS3伪元素

**作用：**

::before 和::after 的主要作用是在元素内容前后加上指定内容

伪类与伪元素都是用于向选择器加特殊效果

伪类与伪元素的本质区别就是是否抽象创造了新元素

伪类只要不是互斥可以叠加使用

伪元素在一个选择器中只能出现一次，并且只能出现在末尾

伪类与伪元素优先级分别与类、标签优先级相同

## 1.28 CSS3新增伪类，以及伪元素？

**CSS3 新增伪类**

p:first-of-type 选择属于其父元素的首个<p>元素的每个<p>元素

p:last-of-type 选择属于其父元素的最后<p>元素的每个<p>元素

p:nth-child(n) 选择属于其父元素的第 n 个子元素的每个<p>元素

p:nth-last-child(n) 选择属于其父元素的倒数第 n 个子元素的每个<p>元素

p:nth-of-type(n) 选择属于其父元素第 n 个<p>元素的每个<p>元素

p:nth-last-of-type(n)

选择属于其父元素倒数第 n 个<p>元素的每个<p>元素

p:last-child 选择属于其父元素最后一个子元素的每个<p>元素

p:target

选择当前活动的<p>元素

:not(p) 选择非<p>元素的每个元素

:enabled 控制表单控件的可用状态

:disabled

控制表单控件的禁用状态

:checked

单选框或复选框被选中

**伪元素**

::first-letter 将样式添加到文本的首字母

::first-line 将样式添加到文本的首行

::before 在某元素之前插入某些内容

::after 在某元素之后插入某些内容

## 1.29 未知高度元素垂直居中、垂直居中的实现方式有哪些？

1. 绝对定位+css3 transform:translate(-50%，-50%)

```css
.wrap{
 position:relative;
}
.child{
 position: absolute;
 top:50%;
 left:50%;
 -webkit-transform:translate(-50%,-50%);
}
```

2. **css3** 的flex布局

```css
.wrap{
 display:flex;
 justify-content:center;
}
.child{
 align-self:center;
}
```

3. table布局

```html
<div class="wrap">
<div class="child">
<div>sadgsdgasgd</div>
</div>
</div>
<style>
.wrap{
 display:table;
 text-align:center;
}
.child{
 background:#ccc;
 display:table-cell;
 vertical-align:middle;
}
.child div{
 width:300px;
 height:150px;
 background:red;
 margin:0 auto;
}
</style>
```

## 1.30 图片垂直居中

**1.** 使用flex实现图片垂直居中

```html
<div class="flexbox">
 <img src="1.jpg" alt="">
</div>
<style>
.flexbox{
    width: 300px;
    height: 250px;
    background:#fff;
    display: flex;
    align-items:center
  }
.flexbox img{
    width: 100px;
    height: 100px;
    align-items: center;
 }
</style>
```

2. 利用Display: table;实现img图片垂直居中

```html
<div class="tablebox">
<div id="imgbox">
<img src="1.jpg" alt="">
</div></div>
<style>
.tablebox{width: 300px;height: 250px;background: #fff;display: table}
#imgbox{display: table-cell;vertical-align: middle;}
#imgbox img{width: 100px}
</style>
```

3. 用绝对定位实现垂直居中

```html
<div class="posdiv">
<img src="1.jpg" alt=""></div>
<style>
.posdiv{
    width: 300px;height: 250px;
    background: #fff;
    position: relative;
margin:0 auto}
.posdiv img{width: 100px;position: absolute;top: 50%;margin-top: -50px;}
</style>
```

## 1.31 文本元素居中

1. 水平居中：text-align
2. 垂直居中：line-height 和height设置一样
3. 多行文本垂直居中
   * 父级元素高度不固定（padding-top和padding-bottom）
   * 父级元素高度固定 （vertical-align:middle +display:table-cell ）

## 1.32 CSS实现一个等腰三角形

主要是通过把宽高设置成0，边框宽度设置宽一些，设置其中三个边透明，只留一个边显示

```html
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8" />
<title>测试</title>
<style type="text/css">
    div {
        width:0px;height:0px;margin:100px auto;
        border-left:80px solid transparent;
        border-right:80px solid transparent;
        border-bottom:138.56px solid #A962CE; /*--三角形的高--*/
    }
</style>
</head>
<body>
<div>
</div>
</body>
</html>
```

## 1.33 **画** **0.5px** 的直线

1. 使用scale缩放

   ```html
   <style>
   .hr.scale-half {
    height: 1px;
    transform: scaleY(0.5);
   }
   </style>
   <p>1px + scaleY(0.5)</p>
   <div class="hr scale-half"></div>
   <!--
   Chrome/Safari都变虚了，只有Firefox比较完美看起来是实的而且还很细，效果和直接设置0.5px一
   样。所以通过transform: scale会导致Chrome变虚了，而粗细几乎没有变化。但是如果加上transformorigin: 50% 100%：
   -->
   .hr.scale-half {
    height: 1px;
    transform: scaleY(0.5);
    transform-origin: 50% 100%;
   }
   ```

2. 线性渐变linear-gradient

   ```html
   <style>
   .hr.gradient {
   height: 1px;
   background: linear-gradient(0deg, #fff, #000);
   }
   </style>
   <p>linear-gradient(0deg, #fff, #000)</p>
   <div class="hr gradient"></div>
   ```

3. boxshadow

   ```html
   <style>
   .hr.boxshadow {
    height: 1px;
    background: none;
    box-shadow: 0 0.5px 0 #000;
   }
   </style>
   <p>box-shadow: 0 0.5px 0 #000</p>
   <div class="hr boxshadow"></div>
   ```

4. viewport

   ```html
   <meta name="viewport" content="width=device-width,initial-sacle=0.5">
   <!--
   width=device-width表示将viewport视窗的宽度调整为设备的宽度，这个宽度通常是指物理上宽度
   initial-sacle=0.5 缩放0.5
   -->
   ```

## 1.34 移动端适配方案

1. **viewport** **适配**

```html
<meta name="viewport" content="width=750,initial-scale=0.5">
<!--
initial-scale = 屏幕的宽度 / 设计稿的宽度
为了适配其他屏幕，需要动态的设置 initial-scale 的值
-->
<head>
<script>
const WIDTH = 750
const mobileAdapter = () => {
let scale = screen.width / WIDTH
let content = `width=${WIDTH}, initial-scale=${scale}, maximumscale=${scale}, minimum-scale=${scale}`
let meta = document.querySelector('meta[name=viewport]')
if (!meta) {
meta = document.createElement('meta')
meta.setAttribute('name', 'viewport')
document.head.appendChild(meta)
}
meta.setAttribute('content',content)
}
mobileAdapter()
window.onorientationchange = mobileAdapter //屏幕翻转时再次执行
</script>
</head>
```

**缺点**：边线问题，不同尺寸下，边线的粗细是不一样的（等比缩放后），全部元素都是等比缩放，实际显示效果可能不太好

2. **vw** **适配（部分等比缩放）**

   * 开发者拿到设计稿（假设设计稿尺寸为750px，设计稿的元素标注是基于此宽度标注）
   * 开始开发，对设计稿的标注进行转换，把px换成vw。比如页面元素字体标注的大小是32px，换成vw为 (100/750)*32 vw
   * 对于需要等比缩放的元素，CSS使用转换后的单位
   * 对于不需要缩放的元素，比如边框阴影，使用固定单位px

   ```html
   <head>
   <meta name="viewport" content="width=device-width, initial-scale=1, maximumscale=1, minimum-scale=1">
   <script>
    const WIDTH = 750
    //:root { --width: 0.133333 } 1像素等于多少 vw
    document.documentElement.style.setProperty('--width', (100 / WIDTH))
   </script>
   </head>
   ```

3. **rem适配**
4. **弹性盒适配（合理布局）**

## 1.35 link 和 @import 的区别

1. 引入的内容不同

link 除了引用样式文件，还可以引用图片等资源文件，而 @import 只引用样式文件

2. 加载顺序不同

link 引用 CSS 时，在页面载入时同时加载；@import 需要页面网页完全载入以后加载

3. 兼容性不同

link 是 XHTML 标签，无兼容问题；@import 是在 CSS2.1 提出的，低版本的浏览器不支持

4. 对 JS 的支持不同

link 支持使用 Javascript 控制 DOM 去改变样式；而 @import 不支持

## 1.36 iframe有什么优点、缺点?

**优点：**

1. iframe能够原封不动的把嵌入的网页展现出来。
2. 如果有多个网页引用iframe，那么你只需要修改iframe的内容，就可以实现调用的每一个页面内
   容的更改，方便快捷。
3. 网页如果为了统一风格，头部和版本都是一样的，就可以写成一个页面，用iframe来嵌套，可以
   增加代码的可重用。
4. 如果遇到加载缓慢的第三方内容如图标和广告，这些问题可以由iframe来解决。

**缺点：**

1. iframe会阻塞主页面的onload事件；
2. iframe和主页面共享连接池，而浏览器对相同域的连接有限制，所以会影响页面的并行加载。会
   产生很多页面，不容易管理。
3. iframe框架结构有时会让人感到迷惑，如果框架个数多的话，可能会出现上下、左右滚动条，会
   分散访问者的注意力，用户体验度差。
4. 代码复杂，无法被一些搜索引擎索引到，这一点很关键，现在的搜索引擎爬虫还不能很好的处理
   iframe中的内容，所以使用iframe会不利于搜索引擎优化（SEO）。
5. 很多的移动设备无法完全显示框架，设备兼容性差。
6. iframe框架页面会增加服务器的http请求，对于大型网站是不可取的。

# JavaScript

## 1.1 let var const的区别？

**var ES5变量声明方式**

1. 在变量未赋值时，变量为undefined（未使用声明变量时也为undefined）
2. 作用域 var的作用域为方法作用域；只要在方法内定义了，整个方法内的定义变量后的代码都可以使用

**let ES6变量声明方式**

1. 在变量为声明前直接使用会报错
2. 作用域   let为块级作用域   通常let比var范围要小
3. let进制重复声明变量，否则会报错；var可以重复声明

**const ES6变量声明**

1. const为常量声明方式；声明变量时必须初始化，在后面出现的代码中不能再修改常量的值
2. const实际上保证的，并不是变量的值不得改动，而时变量指向的哪个内存地址不得改动

## 1.2 js数据类型，区别

**基本数据类型：**

number，string，boolean，null，undefined，symbol，bigint

**引用数据类型：**

object（对象），function（函数）

object：普通对象，数组对象，正则对象，日期对象，math数学函数对象。

**两种数据存储方式：**

基本数据类型是直接存储在栈中的简单数据段，占据空间小、大小固定，属于被频繁使用的数据。栈是存储基本数据类型值和执行代码的空间。

引用数据类型是存储在堆内存中，占据空间大、大小不固定。引用数据类型在栈中存储了指针，该指针指向队中该实体的起始地址，当解释器寻找引用值时，会检索其在栈中的地址，取得地址后从堆中获得实体。

**两种数据类型的区别：**

1. 堆比栈空间大，栈比堆运行速度快
2. 堆内存是无序存储，可以根据引用直接获取
3. 基础数据类型比较稳定，而且相对来说占用的内存小
4. 引用数据类型大小是动态的，而且是无限的

## 1.3 **Javascript 创建对象的几种方式？**

1. 简单对象的创建 使用对象字面量的方式{}

```javascript
const Cat = {};
```

2. new 一个function

```javascript
function Person(){
}
const personOne=new Person();
```

3. 使用工厂方式来创建（Object 关键字）

```javascript
const wcDog =new Object();
```

4. 使用 Object.create() 创建对象（使用现有对象作为原型）

```javascript
const person = Object.create(anotherPerson);
```

5. 使用 ES6 中的类（Class）创建对象（其实质还是使用构造函数）：

```javascript
class Person {
  constructor(name) {
    this.name = name;
  }
}
const person = new Person('John');
```

## 1.4 ==、===和object.is 区别

1. == 值比较值
2. ===值和类型都比较
3. object.is 和 === 区别  +-0 false   NaN true（object.is 只比较值是否相等，而不考虑类型）

```javascript
console.log(+0 === -0);       //true
console.log(NaN === NaN);     //false
Object.is(+0,-0)              //false
Object.is(NaN,NaN)            //true
```

## 1.5 如何区分数组和对象？

1. 通过 ES6 中的 Array.isArray

```javascript
Array.isArray([]) //true
Array.isArray({}) //false
```

2. 通过 instanceof 来识别

```javascript
[] instanceof Array //true
{} instanceof Array //false
```

3. 通过调用 constructor 来识别

```javascript
{}.constructor //返回 object
[].constructor //返回 Array
```

4. 通过 Object.prototype.toString.call 方法来识别

```javascript
Object.prototype.toString.call([]) //["object Array"]
Object.prototype.toString.call({}) //["object Object"]
```

## 1.6 作用域和作用域链

作用域就是一个独立的地盘，让变量不会外泄、暴露出去。也就是说作用域最大的用处就是隔离
变量，不同作用域下同名变量不会有冲突

1. ES6 之前 JavaScript 没有块级作用域,只有全局作用域和函数作用域。
2. ES6 的到来，为我们提供了‘块级作用域’,可通过新增命令 let 和 const 来体现

**什么是作用域链？**

* 当代码在一个环境中执行时，会创建变量对象的一个作用域链

* 由子级作用域返回父级作用域中寻找变量，就叫做作用域链

* 作用域链中的下一个变量对象来自包含环境，也叫外部环境。而再下一个变量对象则来自中的最后一个对象

* 作用域链前端始终都是当前执行的代码所在环境的变量对象，如果环境是函数，则将其活动对象作为变量对象

**如何延长作用域链？**

执行环境的类型只有两种，全局和局部（函数）。但是有些语句可以在作用域链的前端临时增加一个变量对象，该变量对象会在代码执行后被移除具体来说就是执行这两个语句时，作用域链都会得到加强

1. try - catch 语句的 catch 块；会创建一个新的变量对象，包含的是被抛出的错误对象的声明

2. with 语句。with 语句会将指定的对象添加到作用域链中

## 1.7 constructor的理解

创建的每个函数都有一个prototype（原型）对象，这个属性是一个指针，指向一个对象。在默认情况下，所有原型对象都会自动获得一个constructor属性，之后属性是一个指向prototype属性坐在函数的指针。当调用构造函数创建一个新实例后，该实例的内部将包含一个指针，指向构造函数的原型对象。注意当将构造函数的prototype设置为等于一个以对象字面量形式创建的新对象时，constructor属性不再指向该构造函数

## 1.8 webworker和websocket

web socket：在一个单独的持久连接上提供全双工、双向的通信。使用自定义的协议（ws\://、wss\://），同源策略对web socket不适用。
web worker：运行在后台的JavaScript，不影响页面的性能。
创建worker：var worker = new Worker(url);
向worker发送数据：worker.postMessage(data);
接收worker返回的数据：worker.onmessage
终止一个worker的执行：worker.terminate();

## 1.9 XML与JSON的区别？

1. 数据体积方面。JSON相对于XML来讲，数据的体积小，传递的速度更快些。
2. 数据交互方面。JSON与JavaScript的交互更加方便，更容易解析处理，更好的数据交互。
3. 数据描述方面。JSON对数据的描述性比XML较差。
4. 传输速度方面。JSON的速度要远远快于XML。

## 1.10 map 和 forEach 的区别？

**相同点：**

1. 都是循环遍历数组中的每一项
2. 每次执行匿名函数都支持三个参数，参数分别为item（当前每一项），index（索引值），
   arr（原数组）
3. 匿名函数中的this都是指向window
4. 只能遍历数组

**不同点：**

1. map()会分配内存空间存储新数组并返回，forEach()不会返回数据。
2. forEach()允许callback更改原始数组的元素。map()返回新的数组。

## 1.11 for of 可以遍历哪些对象？

for..of..: 它是es6新增的一个遍历方法，但只限于迭代器(iterator), 所以普通的对象用for..of遍历
是会报错的。
可迭代的对象：包括Array, Map, Set, String, TypedArray, arguments对象等等

## 1.13 new操作符具体干了什么呢?

1. 创建空对象；
   var obj = {};
2. 设置新对象的constructor属性为构造函数的名称，设置新对象的proto属性指向构造函数的
   prototype对象；
   obj.proto = ClassA.prototype;
   扩展了新对象的原型链。
3. 使用新对象调用函数，函数中的this被指向新实例对象：
   ClassA.call(obj); //{}.构造函数();
4. 返回this指针。当存在显示的返回时，返回return后面的内容。新建的空对象作废。

## 1.14 作用域

作用域就是一个独立的地盘，让变量不会外泄、暴露出去。也就是说作用域最大的用处就是隔离
变量，不同作用域下同名变量不会有冲突

1. ES6 之前 JavaScript 没有块级作用域,只有全局作用域和函数作用域。
2. ES6 的到来，为我们提供了‘块级作用域’,可通过新增命令 let 和 const 来体现

## 1.15 javascript中arguments相关的问题

**arguments**
在js中，我们在调用有参数的函数时，当往这个调用的有参函数传参时，js会把所传的参数全部存到一
个叫arguments的对象里面。它是一个类数组数据
**作用**
有了arguments这个对象之后，我们可以不用给函数预先设定形参了，可以动态地通过arguments为函
数加入参数

## 1.16 instanceOf作用 即原理

instanceof主要作用就是判断一个实例是否属于某种类型

```javascript
function new_instance_of(leftVaule, rightVaule) {
    let rightProto = rightVaule.prototype; // 取右表达式的 prototype 值
    leftVaule = leftVaule.__proto__; // 取左表达式的__proto__值
    while (true) {
        if (leftVaule === null) {
            return false;
        }
        if (leftVaule === rightProto) {
            return true;
        }
        leftVaule = leftVaule.__proto__
    }
}
```

其实 instanceof 主要的实现原理就是只要右边变量的 prototype 在左边变量的原型链上即可。因此，instanceof 在查找的过程中会遍历左边变量的原型链，直到找到右边变量的 prototype，如果查找失败，则会返回 false，告诉我们左边变量并非是右边变量的实例。

## 1.17 数组和伪数组的区别?

1. 定义

* 数组是一个特殊对象,与常规对象的区别：
  * 当由新元素添加到列表中时，自动更新length属性
  * 设置length属性，可以截断数组
  * 从Array.prototype中继承了方法
  * 属性为'Array'
* 伪数组是一个拥有length属性，并且他属性为非负整数的普通对象，伪数组不能直接调用数组方法。

2. 区别
   本质：伪数组数组是简单对象，它的原型关系与数组不同

```javascript
    let arrayLike = {
        length: 10,
    };
    console.log(arrayLike instanceof Array); // false
    console.log(arrayLike.__proto__.constructor === Array); // false
    console.log(arrayLike.toString()); // [object Object]
    console.log(arrayLike.valueOf()); // {length: 10}
    let array = [];
    console.log(array instanceof Array); // true
    console.log(array.__proto__.constructor === Array); // true
    console.log(array.toString()); // ''
    console.log(array.valueOf()); // []
```

3. 伪数组转换为数组

* 转换方法
  * 使用 Array.from()
  * 使用 Array.prototype.slice.call()
  * 使用 Array.prototype.forEach() 进行属性遍历并组成新的数组
  * **使用扩展运算符（...）**
* 转换须知
  * 转换后的数组长度由 length 属性决定。索引不连续时转换结果是连续的，会自动补位

```javascript
    let al1 = {
        length: 4,
        0: 0,
        1: 1,
        3: 3,
        4: 4,
        5: 5,
    };
    console.log(Array.from(al1)) // [0, 1, undefined, 3]
    // 2.仅考虑 0或正整数 的索引
    let al2 = {
        length: 4,
        '-1': -1,
        '0': 0,
        a: 'a',
        1: 1
    };
    console.log(Array.from(al2)); // [0, 1, undefined, undefined]
    // 3.使用slice转换产生稀疏数组
    let al2 = {
        length: 4,
        '-1': -1,
        '0': 0,
        a: 'a',
        1: 1
    };
    console.log(Array.prototype.slice.call(al2)); //[0, 1, empty × 2]
 // 4.使用展开运算符
 let pseudoArray = {0: "a", 1: "b", 2: "c", length: 3};  
 let realArray = [...pseudoArray];  
 console.log(realArray);  // ["a", "b", "c"]  
    // 5.使用数组方法操作伪数组注意地方
    let arrayLike2 = {
        2: 3,
        3: 4,
        length: 2,
        push: Array.prototype.push
    }
    // push 操作的是索引值为 length 的位置
    arrayLike2.push(1);
    console.log(arrayLike2); // {2: 1, 3: 4, length: 3, push: ƒ}
    arrayLike2.push(2);
    console.log(arrayLike2); // {2: 1, 3: 2, length: 4, push: ƒ}
```

## 1.18 介绍下 Set、Map、WeakSet 和 WeakMap的区别？

**Set**

1. 成员不能重复；
2. 只有键值，没有键名，有点类似数组；
3. 可以遍历，方法有 add、delete、has

**WeakSet**

1. 成员都是对象（引用）；
2. 成员都是弱引用，随时可以消失（不计入垃圾回收机制）。可以用来保存 DOM 节点，不容易造成内存泄露；
3. 不能遍历，方法有 add、delete、has ；

**Map**

1. 本质上是键值对的集合，类似集合；
2. 可以遍历，方法很多，可以跟各种数据格式转换；

**WeakMap**

1. 只接收对象为键名（null 除外），不接受其他类型的值作为键名；
2. 键名指向的对象，不计入垃圾回收机制；
3. 不能遍历，方法同 get、set、has、delete ；

## 1.19 简单说说 js 中有哪几种内存泄露的情况

1. 意外的全局变量；
2. 闭包；
3. 未被清空的定时器；
4. 未被销毁的事件监听；
5. DOM 引用；

## 1.20 json和xml数据的区别?

1. 数据体积方面：xml是重量级的，json是轻量级的，传递的速度更快些。
2. 数据传输方面：xml在传输过程中比较占带宽，json占带宽少，易于压缩。
3. 数据交互方面：json与javascript的交互更加方便，更容易解析处理，更好的进行数据交互
4. 数据描述方面：json对数据的描述性比xml较差
5. xml和json都用在项目交互下，xml多用于做配置文件，json用于数据交互。

## 1.21 JavaScript有几种方法判断变量的类型?

1. 使用typeof检测当需要判断变量是否是number, string, boolean, function, undefined等类型时，可以使用typeof进行判断。 (typeof num === 'number')
2. 使用instanceof检测instanceof运算符与typeof运算符相似，用于识别正在处理的对象的类型。与typeof方法不同的是，instanceof 方法要求开发者明确地确认对象为某特定类型。(obj instanceof Array)
3. 使用constructor检测constructor本来是原型对象上的属性，指向构造函数。但是根据实例对象寻找属性的顺序，若实例对象上没有实例属性或方法时，就去原型链上寻找，因此，实例对象也是能使用constructor属性的。

## 1.22  Math.min()< Math.max()

false
按常规的思路，这段代码应该输出 true，毕竟最小值小于最大值。但是却输出 false

## 1.23 promise和 async await 区别?

**概念**
Promise 是异步编程的一种解决方案，比传统的解决方案——回调函数和事件——更合理和更强
大，简单地说，Promise好比容器，里面存放着一些未来才会执行完毕（异步）的事件的结果，而
这些结果一旦生成是无法改变的
async await也是异步编程的一种解决方案，他遵循的是Generator 函数的语法糖，他拥有内置执

行器，不需要额外的调用直接会自动执行并输出结果，它返回的是一个Promise对象

**两者的区别**

1. Promise的出现解决了传统callback函数导致的“地域回调”问题，但它的语法导致了它向纵向
   发展行成了一个回调链，遇到复杂的业务场景，这样的语法显然也是不美观的。而async
   await代码看起来会简洁些，使得异步代码看起来像同步代码，await的本质是可以提供等同
   于”同步效果“的等待异步返回能力的语法糖，只有这一句代码执行完，才会执行下一句。
2. async await与Promise一样，是非阻塞的。
3. async await是基于Promise实现的，可以说是改良版的Promise，它不能用于普通的回调函
   数。

## 1.24 defer和async区别?

* `defer`要等到整个页面在内存中正常渲染结束（DOM结构完全生成，以及其他脚本执行完成），才会执行。多个defer脚本会按照它们在页面出现的顺序加载。==“渲染完再执行”==
* `async`一旦下载完，渲染引擎就会中断渲染，执行这个脚本以后，再继续渲染。多个async脚本是不能保证加载顺序的。==“下载完就执行”==

## 1.25 同步和异步

**同步**

* 指在 主线程上排队执行的任务，只有前一个任务执行完毕，才能继续执行下一个任务。
* 也就是调用一旦开始，必须这个调用 返回结果(划重点——）才能继续往后执行。程序的执行顺序
  和任务排列顺序是一致的。

**异步**

* 异步任务是指不进入主线程，而进入 任务队列的任务，只有任务队列通知主线程，某个异步任务可以执行了，该任务才会进入主线程。
* 每一个任务有一个或多个 回调函数。前一个任务结束后，不是执行后一个任务,而是执行回调函数，后一个任务则是不等前一个任务结束就执行。
* 程序的执行顺序和任务的排列顺序是不一致的，异步的。
* 我们常用的setTimeout和setInterval函数，Ajax都是异步操作。

## 1.26 javascript中arguments相关的问题？

**arguments**

在js中，我们在调用有参数的函数时，当往这个调用的有参函数传参时，js会把所传的参数全部存到一个叫arguments的对象里面。它是一个类数组数据

**由来**

Javascrip中每个函数都会有一个Arguments对象实例arguments，引用着函数的实参。它是寄生在js函数当中的，不能显式创建，arguments对象只有函数开始时才可用

**作用**

有了arguments这个对象之后，我们可以不用给函数预先设定形参了，可以动态地通过arguments为函数加入参数

## 1.27 null 和 undefined 的区别，如何让一个属性变为null

**undefined**

1. 声明了一个变量，但没有赋值
2. 访问对象上不存在的属性
3. 函数定义了形参，但没有传递实参
4. 使用 void 对表达式求值

**null**

1. null是一个空值
2. null 有属于自己的类型 Null，而不属于Object类型
3. 二进制的前三位为 0 会被 typeof 判断为对象类型

## 1.28 简单说说 js 中有哪几种内存泄露的情况

1. 意外的全局变量；
2. 闭包；
3. 未被清空的定时器；
4. 未被销毁的事件监听；
5. DOM 引用；

## 1.29 call appy bind的作用和区别？

**作用：**

都可以改变函数内部的this指向

**区别点：**

1. call 和 apply 会调用函数，并且改变函数内部this指向。
2. call 和 apply 传递的参数不一样，call 传递参数arg1,arg2...形式 apply 必须数组形式[arg]
3. bind 不会调用函数，可以改变函数内部this指向

## 1.30 this指向（普通函数、箭头函数）

1. 谁调用了函数或者方法，那么这个函数或者对象中的this就指向谁
2. 匿名函数中的this：匿名函数的执行具有全局性，则匿名函数中的this指向是window，而不是调用该匿名函数的对象

**箭头函数中的this**

* 箭头函数中的this是在函数定义的时候就确定下来的，而不是在函数调用的时候确定的
* 箭头函数中的this指向父级作用域的执行上下文；
* 箭头函数无法使用apply、call和bind方法改变this指向，因为其this值在函数定义的时候就被确定下来

## 1.31 箭头函数能否当构造函数

**箭头函数表达式**的语法比函数表达式更简洁，并且没有自己的 this ， arguments ， super 或new.target 。箭头函数表达式更适用于那些本来需要匿名函数的地方，并且它不能用作构造函数

## 1.32 继承，优缺点 及方法有哪些？

**继承的好处**

a：提高了代码的复用性

b：提高了代码的维护性

c：让类与类之间产生了关系，是多态的前提

**继承的弊端**

类的耦合性增强了,但是开发的原则：高内聚，低耦合

### 1.32.1原型链继承

实现方式：将子类的原型链指向父类的对象实例

```js
function Parent(){
 this.name = "parent";
 this.list = ['坤'];
}
Parent.prototype.sayHi = function(){
 console.log('hello');
}
function Child(){

}
Child.prototype = new Parent();
let child = new Child();
console.log(child.name); 
child.sayHi();
```

**原理：**子类实例child的`__proto__` 指向Child的原型链prototype，而Child.prototype指向Parent类的对象实例，该父类对象实例的 `__proto__` 指向Parent.prototype,所以Child可继承Parent的构造函数属性、方法和原型链属性、方法

**优点：**可继承构造函数的属性，父类构造函数的属性，父类原型的属性

**缺点：**

1. 无法向父类构造函数传参；
2. 共享父类实例的属性（若父类共有属性为引用类型，一个子类实例更改父类构造函数共有属性时会导致继承的共有属性发生变化）

```js
var a = new Child();
var b = new Child();
a.list.push('rap');
console.log(b.list); // ['坤','rap']
```

### 1.32.2 构造函数继承

实现方式：在子类构造函数中使用call或者apply劫持父类构造函数方法，并传入参数

```js
function Parent(name, id){
    this.id = id
    this.name = name
    this.printName = function(){
     console.log(this.name)
    }
}
Parent.prototype.sayName = function(){
 console.log(this.name)
};
function Child(name, id){
 Parent.call(this, name, id) // Parent.apply(this, arguments);
}
var child = new Child("坤", "1")
child.printName()  // 坤
child.sayName()  // Error
```

**原理：**使用call或者apply改变子类函数的作用域，使this执行父类构造函数，子类因此可以继承父类共有属性

优点：可解决原型链继承 **共享** 的问题

缺点： 不可继承父类的原型方法，构造函数不可以被复用

### 1.32.3 组合继承

**原理：**综合使用构造函数继承和原型链继承

```js
function Parent(name, id){
    this.id = id;
    this.name = name;
    this.list = ['rap'];
    this.printName = function(){
     console.log(this.name);
    }
}
Parent.prototype.sayName = function(){
 console.log(this.name);
};
function Child(name, id){
 Parent.call(this, name, id); // Parent.apply(this, arguments);
}
Child.prototype = new Parent();
var child = new Child("坤坤", "1");
child.printName();  // 坤坤
child.sayName()  // 坤坤
var a = new Child();
var b = new Child();
a.list.push('篮球');
console.log(b.list); // ['rap']    
```

**优点：**可继承父类原型上的属性，且可传参；每个新实例引入的构造函数是私有的

**缺点：**会执行两次父类的构造函数，消耗较大内存，子类的构造函数会代替原型上的那个父类构造函数

### 1.32.4 原型式继承

**原理：**类似Object.create，用一个函数包装一个对象，然后返回这个函数的调用，这个函数就变成了个可以随意增添属性的实例或对象，结果是将子对象的  `__proto__` 指向父对象

```js
let parent = {
 name: ['坤坤']
}
function copy(object) {
 function fn() {}
 fn.prototype = object
 return new F()
}
var child = copy(parent)
```

**缺点：** 共享引用数据类型

### 1.32.5 寄生式继承

**原理：**扩展原型式继承

```js
function copy(object) {
 function fn() {}
 fn.prototype = object
 return new F()
}
function createObject(obj) {
 let obj = copy(obj);
 obj.getNames = function() {
  console.log(this.names)
  return this.names
 }
 return obj
}
```

**优点：**可添加新的属性和方法

### 1.32.6 寄生组合式继承

**原理：**改进组合继承，利用寄生式继承的思想继承原型

```js
function inheritPrototype(subClass, superClass) {
 // 复制一份父类的原型
 let p = copy(superClass.prototype);
 // 修正构造函数
 p.constructor = subClass;
 // 设置子类原型
 subClass.prototype = p;
}
function Parent(name, id){
    this.id = id;
    this.name = name;
    this.list = ['a'];
    this.printName = function(){
     console.log(this.name);
    }
}
Parent.prototype.sayName = function(){
 console.log(this.name);
};
function Child(name, id){
 Parent.call(this, name, id);
// Parent.apply(this, arguments);
}
inheritPrototype(Child, Parent);
```

### 1.32.7 ES6 class extends

```js
class A {
 constructor() {
  this.a = 'hello';
 }
}
class B extends A {
    constructor() {
     super();
     this.b = 'world';
    }
}
let b = new B();
```

## 1.33 扩展运算符

### 1.33.1哪些类型能被扩展操作符?

**类型：**数组、对象、字符串

* 复杂数据类型都可以，当要转化为可迭代数据结构时可设置对象的迭代器对扩展运算符扩展出来的值进行操作。

* 基础数据只有string可以使用扩展运算符，number,boolean,null,undefined无效

### 1.33.2 场景

```js
// 1、函数调用
function add(x, y) {
 return x + y
}
add(...[4, 38])

function f(a, b, c, d, e) { }
f(1, ...[1, 2], 2, ...[3])

//2.往数组里push多个元素
var arr1 = ['子异', '坤坤'];
var arr2 = ['说', '唱', '跳'];
arr1.push(...arr2);
console.log(arr1); //['子异', '坤坤','说', '唱', '跳']

//3.替代函数的apply方法
function f(a, b, c) { }
var args = [0, 1, 2];
f.apply(null, args);  //ES5 的写法
f(...args);    //ES6的写法

//4.求一个数组的最大数简化
Math.max.apply(null, [14, 3, 77]) //ES5 的写法
Math.max(...[14, 3, 77]) //ES6 的写法，等同于Math.max(14, 3, 77)

//5.扩展运算符后面可以放表达式
const arr = [...(5 > 0 ? ['a'] : []),'b'];
console.log(arr); //['a','b']

//6.与解构赋值结合，用于生成数组
const a1 = [1, 2];
const a2 = [...a1]; //写法1
const [...a2] = a1; //写法2
const [first, ...rest] = [1, 2, 3, 4, 5];
first //1
rest //[2, 3, 4, 5]
const [first, ...rest] = [];
first //undefined
rest //[]
const [first, ...rest] = ["foo"];
first //"foo"
rest //[]
//1234567891011121314151617

//7.合并数组
[...arr1, ...arr2, ...arr3] //[ 'a', 'b', 'c', 'd', 'e' ]
123
//8.数组的克隆
var arr1 = [0, 1, 2];
var arr2 = [...arr1];
arr1[0]=100;
console.log(arr2); //[0, 1, 2]
/* 乍一看，arr2与arr1不共用引用地址，arr2不随着arr1变化，接着往下看 */
var arr1 = [0, [1,11,111], 2];
var arr2 = [...arr1];
arr1[1][0]=100;
console.log(arr2); //[0, [100,11,111], 2]
```

## 1.34 实现异步的方法

### 1.34.1 回调函数

```js
ajax(url, () => {
// 处理逻辑
    ajax(url1, () => {
    // 处理逻辑
        ajax(url2, () => {
        // 处理逻辑
        })
    })
})
```

**优点：**简单、容易理解和实现

**缺点：**不利阅读和维护，耦合度高，不能使用try...catch捕获，不能直接 return

### 1.34.2 promise

本意是承诺，**这个承诺一旦从等待状态变成为其他状态就永远不能更改状态了**

**Promise的三种状态**

* Pending----Promise对象实例创建时候的初始状态

* Fulfilled----可以理解为成功的状态
* Rejected----可以理解为失败的状态

```js
let p = new Promise((resolve, reject) => {
    reject('reject')
    resolve('success')//无效代码不会执行
})
p.then( value => {
    console.log(value)
},
reason => {
 console.log(reason)//reject
})
```

当我们在构造 Promise 的时候，构造函数内部的代码是立即执行的

```js
new Promise((resolve, reject) => {
    console.log('1')
    resolve('success')
})
console.log('2')
```

promise的链式调用

* 每次调用返回的都是一个新的Promise实例(这就是then可用链式调用的原因)

* 如果then中返回的是一个结果的话会把这个结果传递下一次then中的成功回调

* 如果then中出现异常,会走下一个then的失败回调

* 在 then中使用了return，那么 return 的值会被Promise.resolve() 包装(见例1，2)

* then中可以不传递参数，如果不传递会透到下一个then中(见例3)
* catch 会捕获到没有捕获的异常

```js
Promise.resolve(1)
.then(res => {
console.log(res)
return 2 //包装成 Promise.resolve(2)
})
.catch(err => 3)
.then(res => console.log(res))

ajax(url).then(res => {
 console.log(res)
 return ajax(url1)
}).then(res => {
 console.log(res)
 return ajax(url2)
}).then(res => console.log(res))
```

存在一个缺点：无法取消promise，错误需要通过回调函数捕获

### 1.34.3 生成器generator/yield

**特点：**控制函数的执行

* Generator 函数是一个状态机，封装了多个内部状态
* Generator 函数除了状态机，还是一个遍历器对象生成函数
* 可暂停函数, yield可暂停，next方法可启动，每次返回的是yield后的表达式结果
* yield表达式本身没有返回值，或者说总是返回undefined。next方法可以带一个参数，该参数就会被当作上一个yield表达式的返回值

```js
function *foo(x) {
    let y = 2 * (yield (x + 1))      
    let z = yield (y / 5)           
    return (x + y + z)
}
let it = foo(2)
console.log(it.next())   // => {value: 3, done: false}
console.log(it.next(20)) // => {value: 8, done: false}
console.log(it.next(30))  // => {value: 72, done: true}

// 解决回调地狱
function *fetch() {
 yield ajax(url, () => {})
 yield ajax(url1, () => {})
 yield ajax(url2, () => {})
}
let it = fetch()
let result1 = it.next()
let result2 = it.next()
let result3 = it.next()
```

### 1.34.3 async/await

**特点：**

* async/await是基于Promise实现的，它不能用于普通的回调函数
* async/await与Promise一样，是非阻塞的

```js
async function fn() {
 return "async"
}
console.log(fn()) // -> Promise {<resolved>: "async"}
```

类似generator调用方式

```js
async function ff() {
    await ajax(url1, ()=>{})
    await ajax(url2,()=>{})
    await ajax(url3,()=>{})
}
await ff()
```

模拟一个并发请求

```js
function readAll() {
    
    read1()
 read2()//这个函数同步执行
}
async function read1() {
    let r = await ajax(url1,()=>{})
 console.log(r)
}
async function read2() {
 let r = await ajax(url2,()=>{})
 console.log(r)
}
readAll()
```

## 1.35 循环i 一次性定时器中输出什么，如何解决？

下段代码输出

```js
for (var i = 0; i< 10; i++){
    setTimeout((i) => {
        console.log(i)
    }, 0)
}
```

期望输出0-9

结果输出 10个9，原因：setTimeout是异步的，而var 这个时候是全局变量，所以打印10个9

方法一：

```js
for (var i = 0; i< 10; i++){
    setTimeout((i) => {
        console.log(i)
    }, 1000,i)
}
```

方法二：

```js
for (let i = 0; i< 10; i++){
    setTimeout(() => {
        console.log(i)
    }, 1000)
}
```

方法三：

```js
for (var i = 0; i< 10; i++){
 ((i)=>{
        setTimeout(() => {
            console.log(i)
        },1000);
    })(i)
}
```

方法四：

```js
for (var i = 0; i< 10; i++){
 setTimeout(console.log(i),1000);
}
for (var i = 0; i< 10; i++){
 setTimeout((()=>console.log(i))(),1000);
}
```

方法五：

```js
for (var i = 0; i< 10; i++){
 try{
  throw i
 }catch(i){
        setTimeout(() => {
            console.log(i)
        }, 1000)
 }
}
```

## 1.36 为什么js是单线程

**用途：**js在创立之初主要是应用于用户与浏览器的交互，以及操作dom，这一特性决定了，只能是单线程，否则会带来复杂的同步问题。

​  例如： 如果js被设计了多线程，如果有一个线程要修改一个dom元素，另一个线程要删除这个dom，这时候就不能处理。避免这个问题，浏览器就设计了单线程，避免了这个麻烦

## 1.37 死锁

死锁是指两个或两个以上的进程在执行过程中，由于竞争资源而造成阻塞的现象，若无外力作用，它们都将无法继续执行

**产生原因：**

* 竞争资源引起进程死锁
* 可剥夺和非剥夺资源
* 竞争非剥夺资源
* 竞争临时性资源
* 进程推进顺序不当

**产生条件：**

1. 互斥条件：涉及的资源是非共享的
   * 涉及的资源是非共享的,一段时间内某资源只由一个进程占用,如果此时还有其它进程请求资源，则请求者只能等待，直至占有资源的进程用毕释放

2. 不剥夺条件：不能强行剥夺进程拥有的资源
   * 进程已获得的资源，在未使用完之前，不能被剥夺，只能在使用完时由自己释放

3. 请求和保持条件：进程在等待一新资源时继续占有已分配的资源
   * 指进程已经保持至少一个资源，但又提出了新的资源请求，而该资源已被其它进程占有，此时请求进程阻塞，但又对自己已获得的其它资源保持不放 环路等待条件：存在一种进程的循环链，链中的每一个进程已获得的资源同时被链中的下一个进程所请求 在发生死锁时，必然存在一个进程——资源的环形链

解决办法

只要打破四个必要条件中的一个就能有效防止死锁的发生

## 1.38 暂时性死区

暂时性死区的本质就是，只要一进入当前作用域，所要使用的变量就已经存在了，但是不可获取，只有等到声明变量的那一行代码出现，才可以获取和使用该变量

let 、const具有暂时性死区

var 不具有暂时性死区

# 浏览器

## **1.1 cookie sessionStorage localStorage** **区别**

**共同点：**

都是保存在浏览器端、且同源的

**区别：**

1. cookie数据始终在同源的http请求中携带（即使不需要），即cookie在浏览器和服务器间来回传递，而sessionStorage和localStorage不会自动把数据发送给服务器，仅在本地保存。cookie数据还有路径（path）的概念，可以限制cookie只属于某个路径下

2. 存储大小限制也不同，cookie数据不能超过4K，同时因为每次http请求都会携带cookie、所以cookie只适合保存很小的数据，如会话标识。sessionStorage和localStorage虽然也有存储大小的限制，但比cookie大得多，可以达到5M或更大

3. 数据有效期不同，sessionStorage：仅在当前浏览器窗口关闭之前有效；localStorage：始终有效，窗口或浏览器关闭也一直保存，因此用作持久数cookie：只在设置的cookie过期时间之前有效，即使窗口关闭或浏览器关闭

4. 作用域不同，sessionStorage不在不同的浏览器窗口中共享，即使是同一个页面；localstorage在所有同源窗口中都是共享的；cookie也是在所有同源窗口中都是共享的

5. web Storage支持事件通知机制，可以将数据更新的通知发送给监听者
6. Storage的api接口使用更方便

## 1.2 如何写一个会过期的localStorage，说说想法

**惰性删除 和 定时删除**

**惰性删除**

惰性删除是指，某个键值过期后，该键值不会被马上删除，而是等到下次被使用的时候，才会被检查到过期，此时才能得到删除。

```js
var lsc = (function (self) {
var prefix = 'lsc_'
    /**
    * 增加一个键值对数据
    * @param key 键
    * @param val 值
    * @param expires 过期时间，单位为秒
    */
    self.set = function(key, val, expires) {
        key = prefix + key;
        val = JSON.stringify({'val': val, 'expires': new Date().getTime() + expires * 1000});
        localStorage.setItem(key, val);
    };
    /**
    * 读取对应键的值数据
    * @param key 键
    * @returns {null|*} 对应键的值
    */
    self.get = function(key) {
        key = prefix + key;
        var val = localStorage.getItem(key);
        if (!val) {
            return null;
        }
     val = JSON.parse(val);
        if (val.expires < new Date().getTime()) {
            localStorage.removeItem(key);
            return null;
        }
     return val.val;
    };
    return self;
}(lsc || {}));
```

**定时删除**

定时删除是指，每隔一段时间执行一次删除操作

1. 随机测试20个设置了过期时间的key。
2. 删除所有发现的已过期的key。
3. 若删除的key超过5个则重复**步骤****1**，直至重复500次。

```javascript
var lsc = (function (self) {
 var prefix = 'lsc_'
 var list = [];
    //初始化
    self.init = function () {
        var keys = Object.keys(localStorage);
        var reg = new RegExp('^' + prefix);
        var temp = [];
        //遍历所有localStorage中的所有key
        for (var i = 0; i < keys.length; i++) {
            //找出可过期缓存的key
            if (reg.test(keys[i])) {
                temp.push(keys[i]);
            }
        }
        list = temp;
 };
 self.init();
 self.check = function () {
        if (!list || list.length == 0) {
            return;
        }
     var checkCount = 0;
    while (checkCount < 500) {
     var expireCount = 0;
        // 随机测试20个设置了过期时间的key
        for (var i = 0; i < 20; i++) {
            if (list.length == 0) {
                break;
            }
            var index = Math.floor(Math.random() * list.length);
            var key = list[index];
            var val = localStorage.getItem(list[index]);
            // 从list中删除被惰性删除的key
            if (!val) {
                list.splice(index, 1);
                expireCount++;
                continue;
            }
            val = JSON.parse(val);
            // 删除所有发现的已过期的key
            if (val.expires < new Date().getTime()) {
                list.splice(index, 1);
                localStorage.removeItem(key);
                expireCount++;
            }
        }
        // 若删除的key不超过5个则跳出循环
        if (expireCount <= 5 || list.length == 0) {
            break;
        }
  checkCount++;
  }
 }
    //每隔一秒执行一次定时删除
    window.setInterval(self.check, 1000);
    return self;
}(lsc || {}));
```

## 1.3 **localStorage** **能跨域吗**

不能

**解决办法**

* 通过postMessage来实现跨源通信
* 可以实现一个公共的iframe部署在某个域名中，作为共享域
* 将需要实现localStorage跨域通信的页面嵌入这个iframe

## **1.4 memory cache** **如何开启**

memory cache 如何开启是一种比较特殊的缓存，他不受max-age、no-cache等配置的影响，即使我们不设置缓存，如果当前的内存空间比较充裕的话，一些资源还是会被缓存下来。但这种缓存是暂时的，一旦关闭了浏览器，这一部分用于缓存的内存空间就会被释放掉。如果真的不想使用缓存，可以设置no-store，这样，即便是内存缓存，也不会生效

## 1.5 localstorage的注意哪些问题

1. 兼容性问题
2. localStorage在浏览器的隐私模式下面是不可读取的
3. localStorage本质上是对字符串的读取，如果存储内容多的话会消耗内存空间，会导致页面变卡
4. localStorage不能被爬虫抓取到

## 1.6 浏览器输入URL发生了什么

1. URL 解析
2. DNS 查询
3. TCP 连接
4. 处理请求
5. 接受响应
6. 渲染页面

## 1.7 浏览器是如何渲染页面的？

不同浏览器内核渲染机制有所区别

1. HTML 被 HTML 解析器解析成 DOM 树；
2. CSS 被 CSS 解析器解析成 CSSOM 树；
3. 结合 DOM 树和 CSSOM 树，生成一棵渲染树(Render Tree)，这一过程称为 Attachment；
4. 生成布局(flow)，浏览器在屏幕上“画”出渲染树中的所有节点；
5. 将布局绘制(paint)在屏幕上，显示出整个页面。

webkit

![image-20230810145750627](C:\Users\admin\AppData\Roaming\Typora\typora-user-images\image-20230810145750627.png)

Gecko

![image-20230810145831120](C:\Users\admin\AppData\Roaming\Typora\typora-user-images\image-20230810145831120.png)

## 1.8 重绘、重排

**概念**

1. 重排(Reflow)：当渲染树的一部分必须更新并且节点的尺寸发生了变化，浏览器会使渲染树中受到影响的部分失效，并重新构造渲染树
2. 重绘(Repaint)：是在一个元素的外观被改变所触发的浏览器行为，浏览器会根据元素的新属性重新绘制，使元素呈现新的外观。比如改变某个元素的背景色、文字颜色、边框颜色等等

**区别：**

重绘不一定需要重排（比如颜色的改变），重排必然导致重绘（比如改变网页位置）

**引发重排**

1. 添加、删除可见的dom
2. 元素的位置改变
3. 元素的尺寸改变(外边距、内边距、边框厚度、宽高、等几何属性)
4. 页面渲染初始化
5. 浏览器窗口尺寸改变
6. 获取某些属性。当获取一些属性时，浏览器为取得正确的值也会触发重排,它会导致队列刷新，这些属性包括：offsetTop、offsetLeft、 offsetWidth、offsetHeight、scrollTop、scrollLeft、scrollWidth、scrollHeight、clientTop、clientLeft、clientWidth、clientHeight、getComputedStyle() (currentStyle in IE)。所以，在多次使用这些值时应进行缓存

**优化方案**

浏览器会维护1个队列，把所有会引起重排，重绘的操作放入这个队列，等队列中的操作到一定数量或者到了一定时间间隔，浏览器就会flush队列，进行一批处理，这样多次重排，重绘变成一次重排重绘

减少 reflow/repaint：

1. 不要一条一条地修改 DOM 的样式。可以先定义好 css 的 class，然后修改 DOM 的className。

2. 不要把 DOM 结点的属性值放在一个循环里当成循环里的变量。

3. 为动画的 HTML 元件使用 fixed 或 absoult 的 position，那么修改他们的 CSS 是不会reflow 的。

4. 千万不要使用 table 布局。因为可能很小的一个小改动会造成整个 table 的重新布局。(table及其内部元素除外，它可能需要多次计算才能确定好其在渲染树中节点的属性，通常要花3倍于同等元素的时间。这也是为什么我们要避免使用table做布局的一个原因。)

5. 不要在布局信息改变的时候做查询（会导致渲染队列强制刷新）

## 1.9 事件循环（Event loop）

主线程从"任务队列"中读取执行事件，这个过程是循环不断的，这个机制被称为事件循环

**JavaScript 的事件分两种**

1. 宏任务：包括整体代码 script，setTimeout，setInterval
2. 微任务：Promise.then(非 new Promise)，process.nextTick(node 中)

**具体执行：**

事件的执行顺序——先执行宏任务，然后执行微任务，任务有同步的任务和异步的任务，同步的进入主线程，异步的进入 Event Table 并注册函数，异步事件完成后，会将回调函数放在队列中，如果还有异步的宏任务，那么就会进行循环执行上述的操作

主 线程会不断从任务队列中按顺序取任务执行，每执行完一个任务都会检查microtask队列是否为空（执行完一个 任务的具体标志是函数执行栈为空），如果不为空则会一次性执行完所有microtask。然后再进入下一个循环去 任务队列中取下一个任务执行

**详细步骤**：

1. 选择当前要执行的宏任务队列，选择一个最先进入任务队列的宏任务，如果没有宏任务可以选择，则会 跳转至microtask的执行步骤。

2. 将事件循环的当前运行宏任务设置为已选择的宏任务。
3. 运行宏任务。
4. 将事件循环的当前运行任务设置为null。
5. 将运行完的宏任务从宏任务队列中移除。
6. microtasks步骤：进入microtask检查点。
7. 更新界面渲染。
8. 返回第一步。

**执行进入microtask检查的的具体步骤如下:**

1. 设置进入microtask检查点的标志为true。
2. 当事件循环的微任务队列不为空时：选择一个最先进入microtask队列的microtask；设置事

件循环的当 前运行任务为已选择的microtask；运行microtask；设置事件循环的当前运行任务

为null；将运行结束 的microtask从microtask队列中移除。

3. 对于相应事件循环的每个环境设置对象（environment settings object）,通知它们哪些

promise为 rejected。

4. 清理indexedDB的事务。
5. 设置进入microtask检查点的标志为false。

**注意**

当前执行栈执行完毕时会立刻先处理所有微任务队列中的事件,然后再去宏任务队列中取出一个事件。同一次事件循环中,微任务永远在宏任务之前执行

## 1.10 let a = 1 挂载在哪里？

var a 挂载在window下。而let是挂载在 全局函数下面

## 1.11 浏览器垃圾回收机制

浏览器的 Javascript 具有自动垃圾回收机制(GC:Garbage Collecation),执行环境会负责管理代码执行过程中使用的内存

**原理：**

垃圾收集器会定期（周期性）找出那些不在继续使用的变量，然后释放其内存

```javascript
function fn1() {
 var obj = {name: 'hanzichi', age: 10};
}
function fn2() {
    var obj = {name:'hanzichi', age: 10};
    return obj;
}
var a = fn1();
var b = fn2();
/*
 首先定义了两个function，分别叫做fn1和fn2,当fn1被调用时，进入fn1的环境，会开辟一块内存存放对象{name: 'hanzichi', age: 10}，而当调用结束后，出了fn1的环境，那么该块内存会被js引擎中的垃圾回收器自动释放；在fn2被调用的过程中，返回的对象被全局变量b所指向，所以该块内存并不会被释放
*/
```

**问题**

到底哪个变量是没有用的？

**解决**

所以垃圾收集器必须跟踪到底哪个变量没用，对于不再有用的变量打上标记，以备将来收回其内存。用于标记的无用变量的策略可能因实现而有所区别，通常

情况下有两种实现方式：**标记清除**和**引用计数**。引用计数不太常用，标记清除较为常用。

**标记清除**

```javascript
function test(){
 var a = 10 ; //被标记 ，进入环境
 var b = 20 ; //被标记 ，进入环境
}
test(); //执行完毕 之后 a、b又被标离开环境，被回收。
```

**引用计数**

```javascript
function test(){
var a = {} ; //a的引用次数为0
var b = a ; //a的引用次数加1，为1
var c =a; //a的引用次数再加1，为2
var b ={}; //a的引用次数减1，为1
}
test(); 
```

**GC****方案**

​ **1.** **基础方案**

​ Javascript引擎基础GC方案是（simple GC）：mark and sweep（标记清除），即：

1. 遍历所有可访问的对象。
2. 回收已不可访问的对象。

​ **2. GC的缺陷**

​ 和其他语言一样，javascript的GC策略也无法避免一个问题：GC时，停止响应其他操作，这是为了安全考虑。而Javascript的GC在100ms甚至以上，对一般的应用还好，但对于JS游戏，动画对连贯性要求比较高的应用，就麻烦了。这就是新引擎需要优化的点：避免GC造成的长时间停止响应。

​ **3. GC优化策略**

1. **分代回收**（Generation GC） 这个和Java回收策略思想是一致的，也是V8所主要采用的。目的是通过区分“临时”与“持久”对象；多回收“临时对象”区（young generation），少回收“持久对象”区（tenured generation），减少每次需遍历的对象，从而减少每次GC的耗时

![image-20230810163252320](C:\Users\admin\AppData\Roaming\Typora\typora-user-images\image-20230810163252320.png)

补充：对于tenured generation对象，有额外的开销：把它从young generation迁移到tenured generation，另外，如果被引用了，那引用的指向也需要修改。

2. **增量GC** 这个方案的思想很简单，就是“每次处理一点，下次再处理一点，如此类推”

![image-20230810163307127](C:\Users\admin\AppData\Roaming\Typora\typora-user-images\image-20230810163307127.png)

​  这种方案，虽然耗时短，但中断较多，带来了上下文切换频繁的问题。

​  因为每种方案都其适用场景和缺点，因此在实际应用中，会根据实际情况选择方案。

​  比如：低 (对象/s) 比率时，中断执行GC的频率，simple GC更低些；如果大量对象都是长期“存活”，则分代处理优势也不大。

## 1.12 cookie

1. **cookie是什么？**

* cookie 是存储于访问者计算机中的变量。每当一台计算机通过浏览器来访问某个页面时，那么就可以通过 JavaScript 来创建和读取 cookie。

* 实际上 cookie 是存于用户硬盘的一个文件，这个文件通常对应于一个域名，当浏览器再次访问这个域名时，便使这个cookie可用。因此，cookie可以跨越一个域名下的多个网页，但不能跨越多个域名使用。

* 不同浏览器对 cookie 的实现也不一样。即保存在一个浏览器中的 cookie 到另外一个浏览器是 不能获取的。

2. 怎么使用 cookie？

语法

```javascript
document.cookie = "name=value;expires=evalue; path=pvalue; domain=dvalue;secure;”
```

3. **注意事项**

* cookie可能被禁用。当用户非常注重个人隐私保护时，他很可能禁用浏览器的cookie功能
* cookie是与浏览器相关的。这意味着即使访问的是同一个页面，不同浏览器之间所保存的cookie也是不能互相访问的
* cookie可能被删除。因为每个cookie都是硬盘上的一个文件，因此很有可能被用户删除
* cookie安全性不够高。所有的cookie都是以纯文本的形式记录于文件中，因此如果要保存用户名密码等信息时，最好事先经过加密处理
* cookie 在保存时，只要后面保存的 name 相同，那么就会覆盖前面的 cookie，注意是完全覆盖，包括失效时间，pat

4. **cookie禁用**

sessionID通过cookie保存在客户端，如果将cookie禁用，必将对session的使用造成一定的影响

解决办法：url重写

## 1.13 调试工具

### a.谷歌浏览器

1. Elements：可查看网页页面代码（修改只是当前使用有效），也可实时调试修改页面ccs代码样式。

2. console：记录开发者开发过程中的日志信息，也可在里面写js代码。一般页面运行时js报错都是可以在这里看到反馈和定位bug原因及其位置。

3. Sources：断点调试JS，可以查看程序代码执行的过程，断点调试对于每一个程序员来说可是很重要。

4. Network：从发起网页页面请求开始，分析HTTP请求后得到的各个请求资源信息（“小编有时候就利用这下载一些网站不给下载的在线视频，比如教学视频”）。

5. Timeline：记录并分析网站的生命周期所发生的各类事件，分析渲染js执行的每一个阶段。
6. Application：记录网站加载的各个资源信息。
7. Security：判断网页是否安全。
8. Audits：对当前网页的网络利用及网页性能进行检测，并给出一些优化建议。

### b.其他

**postman**

Postman 是调试接口的最佳工具之一，使用 Postman，我们可以调整请求，分析响应和调试问题

**CSSLint**

CSSLint 是一个用来帮你找出 CSS 代码中问题的工具，它可做基本的语法检查以及使用一套预设的规则 来检查代码中的问题，规则是可以扩展的

**Sentry**

Sentry就是来帮我们解决这个问题的，它是是一个实时事件日志记录和聚合平台。它专门用于监视错误 和提取执行适当的事后操作所需的所有信息, 而无需使用标准用户反馈循环的任何麻烦

**BrowserStack**

BrowserStack 是一款提供网站浏览器兼容性测试的在线云端测试工具，从而开发测试人员不必再准备 很多虚拟机或者手机模拟器

# 网络传输

## 1.1 跨域

**跨域是什么？**

跨域（Cross-Origin）指的是在浏览器中，当一个请求的源（Origin）与目标资源的源不一致时，即发生跨域访问。在默认情况下，浏览器的同源策略（Same-Origin Policy）会阻止这种跨域访问。同源策略是为了保护用户的信息安全，防止恶意网站对其他网站的资源进行访问和操作。

**同源策略规定几个约束**

1. 协议相同
1. 域名相同
1. 端口号相同

**同源策略限制内容有**

* cookie、localstorage、indexedDB 等
* dom节点
* ajax 请求

**不受同源策略影响**

<code><img src='' /></code>

<code><link href='' /></code>

<code><script src='' /></code>

当存在跨域请求时，浏览器的安全策略也不同

* post、get、heade等请求，浏览器会自动发送一个跨域请求的预检请求（options）到目标资源的服务器，如果服务器返回的响应满足一定条件，浏览器会继续发送正式的请求，否则会跨域

* put、delete、等，浏览器会先发送一个预检请求到目标资源的服务器服务器返回的响应满足条件后，浏览器发送正式请求。与简单请求不同的是，非简单请求血药确保服务器在响应中设置了跨域请求所允许的响应首部字段

**解决方案**

* jsonp

**原理：**利用 <script> 标签没有跨域限制的漏洞，网页可以得到从其他来源动态产生的 JSON 数据。JSONP 请求一定 需要对方的服务器做支持才可以

**优缺点：**JSONP优点是简单兼容性好，可用于解决主流浏览器的跨域数据访问的问题

**缺点：**仅支持get方法 具有局限性, 不安全可能会遭受XSS攻击

实现流程

```html
<script src='http://www.baidu.com?callback=fn'></script>
<script>
function fn(r) {
    console.log(r)
}
</script>

```

* cors

服务器端设置 Access-Control-Allow-Origin: 白名单/*

注意：`*`不能使用cookie

* postMessage
* iframe

## 1.2 有什么方法可以保持前后端通信

实现保持前后端实时通信的方式有以下几种

* WebSocket： IE10以上才支持，Chrome16, FireFox11,Safari7以及Opera12以上完全支持，移动端形势大

* event-source: IE完全不支持（注意是任何版本都不支持），Edge76，Chrome6,Firefox6,Safari5和Opera以上支持， 移动端形势大好

* AJAX轮询： 用于兼容低版本的浏览器

* 永久帧（ forever iframe）可用于兼容低版本的浏览器

* flash socket 可用于兼容低版本的浏览器

**优缺点**

* **websocket**

**优点：**WebSocket 是 HTML5 开始提供的一种在单个 TCP 连接上进行全双工通讯的协议，可从HTTP升级而来，浏览器和服务器只需要一次握手，就可以进行持续的，双向的数据传输，因此能显著节约资源和带宽

**缺点：**

1. 兼容问题、
2. 不支持断线重连，需要手写心跳连接的逻辑
3. 通信机制相对复杂

* **event-source**

**优点：**

1. 只需一次请求，便可以stream的方式多次传送数据，节约资源和带宽
2. 相对WebSocket来说简单易用
3. 内置断线重连功能(retry)

**缺点：**

1. 是单向的，只支持服务端->客户端的数据传送，客户端到服务端的通信仍然依靠AJAX，没有”一家人整整齐齐“的感觉
2. 兼容性令人担忧，IE浏览器完全不支持

* **ajax轮询**

**优点：**兼容性良好，对标低版本IE

**缺点：**请求中有大半是无用的请求，浪费资源

* **Flash Socket**

**优点：** 兼容低版本浏览器

**缺点：**

1. 浏览器开启时flash需要用户确认
2. 加载时间长，用户体验较差
3. 大多数移动端浏览器不支持flash，为重灾区

* **永久帧**

**缺点：** iframe会产生进度条一直存在的问题，用户体验差

**优点：**兼容低版本IE浏览器

**综上：**

**综合兼容性和用户体验的问题，我在项目中选用了WebSocket ->server-sent-event -> AJAX轮询这三种方式做从上到下的兼容**

# 算法

## 1.1 顺序存储结构和链式存储结构

**优缺点**

1. 顺序存储时，相邻数据元素的存放地址也相邻（逻辑与物理统一）；要求内存中可用存储单元的地址必须是连续的。

​  优点：存储密度大（＝1），存储空间利用率高

​  缺点：插入或删除元素时不方便

2. 链式存储时，相邻数据元素可随意存放，但所占存储空间分两部分，一部分存放结点值，另一部分存放表示结点间关系的指针

​  优点：插入或删除元素时很方便，使用灵活

​  缺点：存储密度小（<1），存储空间利用率低

**场景**

1. 顺序表适宜于做查找这样的静态操作
1. 链表宜于做插入、删除这样的动态操作
1. 若线性表的长度变化不大，且其主要操作是查找，则采用顺序表
1. 若线性表的长度变化较大，且其主要操作是插入、删除操作，则采用链表

**顺序表与链表的比较**

* **基于空间的比较**
  * 存储分配的方式
    * 顺序表的存储空间是静态分配的
    * 链表的存储空间是动态分配的
  * 存储密度 = 结点数据本身所占的存储量/结点结构所占的存储总量
    * 顺序表的存储密度 = 1
    * 链表的存储密度 < 1

* **基于时间的比较**
  * 存取方式
    * 顺序表可以随机存取，也可以顺序存取
    * 链表是顺序存取的
  * 插入/删除时移动元素个数
    * 顺序表平均需要移动近一半元素
    * 链表不需要移动元素，只需要修改指针

# Vue

## 1.1 怎样理解 Vue 的单向数据流？

1. 数据从父级组件传递给子组件，只能单向绑定
2. 子组件内部不能直接修改从父级传递过来的数据
3. 所有的 prop 都使得其父子 prop 之间形成了一个单向下行绑定：父级 prop 的更新会向下流动到子组件中，但是反过来则不行，这样会防止从子组件意外改变父级组件的状态， 从而导致你的应用的数据流向难以理解。&#x20;
4. 每次父级组件发生更新时，子组件中所有的 prop 都将会刷新为最新的值，这意味着你不应该在一个子组件内部改变 prop。如果你这样做了，Vue 会在浏览器的控制台中发出警 告&#x20;
5. 子组件想修改时，只能通过 \$emit 派发一个自定义事件，父组件接收到后，由父组件 修改

## 1.2 谈谈你对 Vue 生命周期的理解？

**（1）生命周期是什么？**

Vue 实例有一个完整的生命周期，也就是从开始创建、初始化数据、编译模版、挂载 Dom -> 渲染、更新 -> 渲染、卸载等一系列过程，我们称这是 Vue 的生命周期

**（2）各个生命周期的作用**

| beforeCreate  | 组件实例被创建之初，组件的属性生效之前                                 |
| :------------ | :--------------------------------------------------------------------- |
| created       | 组件实例已经完全创建，属性也绑定，但真实 dom 还没有生成，\$el 还不可用 |
| beforeMount   | 在挂载开始之前被调用：相关的 render 函数首次被调用                     |
| mounted       | el 被新创建的 vm.\$el 替换，并挂载到实例上去之后调用该钩子             |
| beforeUpdate  | 组件数据更新之前调用，发生在虚拟 DOM 打补丁之前                        |
| update        | 组件数据更新之后                                                       |
| activited     | keep-alive 专属，组件被激活时调用                                      |
| deadctivated  | keep-alive 专属，组件被销毁时调用                                      |
| beforeDestory | 组件销毁前调用                                                         |
| destoryed     | 组件销毁后调用                                                         |

## 1.3 谈谈你对 keep-alive 的了解？

keep-alive 是 Vue 内置的一个组件，可以使被包含的组件保留状态，避免重新渲染 ，其有以下特性：

* 一般结合路由和动态组件一起使用，用于缓存组件
* 提供 include 和 exclude 属性，两者都支持字符串或正则表达式， include 表示只有名称匹配的组件会被缓存，exclude 表示任何名称匹配的组件都不会被缓存 ，其中 exclude 的优先级比 include 高
* 对应两个钩子函数 activated 和 deactivated ，当组件被激活时，触发钩子函数 activated，当组件被移除时，触发钩子函数 deactivated

## 1.4 组件中 data 为什么是一个函数？

因为组件是用来复用的，且 JS 里对象是引用关系，如果组件中 data 是一个对象，那么这样作用域没有隔离，子组件中的 data 属性值会相互影响

如果组件中 data 选项是一个函数，那么每个实例可以维护一份被返回对象的独立的拷贝，组件实例之间的 data 属性值不会互相影响；而 new Vue 的实例，是不会被复用的，因此不存在引用对象的问题

## 1.5 你对vue项目哪些优化？

**（1）代码层面的优化**

* v-if 和 v-show 区分使用场景
* computed 和 watch 区分使用场景
* v-for 遍历必须为 item 添加 key，且避免同时使用 v-if
* 长列表性能优化
* 事件的销毁
* 图片资源懒加载
* 路由懒加载
* 第三方插件的按需引入
* 优化无限列表性能
* 服务端渲染 SSR or 预渲染

**（2）Webpack 层面的优化**

* Webpack 对图片进行压缩
* 减少 ES6 转为 ES5 的冗余代码
* 提取公共代码
* 模板预编译
* 提取组件的 CSS
* 优化 SourceMap
* 构建结果输出分析
* Vue 项目的编译优化

**（3）基础的 Web 技术的优化**

* 开启 gzip 压缩
* 浏览器缓存
* CDN 的使用
* 使用 Chrome Performance 查找性能瓶颈

## 1.6 vue中的key有什么作用？

key 是为 Vue 中 vnode 的唯一标记，通过这个 key，我们的 diff 操作可以更准确、更快速

Vue 的 diff 过程可以概括为：oldCh 和 newCh 各有两个头尾的变量 oldStartIndex、oldEndIndex 和 newStartIndex、newEndIndex，它们会新节点和旧节点会进行两两对比，即一共有4种比较方式：newStartIndex 和oldStartIndex 、newEndIndex 和 oldEndIndex 、newStartIndex 和 oldEndIndex 、newEndIndex 和 oldStartIndex，如果以上 4 种比较都没匹配，如果设置了key，就会用 key 再进行比较，在比较的过程中，遍历会往中间靠，一旦 StartIdx > EndIdx 表明 oldCh 和 newCh 至少有一个已经遍历完了，就会结束比较

所以 Vue 中 key 的作用是：key 是为 Vue 中 vnode 的唯一标记，通过这个 key，我们的 diff 操作可以更准确、更快速

## 1.7 虚拟dom的优缺点

**优点：**

* 保证性能下限： 框架的虚拟 DOM 需要适配任何上层 API 可能产生的操作，它的一些 DOM 操作的实现必须是普适的，所以它的性能并不是最优的；但是比起粗暴的 DOM 操作性能要好很多，因此框架的虚拟 DOM 至少可以保证在你不需要手动优化的情况下，依然可以提供还不错的性能，即保证性能的下限；
* 无需手动操作 DOM： 我们不再需要手动去操作 DOM，只需要写好 View-Model 的代码逻辑，框架会根据虚拟 DOM 和 数据双向绑定，帮我们以可预期的方式更新视图，极大提高我们的开发效率；
* 跨平台： 虚拟 DOM 本质上是 JavaScript 对象,而 DOM 与平台强相关，相比之下虚拟 DOM 可以进行更方便地跨平台操作，例如服务器渲染、weex 开发等等

**缺点：**

无法进行极致优化： 虽然虚拟 DOM + 合理的优化，足以应对绝大部分应用的性能需求，但在一些性能要求极高的应用中虚拟 DOM 无法进行针对性的极致优化:比如动画等等

## 1.8 虚拟dom实现原理？

**虚拟 DOM 的实现原理主要包括以下 3 部分：**

* 用 JavaScript 对象模拟真实 DOM 树，对真实 DOM 进行抽象；
* diff 算法 — 比较两棵虚拟 DOM 树的差异；
* pach 算法 — 将两个虚拟 DOM 对象的差异应用到真正的 DOM 树

## 1.9 Vue 是如何实现数据双向绑定的？

Vue 数据双向绑定主要是指：数据变化更新视图

* 输入框内容变化时，Data 中的数据同步变化。即 View => Data 的变化。
* Data 中的数据变化时，文本节点的内容同步变化。即 Data => View 的变化

Vue 主要通过以下 4 个步骤来实现数据双向绑定的：

* 实现一个监听器 Observer：对数据对象进行遍历，包括子属性对象的属性，利用 Object.defineProperty() 对属性都加上 setter 和 getter。这样的话，给这个对象的某个值赋值，就会触发 setter，那么就能监听到了数据变化
* 实现一个解析器 Compile：解析 Vue 模板指令，将模板中的变量都替换成数据，然后初始化渲染页面视图，并将每个指令对应的节点绑定更新函数，添加监听数据的订阅者，一旦数据有变动，收到通知，调用更新函数进行数据更新
* 实现一个订阅者 Watcher：Watcher 订阅者是 Observer 和 Compile 之间通信的桥梁 ，主要的任务是订阅 Observer 中的属性值变化的消息，当收到属性值变化的消息时，触发解析器 Compile 中对应的更新函
* 实现一个订阅器 Dep：订阅器采用 发布-订阅 设计模式，用来收集订阅者 Watcher，对监听器 Observer 和 订阅者 Watcher 进行统一管理

## 1.20 Vue-router 有哪几种路由守卫?

1. 全局守卫：beforeEach
2. 后置守卫：afterEach
3. 全局解析守卫：beforeResolve
4. 路由独享守卫：beforeEnter

## 1.21 Vue-router 的钩子函数都有哪些?

关于 vue-router 中的钩子函数主要分为 3 类

* 全局钩子函数要beforeEach 函数有三个参数,分别是&#x20;

1. to\:router 即将进入的路由对象&#x20;
2. from:当前导航即将离开的路由
3. next\:function,进行管道中的一个钩子，如果执行完了,则导航的状态就是 confirmed （确认的）否则为 false,终止导航

* 单独路由独享组件
  beforeEnter
* 组件内钩子&#x20;

  1. beforeRouterEnter&#x20;
  2. beforeRouterUpdate&#x20;
  3. beforeRouterLeave

## 1.22 vue-router 路由模式有几种？

vue-router 有 3 种路由模式：hash、history、abstract

* hash: 使用 URL hash 值来作路由。支持所有浏览器，包括不支持 HTML5 History Api 的浏览器；
* history : 依赖 HTML5 History API 和服务器配置。具体可以查看 HTML5 History 模式；
* abstract : 支持所有 JavaScript 运行环境，如 Node.js 服务器端。如果发现没有浏览器的 API，路由会自动强制进入这个模式.

## 1.23 说下 vue-router 中常用的 hash 和 history 路由模式实现原理吗？

**（1）hash 模式的实现原理**

* URL 中 hash 值只是客户端的一种状态，也就是说当向服务器端发出请求时，hash 部分不会被发送；
* hash 值的改变，都会在浏览器的访问历史中增加一个记录。因此我们能通过浏览器的回退、前进按钮控制hash 的切换；
* 可以通过 a 标签，并设置 href 属性，当用户点击这个标签后，URL 的 hash 值会发生改变；或者使用 JavaScript 来对 loaction.hash 进行赋值，改变 URL 的 hash 值；
* 我们可以使用 hashchange 事件来监听 hash 值的变化，从而对页面进行跳转（渲染）

**（2）history 模式的实现原理**

* pushState 和 repalceState 两个 API 来操作实现 URL 的变化 ；
* 我们可以使用 popstate 事件来监听 url 的变化，从而对页面进行跳转（渲染）；
* history.pushState() 或 history.replaceState() 不会触发 popstate 事件，这时我们需要手动触发页面跳转（渲染）

## 1.24 vuex 包括几个模块

Vuex 是一个专为 Vue.js 应用程序开发的状态管理模式。每一个 Vuex 应用的核心就是 store（仓库）。“store” 基本上就是一个容器，它包含着你的应用中大部分的状态 ( state )。

（1）Vuex 的状态存储是响应式的。当 Vue 组件从 store 中读取状态的时候，若 store 中的状态发生变化，那么相应的组件也会相应地得到高效更新。

（2）改变 store 中的状态的唯一途径就是显式地提交 (commit) mutation。这样使得我们可以方便地跟踪每一个状态的变化。

* State：定义了应用状态的数据结构，可以在这里设置默认的初始状态。
* Getter：允许组件从 Store 中获取数据，mapGetters 辅助函数仅仅是将 store 中的 getter 映射到局部计算属性。
* Mutation：是唯一更改 store 中状态的方法，且必须是同步函数。
* Action：用于提交 mutation，而不是直接变更状态，可以包含任意异步操作。
* Module：允许将单一的 Store 拆分为多个 store 且同时保存在单一的状态树中

## 1.25 Object.defineProperty 和 Proxy 的区别

Object.defineProperty 和 Proxy 的区别如下:

1. Proxy 可以直接监听对象而非属性；&#x20;
2. Proxy 可以直接监听数组的变化；
3. Proxy 有多达 13 种拦截方法,不限于 apply、ownKeys、deleteProperty、has 等等 是 Object.defineProperty 不具备的&#x20;
4. Proxy 返回的是一个新对象,我们可以只操作新的对象达到目的,而 Object.defineProperty 只能遍历对象属性直接修改
5. Proxy 作为新标准将受到浏览器厂商重点持续的性能优化，也就是传说中的新标准 的性能红利&#x20;
6. Object.defineProperty 兼容性好，支持 IE9，而 Proxy 的存在浏览器兼容性问题, 而且无法用 polyfill 磨平，因此 Vue 的作者才声明需要等到下个大版本( 3.0 )才能用 Proxy 重 写

## 1.26 MVVM 和 MVC 区别是什么？哪些场景适合？

**1、基本定义**&#x20;

MVVM 即 Model-View-ViewModel 的简写，即模型-视图-视图模型，模型（Model） 指的是后端传递的数据，视图(View)指的是所看到的页面，视图模型(ViewModel)是 mvvm 模式 的核心，它是连接 view 和 model 的桥梁。它有两个方向：&#x20;

1. 一是将模型（Model）转化成视图(View)，即将后端传递的数据转化成所看到 的页面，实现的方式是：数据绑定
2. 二是将视图(View)转化成模型(Model)，即将所看到的页面转化成后端的数据。 实现的方式是：DOM 事件监听，这两个方向都实现的，我们称之为数据的双向绑定
3. MVC 基本定义 MVC 是 Model-View- Controller 的简写。即模型-视图-控制器。M 和 V 指的意思和 MVVM 中的 M 和 V 意思一样。C 即 Controller 指的是页面业务逻辑，使用 MVC 的目的就是将 M 和 V 的代码分离。MVC 是单向通信。也就是 View 跟 Model，必须通过 Controller 来承上启 下&#x20;

**2、使用场景**

&#x20;主要就是 MVC 中 Controller 演变成 MVVM 中的 viewModel，MVVM 主要解决了 MVC中大量的 DOM 操作使页面渲染性能降低，加载速度变慢，影响用户体验，vue 数据驱动，通 过数据来显示视图层而不是节点操作， 场景：数据操作比较多的场景，需要大量操作 DOM 元 素时，采用 MVVM 的开发方式，会更加便捷，让开发者更多的精力放在数据的变化上，解放繁 琐的操作 DOM 元素

**3、两者之间的区别**

&#x20;MVC 和 MVVM 其实区别并不大，都是一种设计思想， MVC 和 MVVM 的区别并不是VM 完全取代了 C，只是在 MVC 的基础上增加了一层 VM，只不过是弱化了 C 的概念， ViewModel 存在目的在于抽离 Controller 中展示的业务逻辑，而不是替代 Controller，其它视图 操作业务等还是应该放在 Controller 中实现，也就是说 MVVM 实现的是业务逻辑组件的重用， 使开发更高效，结构更清晰，增加代码的复用性

## 1.27 vue 中如何重置 data?

要初始化 data 中的数据，可以使用 Object.assign()方法，实现重置 data 中的数据，以下就是对该方法的详细介绍，以及如何使用该方法，重置 data 中的数据

1. Object.assign()方法基本定义&#x20;
2. Object.assign() 方法用于将所有可枚举属性的值从一个或多个源对象复制到目 标对象。它将返回目标对象。
3. 用法： Object.assign(target, …sources)，第一个参数是目标对象，第二个参数 是源对象，就是将源对象属性复制到目标对象，返回目标对象

## 1.28 vue3 新特性有哪些？

1、性能提升

* 响应式性能提升，由原来的 Object.defineProperty 改为基于ES6的 Proxy ，使其速度更快，消除警告。
* 重写了 Vdom ，突破了 Vdom 的性能瓶颈。
* 进行模板编译优化。
* 更加高效的组件初始化

2、更好的支持 typeScript

* 有更好的类型推断，使得 Vue3 把 typeScript 支持得非常好

3、新增Composition API

* Composition API 是 vue3 新增的功能，比 mixin 更强大。它可以把各个功能模块独立开来，提高代码逻辑的可复用性，同时代码压缩性更强

4、新增组件

* Fragment 不再限制 template 只有一个根几点。
* Teleport 传送门，允许我们将控制的内容传送到任意的 DOM 中。
* Supense 等待异步组件时渲染一些额外的内容，让应用有更好的用户体验。

5、Tree-shaking：支持摇树优化

* 摇树优化后会将不需要的模块修剪掉，真正需要的模块打到包内。优化后的项目体积只有原来的一半，加载速度更快

6、Custom Renderer API： 自定义渲染器

* 实现 DOM 的方式进行 WebGL 编程

## 1.29 vue3 组合式API生命周期钩子函数有变化吗?

setup 是围绕 beforeCreate 和 created 生命周期钩子运行的，所以不需要显示的定义它们。其他的钩子都可以编写到 setup 内

## 1.30 watch 和 watchEffect 的区别？

watch 和 watchEffect 都是监听器，watchEffect 是一个副作用函数。它们之间的区别有：

1. watch 需要传入监听的数据源，而 watchEffect 可以自动手机数据源作为依赖。
2. watch 可以访问倒改变之前和之后的值，watchEffect 只能获取改变后的值。
3. watch 运行的时候不会立即执行，值改变后才会执行，而 watchEffect 运行后可立即执行。这一点可以通过 watch 的配置项 immediate 改变。

## 1.31 vue中v-if和v-for优先级在vue2和vue3中的区别

实践中不管是vue2或者vue3都不应该把v-if和v-for放在一起使用。

* 在 vue 2.x 中，在一个元素上同时使用 v-if 和 v-for 时， v-for 会优先作用。
* 在 vue 3.x 中， v-if 总是优先于 v-for 生效。
* vue2中v-for的优先级是高于v-if的，放在一起，会先执行循环在判断条件，并且如果值渲染列表中一小部分元素，也得再每次重渲染的时候遍历整个列表，比较浪费资源。
* vue3中v-if的优先级是高于v-for的，所以v-if执行时，它调用相应的变量如果不存在，就会导致异常

## 1.32 script setup 是干啥的？

scrtpt setup 是 vue3 的语法糖，简化了组合式 API 的写法，并且运行性能更好。使用 script setup 语法糖的特点：

* 属性和方法无需返回，可以直接使用。
* 引入组件的时候，会自动注册，无需通过 components 手动注册。
* 使用 defineProps 接收父组件传递的值。
* useAttrs 获取属性，useSlots 获取插槽，defineEmits 获取自定义事件。
* 默认不会对外暴露任何属性，如果有需要可使用 defineExpose 。

## 1.33 vue常用的修饰符

* .stop：等同于 JavaScript 中的 event.stopPropagation() ，防止事件冒泡；
* .prevent ：等同于 JavaScript 中的 event.preventDefault() ，防止执行预设的行为（如果事件可取消，则取消该事件，而不停止事件的进一步传播）；作用是阻止默认事件（例如a标签的跳转
* .capture ：与事件冒泡的方向相反，事件捕获由外到内；
* .self ：只会触发自己范围内的事件，不包含子元素；
* .once ：只会触发一次。
* .trim修饰符的作用是把v-model绑定的值的首尾空格给去掉。在实际开发中我们一般用于搜索框的内容修饰，过滤掉用户多输入前后空格导致内容查不出来的情况。
* .left，.right，.middle这三个修饰符是鼠标的左中右按键触发的事件.

## 1.34 vue2.0 和 vue3.0 有什么区别？ 双向绑定更新

vue2 的双向数据绑定是利⽤ES5 的⼀个 API ，Object.defineProperty()对数据进⾏劫持 结合 发布订阅模式的⽅式来实现的。

vue3 中使⽤了 ES6 的 ProxyAPI 对数据代理，通过 reactive() 函数给每⼀个对象都包⼀层 Proxy，通过 Proxy 监听属性的变化，从⽽ 实现对数据的监控。

这⾥是相⽐于vue2版本，使⽤proxy的优势如下

1. defineProperty只能监听某个属性，不能对全对象监听 可以省去for in、闭包等内容来提升效率（直接绑定整个对象即可）

2. 监听数组，不⽤再去单独的对数组做特异性操作,通过Proxy可以直接拦截所有对象类型数据的操作，完美⽀持对数组的监听。

**获取props**

vue2在script代码块可以直接获取props，vue3通过setup指令传递

**API不同**

Vue2使⽤的是选项类型API（Options API），Vue3使⽤的是合成型API（Composition API）

**建立数据data**

vue2是把数据放入data中，vue3就需要使用一个新的setup()方法，此方法在组件初始化构造得时候触发。

**生命周期不同**

| vue2          | vue3                                           |
| ------------- | ---------------------------------------------- |
| beforeCreate  | setup() 开始创建组件之前，创建的是data和method |
| created       | setup()                                        |
| beforeMount   | onBeforeMount 组件挂载到节点上之前执行的函数   |
| mounted       | onMounted 组件挂载完成后执行的函数             |
| beforeUpdate  | onBeforeUpdate 组件更新之前执行的函数          |
| updated       | onUpdated 组件更新完成之后执行的函数           |
| beforeDestroy | onBeforeUnmount 组件挂载到节点上之前执行的函数 |
| destroyed     | onUnmounted 组件卸载之前执行的函数             |
| activated     | onActivated 组件卸载完成后执行的函数           |
| deactivated   | onDeactivated                                  |

**关于v-if和v-for的优先级:**

vue2 在一个元素上同时使用 v-if 和 v-for  v-for会优先执行

vue3 v-if 总会优先于  v-for生效

**vue2和vue3的diff算法**

**vue2**

vue2 diff算法就是进行虚拟节点对比，并返回一个patch对象，用来存储两个节点 不同的地方，最后用patch记录的消息去局部更新Dom。

vue2 diff算法会比较每一个vnode,而对于一些不参与更新的元素，进行比较是有 点消耗性能的。

**vue3**

vue3 diff算法在初始化的时候会给每个虚拟节点添加一个patchFlags，patchFlags 就是优化的标识。

只会比较patchFlags发生变化的vnode,进行更新视图，对于没有变化的元素做静 态标记，在渲染的时候直接复用。

## 1.35 reactive与ref的区别？

Vue3 中的 ref 和 reactive 是 Vue3 中用于数据管理的两种不同的响应式 API。

ref 用于创建一个包装简单值的响应式引用，例如一个数字、字符串或对象。当 ref 创建一个响应式引用时，它返回一个对象，该对象具有一个 value 属性，该属性指向实际值。当 ref 返回的对象中的 value 属性更改时，组件将自动重新渲染。

reactive 用于创建一个响应式对象，该对象可以包含多个属性和嵌套属性。当使用 reactive 创建响应式对象时，返回的对象是一个代理对象，该对象具有与原始对象相同的属性，并且任何对代理对象属性的更改都将触发组件的重新渲染。

## 1.36 \$route 和 \$router 的区别？

\$route 是“路由信息对象”，包括 path，params，hash，query，fullPath，matched，name 等路由信息参数

\$router 是“路由实例”想要导航到不同URL 对象包括了路由的跳转方法，钩子函数等。

## 1.37 v-on可以监听多个方法吗？

可以一个元素绑定多个事件的两种写法，一个事件绑定多个函数的两种写法，修饰符的使用。

`<a>`doSomething `</a>`

在method方法里面分别写两个事件；

\<button @click="a(),b()">点我ab\</button>

## 1.38 v-model的使用？

v-model实现双向绑定的语法糖，常用于表单与组件之间的数据双向绑定.

V-model的原理：

* v-bind绑定一个value属性

* v-on指令给当前元素绑定input事件

可看出v-model绑定在表单上时，v-model其实就是v-bind绑定value和v-on监听input事件的结合体

组件上的双向绑定（原理）

v-model绑定在组件上的时候做了以下步骤

* 在父组件内给子组件标签添加 v-model ，其实就是给子组件绑定了 value 属性
* 子组件内使用 prop 创建 创建 value 属性可以拿到父组件传递下来的值，名字必须是 value。
* 子组件内部更改 value 的时候，必须通过 $emit 派发一个 input 事件，并携最新的值
* v-model 会自动监听 input 事件，把接收到的最新的值同步赋值到 v-model 绑定的变量上

## 1.39 vue遇到的坑，如何解决的？

* 用webpack打包后访问index.html出现资源加载404问题，解决：开发环境的static文件夹是基于根目录的，所以直接用‘/’ 。
* vue中，假如，你引入某个样式，然后这个样式里面有引用到图片，如果你的文件中没有这个图片，这时候，即使你没有引用这个图片对应的类名，但是只要你有引入这个css文件，他找不到相应路径图片也会报错！！！
* 用for循环出来的列表，在设置列表中的元素的动态属性时，需要加bind属性“：”，不然动态属性设置不出来
* 在vue中的html中的img中的src不可以直接设置为变量，在data里面直接引路径，只能通过import的形式引入,值得注意的是，引用这个方式的时候src是变量需要加“：”，不然会报错！！！！！
* 在中使用v-for="(item ,index) in list"进行循环时，需要注意加：\:key=“index”,不然会出现警告！
* 父组件ajax异步更新数据，子组件props获取不到

应用场景

当父组件  axjos  获取数据，子组件使用  props  接收数据时，执行  mounted  的时候  axjos  还没有返回数据，而且  mounted 只执行一次，这时   props  中接收的数据为空

解决方案：在对应组件中判断数据的长度

## 1.40 说说vue中的diff算法？

diff算法 当data发生改变 会根据新的数据生成一个新的虚拟dom ，新的虚拟dom和旧的虚拟dom进行对比，这个对比的过程就是diff算法。

Vue2 是全量 Diff（当数据发生变化，它就会新生成一个DOM树，并和之前的DOM树进行比较，找到不同的节点然后更新。）；Vue3 是静态标记 + 非全量 Diff（Vue 3在创建虚拟DOM树的时候，会根据DOM中的内容会不会发生变化，添加一个静态标记。之后在与上次虚拟节点进行对比的时候，就只会对比这些带有静态标记的节点。）

使用最长递增子序列优化对比流程，可以最大程度的减少 DOM 的移动，达到最少的 DOM 操作

## 1.41 vue中怎么设置全局变量和全局组件？

在main.js中

app.config.globalProperties.\$key = '' //定义全局变量

import {getCurrentInstance} from 'vue';

  setup(){

    const { proxy } = getCurrentInstance();

    console.log(proxy.\$key);

  }

## 1.45 vue中给对象添加新属性时，界面不刷新怎么办?

vue2的响应式原理使用的是对象代理去实现的,对象代理中有一个get和set方法,当我们访问对象的时候就会触发get方法,当我们对对象中的值进行修改时会触发set方法。但是当我们给对象添加一个新的属性时对象代理是检测不到的,所以就会出现直接给对象添加属性响应式不生效的问题。

所以在vue中可以使用this.\$set(对象名,‘属性名’,属性值)的方法去给对象添加属性,或者使用Vue.set(对象名,‘属性名’,属性值)的方法进行添加,添加之后的属性就带有响应式了

## 1.46 vuex中的辅助函数怎么使用？

vuex的辅助函数有4个

* mapState 函数返回的是一个对象。通常，我们需要使用一个工具函数将多个对象合并为一个，以使我们可以将最终对象传给 computed 属性。
* mapGetters 辅助函数仅仅是将 store 中的 getter 映射到局部计算属性，因此你可以这样来使用他
* mapMutations 辅助函数将组件中的 methods 映射为 store.commit，其原理就是将this.montify 映射为this.\$store.commit(‘montify’)
* mapActions在组件中使用 this.\$store.dispatch('prodect') 分发 action，或者使用 mapActions 辅助函数将组件的 methods 映射为 store.dispatch 调用

## 1.47 刷新浏览器后，Vuex的数据是否存在？如何解决？

原因：因为 store 里的数据是保存在运行内存中的，当页面刷新时，页面会重新加载vue实例，store里面的数据就会被重新赋值初始化。

localStorage 或者就是sessionStorage

下载持久化存储插件。比如使用：vuex-along 的实质也是将 vuex 中的数据存放到 localStorage 或者 sessionStroage 中，只不过这个存取过程组件会帮我们完成，我们只需要用vuex的读取数据方式操作就可以了

## &#x20;1.48 vue路由跳转传参的方式有哪些？

**params传参(显示参数)**

* 在url中会显示出传参的值，刷新页面不会失去拿到的参数，使用该方式传值的时候，需要子路由提前配置好参数

**params传参(不显示参数)**

* 在url中不会显示出传参的值，但刷新页面会失去拿到的参数，使用该方式 传值 的时候，需要子路由提前配置好name参数

**query 传参**

* query 传过去的参数会拼接在地址栏中（?name=xx），刷新页面数据不会丢失，使用path和name都可以

**VUE几种路由跳转几种方式的区别**

* this.\$router.push：跳转到指定url路径，并想history栈中添加一个记录，点击后退会返回到上一个页面
* this.\$router.replace：跳转到指定url路径，但是history栈中不会有记录，点击返回会跳转到上上个页面 (就是直接替换了当前页面)
* this.\$router.go(n)：向前或者向后跳转n个页面，n可为正整数或负整数

## 1.50 单页面应用和多页面应用区别及优缺点？

**单页面**：顾名思义，只有一个页面。一般是一个主页和多个路由页面组成。

优点：

* 公共资源不重新加载，局部加载，服务器压力小
* 切换速度快，用户体验好
* 前后端分离

缺点：

* 不利于SEO（可以优化：比如路由懒加载等）
* 初次加载时耗时多
* 开发难度较大（相对多页面）

**多页面**（Multi Page Application——MPA）：有多个HTML页面，跳转的时候是从一个html页面跳到另一个页面。

优点：

* 利于SEO。
* 更容易扩展。
* 更易数据分析。

缺点：

* 开发成本高。
* 服务器压力大。
* 用户体验相对较差。

## 1.51 EventBus注册在全局上时，路由切换时会重复触发事件，如何解决呢？

* 添加Bus.\$off来关闭

  beforeDestroy () {

  bus.\$off('get', this.myhandle)

  }
* 如果想要用bus 来进行页面组件之间的数据传递，需要注意亮点，组件emit事件应在beforeDestory声明周期内。其次，组件B内的\$on记得要销毁。&#x20;

## 1.52 自定义指令详解

为什么需要自定义指令：因为vue是MVVM模式，只需要关注于数据和业务逻辑，不需要关注DOM的操作，但是有时候面对一些特殊的业务需求时，需要进行DOM的操作，这个时候就需要进行自定义指令。

自定义局部指令:在options api选项中的directives中设置。局部自定义指令是一个对象，对象的属性是自定义指令的名称，对象中属性的值是自定义指令的钩子函数对象

自定义全局指令:在app的directive方法。参数一（name）：自定义指令的名称。参数二（hooks）：自定义指令的钩子函数对象

## 1.53 slot是什么？有什么作用？原理是什么？

slot又名插槽，是Vue的内容分发机制，组件内部的模板引擎使用slot元素作为承载分发内容的出口。插槽slot是子组件的一个模板标签元素，而这一个标签元素是否显示，以及怎么显示是由父组件决定的。

**slot又分三类，默认插槽，具名插槽和作用域插槽。**

* 默认插槽：又名匿名插槽，当slot没有指定name属性值的时候一个默认显示插槽，一个组件内只有有一个匿名插槽。
* 具名插槽：带有具体名字的插槽，也就是带有name属性的slot，一个组件可以出现多个具名插槽。
* 作用域插槽：默认插槽、具名插槽的一个变体，可以是匿名插槽，也可以是具名插槽，该插槽的不同点是在子组件渲染作用域插槽时，可以将子组件内部的数据传递给父组件，让父组件根据子组件的传递过来的数据决定如何渲染该插槽。

**实现原理：**

当子组件vm实例化时，获取到父组件传入的slot标签的内容，存放在vm.\$slot中，默认插槽为vm.\$slot.default具名插槽为vm.\$slot.xxx，xxx 为插槽名

当组件执行渲染函数时候，遇到slot标签，使用slot中的内容进行替换，此时可以为插槽传递数据，若存在数据，则可称该插槽为作用域插槽

## 1.54 \$nextTick的使用

用法：将回调延迟到下次DOM更新循环之后执行。在修改数据之后立即使用它，然后等待DOM更新。它跟全局方法 Vue.nextTick 一样，不同的是回调的 this 自动绑定到调用它的实例上。

**\$nextTick() 的应用场景**

在vue的生命周期 created() 钩子函数中进行 dom 操作，一定要放在 \$nextTick() 函数中执行。在 created() 钩子函数执行的时候 DOM 其实并未进行任何渲染，而此时进行 DOM 操作无异于徒劳，所以此处一定要将 DOM 操作的代码放进 nextTick() 的回调函数中。

mounted() 钩子函数，因为该钩子函数执行时，所有的 DOM 挂载和 渲染都已完成，此时在该钩子函数中进行任何 DOM 操作都不会有问题

在数据变化后要执行某个操作，而这个操作需要随数据改变而改变DOM结构时，这个操作都是需要放置 \$nextTick() 的回调函数中。

# React

## 1.1 虚拟dom和真实dom

**什么是虚拟dom？**

虚拟 dom 相当于在 js 和真实 dom 中间加了一个缓存，利用 dom diff 算法避免了没有必要的 dom操作，从而 提高性能。

1. 用 JavaScript 对象结构表示 DOM 树的结构
2. 用这个树构建一个真正的 DOM 树，插到文档当中当状态变更的时候，重新构造一棵新的对象树。
3. 用新的树和旧的树进行比较，记录两棵树差异把 2 所记录的差异应用到步骤 1 所构建的真正的DOM 树上，视图就更新了。

**虚拟dom和real dom区别 性能差异**

减少DOM的操作：虚拟dom可以将多次操作合并为一次操作，减少DOM操作的次数

| **Real DOM**              | **Virtual DOM**          |
| ------------------------- | ------------------------ |
| 更新缓慢                  | 更新更快                 |
| 可以直接更新 HTML         | 无法直接更新 HTML        |
| 如果元素更新，则创建新DOM | 如果元素更新，则更新 JSX |
| DOM操作代价很高           | DOM 操作非常简单         |
| 消耗的内存较多            | 很少的内存消耗           |

## 1.2 **react组件间通信**

* 父组件向子组件通讯: 父组件可以向子组件通过传 props 的方式，向子组件进行通讯

* 子组件向父组件通讯: props+回调的方式,父组件向子组件传递props进行通讯，此props为作用域为父组件自身的函数，子组件调用该函数，将子组件想要传递的信息，作为参数，传递到父组件的作用域中

* 兄弟组件通信: 找到这两个兄弟节点共同的父节点,结合上面两种方式由父节点转发信息进行通信
* 跨层级通信: Context 设计目的是为了共享那些对于一个组件树而言是“全局”的数据，例如当前认证的用户、主题或首选语言
* 发布订阅模式: 发布者发布事件，订阅者监听事件并做出反应,我们可以通过引入event模块进行通信
* 全局状态管理工具: 借助Redux或者Mobx等全局状态管理工具进行通信,这种工具会维护一个全局状态中心Store,并根据不同的事件产生新的状态

## 1.3 **redux的原理**

**Redux**：Redux 是当今最热门的前端开发库之一。它是 JavaScript 程序的可预测状态容器，用于整个应用的状态管理。使用 Redux 开发的应用易于测试，可以在不同环境中运行，并显示一致的行为

**数据流**

1. 首先，用户（通过View）发出Action，发出方式就用到了dispatch方法
2. 然后，Store自动调用Reducer，并且传入两个参数：当前State和收到的Action，Reducer会返回新的State

3. State一旦有变化，Store就会调用监听函数，来更新View

**Redux遵循的三个原则是什么**

1. 单一事实来源：整个应用的状态存储在单个 store 中的对象/状态树里。单一状态树可以更容易地跟踪随时间的变化，并调试或检查应用程序。

2. 状态是只读的：改变状态的唯一方法是去触发一个动作。动作是描述变化的普通 JS 对象。就像state 是数据的最小表示一样，该操作是对数据更改的最小表示。

3. 使用纯函数进行更改：为了指定状态树如何通过操作进行转换，你需要纯函数。纯函数是那些返回值仅取决于其参数值的函数。

**单一事实来源怎么理解？**

Redux 使用 “Store” 将程序的整个状态存储在同一个地方。因此所有组件的状态都存储在 Store 中，并且它们从 Store 本身接收更新。单一状态树可以更容易地跟踪随时间的变化，并调试或检查程序。

**组件组成**

1. **Action** – 这是一个用来描述发生了什么事情的对象
2. **Reducer** – 这是一个确定状态将如何变化的地方
3. **Store** – 整个程序的状态/对象树保存在Store中
4. **View** – 只显示 Store 提供的数据

**如何在** **Redux** **中定义** **Action？**

React 中的 Action 必须具有 type 属性，该属性指示正在执行的 ACTION 的类型。必须将它们定义为字符串常量，并且还可以向其添加更多的属性。在 Redux 中，action 被名为 Action Creators 的函数所创建

**解释** **Reducer** **的作用**

Reducers 是纯函数，它规定应用程序的状态怎样因响应 ACTION 而改变。Reducers 通过接受先前的状态和 action 来工作，然后它返回一个新的状态。它根据操作的类型确定需要执行哪种更新，然后返回新的值。如果不需要完成任务，它会返回原来的状态。

**Store** **在** **Redux** **中的意义是什么？**

Store 是一个 JavaScript 对象，它可以保存程序的状态，并提供一些方法来访问状态、调度操作和注册侦听器。应用程序的整个状态/对象树保存在单一存储中。因此，Redux 非常简单且是可预测的。我们可以将中间件传递到 store 来处理数据，并记录改变存储状态的各种操作。所有操作都通过 reducer 返回一个新状态。

**Redux** **有哪些优点？**

* 结果的可预测性 - 由于总是存在一个真实来源，即 store ，因此不存在如何将当前状态与动作和应用的其他部分同步的问题
* 可维护性 - 代码变得更容易维护，具有可预测的结果和严格的结构
* 服务器端渲染 - 你只需将服务器上创建的 store 传到客户端即可。这对初始渲染非常有用，并且可以优化应用性能，从而提供更好的用户体验
* 开发人员工具 - 从操作到状态更改，开发人员可以实时跟踪应用中发生的所有事情
* 社区和生态系统 - Redux 背后有一个巨大的社区，这使得它更加迷人。一个由才华横溢的人组成的大型社区为库的改进做出了贡献，并开发了各种应用
* 易于测试 - Redux 的代码主要是小巧、纯粹和独立的功能。这使代码可测试且独立
* 组织 - Redux 准确地说明了代码的组织方式，这使得代码在团队使用时更加一致和简单

## 1.4 **React组件生命周期的阶段是什么？**

1. 初始渲染阶段：这是组件即将开始其生命之旅并进入 DOM 的阶段。
2. 更新阶段：一旦组件被添加到 DOM，它只有在 prop 或状态发生变化时才可能更新和重新渲染。这些只发生在这个阶段。

3. 卸载阶段：这是组件生命周期的最后阶段，组件被销毁并从 DOM 中删除。

## 1.5 **详细解释React 组件的生命周期方法**

**挂载阶段:**

* constructor: 构造函数，最先被执行,我们通常在构造函数里初始化state对象或者给自定义方法绑定this

* getDerivedStateFromProps: static getDerivedStateFromProps(nextProps, prevState) ,这是个静态方法,当我们接收到新的属性想去修改我们state，可以使用getDerivedStateFromProps

* render: render函数是纯函数，只返回需要渲染的东西，不应该包含其它的业务逻辑,可以返回原生的DOM、React组件、Fragment、Portals、字符串和数字、Boolean和null等内容

* componentDidMount: 组件装载之后调用，此时我们可以获取到DOM节点并操作，比如对canvas，svg的操作，服务器请求，订阅都可以写在这个里面，但是记得在componentWillUnmount中取消订阅

**更新阶段:**

* getDerivedStateFromProps: 此方法在更新个挂载阶段都可能会调用
* shouldComponentUpdate: shouldComponentUpdate(nextProps, nextState) ,有两个参数nextProps和nextState，表示新的属性和变化之后的state，返回一个布尔值，true表示会触发重新渲染，false表示不会触发重新渲染，默认返回true,我们通常利用此生命周期来优化React程序性能
* render: 更新阶段也会触发此生命周期
* getSnapshotBeforeUpdate: getSnapshotBeforeUpdate(prevProps, prevState) ,这个方法在render之后，componentDidUpdate之前调用，有两个参数prevProps和prevState，表示之前的属性和之前的state，这个函数有一个返回值，会作为第三个参数传给componentDidUpdate，如果你不想要返回值，可以返回null，此生命周期必须与componentDidUpdate搭配使用
* componentDidUpdate: componentDidUpdate(prevProps, prevState, snapshot) ,该方法在getSnapshotBeforeUpdate方法之后被调用，有三个参数prevProps，prevState，snapshot，表示之前的props，之前的state，和snapshot。第三个参数是getSnapshotBeforeUpdate返回的,如果触发某些回调函数时需要用到 DOM 元素的状态，则将对比或计算的过程迁移至getSnapshotBeforeUpdate，然后在 componentDidUpdate 中统一触发回调或更新状态

**卸载阶段:**

* componentWillUnmount: 当我们的组件被卸载或者销毁了就会调用，我们可以在这个函数里去清除一些定时器，取消网络请求，清理无效的DOM元素等垃圾清理工作

**扩展：**

React 16之后有三个生命周期被废弃(但并未删除)

* componentWillMount

* componentWillReceiveProps

* componentWillUpdate

官方计划在17版本完全删除这三个函数，只保留UNSAVE_前缀的三个函数，目的是为了向下兼容，但是对于开发者而言应该尽量避免使用他们，而是使用新增的生命周期函数替代它们

## 1.6 router

1. 什么是React 路由？

React 路由是一个构建在 React 之上的强大的路由库，它有助于向应用程序添加新的屏幕和流。这使 URL 与网页上显示的数据保持同步。它负责维护标准化的结构和行为，并用于开发单页 Web 应用。 React 路由有一个简单的API。

2. 为什么需要 React 中的路由？

Router 用于定义多个路由，当用户定义特定的 URL 时，如果此 URL 与 Router 内定义的任何 “路

由” 的路径匹配，则用户将重定向到该特定路由。所以基本上我们需要在自己的应用中添加一个

Router 库，允许创建多个路由，每个路由都会向我们提供一个独特的视图

3. 为什么React Router v4中使用 switch 关键字 ？

虽然 <div> 用于封装 Router 中的多个路由，当你想要仅显示要在多个定义的路线中呈现的单个路

线时，可以使用 “switch” 关键字。使用时， <switch> 标记会按顺序将已定义的 URL 与已定义的

路由进行匹配。找到第一个匹配项后，它将渲染指定的路径。从而绕过其它路线。

4. 列出 React Router 的优点

​ 4.1 就像 React 基于组件一样，在 React Router v4 中，API 是 'All About Components'。可以将Router 可视化为单个根组件（），其中我们将特定的子路由（）包起来。

​ 4.2 无需手动设置历史值：在 React Router v4 中，我们要做的就是将路由包装在 组件中。

​ 4.3 包是分开的：共有三个包，分别用于 Web、Native 和 Core。这使我们应用更加紧凑。基于类似的编码风格很容易进行切换。

## 1.7 React **的** **refs** 有什么了解？

Refs 是 React 中引用的简写。它是一个有助于存储对特定的 React 元素或组件的引用的属性，它将由组件渲染配置函数返回。用于对 render() 返回的特定元素或组件的引用。当需要进行 DOM 测量或向组件添加方法时，它们会派上用场。

```react
class ReferenceDemo extends React.Component{
    display() {
        const name = this.inputDemo.value;
        document.getElementById('disp').innerHTML = name;
    }
    render() {
        return(
            <div>
            Name: <input type="text" ref={input => this.inputDemo = input} />
            <button name="Click" onClick={this.display}>Click</button>
            <h2>Hello <span id="disp"></span> !!!</h2>
            </div>
        );
    }
}
```

## 1.8 列出一些应该使用 Refs 的情况

React并不是将click事件绑在该div的真实DOM上，而是在document处监听所有支持的事件，当事件发生并冒泡至document处时，React将事件内容封装并交由真正的处理函数运行。这样的方式不仅减少了内存消耗，还能在组件挂载销毁时统一订阅和移除事件。

另外冒泡到 document 上的事件也不是原生浏览器事件，而是 React 自己实现的合成事件（SyntheticEvent）。因此我们如果不想要事件冒泡的话，调用 event.stopPropagation 是无效的，而应该调用event.preventDefault

![image-20230810214434062](C:\Users\admin\AppData\Roaming\Typora\typora-user-images\image-20230810214434062.png)

## 1.9 redux-saga和mobx的比较

1. **状态管理**

* redux-sage 是 redux 的一个异步处理的中间件。

* mobx 是数据管理库，和 redux 一样。

2. **设计思想**

* redux-sage 属于 flux 体系， 函数式编程思想。

* mobx 不属于 flux 体系，面向对象编程和响应式编程。

3. **主要特点**

* redux-sage 因为是中间件，更关注异步处理的，通过 Generator 函数来将异步变为同步，使代码可读性高，结构清晰。action 也不是 action creator 而是 pure action，在 Generator 函数中通过 call 或者 put 方法直接声明式调用，并自带一些方法，如 takeEvery，takeLast，race等，控制多个异步操作，让多个异步更简单。

* mobx 是更简单更方便更灵活的处理数据。 Store 是包含了 state 和 action。state 包装成一个可被观察的对象， action 可以直接修改 state，之后通过 Computed values 将依赖 state 的计算属性更新 ，之后触发 Reactions 响应依赖 state 的变更，输出相应的副作用 ，但不生成新的 state。

4. **数据可变性**

* redux-sage 强调 state 不可变，不能直接操作 state，通过 action 和 reducer 在原来的 state 的基础上返回一个新的 state 达到改变 state 的目的。

* mobx 直接在方法中更改 state，同时所有使用的 state 都发生变化，不生成新的 state。

5. **写法难易度**

* redux-sage 比 redux 在 action 和 reducer 上要简单一些。需要用 dispatch 触发 state 的改变，需要 mapStateToProps 订阅 state。

* mobx 在非严格模式下不用 action 和 reducer，在严格模式下需要在 action 中修改 state，并且自动触发相关依赖的更新。

6. **使用场景**

* redux-sage 很好的解决了 redux 关于异步处理时的复杂度和代码冗余的问题，数据流向比较好追踪。但是 redux 的学习成本比 较高，代码比较冗余，不是特别需要状态管理，最好用别的方式代替。

* mobx 学习成本低，能快速上手，代码比较简洁。但是可能因为代码编写的原因和数据更新时相对黑盒，导致数据流向不利于追踪。

## 1.10 简述一下 **React** 的源码实现

1. React 的实现主要分为 Component 和 Element ；
2. Component 属于 React 实例，在创建实例的过程中会在实例中注册 state 和 props 属性，还会依次调用内置的生命周期函数；

3. Component 中有一个 render 函数， render 函数要求返回一个 Element 对象（或 null ）；
4. Element 对象分为原生 Element 对象和组件式对象，原生 Element + 组件式对象会被一起解析成虚拟 DOM 树，并且内部使用的 state 和 props 也以 AST 的形式注入到这棵虚拟 DOM 树之中；

5. 在渲染虚拟 DOM 树的前后，会触发 React Component 的一些生命周期钩子函数，比如componentWillMount 和 componentDidMount ，在虚拟 DOM 树解析完成后将被渲染成真实DOM 树；

6. 调用 setState 时，会调用更新函数更新 Component 的 state ，并且触发内部的一个updater ，调用 render 生成新的虚拟 DOM 树，利用 diff 算法与旧的虚拟 DOM 树进行比对，比对以后利用最优的方案进行 DOM 节点的更新，这也是 React 单向数据流的原理（与 Vue 的MVVM 不同之处）。

## 1.11 setState到底是异步还是同步

有时表现出异步,有时表现出同步

1. setState 只在合成事件和钩子函数中是“异步”的，在原生事件和 setTimeout 中都是同步的。
2. setState 的异步并不是说内部由异步代码实现，其实本身执行的过程和代码都是同步的，只是合成事件和钩子函数的调用顺序在更新之前，导致在合成事件和钩子函数中没法立马拿到更新后的值，形成了所谓的“异步”，当然可以通过第二个参数 setState(partialState, callback)中的 callback 拿到更新后的结果。

3. setState 的批量更新优化也是建立在“异步”（合成事件、钩子函数）之上的，在原生事件和setTimeout 中不会批量更新，在“异步”中如果对同一个值进行多次 setState ， setState 的批量更新策略会对其进行覆盖，取最后一次的执行，如果是同时 setState 多个不同的值，在更新时会对其进行合并批量更新。

## 1.12  redux异步中间件之间的优劣?

**redux-thunk优点:**

* 体积小: redux-thunk的实现方式很简单,只有不到20行代码

* 使用简单: redux-thunk没有引入像redux-saga或者redux-observable额外的范式,上手简单

**redux-thunk缺陷:**

* 样板代码过多: 与redux本身一样,通常一个请求需要大量的代码,而且很多都是重复性质的

* 耦合严重: 异步操作与redux的action偶合在一起,不方便管理

* 功能孱弱: 有一些实际开发中常用的功能需要自己进行封装

**redux-saga优点:**

* 异步解耦: 异步操作被被转移到单独 saga.js 中，不再是掺杂在 action.js 或 component.js 中

* action摆脱thunk function: dispatch 的参数依然是一个纯粹的 action (FSA)，而不是充满 “黑魔法” thunk function

* 异常处理: 受益于 generator function 的 saga 实现，代码异常/请求失败 都可以直接通过try/catch 语法直接捕获处理

* 功能强大: redux-saga提供了大量的Saga 辅助函数和Effect 创建器供开发者使用,开发者无须封装或者简单封装即可使用

* 灵活: redux-saga可以将多个Saga可以串行/并行组合起来,形成一个非常实用的异步flow
* 易测试，提供了各种case的测试方案，包括mock task，分支覆盖等等

**redux-saga缺陷:**

* 额外的学习成本: redux-saga不仅在使用难以理解的 generator function,而且有数十个API,学习成本远超redux-thunk,最重要的是你的额外学习成本是只服务于这个库的,与redux-observable不同,redux-observable虽然也有额外学习成本但是背后是rxjs和一整套思想
* 体积庞大: 体积略大,代码近2000行，min版25KB左右

* 功能过剩: 实际上并发控制等功能很难用到,但是我们依然需要引入这些代码

* ts支持不友好: yield无法返回TS类型

**redux-observable优点:**

* 功能最强: 由于背靠rxjs这个强大的响应式编程的库,借助rxjs的操作符,你可以几乎做任何你能想到的异步处理

* 背靠rxjs: 由于有rxjs的加持,如果你已经学习了rxjs,redux-observable的学习成本并不高,而且随着

* rxjs的升级redux-observable也会变得更强大

**redux-observable缺陷:**

* 学习成本奇高: 如果你不会rxjs,则需要额外学习两个复杂的库

* 社区一般: redux-observable的下载量只有redux-saga的1/5,社区也不够活跃,在复杂异步流中间件

* 这个层面redux-saga仍处于领导地位

## 1.13 state **和** props 区别是啥？

props和state是普通的 JS 对象。虽然它们都包含影响渲染输出的信息，但是它们在组件方面的功能是不同的。即

* state 是组件自己管理数据，控制自己的状态，可变
* props 是外部传入的数据参数，不可变；
* 没有state的叫做无状态组件，有state的叫做有状态组件；
* 多用 props，少用 state，也就是多写无状态组件。

## 1.14  当调用setState时，React render 是如何工作的？

* 虚拟 DOM 渲染:当render方法被调用时，它返回一个新的组件的虚拟 DOM 结构。当调用setState()时，render会被再次调用，因为默认情况下shouldComponentUpdate总是返回true，所以默认情况下React 是没有优化的。

* 原生 DOM 渲染:React 只会在虚拟DOM中修改真实DOM节点，而且修改的次数非常少——这是很棒的React特性，它优化了真实DOM的变化，使React变得更快。

## 1.15 hooks

### Hooks简介

React的组件创建方式，一种是类组件，一种是纯函数组件

* 纯函数组件没有状态
* 纯函数组件没有生命周期
* 纯函数组件没有this

**使用Hooks的优点：**

* 告别难以理解的Class( this 和 生命周期 的痛点)
* 解决业务逻辑难以拆分的问题
* 使状态逻辑复用变得简单可行
* 函数组件从设计思想上来看更加契合React的理念

**Hooks并非万能**:

* Hooks暂时还不能完全的为函数组件补齐类组件地能力（如生命周期的getSnapshotBeforeUpdate、componentDidCatch方法暂时还未实现）
* 将类组件的复杂变成函数组件的轻量，可能使用者并不能很好地消化这种复杂
* Hooks在使用层面有着严格地规则约束

### Hook函数（9种）

1. useState()：状态钩子
2. useContext()：共享状态钩子
3. useEffect()：副作用钩子
4. useReducer()：Action钩子
5. userRefef()：Ref Hook可以**在函数组件中存储、查找组件内的标签或任意其它数据**
6. useMemo()： 主要**用来解决使用React hooks产生的无用渲染的性能问题**
7. useCallback()： 主要**是为了性能的优化**
8. useLayoutEffect() ：和useEffect相同，**都是用来执行副作用，但是它会在所有的DOM变更之后同步调用effect**。useLayoutEffect和useEffect最大的区别就是一个是同步，一个是异步。
9. useImperativeHandle()： 可以**在使用 ref 时自定义暴露给父组件的实例值。**

### 自定义Hooks

**自定义 Hooks：是一个函数，其名称以 “use” 开头，函数内部可以调用其他的 Hook**

**自定义Hooks：可以封装状态，能够更好的实现状态共享**

# 打包工具

## 1.1 前端为什么要进行打包和构建

1. 体积更小（Tree-Shaking、压缩、合并），加载更快
2. 编译高级语言和语法（TS，ES6+，模块化，scss）
3. 兼容性和错误检查（Polyfill、postcss、eslint)
4. 统一、高效的开发环境
5. 统一的构建流程和产出标准
6. 集成公司构建规范（提测、上线等）

## 1.2 如何提高webpack的构建速度

1. 优化babel-loader 开启缓存
2. 使用module中的Noparse，不去解析属性值代表的库的依赖（需要在webpack.config.js的module节点添加noParse配置，使用|分割）
3. 可以使用webpack内置插件lgnorePlugin插件（作用：忽略第三方包指定目录，让这些指定目录不要被打包进去）
4. 使用happyPack多进程打包（需要下载）
5. 使用parallelUgligyPlugin多进程压缩js（默认使用uglifyJs来压缩代码，单进程）

## 1.3 代码分割的本质是什么？

1. 代码分割的本质就是在源代码直接上线和达成唯一脚本main.bundle.js这两种极端方案之间的一种更适合实际场景的中间状态。
2. 源码直接上线：虽然过程可控，但是http请求多，性能开销大。
3. 打包成唯一脚本：服务器压力小，但是页面空白期长，用户体验不好。

## 1.4webpack的基本功能有哪些？

| 名称     | 内容                                                                   |
| :------- | :--------------------------------------------------------------------- |
| 代码转换 | typescript编译成JavaScript、scss编辑成css                              |
| 文件优化 | 压缩JavaScript、css、html、压缩合并图片                                |
| 代码分割 | 提取多个页面的公共代码、提取首屏不需要执行部分的代码让其异步加载       |
| 模块合并 | 采用模块化的项目有很多模块和文件，需要构建功能把模块分类合并成一个文件 |
| 自动刷新 | 监听本地源代码的变化，自动构建，刷新浏览器                             |
| 代码校验 | 在代码被提交到仓库前需要检测代码是否符合规范，以及单元测试是否通过     |
| 自动发布 | 更新完代码后，自动构建出线上发布代码并传输给发布系统                   |

## 1.5 文件指纹是什么？

 文件指纹是打包之后的文件后缀名。

        chunkhash：和webpack打包的chunk有关，不同的entry会生出不同的chunkhash。

                js后缀名：filename:'\[name]\[chunkhash:8].js',

        contenthash：根据文件内容来定义hash，文件内容不变，则其不变。

                css后缀名：filename:'\[name]\[contenthash:8].css',

        hash：和整个项目构建有关，只要项目文件有修改，整个构建的hash值就会修改。

                img后缀名：name:'\[name]\[hash:8].\[ext]'

## &#x20;1.6 为什么说vite比webpack更快？

1. webpack会先打包，然后启动开发服务器，请求服务器时直接给予打包结果。
2. vite是直接启动开发服务器，请求哪个模块再对该模块进行实时编译。
3. vite在启动的时候不需要打包，意味着不需要分析模块的依赖、不需要编译，因此启动速度非常快。
4. &#x20;当浏览器请求某个模块时，再根据需要对模块内容进行编译。这种按需动态编译的方式，极大的缩减了编译时间，项目越复杂、模块越多，vite的优势越明显。
5. &#x20;在HMR方面，当改动了一个模块后，仅需让浏览器重新请求该模块即可，不像webpack那样需要把该模块的相关依赖模块全部编译一次，效率更高。
6. &#x20;当需要打包到生产环境时，vite使用传统的rollup进行打包，因此，vite的主要优势在开发阶段。另外，由于vite利用的是ES Module，因此在代码中不可以使用CommonJS&#x20;

## 1.7 vite工作原理

vite是一种现代化的前端开发工具，其工作原理主要分为以下几个步骤

1. 基于ESM构建：Vite作为一款基于ESM的前端构建工具，通过ES模块提供的动态导入功能来实现快速的开发和构建。
2. 零配置开发：Vite允许开发者在不需要任何配置的情况下启动一个服务器进行开发，通过对文件的即时编译和缓存，来提高开发效率。
3. 基于浏览器原生的ESM加载：Vite将所有文件视为ES模块，并且在开发时会直接从源代码加载模块，而不是打包后的文件，从而可以避免打包的过程带来的性能损失。
4. 按需编译和缓存：Vite会按需编译和缓存依赖项，只有当需要更新时才会进行重新编译，缓存让开发者可以忽略无关的代码变化。
5. 插件化架构：Vite的插件化架构可以方便地扩展其功能，例如使用插件来处理CSS、处理图片、压缩源代码等等。

## &#x20;1.8 vite核心原理

* Vite其核心原理是利用浏览器现在已经支持ES6的import，碰见import就会发送一个HTTP请求去加载文件。
* Vite整个过程中没有对文件进行打包编译，做到了真正的按需加载，所以其运行速度比原始的webpack开发编译速度快出许多！

**特点：**

1. 快速的冷启动：基于Esbuild的依赖进行预编译优化 （Esbuild 打包速度太快了，比类似的工具快10\~100倍 ）
2. 增加缓存策略：源码模块使用协商缓存，依赖模块使用强缓；因此一旦被缓存它们将不需要再次请求
3. &#x20;HMR（热更新）：当修改代码时，HMR 能够在不刷新页面的情况下，把页面中发生变化的模块，替换成新的模块，同时不影响其他模块的正常运作
4. &#x20;基于 Rollup 打包：生产环境下由于esbuild对css和代码分割并使用Rollup进行打包
5. 高效的热更新：基于ESM实现，同时利用HTTP头来加速整个页面的重新加载&#x20;

## 1.9 Vite 冷启动为什么快

vite 运行 Dev 命令后只做了两件事情

1. 启动本地服务器并注册了一些中间件
2. 使用 ESbuild 预构建模块

## 1.10 vite生产环境缺点

1.  Vite 在是直接把转化后的 es module 的JavaScript，扔给浏览器，让浏览器根据依赖关系，自己去加载依赖
2. 那有人就会说了，那放到 生产环境 时，是不是可以不打包，直接在开个 Vite 服务就行，反正浏览器会自己去根据依赖关系去自己加载依赖。答案是不行的，为啥呢：

   1、你代码是放在服务器的，过多的浏览器加载依赖肯定会引起更多的网络请求

   2、为了在生产环境中获得最佳的加载性能，最好还是将代码进行 tree-shaking、懒加载和 chunk 分割、CSS处理，这些优化操作，目前 esbuild 还不怎么完善&#x20;

## &#x20;1.11 vite和webpack优缺点对比

* 更快的启动时间和更新速度
* 更好的开发体验：自动打开浏览器、自动刷新页面 配置简单。
* 不需要过多的配置就可以搭建基本的开发环境 更少的依赖。
* 借助原生的ES模块
* 避免了过多的额外依赖

&#x20;**缺点：**

* vite的构建技术主要用于中小型项目，对于大型项目的支持不如webpack&#x20;
* vite主要是针对vue3的单页面应用，对于多页面应用、ssr应用、自定义流程应用不如webpack&#x20;
* 开发环境首屏加载慢，懒加载慢&#x20;
* vite由于基于原生ES模块，不支持commonJs；webpack关注兼容性，vite关注浏览器端的开发体验，vite的生态还不如webpack
