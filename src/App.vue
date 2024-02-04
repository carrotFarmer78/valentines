<template>

<div class="card">
  <div v-if="!isHiddenNo" class="title">
    💙~ Will you be my valentines? ~💜
  </div>
  <div v-else class="title">How could you do this to me?😔 </div>

  <div v-if="!desic" class="buttons">
    <button @click="toggleYes" class="yesB">Yes 😍😍😍😍</button>
    <button @click="toggleNo" class="noB">Ew 🤢</button>
  </div>
  <img v-if="isHiddenYes" src="../src/gifs/yippie.gif">
  <img v-if="isHiddenNo" src="../src/gifs/wolf.gif">
</div>
</template>


<script setup>
import {ref} from 'vue';
const isHiddenYes = ref(false);
const isHiddenNo = ref(false);
const desic = ref(false);

function toggleYes(){
  isHiddenYes.value = !isHiddenYes.value
  toggledesic()
}
function toggleNo(){
  isHiddenNo.value = !isHiddenNo.value
  toggledesic()
}
function toggledesic(){
  desic.value = !desic.value
}


</script>

<style>

body{
  background-color: pink;
}
.title{
  text-align: center;
  padding-top: 100px;
  font-size: 90px;
  font-family: 'Comic Neue', cursive;
}
.card{
  display: flex;
  justify-content: center;
  flex-direction: column;
}
.buttons{
  display: flex;
  justify-content: center;
}
button{
  margin: 30px;
  padding: 15px 80px;

  border-radius: 25px;
  font-size: 90px;
}
img{
  display: block;
  margin-left: auto;
  margin-right: auto;
  width: 33%;
}
</style>