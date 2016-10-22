<template>
  <div id="app">
    <img class="logo" src="./assets/logo.png">
    <br></br>
    <ul>
      <li  v-for="tag in tags">
        <color-picker v-model="tag.color">
            嘿嘿嘿
        </color-picker>
        <hr>
      </li>
      </ul>
  </div>
</template>

<script>
import ColorPicker from './components/ColorPicker.vue'
export default {
  data: function () {
    return {
      tags: [
        {color: '#FF0000', name: '1'},
        {color: '#FFCC00', name: '1'},
        {color: '#FFEE00', name: '1'},
        {color: '#DDEE00', name: '1'}
      ]
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
