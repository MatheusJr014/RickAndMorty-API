<script setup>
import {ref} from 'vue'

let num = ref(0)

</script>
<template>

<nav class="navbar navbar-expand-lg">
  <div class="container-fluid">
    <router-Link class="navbar-brand" to="/">RickAndMorty</router-Link>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarNav">
      <ul class="navbar-nav">
        <li class="nav-item">
          <router-Link class="nav-link" aria-current="page" to="/">Inicio</router-Link>
        </li>
        <li class="nav-item">
          <router-Link class="nav-link" aria-current="page" to="/about">Sobre</router-Link>
        </li>
      </ul>
    </div>
  </div>
</nav>
<div class="main">
  <router-view></router-view>
</div>


</template>
<style>

nav{
  background-color: rgba(42,56,67,255)
  
}

body{
  background-color: rgba(42,56,67,255)
}
.nav-link, .navbar-brand{
  font-size: x-large;
  color:  rgba(157,202,59,255); 
  
}



</style>