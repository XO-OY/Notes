# JS

## 反射

    var func = eval(funcName);
    if(typeof func == 'function'){
        func.call(this); 
    }
