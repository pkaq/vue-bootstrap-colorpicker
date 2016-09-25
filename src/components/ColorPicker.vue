<template>
  <!-- 顏色拾取器 -->
  <div class="btn-group colorpicker">
    <a class="label dropdown-toggle" :style={'background-color':color} type="button" data-toggle="dropdown">
      <slot>{{ content }}</slot>
    </a>

    <ul class="dropdown-menu" role="menu">
      <li v-for="color in colors">
        <span class="label text-left" :style={'background-color':color} @click="colorpick(color)"> </span>
      </li>
    </ul>
  </div>
  <!-- //END 顏色拾取器 -->
</template>
<script>
  export default {
    props: {
      content: {
        type: String,
        default: function () {
          return ' ~ PKAQ ~ '
        }
      },
      colors: {
        type: Array,
        default: function () {
          return ['#FFAC0C', '#309BAC', '#247B79', '#8AA766', '#F6C048', '#B52F85', '#707070', '#9386BD', '#D74063', '#F4889F', '#8B7366']
        }
      },
      color: String
    },
    methods: {
      colorpick: function (color) {
        this.color = color
      }
    }
  }
</script>
<style lang="stylus">
  .colorpicker
    a
      color #000
      background #cfcfcf
      padding 5px
    ul
      width 236px
    li
      float left
      width 36px
      height 36px
      margin 3px 5px
      span
        width 100%
        height 100%
        display block
        cursor pointer
</style>
