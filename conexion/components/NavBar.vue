<template>
    <nav class="navbar navbar-expand-lg navbar-light " style="background:darkblue">
  <a class="navbar-brand" href="#" style="color:white">ADATAR</a>
  <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
    <span class="navbar-toggler-icon"></span>
  </button>

  <div class="collapse navbar-collapse" id="navbarSupportedContent">
    <ul class="navbar-nav mr-auto">
      <li class="nav-item active">
        <router-link class="nav-link" to="/" style="color:white">INICIO</router-link>
      </li>
      <li class="nav-item">
        <router-link class="nav-link" to="/user" style="color:white">USUARIOS</router-link>
      </li>
    </ul>
  </div>
</nav>
</template>