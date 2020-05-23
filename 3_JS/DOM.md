### Document Object Model 文档对象模型

DOM 是 JavaScript 用来操纵网页的接口。
思路是把网页转换成一个 JS 对象，里面有许多小的节点对象，通过对节点对象的操作就可以各种功能。

DOM 对象，是由许多的节点对象（Node）组成的。
有七种类型：
Document：整个文档树，位于顶层
DocumentType：表示文档树的类型（<!DOCTYPE HTML>）
Elentment: 网页中的各种标签
Attr：Element 的属性
Text：Element 之间的文本
Comment：注释
DocumentFragment: 文档的片段

浏览器提供了 Node 接口，所有节点都继承了 Node 接口的属性和方法

### Document 节点

#### 1.获取元素节点内容

1.1 **获取单个节点对象**：getElementById()，参数 id 字符串，返回值 Element 对象， 没找到返回 null
1.2 **获取多个节点对象**：getElementsByTagName, 参数 元素 字符串， 返回获取过来元素对象的集合，以类数组对象（HTMLCollection 实例）存储。如果没有匹配元素，返回一个空的集合。如果要根据父元素获取节点下的子节点元素，要指明父元素是哪个对象。
因为这里返回值是伪数组形式，必须用 getElementsByTagName('ol')[0]
H5 新增方法 注意以下只兼容 IE9 以上。
1.3 **通过类名获取**: getElementsByClassName(),参数 类名 字符串，返回匹配的元素集合。
1.4 **根据指定选择器返回第一个元素对象**：querySelect(),参数 CSS 选择器字符串，返回值匹配的第一个元素对象
1.5 **根据指定选择器返回所有元素**：querySelectAll(), 参数 CSS 选择器字符串，返回所有匹配的元素对象
1.6 **获取 body**：可以用前面的方法获取，或者通过 Document.body 这个专属方法
1.7 **获取 HTML**：可以用前面的方法获取，或者通过 Document.docuemntElment
`
