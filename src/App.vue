<template>
  <div id="app">
    <img class="logo" src="./assets/logo.png">
    <br></br>
    <color-picker :color="color" >
        嘿嘿嘿
    </color-picker>
  </div>
</template>

<script>
import ColorPicker from './components/ColorPicker.vue'

export default {
  data: function () {
    return {
      color: '#309BAC'
    }
  },
  components: {
    ColorPicker
  }
}
</script>

<style>
html {
  height: 100%;
}

body {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 100%;
}

#app {
  color: #2c3e50;
  margin-top: -100px;
  max-width: 600px;
  font-family: Source Sans Pro, Helvetica, sans-serif;
  text-align: center;
}

#app a {
  color: #42b983;
  text-decoration: none;
}

.logo {
  width: 100px;
  height: 100px
}
</style>
