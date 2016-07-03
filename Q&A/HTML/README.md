#### Doctype作用？严格模式与混杂模式如何区分？它们有何意义?
> - 标签 `<!DOCTYPE>`指示web浏览器使用html(html或xhtml)版本进行编写指令，它必须是html文档的第一行，位于`<html>`标签之前
- 该标签可声明三种 DTD 类型，分别表示严格版本，过渡版本以及基于框架的 HTML 文档。#### Doctype作用？严格模式与混杂模式如何区分？它们有何意义?

> - HTML5 为什么只需要写 `<!DOCTYPE HTML>` ?
- 由于HTML4是基于SGML的，所以 `<!DOCTYPE` 声明引用 DTD ，DTD 规定了标记语言的规则，这样浏览器才能正确地呈现内容。
 HTML5 不是基于 SGML，所以不需要引用 DTD。