```
添加 lay-ignore
input type="radio" name="is_status" class="is_status0" value="0" title="禁用" lay-ignore>禁用
```

如果隐藏再显示就会导致之前点击过的状态还在，这时候可以考虑动态输入

```
$('.showradio').html('..........XXX..........');
```



