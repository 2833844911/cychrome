# 该浏览器是对Chromium源码进行修改，达到可以更加方便的让我们对js源码进行分析

## 下载连接
````
https://wwd.lanzoum.com/i9moa0doa88j
密码:7yxb
视频使用教程：https://www.bilibili.com/video/BV1eV4y1L7dn/?vd_source=93dc7417d09246b7259569c65e2eb085
````
### 1.代理`localStorage`和`sessionStorage`实现对本地数据库的监控
### 之后将会更新代理document，window，location等属性，实现浏览器的监控
````
localStorage = new Proxy(localStorage,{
    get(target, propKey, receiver){
        debugger;
        return Reflect.get(target, propKey, target);
    },
    set(target, propKey, value, receiver){
        debugger;
        return Reflect.set(target, propKey, value2, target);
    }
});
sessionStorage = new Proxy(sessionStorage,{
    get(target, propKey, receiver){
        debugger;
        return Reflect.get(target, propKey, target);
    },
    set(target, propKey, value, receiver){
        debugger;
        return Reflect.set(target, propKey, value2, target);
    }
});
````

### 2.事件中的`isTrusted`可被修改，这样子就可以用js模拟轨迹不被检测

### 3.对js修改location属性跳转页面可断点
```
//首先启动这个函数开启断点
window.cbbhooklocationhref()
//开启完成后
location.href = "http://www.baidu.com" //通过location跳转页面将被debugger
location.host = "dsdsdsd" //通过location跳转页面将被debugger
```

### 4.随机audio指纹
```javascript
//随机切换audio指纹
window.cbbhookaudio()
```

### 5.随机canvas指纹
```javascript
//随机切换canvas指纹
window.cbbhookCanvas()
```

### 5.随机webgl指纹
```javascript
//随机切换webgl指纹
window.cbbhookwebgl()
```

# 无感浏览器底层插桩打印调用的浏览器函数 不会被检测
```
下载链接：
https://wwd.lanzoum.com/imMmZ0e9gc9g
密码:5x3i
```
###使用 （教程b站有哦）
```javascript
//开启打印
window.cbbopen()
```

### 欢迎加入星球哦
星球连接`https://t.zsxq.com/06bIUvBEM`


