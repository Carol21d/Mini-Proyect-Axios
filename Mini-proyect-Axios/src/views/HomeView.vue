<script setup>
import { onMounted } from "vue";
import axios from "axios";

const characters = [];
const onSubmit = async () => {
  const res = await axios.get("https://rickandmortyapi.com/api/character/");
  
  characters.push(...res.data.results);
  console.log(res.data.results);
};

onMounted(onSubmit);
characters;





</script>

<template>



  
</template>
