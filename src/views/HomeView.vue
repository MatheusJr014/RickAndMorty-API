<script setup>
import { onMounted, reactive,ref } from 'vue';
import ListRicks from '../components/ListRicks.vue'; 
let ricks = reactive(ref()); 

onMounted(() => {
  fetch("https://rickandmortyapi.com/api/character")
  .then(response => response.json())
  .then(response => {
    ricks.value = response.results;
    console.log(ricks);
  })
})
</script>
<template>
  <main>
  <div class="container">
        <ListRicks v-for="rickandmorty in ricks"
                :key="rickandmorty.name"
                :name="rickandmorty.name"
                :url="rickandmorty.url"
                :gender="rickandmorty.gender"
                :species="rickandmorty.species"
                :status="rickandmorty.status"
                :location="rickandmorty.location.name"
                :episode="rickandmorty.episode"
                />
  </div> 
<footer class="">
  <div class="dados">
    Unimar | ADS | {{ new Date().getFullYear() }}
  </div>
</footer>
  </main>
</template>

<style> 
.container{
  display: flex; 
  flex-wrap: wrap;
}

footer{
  background-color:   rgba(19, 35, 47, 0.9);
  position:relative;
  bottom: 0;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  height: 50px;
}
.dados{
  color: rgba(157,202,59,255); 
}


</style> 
