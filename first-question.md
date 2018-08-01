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
```



