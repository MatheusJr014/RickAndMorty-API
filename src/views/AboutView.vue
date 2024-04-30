<template>
<div class="container">
  <div class="card" style="width: 18rem;">
    <img src="/assets/Matheus.jpg" class="img-main" alt="...">
    <div class="card-body">
      <h5 class="card-title">Matheus Junior </h5>
      <p class="card-text"><b>RA:</b> 1967152</p>
      <p class="card-text"><b>CURSO:</b> Analise e Desenvolvimento de Sistemas</p>
      <p class="card-text"><b>TERMO:</b> 3°</p>
      <p class="card-text"><b>TURMA:</b> C</p>
    </div>
  </div>
</div>
<footer>
  <div class="dados">
    Unimar | ADS | {{ new Date().getFullYear() }}
  </div>
</footer>
</template>

<style scoped>
.container{
  max-width: 19rem;
}
footer{
  background-color:  rgba(19, 35, 47, 0.9); ;
  position:fixed;
  bottom: 0;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  height: 50px;
}
</style>
