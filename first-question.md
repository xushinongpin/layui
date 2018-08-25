```
table.reload(); 

重新加在定义要传的数据
where: {
    id:cid,
    pankou:pankou,
},

重置where的查询条件
done: function(res, curr, count){
    this.where={};
}

重新加载新的地址
url: a/b/c,

完整的重加在
//执行重载
table.reload('testReload', {
    url: url,
    page: {
        curr: 1 //重新从第 1 页开始
    }
    ,where: {
        id:cid,
        pankou:pankou,
    },done: function(res, curr, count){
        this.where={};
    }
});
```

监听点击传标签带的数据

```
$('.qiehuancode').on('click', function(){
    var othis = $(this),type = $(this).data('type');
    active[type] ? active[type].call(this,othis) : '';
});
```

后台传的数据

```
code: 0,
msg: "",
count: 1000,
data:[{},{}]
```

有时候自己传来的数据想显示怎么办？利用done，比如

```
,done:  function(res, curr, count){
    $('#layui-laypage-1').append('<span class="layui-laypage-count"> 总计： '+res.sum+'</span>');
}
如果嵌套在原本table里面，点击分页后他将会消息，可以考虑写到外层的标签上，比如
$('.sum').html('<span class="sum-title"> 总计： '+res.sum+'</span>');
```

自定义模版

```
,templet:function(d){return d.odds + '<i class="layui-icon">&#xe642;</i>';} 此处嵌套修改标签样式
,templet:function(d){status_arr = {'0':'启用', '1':'可用', '3':'冻结'};return status_arr[d.is_status]}
```

添加table值的点击事件

```
cols 对应字段添加 ,event:"xxx"
table.on('tool(test)', function(obj){
    var data = obj.data; //获得当前行数据
    var layEvent = obj.event; //获得 lay-event 对应的值（也可以是表头的 event 参数对应的值）
    //如果是点击代理进去
    if(layEvent === 'XXX'){
    }
    return false;
});
```

定义 $ = layui.$, 报Uncaught SyntaxError: Identifier '$' has already been declared，【有可能你上面或者下面定义了，重复定义导致的】





