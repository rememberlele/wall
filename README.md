## 简单介绍

### when.js 是一个轻量级的Promises/A+和when()的实现。promise是对异步编程的一种抽象。它是一个代理对象，代表一个必须进行异步处理的函数返回的值或抛出的异常。

## 使用说明
### 外链形式  
``` html
<script>
    window.define = function(factory) {
        try{ delete window.define; } catch(e){ window.define = void 0; } // IE
        window.when = factory();
    };
    window.define.amd = {};
</script>
<script src="/module/when/2.5.1/when.js"></script>
```

```html
	<script>
	var timer = function() {
    var deferred = when.defer();

    var id = setTimeout(function() {
        deferred.resolve(id);
    }, 1000);

    return deferred.promise;
	};

	timer().then(function(id) { alert(id) });
	</script>
```

### 模块加载形式
when.js是标准的AMD模块，可以使用模块方式引入： 
```
<script>
require(['module/when/2.5.1/when'], function(when) {
    var timer = function() {
        var deferred = when.defer();

        var id = setTimeout(function() {
            deferred.resolve(id);
        }, 1000);

        return deferred.promise;
    };

    timer().then(function(id) { alert(id) });
});
</script>
```

# 使用主题



# 基本名词
标题(title)、副标题(subtitle)、图例(lengend)、数据系列(series)、X轴(xAxis)、Y轴(yAxis)、商标(credits)、提示(tooltip)等  
[![Highcharts官方API截图](http://p2.qhimg.com/t0173fe0ea48743b0c4.png)](http://www.highcharts.com/docs/chart-concepts/understanding-highcharts '')


# 详细文档请参考：  
1. [Highcharts官方文档](http://www.highcharts.com/docs 'Highcharts官方文档')  
2. [Highcharts官方API](http://api.highcharts.com/highcharts 'Highcharts官方API')  
[![Highcharts官方API截图](http://p3.qhimg.com/t010f9cd846a3539881.png)](http://api.highcharts.com/highcharts '')
