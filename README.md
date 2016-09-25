# vue-bootstrap-colorpicker

> 基于bootstrap3.x的vue颜色拾取器(vue-colorpicker base on bootstrap)


## 安装

``` bash
# install dependencies
npm install vue-bootstrap-colorpicker
```
## 使用
```javascript
import ColorPicker from './components/ColorPicker.vue'
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


