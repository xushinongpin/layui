清空原来input里面的内容

```
$('.xxx').val(''); //赋值直接在引号里面填写
```

选中

```
复选框选中
$('input[name="user_type[qwe]"][value=qwe]').attr("checked", true);
$('.is_status').attr("checked",1);
```

select上需要有搜索的加上

```
  lay-search=""
```

jq选中select

```
$('#default_pay option[value='+pay_id+']').attr('selected','');
form.render(); //刷新select选择框渲染
```

选择器【选择后触发】

```
<select lay-filter="aaa"></select>
form.on('select(aaa)',function (data) {
    console.log(data);
});
```



