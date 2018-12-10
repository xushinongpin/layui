将数组弄成字符串

```
arr.join('') 或 arr.toString('')
同
都不加引号 - 默认逗号隔开
异
join 加了引号 - 隔开的字符取决于引号里面的东西，不填表示不用隔开
toString  加了引号或者任意东西 - 都是逗号隔开
注意：
arr 是否需要自然键的问题
```

定义下固定值 object

```
name = {name:'1',name2:'2'}
```

数组数组传到后台是不行的，要转成对象

```
JSON.stringify(arr)
或者
Object.setPrototypeOf(newdata, Object.prototype);
```

自定义变量对象键

```
{[data.id]:{field:value}}
```

判断数组是否存在

```
obj = layui.data('obj').obj;
Object.values(obj).indexOf('what')  存在将返回对应key，不存在返回-1
```

遍历

```
layui.each(data,function (index,item) {

})
```

删除对象的某个值

```
delete data.field[index];
```

将将字符串打散为数组

```
item.split("")
```

判断是否存在某字符串

```
data.match(search) !== null
```

判断对象是否存在某键

```
data.hasOwnProperty('abc')
```

查找替换

```
str.replace("，",",");//替换第一位
str.replace(/，/g,",");//替换所有
```



