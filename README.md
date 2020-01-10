## plugs

[![Build Status](https://travis-ci.org/Stevenzwzhai/plugs.svg?branch=master)](https://travis-ci.org/Stevenzwzhai/plugs)

工作中对于框架的依赖越来越少，所以后面经常自己封装一些所需要用到的模块或者插件。我这里只做了实现，至于在项目中如何去封装，还要看具体框架、模块机制来做，所以我这里只作为一个实现方式的参考。

#### 1.数组处理
我们从后端返回的列表数据往往需要进行二次加工，以便于前端更方便的处理和显示，这里我写了几个我经常会用到的一些方法。
<https://github.com/Stevenzwzhai/plugs/tree/master/Array-Deal>

#### 2.数组去重
这个问题其实很久以来就有，搜索的时候可以搜出一堆方法，而其中最受欢迎的就是hash去重，但是它还是有一些缺陷，我前几天写过一篇相关文章：[数组去重完整版](http://www.jianshu.com/p/e13be5d9b8f4),经常逛掘金的同学应该看过。代码地址<https://github.com/Stevenzwzhai/plugs/tree/master/Array-Removal>

#### 3.数据绑定
最近几年，双向数据非常火，一开始是angular，之后vue也做了实现，不过二者实现方式不同，前者使用脏检查，后者使用Object.defineProperty()，这里我简单地做了实现<https://github.com/Stevenzwzhai/plugs/tree/master/data-bind>

#### 4.模态框
用过bootstrap的同学都应该经常会用到模态框，最然bootstrap被广大前端er所排斥，但不可否认，它做的很多控件还是很好用的，最近工作项目中会有弹窗，所以我简单地做了一个弹窗动画，模拟bootstrap的模态框，当然动画是很简单，可是最终让它正常运行就没那么简单了，我之前也写过文章[js实现类bootstrap模态框动画](http://www.jianshu.com/p/e1f8af3f5316),代码地址<https://github.com/Stevenzwzhai/plugs/tree/master/dialog>

#### 5.移动端拖拽
大家都懂，地址(demo1.html)<https://github.com/Stevenzwzhai/plugs/tree/master/drag>
pc拖拽，鼠标快速移动也可正常拖动，地址(demo2.html)<https://github.com/Stevenzwzhai/plugs/tree/master/drag>

#### 6.元素显示隐藏
用过angular或者vue的同学都了解，在可以用指令来控制元素在渲染后的显示隐藏，很方便，不用我们在额外的操作dom元素，但是对于所用框架没有这个功能的同学就有点不爽了，所以我这里做了个原生的实现，可以根据指令来控制元素的显示隐藏，当然，指令你可以更换成你自己想要的。<https://github.com/Stevenzwzhai/plugs/tree/master/element-show>

#### 7.事件触发器
事件触发器是一个框架的基本组成，这里我做了一个简单地事件触发模块，支持事件绑定、触发、解绑，以及单次绑定事件。<https://github.com/Stevenzwzhai/plugs/tree/master/emitter>

#### 8.模板引擎
我们在渲染的时候经常会用到各种模板引擎，template、artTemplate，或者angular、vue中的，我用es6的$()和new Function，做了个简单地模板渲染，包括简单内容渲染和列表渲染，并把之前的元素显示隐藏加了进去<https://github.com/Stevenzwzhai/plugs/tree/master/es6-template>

#### 9.模糊查询
模糊查询一般都会去请求后端接口，但是当数据量不多，而且是一次返回全部数据的情况，前端去做模糊查询是最佳选择，之前写过一篇文章有介绍:[js前端实现模糊查询](http://www.cnblogs.com/Upton/p/5999179.html),代码地址<https://github.com/Stevenzwzhai/plugs/tree/master/fuzzySearch>

#### 10.获取元素最终背景色
前一段时间一篇面试文章很火，我也做了其中一个题的实现，还写了博客[一月前端面试--获取元素最终背景色](http://www.jianshu.com/p/e09c67c3bd98),代码地址<https://github.com/Stevenzwzhai/plugs/tree/master/get-background-color>

#### 11.函数链式调用
对于函数链式调用最熟悉的就是jquery了，这里我用es5和es6分别做了链式调用的实现。[用原生js实现的链式调用函数](http://www.cnblogs.com/Upton/p/5951739.html)，代码地址<https://github.com/Stevenzwzhai/plugs/tree/master/js-chaincall>

#### 12.解析url
这个可能用的不多，但是偶尔会用到，解析出url的各个组成部分，并返回一个对象。<https://github.com/Stevenzwzhai/plugs/tree/master/parseQueryString>

#### 13.获取编辑区光标的位置
当你需要自定义选择编辑区的内容时会用到，用来获取光标位置，兼容性不用担心滴。<https://github.com/Stevenzwzhai/plugs/tree/master/selection-%E5%8F%AF%E7%BC%96%E8%BE%91%E5%8C%BA%E5%85%89%E6%A0%87%E4%BD%8D%E7%BD%AE>

#### 14.关于一道面试题
       // 写一个 function 让下面两行代码输出的结果都为 5
      console.log(sum(2, 3));
      console.log(sum(2)(3));
有人应该看过原文，但是作者没写出多个参数怎么办，这里我做了补充<https://github.com/Stevenzwzhai/plugs/tree/master/Sum-1>

#### 15.函数队列
关于实现函数按一定顺序调用的例子，直接看代码<https://github.com/Stevenzwzhai/plugs/tree/master/%E5%87%BD%E6%95%B0%E9%98%9F%E5%88%97>

#### 16.判断一个函数是否为质数的算法
基本思路：负数不是质数。同样的，1和0也不是，因此，首先测试这些数字。此外，2是质数中唯一的偶数。没有必要用一个循环来验证4,6,8。再则，如果一个数字不能被2整除，那么它不能被4，6，8等整除。因此，你的循环必须跳过这些数字。
<https://github.com/Stevenzwzhai/plugs/tree/master/%E5%88%A4%E6%96%AD%E4%B8%80%E4%B8%AA%E6%95%B0%E5%AD%97%E6%98%AF%E5%90%A6%E6%98%AF%E8%B4%A8%E6%95%B0>

#### 16.js无限级分类
关于这个我也有文章具体介绍[无限级分类和循环渲染](http://www.cnblogs.com/Upton/p/6125059.html)

#### 17.自定义短信模板
这里我们的需求是：编辑区可以插入关键字，当然是可以在点击到文本域中的任意位置，关键字以中括号包裹的形式出现【关键字】，删除关键字要整个关键都删掉，而不是自己全删除。
这里我试过使用div+contentable，关键字使用元素插入，虽然删除很方便，但是在计算光标位置的时候就略复杂，所以这里使用正则去判断光标左右中括号的数量来完成，具体看文章：[JavaScript实现自定义短信模板](http://www.jianshu.com/p/dbc4ac17ba4c)代码地址<https://github.com/Stevenzwzhai/plugs/tree/master/%E8%87%AA%E5%AE%9A%E4%B9%89%E6%A8%A1%E6%9D%BF-template>

#### 18.数组排序
这里只写了冒泡排序和快排，这两个很常见，但是仍有一些地方可以进行优化，我这里增加了一些过滤条件以及算法上的优化。<https://github.com/Stevenzwzhai/plugs/blob/master/Array-sort>

#### 19.lazyMan实现
这算是一个经典的面试题了，这里手动实现了下供参考。<https://github.com/Stevenzwzhai/plugs/tree/master/lazyMan>

#### 20.省市区联动选择
使用原生js和vue分别编写：<https://github.com/Stevenzwzhai/city-select>
#### 21.时间轴
实现一个垂直时间轴，点击对应的时间，滑动到中间位置：<https://github.com/Stevenzwzhai/plugins/tree/master/date-line>
#### 22.图品展示插件
这两个是vue组件(基于vue2.x)，可以通过以下方式调用
```
import Yimg from 'Yimg'
export default{
       components:{
              Yimg
       }
}

template:
<Yimg></Yimg>
```
##### Yimg( https://github.com/Stevenzwzhai/plugs/tree/master/Yimg )是一个简单的图片放大查看组件，鼠标悬浮展示一个放大后的图片，参数：
src-> String 图片URL
size-> String/Number 图片大小

##### YGimg( https://github.com/Stevenzwzhai/plugs/tree/master/YGimg )是一个图片组查看器，类似于百度图片查看，可以切换图片，图片展示区可以缩放／旋转／拖拽图片，参数：
title-> String图片查看器弹出时的标题
imgLit-> Array 图片数组，元素格式{url:imgurl},至于为什么是个对象，是为了以后开发更多
show-> Boolean,标示图片查看器显示和隐藏，当然有关闭按钮的。
#### 23.storage的使用
加密存储localStorage和sessionStorage（base64）<https://github.com/Stevenzwzhai/plugs/tree/master/storage>。
#### 24.Number处理
常见的数字处理<https://github.com/Stevenzwzhai/plugs/tree/master/Number>。
#### 25.一些vue指令
常见指令<https://github.com/Stevenzwzhai/plugs/tree/master/vue-directive>。
1.移动端手指按下改变元素的样式
#### 26.深拷贝
深拷贝<https://github.com/Stevenzwzhai/plugs/tree/master/deepClone>。
如果是普通的数组，对象，对象数组都可以使用JSON.parse(JSON.stringify(data))来迅速实现深拷贝，但是如果有函数，JSON.stringify()会把函数转为undefined,再parse就直接没了，所以这里还需要特殊处理一下（因为函数一般不需要深拷贝所以直接引用，如果需要可以对函数拷贝即可）。
#### 25.公告纵向切换效果（vue实现纵向无缝切换）
地址：<https://github.com/Stevenzwzhai/plugs/tree/master/vue-swipe-col>。
演示地址：http://jsrun.net/TmiKp/show
#### 26.操作元素的class
地址：<https://github.com/Stevenzwzhai/plugs/tree/master/className-option>。
包含了添加、删除、替换、在某个前面添加和在某个后面添加。实现了基本的classList功能（如果浏览器支持classList的话就不必使用这个了）。
#### 27.面试题集合
地址：<https://github.com/Stevenzwzhai/plugs/tree/master/interview>。
#### 27.jsonp简单实现
地址：<https://github.com/Stevenzwzhai/plugs/tree/master/jsonp>。
#### 28.微信浏览器不显示x5内核标示的解决方案。
地址：<https://github.com/Stevenzwzhai/plugs/tree/master/wechat-scroll/index.js>。
#### 29.大数计算。
当数字超过js的范围就无法直接运算符计算，这里提供两个大数的加法，这两个数为整数
地址：<https://github.com/Stevenzwzhai/plugs/tree/master/cale-big-num/index.js>。
#### 30.缓存设计。
基于 Localstorage 设计一个缓存系统,在最后新增了设置缓存的过期时间
地址：<https://github.com/Stevenzwzhai/plugs/tree/master/storage-system/index.js>。
#### 31.日期特殊处理
日期的特殊处理，比如获取某个时间点相对现在是几（秒/分/时/天/月/年）前：<https://github.com/Stevenzwzhai/plugs/tree/master/date-deal/index.js>。
#### 32.移动端弹窗-页面滚动
当我们写一些简单的h5页面时，不免会有一些弹窗，当页面是可以滚动的，但是希望在出现弹窗后，手指滑动时页面不要跟着滚动，这个时候就需要特殊处理了：<https://github.com/Stevenzwzhai/plugs/tree/master/dialog-scroll/index.js>。

以上就是全部内容，当然里面有些不足或粗糙，请大家指正，博客园和简书都是我写的文章，如果觉得不错star一下，或者提供更多的实用插件。未完待续。。。

