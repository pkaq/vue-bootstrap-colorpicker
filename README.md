# vue-bootstrap-colorpicker

> 基于bootstrap3.x的vue颜色拾取器(vue-colorpicker base on bootstrap)

![capture](./capture/gif.gif)

此组件强烈依赖于jquery以及bootstrap3,使用时务必引入方可正常.
```html
  <link rel="stylesheet" href="static/css/bootstrap.min.css">
  <script src="static/js/jQuery/jQuery-2.2.0.min.js"></script>
  <script src="static/js/bootstrap/bootstrap.min.js"></script>
```

## 安装

``` bash
# install dependencies
npm install vue-bootstrap-colorpicker
```
## 使用
```javascript
import ColorPicker from 'vue-bootstrap-colorpicker'
...
...

 components: {
    ColorPicker
  }
...
...
  
```

```html
  <color-picker :color.sync="color">嘿嘿嘿</color-picker>
```

## 参数说明
| 参数 | 说明 | 默认值     |
|--------|--------|--------|
|    content |   标签显示的内容     |  ~PKAQ~     | 
|    color   |   当前颜色           |     无      |    
|    colors  |   颜色列表           |     ['#FFAC0C', '#309BAC', '#247B79', '#8AA766', '#F6C048', '#B52F85', '#707070', '#9386BD', '#D74063', '#F4889F', '#8B7366'] |    


