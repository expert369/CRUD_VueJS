<script setup>
import { ref } from 'vue';

let counter = ref(0);

function add() {
  counter.value++;
}

function subtract() {
  counter.value--;
}
</script>

<template>
  <div class="wrapper">
    <div class="container">
      <h1>Simple Counter </h1>
      <h1>{{ counter }}</h1>
      <button @click="add()"> + </button>
      <button @click="subtract()"> - </button>
    </div>
  </div>
</template>

<style scoped>
.wrapper {
  display: flex;
  align-items: center;
  justify-content: center;

}

.container {
  text-align: center;
  border: 2px solid black;
  border-radius: 10px;
  background-image: url(https://i.pinimg.com/originals/48/4b/32/484b325cdb5bdd8bce6d8e3d131fda75.gif);
  background-size: cover;
  width: 900px;
  height: 500px;
  margin: 0 auto; 
}

h1 {
  font-family: sans-serif;
}

button {
  font-size: 16px;
  background: linear-gradient(to bottom, #3498db, #2980b9);
  color: white;
  height: 40px;
  width: 100px;
  border: none;
  border-radius: 5px;
  margin: 5px;
  cursor: pointer;
  position: relative;
  overflow: hidden;
  animation: buttonAnimation 0.3s ease;
}

button:before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 100%;
  background: linear-gradient(to bottom, #2980b9, #3498db);
  transition: bottom 0.3s ease;
}

button:hover {
  animation: buttonHoverAnimation 0.3s ease;
  background: linear-gradient(to bottom, #2980b9, #2575ad);
}

button:hover:before {
  bottom: 0;
}

@keyframes buttonAnimation {
  from {
    transform: scale(0.8);
  }
  to {
    transform: scale(1);
  }
}

@keyframes buttonHoverAnimation {
  from {
    background: linear-gradient(to bottom, #3498db, #2980b9);
  }
  to {
    background: linear-gradient(to bottom, #2980b9, #2575ad);
  }
}



</style>
