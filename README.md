# string 

---
[![Build Status](https://travis-ci.org/dreamstu/string.svg?branch=master)](https://travis-ci.org/dreamstu/string)
[![spm version](http://spmjs.io/badge/string)](http://spmjs.io/package/string)

An string lib on quickjs package!

---

## Install

```
$ spm install string --save
```

## Usage

```js
var string = require('string');
// use string
```


---
## 配置说明

### toString(object) *Mixed*

`释义`
将任意变量转换为字符串的方法。

`参数及返回`
>@param {Mixed} o 任意变量

>@return {String} 返回转换后的字符串




---
### template(str,data) *String|Object*

`释义`
多行或单行字符串模板处理。

`参数及返回`
>@param {String} str 模板字符串

>@param {Object} obj 要套入的数据对象

>@return {String} 返回与数据对象合成后的字符串




---
### isURL(str) *String*

`释义`
判断是否是一个可接受的 url 串。

`参数及返回`
>@param {String} str 要检测的字符串

>@return {Boolean} 如果是可接受的 url 则返回 true


---
### parseURL(str) *String*

`释义`
分解 URL 为一个对象，成员为：scheme, user, pass, host, port, path, query, fragment。

`参数及返回`
>@param {String} str URL 地址

>@return {Object} 如果解析失败则返回 null



---
### buildURL(str) *String*

`释义`
将一个对象（成员为：scheme, user, pass, host, port, path, query, fragment）重新组成为一个字符串。

`参数及返回`
>@param {Object} obj URl 对象

>@return {String} 如果是可接受的 url 则返回 true




---
### mapQuery(uri) *String*

`释义`
将 uri 的查询字符串参数映射成对象。

`参数及返回`
>@param {String} uri 要映射的 uri

>@return {Object} 按照 uri 映射成的对象

`例子`
@example
```js
	seajs.use('string',function(string){
		var url = "http://web.dreamstu.com/?uid=4765078&style=blue";
		// queryObj 则得到一个{uid:"4765078", style:"blue"}的对象。
		var queryObj = string.mapQuery(url);
	});
```


---
### test(str, regex, params) *String|String|String*

`释义`
测试正则的方法。

`参数及返回`
>@param {String} str 待测试的字符串

>@param {String|RegExp} regex 正则表达式，或者正则表达式的字符串

>@param {String} params 正则的参数

>@return {Boolean} 返回结果


---
### contains(string1, string2, separator) *String|String|String*

`释义`
判断string1中是否含有string2字符串。

`参数及返回`
>@param {String} string1 需要被查找的字符串

>@param {String} string2 是否含有的字符串

>@param {String} separator 分隔符，可选

>@return {Boolean} 如果含有，返回 true，否则返回 false


---
### trim(string) *String*

`释义`
清除字符串开头和结尾的空格。

`参数及返回`
>@param {String} string 需要被清除开头和结尾空格的字符串

>@return {String} 返回清除后的字符串


---
### clean(string) *String*

`释义`
清除字符串开头和结尾的空格，并把字符串之间的多个空格转换为一个空格。

`参数及返回`
>@param {String} string 需要被操作的字符串

>@return {String} 返回清除后的字符串


---
### camelCase(string) *String*

`释义`
将“-”连接的字符串转换成驼峰式写法。

`参数及返回`
>@param {String} string 需要被操作的字符串

>@return {String} 返回转换后的字符串


---
### hyphenate(string) *String*

`释义`
将驼峰式写法字符串转换成“-”连接的。

`参数及返回`
>@param {String} string 需要被操作的字符串

>@return {String} 返回转换后的字符串


---
### capitalize(string) *String*

`释义`
将字符串转换成全大写字母。

`参数及返回`
>@param {String} string 需要被操作的字符串

>@return {String} 返回转换后的字符串


---
### escapeRegExp(string) *String*

`释义`
转换 RegExp 正则表达式。

`参数及返回`
>@param {String} string 需要被操作的字符串

>@return {String} 返回转换后的字符串


---
### toInt(string) *String*

`释义`
将字符串转换成整数。

`参数及返回`
>@param {String} string 需要被转换的字符串

>@return {Number} 返回转换后的整数


---
### toFloat(string) *String*

`释义`
将字符串转换成浮点数。

`参数及返回`
>@param {String} string 需要被转换的字符串

>@return {Number} 返回转换后的浮点数


---
### toSingleLine(string) *String*

`释义`
将带换行符的字符串转换成无换行符的字符串。

`参数及返回`
>@param {String} string 需要被转换的字符串

>@return {String} 返回转换后的字符串



---
### toHtml(string) *String*

`释义`
将字符串转换成html源码。

`参数及返回`
>@param {String} string 需要被转换的字符串

>@return {String} 返回转换后的html代码字符串


---
### toTitle(string) *String*

`释义`
将字符串转换成用于title的字符串。

`参数及返回`
>@param {String} string 需要被转换的字符串

>@return {String} 返回转换后的in title字符串


---
### hexToRgb(string) *String*

`释义`
将颜色 Hex 写法转换成 RGB 写法。

`参数及返回`
>@param {String} string 需要被转换的字符串

>@return {String} 返回转换后的字符串


---
### rgbToHex(string) *String*

`释义`
将颜色 RGB 写法转换成 Hex 写法。

`参数及返回`
>@param {String} string 需要被转换的字符串

>@return {String} 返回转换后的字符串


---
### stripScripts(string,option) *String|(Boolean|Function)*

`释义`
脱去script标签。

`参数及返回`
>@param {String} string 需要被转换的字符串

>@param {Boolean|Function} option 若`option`参数为Boolean类型，则表示是否在脱去script标签后，执行其中的代码，若`option`参数为Function类型，则执行`option(scripts, text)`，其中scripts为原参数string，text为脱掉script标签之后的代码

>@return {String} 返回转换后的字符串


---
### toQueryPair(key, value) *String|String*

`释义`
将key和value组合成uri中的查询参数。

`参数及返回`
>@param {String} key 要转换成查询字符串的键对象

>@param {String} value 要转换成查询字符串的值对象

>@return {String} 返回转换后的查询字符串

>注意：此函数会使用`encodeURIComponent()`对键值进行编码


---
### toQueryString(obj) *Object*

`释义`
将obj转换成uri中的查询参数。

`参数及返回`
>@param {Object} obj 要转换成查询字符串的对象

>@return {String} 返回转换后的查询字符串

>注意：此函数会使用`encodeURIComponent()`对键值进行编码


---
### substitute(string, object, regexp) *String|Object|String*

`释义`
代替函数，在文本字符串中用 new_text 替代 old_text。如果需要在某一文本字符串中替换指定的文本，请使用函数 substitute

`参数及返回`
>@param {String} string 待替换的字符串

>@param {Object} object 替换映射

>@param {String} string 用于匹配的正则字符串

>@return {String} 返回替换后的字符串


---
### replaceAll(string, reallyDo, replaceWith, ignoreCase) *String|String|String|String*

`释义`
全局替换指定的字符串。

`参数及返回`
>@param {String} string 待操作的字符串

>@param {String} reallyDo 要替换的字符串

>@param {String} replaceWith 要替换成的字符串

>@param {String} ignoreCase 用于匹配的正则字符串

>@return {String} 返回替换后的字符串


---
### byteLength(string,n) *String|Number*

`释义`
计算字符串的字节长度。

`参数及返回`
>@param {String} string

>@param {Number} n 指定一个中文的字节数, 默认为2

>@return {Number} 返回自己长度


---
### cutRight(string,n) *String|Number*

`释义`
按字符按给定长度裁剪给定字符串。

`参数及返回`
>@param {String} string

>@param {Number} n 指定裁剪长度

>@return {String} 返回裁剪后的字符串


---
### cutByBytes(string,n) *String|Number*

`释义`
按字节按给定长度裁剪给定字符串。

`参数及返回`
>@param {String} string

>@param {Number} n 指定裁剪长度

>@return {String} 返回裁剪后的字符串


---
### isNumber(string) *String*

`释义`
判断给定字符串是否是数字。

`参数及返回`
>@param {String} string

>@return {String} 是数字返回true，不是数字返回false



---
### isEmail(string) *String*

`释义`
判断一个字符串是否是邮箱格式。

`参数及返回`
>@param {String} string

>@return {String} 是返回true，不是返回false



---
### encodeHtmlSimple(string) *String*

`释义`
JS安全API v1.1
html正文编码, 对需要出现在HTML正文里(除了HTML属性外)的不信任输入进行编码。

`参数及返回`
>@param {String} string

>@return {String} 返回编码后的字符串




---
### decodeHtmlSimple(string) *String*

`释义`
JS安全API v1.1
html正文解码, 对HtmlEncode函数的结果进行解码。

`参数及返回`
>@param {String} string

>@return {String} 返回编码后的字符串




---
### decodeHtmlSimple2(string) *String*

`释义`
JS安全API v1.1
html正文解码, 对HtmlEncode函数的结果进行解码。

`参数及返回`
>@param {String} string

>@return {String} 返回编码后的字符串




---
### encodeHtmlAttributeSimple(string) *String*

`释义`
html属性编码：对需要出现在HTML属性里的不信任输入进行编码
注意:
>(1)该函数不适用于属性为一个URL地址的编码.这些标记包括:a/img/frame/iframe/script/xml/embed/object...
属性包括:href/src/lowsrc/dynsrc/background/...

>(2)该函数不适用于属性名为 style="[Un-trusted input]" 的编码。

`参数及返回`
>@param {String} string

>@return {String} 返回编码后的字符串




---
### encodeHtml(string) *String*

`释义`
用做过滤直接放到HTML里的

`参数及返回`
>@param {String} string

>@return {String} 返回编码后的字符串





---
### encodeHtmlAttribute(string) *String*

`释义`
用做过滤HTML标签里面的东东 比如这个例子里的``&lt;input value="XXXX"&gt;``  XXXX就是要过滤的

`参数及返回`
>@param {String} string

>@return {String} 返回编码后的字符串






---
### encodeScript(string) *String*

`释义`
用做过滤直接放到HTML里js中的

`参数及返回`
>@param {String} string

>@return {String} 返回编码后的字符串







---
### encodeHrefScript(string) *String*

`释义`
用做过滤直接放到``<a href="javascript:XXXX">``中的

`参数及返回`
>@param {String} string

>@return {String} 返回编码后的字符串





---
### encodeRegExp(string) *String*

`释义`
用做过滤直接放到正则表达式中的

`参数及返回`
>@param {String} string

>@return {String} 返回编码后的字符串





---
### encodeUrl(string) *String*

`释义`
用做过滤直接URL参数里的  比如 ``http://show8.qq.com/abc_cgi?a=XXX``  XXX就是要过滤的

`参数及返回`
>@param {String} string

>@return {String} 返回编码后的字符串




---
### encodeUriComponent(string) *String*

`释义`
对需要出现在一个URI的一部分的不信任输入进行编码 

例如:
``<a href="http://search.msn.com/results.aspx?q1=[Un-trusted-input]& q2=[Un-trusted-input]">Click Here!</a>``
以下字符将会被编码: 
除``[a-zA-Z0-9.-_]``以外的字符都会被替换成URL编码

`参数及返回`
>@param {String} string

>@return {String} 返回编码后的字符串




---
### vaildBaturuUrl(string) *String*

`释义`
url转向验证
    描述：对通过javascript语句载入（或转向）的页面进行验证，防止转到第三方网页和跨站脚本攻击
    
    例：
    合法的值
        http://xxx.51baturu.com/hi/redirect.html?url=http://www.qq.com
        http://xxx.51baturu.com/hi/redirect.html?url=a.html
        http://xxx.51baturu.com/hi/redirect.html?url=/a/1.html
    非法的值
        http://xxx.51baturu.com/hi/redirect.html?url=http://www.baidu.com
        http://xxx.51baturu.com/hi/redirect.html?url=javascript:codehere
        http://xxx.51baturu.com/hi/redirect.html?url=//www.qq.com

`参数及返回`
>@param {String} string

>@return {Boolean} 返回值：true -- 合法；false -- 非法




---
### vaildUrl(string) *String*

`释义`
验证给定字符串是否是url, 如果是url 则返回正常的url

`参数及返回`
>@param {String} string

>@return {String} 如果是url 则返回正常的url，否则返回空字符串



---
### getCharWidth(str,fontsize) *String|Number*

`释义`
获取字符实际宽度

`参数及返回`
>@param {String} str 需要计算的字符串

>@param {Number} fontsize 字体大小，可以不填

>@return {Number} 字符实际宽度



---
### getCharWidth(str,fontsize,width) *String|Number|Number*

`释义`
按给定宽度裁剪字符串

`参数及返回`
>param {String} str 

>@param {Number} fontsize 字体大小

>@param {Number} width 限定的宽度

>@return {Number}

