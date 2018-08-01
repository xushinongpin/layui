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

定义下固定值 object

```
name = {name:'1',name2:'2'}
```

数组数组传到后台是不的，行要转成对象

```
JSON.stringify(arr)
```

自定义变量对象键

```
{[data.id]:{field:value}}
```

自定义模版 

```
,templet:function(d){return d.odds + '<i class="layui-icon">&#xe642;</i>';} 此处嵌套修改标签样式
```



