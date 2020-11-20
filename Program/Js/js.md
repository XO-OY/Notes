# JS

## 反射调用方法

    var func = eval(funcName);
    if(typeof func == 'function'){
        func.call(this); 
    }

## 单独js页不能用EL表达式取到后台传值

## 前台直接限制html标签脚本

   后台Encode.forHtml(msg);编码，前台直接用EL表达式接收
