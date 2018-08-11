刷新父层

```
window.parent.location.reload();
var index = parent.layer.getFrameIndex(window.name);
parent.layer.close(index);
或者加end
layer.open({
  type: 2 //此处以iframe举例
  ,title: '当你选择该窗体时，即会在最顶端'
  ,area: ['390px', '260px']
  ,shade: 0
  ,maxmin: true
  ,offset: [ //为了演示，随机坐标
    Math.random()*($(window).height()-300)
    ,Math.random()*($(window).width()-390)
  ] 
  ,content: 'http://layer.layui.com/test/settop.html'
  ,btn: ['继续弹出', '全部关闭'] //只是为了演示
  ,yes: function(){
    $(that).click(); 
  }
  ,btn2: function(){
    layer.closeAll();
  }
  ,zIndex: layer.zIndex //重点1
  ,success: function(layero){
    layer.setTop(layero); //重点2
  }
  ,end: function () {
    location.reload();
  }
});
```



