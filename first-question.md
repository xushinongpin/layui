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



