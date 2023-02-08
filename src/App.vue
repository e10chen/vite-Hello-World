<template>
  
  <HelloWorld msg="Hello Vue 3 + Vite" />
</template>

<script setup>
import HelloWorld from './components/HelloWorld.vue'

// This starter template is using Vue 3 experimental <script setup> SFCs
// Check out https://github.com/vuejs/rfcs/blob/script-setup-2/active-rfcs/0000-script-setup.md
</script>

<style>
 .buttons{
   padding: 5px;
}

.buttons:hover{
  background-color: yellow;
}

.buttons:focus {
  background-color: yellow; 
}

.all{
  border-style: solid;
  border-width: 5px;
  width: 400px;
  max-width: 500px;
  margin: auto;
  background-color: coral;
  margin-top: 10px;
}

.title{
  text-align: center;
  font-size: 40px;
}

.name{
  text-align: center;
}
.content{
   text-align: center;
}
img {
  width: 300px;
}

p {
  text-align: left; 
  text-indent: 5%;
  font-size: 18px;
  padding: 15px;
  color: blue;
}

.detailButton {
  margin: 12px;
  position: center; 
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
