```
$.ajax({
    type:'POST',
    url:url,
    data: data_field,
    dataType:'json'
}).done(function(data){
    layer.close(mask);
    var a = $("<a>");
    a.attr("href",data.file);
    $("body").append(a);
    a.attr("download",data_field.prostatus+"-"+data_field.starttime+"-"+data_field.endtime+"-"+data_field.status+"-"+data_field.type+"XXXX.xls");
    a[0].click();
    a.remove();
});
```

php

```
//生成excel文件
    $objWriter = createWriter($objPHPExcel);
    ob_start();
    $objWriter->save("php://output");
    $xlsData = ob_get_contents();
    ob_end_clean();
    $response = array(
        'op' => 'ok',
        'file' => "data:application/vnd.ms-excel;base64,".base64_encode($xlsData),
    );
    die(json_encode($response));
```



