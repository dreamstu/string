# Demo

---

## Normal usage

````javascript
seajs.use('index', function(string) {
	console.info(string.toString(1));
	console.info(string.isURL("http://baidu.com/"));
	console.info(string.isURL("baidu.com/"));
	console.info(string.buildURL({"scheme":123, "user":"陈建", "pass":0, "host":"www.dreamstu.com", "port":80, "path":"/jslibs", "query":"a=123&b=456", "fragment":0}));
	console.info(string.mapQuery("http://baidu.com?a=123&b=456&c=789"));
	console.info(string.toFloat(100.1));
	console.info(string.toSingleLine("11\r\n11"));
	console.info(string.toHtml("<br/>"));
	console.info(string.toTitle("<i>\我们\</i>"));
	console.info(string.hexToRgb("#fff"));
	string.stripScripts("<script>console.info('嘿嘿')<\/script>",true);
	console.info(string.toQueryPair("a","钢铁是怎样炼成的"));
	console.info(string.toQueryString({"a":1,"b":2}));
	console.info(string.byteLength("开始了，我们"));
	console.info(string.cutRight("我们的歌",2));
	var h = string.encodeHtmlSimple("<body id='1' index='muma'><\/body>")
	console.info(h);
	console.info(string.decodeHtmlSimple(h));
	console.info(string.vaildBaturuUrl("http://www.51baturu.com/hi/redirect.html?url=//www.qq.com"));
});

````
