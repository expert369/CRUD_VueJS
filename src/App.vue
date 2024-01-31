<script setup>
import {ref} from 'vue';
let counter = ref(0);

function add(){
  counter.value++;
}
function substract(){
  counter.value--;
}
</script>

<template>
<div>
  <h1>Simple Counter </h1>
  <h1>{{ counter }}</h1>
  <button @click="add()"> + </button>
  <button @click="substract()"> - </button>
</div>
</template>

<style scoped>
  body{
    text-align: center;
    background-color: rgb(228, 214, 136);
}

h1{
    font-family: sans-serif;
}

/* Counter button */
button{
    font-size: 20px;
    background-color: skyblue;
    height: 70px;
    width: 150px;
    border: 2px solid black;
    border-radius: 10px;
    align-items: center;
    margin-right: 5px;
    margin-left: 5px;
    margin-bottom: 200px;
}

div{
  text-align: center;
  border: 2px solid black;
  border-radius: 10px;
  background-image: linear-gradient(to bottom, gray,skyblue);
  background-image: url(https://i.pinimg.com/originals/48/4b/32/484b325cdb5bdd8bce6d8e3d131fda75.gif);
}
</style>