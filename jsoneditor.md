 




输入数据:
```js
var input_data={
  '标题1':{
    name:'abc',
    data:'1111'
  },
  '标题2':{
    name:'aaa',
    data:{
      '标题3':'333',
      '标题4':'444'
    }
  }
};

$('#xxx').JsonEditor(input_data);
```

显示效果
--标题1

----name:abc

----data:1111

--标题2

----name:aaa

----data

------标题3:333

------标题4:444

## 配置项
### option.node_title_key

如果输入如下配置:
option.node_title_key='name'

那么最后的显示效果为:
--abc
----name:abc
----data:1111
--aaa
----name:aaa
----data:
------标题3:333
------标题4:444

### option.node_child_key

如果输入如下配置:
option.node_title_key='name'
option.node_child_key='data'

那么最后的显示效果为:
--abc
----1111
--aaa
----标题3:333
----标题4:444
 
