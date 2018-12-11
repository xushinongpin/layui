  
在每个 p 元素结尾插入内容：  追加

```
$("button").click(function(){
  $("p").append(" <b>Hello world!</b>");
});
```

设置所有 p 元素的内容： 覆盖

```
$(".btn1").click(function(){
  $("p").html("Hello <b>world</b>!");
});
```



