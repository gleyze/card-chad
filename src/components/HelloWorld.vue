<template>
  <h1>{{ msg }}</h1>

<!-- My custom code -->
<button class="outsideBtn" v-on:click="duplicate">Duplicate</button>
<button class="outsideBtn" v-on:click="background">Background</button>
<button class="outsideBtn" v-on:click="heading">Heading</button>
<button class="outsideBtn" v-on:click="deleter">Delete</button>

<div class="card" v-on:mouseover="hoover">
  <h1 class="title">Chad of Cyber IST</h1>

  <img class="giaImg" src="https://media.discordapp.net/attachments/963095262363017246/1020131830323744788/unknown.png?width=468&height=468" alt="Professor Giacobe">
  
<div class="textbox">
  <details>
    <summary class="haxbtn">Details</summary>
    <p class="description pScale">Professor Giacobe may look like a simple man but perceptions can be misleading. Underneath the facade of a simple college of IST professor lies the holiness of an <strong>IST GOD</strong>!</p>
  </details>

  </div>
</div>


<button id="duplicateBtn" class="btn">Duplicate</button>

<button id="changeBGColorBtn" class = "btn">Change Background Color</button>

<button id="changeTitleBtn" class = "btn">Change title</button>

<button id="deleteBtn" class = "btn">Delete</button>

<section class="all">
<header class ="header">
  <h1 id = "mainTitle" class="title">Shiny Fuecoco!!!:)</h1>
  </header>
<section class="paragraph">
  <img src = "https://www.serebii.net/Shiny/SV/new/909.png" width=300px>
    
  <p>
This is shiny Fuecoco. A low shiny quality Fuecoco. Fuecoco best boy. Fuecoco head empty. Fuecoco is a bipedal crocodilian Pokémon with a mostly red body and a white stomach and face. Its body contains a small flame sac, which constantly leaks fire energy due to its size. Fuecoco is laid-back and does things at its own pace. It enjoys eating, and it will rush towards any food it sees.
  </p>

    <button id = "detailBtn" class="detailButton">Detail</button>
    </a>
   </section>
  
</section>


  <p>
    <a href="https://vitejs.dev/guide/features.html" target="_blank">
      Vite Documentation
    </a>
    |
    <a href="https://v3.vuejs.org/" target="_blank">Vue 3 Documentation</a>
  </p>

  <button type="button" @click="state.count++">count is: {{ state.count }}</button>
  <p>
    Edit
    <code>components/HelloWorld.vue</code> to test hot module replacement.
  </p>
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
    hoover() {
      document.querySelectorAll(".card").forEach((item) => {
        if(!item.classList.contains("hoverCard")){
          item.classList.add("hoverCard");
          console.log(item);
        }
        else{
          item.classList.remove("hoverCard");
          console.log(item);
        }
      });
    },
    
    duplicate() {
      const cloneCard = document.querySelector(".card").cloneNode(true);
      document.body.appendChild(cloneCard);
      console.log(cloneCard);    
    },

    background() {
      document.querySelectorAll(".card").forEach((item) => {
        if(!item.classList.contains("basic")){
          item.classList.add("basic");
          console.log(item);
        }
        else{
          item.classList.remove("basic");
          console.log(item);
        }
      });
    },

    heading() {
      document.querySelectorAll(".title").forEach((item) => {   
        if(item.innerHTML=="something else"){
          item.innerHTML="Chad of Cyber IST";
        }
        else{
          item.innerHTML="something else";
        }
      });
    },

    //Kinda borked rn
    deleter(){
      document.querySelector(".card:last-child").remove();
      console.log(card);
    }
  }
}
</script>

<style scoped>
a {
  color: #42b983;
}
</style>
