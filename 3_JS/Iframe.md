Iframe 是什么？ 是 HTML 标签的一种，是一个嵌入式框架，用来在文档中嵌入其他文档

优点：
iframe 能够原封不动的把嵌入的网页展现出来。

如果有多个网页引用 iframe，那么你只需要修改 iframe 的内容，就可以实现调用的每一个页面内容的更改，方便快捷。

网页如果为了统一风格，头部和版本都是一样的，就可以写成一个页面，用 iframe 来嵌套，可以增加代码的可重用。

如果遇到加载缓慢的第三方内容如图标和广告，这些问题可以由 iframe 来解决。

1. 页面和程序分离,几乎不会受到外界任何 js 或者 css 的影响, 便于使用

2. 可以通过 iframe 嵌套通用的页面, 提高代码的重用率, 比如页面的头部样式和底部版权信息

3. 重新加载页面时, 不需要重载 iframe 框架页的内容, 增加页面重载速度.

4. iframe 可以解决第三方内容加载缓慢的问题.

缺点：

框架结构中出现各种滚动条

iframe 会阻塞主页面的 Onload 事件

搜索引擎的检索程序无法解读这种页面，不利于 SEO

iframe 和主页面共享连接池，而浏览器对相同域的连接有限制，所以会影响页面的并行加载。

1. 会产生很多页面，不容易管理

2. iframe 框架的内容无法被搜索引擎捕获, 所以 iframe 不适用于首页

3. iframe 兼容性较差

4. iframe 有一定的安全风险

5. iframe 会阻塞主页面的 Onload 事件

[iframe](https://www.cnblogs.com/shihaiying/p/11415605.html)