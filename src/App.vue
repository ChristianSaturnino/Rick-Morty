<script setup>
import {ref} from 'vue'
</script>

<template>
<!--menu bootstrap-->
<nav class="navbar navbar-expand-lg bg-body-tertiary" data-bs-theme="dark">
  <div class="container-fluid">
    <!-- <a class="navbar-brand" href="#">App Vue</a> -->
    <router-link class="navbar-brand" to="/">    <a class="navbar-brand" href="#">
      <img src="C:\Users\chris\OneDrive\Área de Trabalho\Estudos\TrabalhosFaculdade\RickMorty\RickMorty\src\assets\image-removebg-preview (6).png" alt="Logo" width="50" height="50" class="d-inline-block align-text-top m-1">
    </a></router-link>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNavAltMarkup" aria-controls="navbarNavAltMarkup" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarNavAltMarkup">
      <div class="navbar-nav">
        <router-link class="nav-link" arial-current="page" to="/">Inicio</router-link>
        <!-- <a class="nav-link" href="#">Features</a> -->
        <router-link class="nav-link" arial-current="page" to="/about">Sobre</router-link>
        <!-- <a class="nav-link" href="#">Pricing</a> -->
        <!-- <a class="nav-link disabled" aria-disabled="true">Disabled</a> -->
      </div>
    </div>
  </div>
</nav>

<div class="mais">
  <router-view></router-view>
</div>

<footer class="bg-dark text-light">
  <div>
    Unimar | ADS | {{ new Date().getUTCFullYear() }}
  </div>
</footer>

</template>

<style>
footer{
  bottom: 0;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  height: 40px;
  margin-top: 30px
}



body{
    background-color: rgb(27, 28, 27)
}
</style>      