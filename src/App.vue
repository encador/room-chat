<script setup lang="ts">

import Board from "@/components/messages/Board.vue";
import Room from "@/components/Room.vue";
import Users from "@/components/Users.vue";
import Input from "@/components/Input.vue";
</script>

<template>
  <div id="container">
    <div id="application">
      <Board id="board"/>
      <Room id="room"/>
      <Users id="users"/>
      <Input id="input"/>
    </div>
  </div>

</template>

<style scoped>
#container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;

}


#application{
  display: grid;
  gap: 0.5rem;
  grid-template-columns: repeat(3, 150px);
  grid-template-rows: repeat(9, 40px);
}
#board{
  grid-column-end: span 2;
  grid-row-end: span 8;
}
#room{
  grid-row-end: span 2;
}
#users{
  grid-row-end: span 6;
}
#input{
  grid-column-end: span 3;
}


</style>
