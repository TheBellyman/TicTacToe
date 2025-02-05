<script setup>
import { ref } from 'vue';
const player = ref("X");
const field = ref(["_","_","_","_","_","_","_","_","_"])

const handlClick = (key) => {
  console.log(key)
  if (player.value === "X") {
    field.value[key] = "X"
    player.value = "O"
  } else {
    field.value[key] = "O"
    player.value = "X"
  }
};
</script>

<template>
  <main class="main">
    <h1>Hello World, lets play Tic Tac Toe</h1>
    <div>
      <div>
        <button @click="handlClick(0)">{{ field[0] }}</button>
        <button @click="handlClick(1)">{{ field[1] }}</button>
        <button  @click="handlClick(2)">{{ field[2] }}</button>
      </div>
      <div>
        <button @click="handlClick(3)">{{ field[3] }}</button>
        <button  @click="handlClick(4)">{{ field[4] }}</button>
        <button  @click="handlClick(5)">{{ field[5] }}</button>
      </div>
      <div>
        <button @click="handlClick(6)">{{ field[6] }}</button>
        <button  @click="handlClick(7)">{{ field[7] }}</button>
        <button  @click="handlClick(8)">{{ field[8] }}</button>
      </div>
    </div>
  </main>
</template>

<style scoped>
button {
  border: none;
  color: rgb(6, 5, 5);
  padding: 15px 32px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 16px;
  margin: 4px 2px;
  cursor: pointer;
  background-color: bisque;
}
</style>
