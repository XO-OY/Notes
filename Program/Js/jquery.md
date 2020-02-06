# JQuery

## 选择器匹配元素

    1.[attribute=value] 匹配给定的属性是某个特定值的元素
    2.[attribute!=value] 匹配所有不含有指定的属性，或者属性不等于特定值的元素
    3.[attribute^=value] 匹配给定的属性是以某些值开始的元素
    4.[attribute$=value] 匹配给定的属性是以某些值结尾的元素
    5.[attribute*=value] 匹配给定的属性是包含某些值的元素
    $(".tabs").find("div[class!=tab][class='tab1 tab2']").html();
    $(".tabs").find("div[class!=tab]").not(".tab.hide").html();
    $(".tabs").find("div[class!=tab]").not(".hide").html();
    $('.tabs > .tab:not(".hide")').html();

## 移除元素属性时用removeAttr，不要置空（e.g. disabled）
