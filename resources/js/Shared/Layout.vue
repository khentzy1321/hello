<template>
<nav class="navbar navbar-expand-lg bg-light opacity-75">
  <div class="container-fluid">
    <a class="navbar-brand" href="#">Musics</a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse d-flex justify-content-end" id="navbarNav">
      <ul class="navbar-nav">

        <li class="nav-item">
          <Link class="nav-link"  :class="{'selected': $page.component=='Home'}" href="/">Home</Link>
        </li>
        <li class="nav-item">
          <Link class="nav-link" :class="{'selected': $page.component=='Mymusic'}" href="/music">My Musics</Link>
        </li>
        <li class="nav-item">
          <Link class="nav-link" :class="{'selected': $page.component=='MusicVideos'}" href="/video"> Music Videos</Link>
        </li>
        <li class="nav-item">
          <Link class="nav-link" :class="{'selected': $page.component=='About'}" href="/about">About</Link>
        </li>
        <li class="nav-item">
          <Link class="nav-link " :class="{'selected': $page.component=='Contact'}" href="/contact">Contact Us</Link>
        </li>
      </ul>
    </div>
  </div>
</nav>

 <section class="container bg-white p-4 rounded-3 mt-4 bg-opacity-50">
    <slot />
    <footer class="text-center mt-5">
    Copyright &copy; @2022. All rghts Reserved.
</footer>
 </section>


</template>

<script setup>
import { Link } from '@inertiajs/inertia-vue3'

</script>

<style scoped>
.section{
    background-color: #ffff;
    opacity: 0.7;
}
.selected {
    color: green;
    font-weight: bold;
}
</style>
