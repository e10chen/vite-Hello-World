<template>
  
  <HelloWorld msg="Hello Vue 3 + Vite" />
</template>

<script setup>
import HelloWorld from './components/HelloWorld.vue'

// This starter template is using Vue 3 experimental <script setup> SFCs
// Check out https://github.com/vuejs/rfcs/blob/script-setup-2/active-rfcs/0000-script-setup.md
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

body {
  background: cyan; 
}

.all{
  border-style: solid;
  border-radius: 20px;
  text-align: center;
  padding: 20px;
  border-width: 5px;
  width: 300px;
  max-width: 500px;
  margin: auto;
  background-color: coral;
  margin-top: 10px;
}

.text { 
  text-indent: 5%;
  font-size: 16px;
  color: blue;
}

.title{
  font-size: 40px;
}

.buttons{
  text-align: center; 
  padding: 5px;
}

.detailButton {
  margin: 1px;
  position: center; 
}

button:hover,
buttons:focus{
  background-color: yellow;
}

.picture {
  border-radius: 10px;
  border: solid white;
  width: 300px;
}

  @media (min-width: 500px) and (max-width: 800px) {
    
    .detailButton {
      display: none;
    }
  }

@media (max-width: 500px) {
  .all{
    transform: scale(0.8);
  }
}
</style>
