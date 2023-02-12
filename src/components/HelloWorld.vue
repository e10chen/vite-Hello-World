<template>
    
  <div class="buttons">
    <button class="copy" v-on:click="copy" >Copy</button>
  
    <button class="toggleBackGroundColor" v-on:click="changeBackground" >Change Background Color</button>
  
    <button class="changeTitle" v-on:click="changeHeading">Change Title</button>
  
    <button class="deleteButton" v-on:click="deleteLast">Delete Last Instance</button>
  
  </div>
  
  <div class="all">
    <h1 class="title">
      Ethan Chen
    </h1>
    
    <img class ="picture" src = "https://media.ed.edmunds-media.com/toyota/tacoma/2020/oem/2020_toyota_tacoma_crew-cab-pickup_trd-off-road_fq_oem_1_1600.jpg" width=200px>
      
    <p class ="text">
  The image above is a Tacoma pickup truck made by the Japanese automaker Toyota. Toyota has been making the Tacoma pickup truck since 1995. The Tacoma has two engines options: 2.7-liter 4-Cylinder and the 3.5-liter V6. It has a miles per gallon of 20 in the city and 23 on the highway.
    </p>
      <button class="detailButton" v-on:mouseover="hoover">      
        Detail
    </button>
  
  </div>
  
  </template>
  
  <script setup>
  import { defineProps, reactive } from 'vue'
  defineProps({
    msg: String
  })
  const state = reactive({ count: 0 })
  </script>
  
  <script>    
 export default {
  
    methods: {  
copy(){
  const copyButton = document.querySelector('.copy');
  const orginalCard = document.querySelector('.all')
  copyButton.addEventListener("click", function(e){   
  const cloneCard = orginalCard.cloneNode(true);
  document.body.appendChild(cloneCard); 
  //cardAmount++;
});
},



deleteLast(){
  const deleteButton = document.querySelector(".deleteButton");
  deleteButton.addEventListener("click", function(e){ 
 // if (cardAmount > 1) {
  document.querySelector('.all:last-child').remove();
  // cardAmount--;
  //}
});
},

hoover(){
// This handler will be executed only once when the cursor
// moves over the unordered list
const detailButton = document.querySelector(".detailButton");
detailButton.addEventListener("mouseenter", function (e) {
  // highlight the mouseenter target
  e.target.style.background= "green";
  detailButton.focus();
});

detailButton.addEventListener("mouseleave", function (e) {
  // highlight the mouseenter target
  e.target.style.background = "";
  detailButton.blur()
});
},

hideText(){
  const detailButton = document.querySelector(".detailButton");
  detailButton.addEventListener("click", function(e){
   var paragraphs = wordsInCard;
  if (paragraphs.style.display === "none"){
    paragraphs.style.display = "block"
  } else {
    paragraphs.style.display = "none";
  }
  
});

},

changeBackground() {
  const toggleButton = document.querySelector(".toggleBackGroundColor");
  toggleButton.addEventListener("click", function(e){   
  var letters = '0123456789ABCDEF';
  var color = '#';
  for (var i = 0; i < 6; i++) {
    color += letters[Math.floor(Math.random() * 16)];
  }
  return document.querySelector('.all').style.backgroundColor = color;

});
},

changeHeading() {
  console.log("CLICKed");
const changeTitle = document.querySelector(".changeTitle");
const cardTitle = document.querySelector(".title");
changeTitle.addEventListener("click", function(e){   
  if (cardTitle.innerHTML === "Ethan Chen") {
    cardTitle.innerHTML = "Something Else";
  } else {
    cardTitle.innerHTML = "Ethan Chen";
  }
});
}
//classList.contains();
    }
  }
  </script>

  <style scoped>
  a {
    color: #42b983;
  }
  </style>
