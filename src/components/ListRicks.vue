<script setup>

const rickandmorty = defineProps(["name","url","gender","status","species","location","episode"]) 
const rickandmortyId = rickandmorty.url.split('/')[5]
const imageUrl = "https://rickandmortyapi.com/api/character/avatar/" + rickandmortyId + ".jpeg"
</script>


<template>
<div class="container" style="max-width: 19rem; flex: auto; ">
  <div class="card border-card mb-3">
        <img :src="imageUrl" class="img-main" alt="">
        <div class="card-body text-dark">
            <h5 class="card-title">{{ rickandmorty.name }}</h5>
            <br>
            <p class="card-text"><b>Especie:</b> {{ rickandmorty.species }}</p>
            <p class="card-text"><b>Gênero:</b> {{ rickandmorty.gender }}</p>
            <p class="card-text"><b>Status:</b> {{ rickandmorty.status }}</p>
            <p class="card-text"><b>Localização:</b> {{ rickandmorty.location }}</p>
            <p class="card-text"><b>Episodios Presentes:</b> {{ rickandmorty.episode.length}}</p>
      </div>
    </div>
</div>
</template>


<style> 

.card-body, .card,.img-main{
  background-color: rgba(19, 35, 47, 0.9);
  border-radius: 10px
}
b{
  color: rgba(157,202,59,255);
}
.card-title{
  color: rgba(157,202,59,255); 
  text-align: center;
}

.card-text{
    color:  rgba(61,161,73,255)
}

</style>