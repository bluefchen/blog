### 1. 扩展内置对象的原型时：

一般情况，尽量不要打`猴子补丁`，如有需要，最好按照下面的格式：
``` javascript
//Object可以是Array String Object Function等
if(typeof Object.prototype.method !== "undefined") {
  Object.prototype.method = function() {
    //方法代码
  }
}
```