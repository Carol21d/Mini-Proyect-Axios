<script setup>
import { onMounted } from "vue";
import axios from "axios";

const characters = [];
const onSubmit = async () => {
  // const res = await axios.get("https://rickandmortyapi.com/api/character/");
  // characters.push(...res.data.results);
  // console.log(res.data.results);
 const res = await axios.post("https://rickandmortyapi.com/api/character/");
   // const res = await axios.get("https://rickandmortyapi.com/api/character/");
};

onMounted(onSubmit);
characters;





</script>

<template>
  <div class="wrapper">
    <div class="wrapper-card">
      <div v-for="character in characters" :name="character.name">
        {{ character.name }}
        

      </div>

    </div>


  </div>



  
</template>
