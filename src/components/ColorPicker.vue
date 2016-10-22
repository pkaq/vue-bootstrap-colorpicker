<template>
  <div class="btn-group colorpicker">
    <a class="label dropdown-toggle" :style="'background-color:' + value" type="button" data-toggle="dropdown">
      <slot>{{ content }}</slot>
    </a>

    <ul class="dropdown-menu" role="menu">
      <li v-for="colo in colors">
        <a class="label text-left" :style="'background-color:' + colo"  @click="picked(colo)">
          <i v-if="colo === value" class="glyphicon glyphicon-ok"></i>
          <i v-else></i>
        </a>
      </li>
    </ul>
  </div>
</template>
<script>
  export default {
    props: {
      value: String,
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
      }
    },
    methods: {
      picked: function (color) {
        this.$emit('input', color)
      }
    }
  }
</script>
<style>
.colorpicker a{
  color: #000;
  background :#cfcfcf;
  padding: 5px;
}

.colorpicker ul {
  width:236px;
}

.colorpicker ul li{
  float: left;
  width: 36px;
  height: 36px;
  margin: 3px 5px;
}

.colorpicker ul li a i{
  color: #fff;
  left: -5px;
}

.colorpicker ul li a{
  width: 100%;
  height: 100%;
  line-height: 30px;
  text-align: center;
  display: block;
  cursor: pointer;
}
.colorpicker ul li a:hover{
  border: 1px #c3c3c3 dashed;
}

</style>
