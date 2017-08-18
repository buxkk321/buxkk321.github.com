 
## 配置项
* node_title_key  (Default:'')
* node_child_key  (Default:'')

### 例1:

输入数据:
```js
var input_data={
  '标题1':{
    key1:'abc',
    key2:'1111'
  },
  '标题2':{
    key1:'aaa',
    key2:{
      '标题3':'333',
      '标题4':'444'
    }
  }
};

$('#xxx').JsonEditor(input_data);
```

默认显示效果    
--标题1  
----key1:abc  
----key2:1111  
--标题2  
----key1:aaa  
----key2  
------标题3:333  
------标题4:444  



### 例2:
更改配置:   
option.node_title_key='key1'

那么最后的显示效果为:    
--abc  
----key1:abc  
----key2:1111  
--aaa  
----key1:aaa  
----key2:  
------标题3:333  
------标题4:444  

* option.node_child_key

### 例2.2:
更改配置:   
option.node_title_key='abc'

那么最后的显示效果为:    
--''(空字符串)   
----key1:abc        
----key2:1111        
--''(空字符串)   
----key1:aaa   
----key2:  
------标题3:333  
------标题4:444  


### 例3:
更改配置:    
option.node_child_key='key2'  

那么最后的显示效果为:     
--标题1:1111    
--标题2   
----标题3:333  
----标题4:444  

### 例4:
更改配置:      
option.node_title_key='key1'  
option.node_child_key='key2'  

显示效果为:    
--abc:1111  
--aaa  
----标题3:333  
----标题4:444  

### 例5:
输入数据:
```js
var input_data={
  '标题1':{
    key1:'abc',
    key2:'1111'
  },
  '标题2':{
    key1:'aaa',
    key2:{
      '标题3':'333',
      '标题4':'444'
      key3:{
        '标题5':'555',
        '标题6':'666'
      }
    }
  }
};
```
更改配置:      
option.node_title_key='key1'  
option.node_child_key='key2.key3'  

显示效果为:    
--abc:''  (空字符串)  
--aaa  
----标题5:555   
----标题6:666   
