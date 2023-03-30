<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
  <div class="bgimg"></div>
  <HelloWorld msg="Welcome to Your Vue.js App" />
  
</template>

<script>
// import {onMounted,ref,computed} from "vue";
// let account_item = ref([]);

import HelloWorld from './components/HelloWorld.vue'
export default {
  name: 'App',
  components: {
    HelloWorld
  }
}


</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  //margin-top: 60px;
}

$ruler: 16px;
$color-red: #AE1100;
$color-bg: #EBECF0;
$color-shadow: #BABECC;
$color-white: #FFF;

html {
  // background:url('http://thekitemap.com/images/feedback-img.jpg') no-repeat;
  // background-size: cover;
  // height:100%;
}
.bgimg{
  position: fixed;
  width:100%;
  height: 100%;
  background:url('./assets/yuan2.webp') no-repeat;
  background-size: cover;
  height:100%;
  background-position:center;
  filter: blur(10px);
  z-index: -1;
}
body{
  margin: 0;
}
body,
p,
input,
select,
textarea,
button {
  font-family: 'Montserrat', sans-serif;
  letter-spacing: -0.2px;
  font-size: $ruler;
}

div,
p {
  color: $color-shadow;
  text-shadow: 1px 1px 1px rgba(255,255,255,0.15);
}


form {
  padding: $ruler;
  width: $ruler*20;
  margin: 0 auto;
}

.segment {
  padding: $ruler*2 0;
  text-align: center;
}

button,
input {
  border: 0;
  outline: 0;
  font-size: $ruler;
  border-radius: $ruler*20;
  padding: $ruler;
  background-color: rgba(255,255,255,0.15);
  text-shadow: 1px 1px 0 rgba(255,255,255,0.15);
}

label {
  display: block;
  margin-bottom: $ruler*1.5;
  width: 100%;
}

input {
  margin-right: $ruler/2;
  box-shadow: inset 2px 2px 5px $color-shadow, inset -5px -5px 10px rgba(255,255,255,0.15);
  width: 100%;
  box-sizing: border-box;
  transition: all 0.2s ease-in-out;
  appearance: none;
  -webkit-appearance: none;

  &:focus {
    box-shadow: inset 1px 1px 2px $color-shadow, inset -1px -1px 2px rgba(255,255,255,0.15);
  }
}

input::-webkit-outer-spin-button,
input::-webkit-inner-spin-button {
  -webkit-appearance: none;
}

button {
  color: #61677C;
  font-weight: bold;
  box-shadow: -5px -5px 20px rgba(255,255,255,0.5), 5px 5px 20px rgba(255,255,255,0.5);
  transition: all 0.2s ease-in-out;
  cursor: pointer;
  font-weight: 600;

  &:hover {
    box-shadow: -2px -2px 5px rgba(255,255,255,0.15), 2px 2px 5px rgba(255,255,255,0.15);
  }

  &:active {
    box-shadow: inset 1px 1px 2px rgba(255,255,255,0.15), inset -1px -1px 2px rgba(255,255,255,0.15);
  }

  .icon {
    margin-right: $ruler/2;
  }

  &.unit {
    border-radius: $ruler/2;
    line-height: 0;
    width: $ruler*3;
    height: $ruler*3;
    display: inline-flex;
    justify-content: center;
    align-items: center;
    margin: 0 $ruler/2;
    font-size: $ruler*1.2;

    .icon {
      margin-right: 0;
    }
  }

  &.red {
    display: block;
    width: 100%;
    color: $color-red;
  }
}

.input-group {
  display: flex;
  align-items: center;
  justify-content: flex-start;

  label {
    margin: 0;
    flex: 1;
  }
}
</style>
