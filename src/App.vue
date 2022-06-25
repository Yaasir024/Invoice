<script setup>
import { RouterLink, RouterView } from "vue-router";
import Nav from "@/components/Nav.vue";
import Header from "@/components/Header.vue";
</script>

<template>
  <div class="app-wrapper">
    <Nav />
    <main>
      <Header />
      <RouterView />
    </main>
  </div>
</template>

<style>
@import "@/assets/base.css";
main {
  width: 100%;
  padding: 0px 5px 25px 6px;
}
/* header {
  height: 40px;
  width: 100%;
  background: yellow;
  margin-bottom: 20px;
} */
.app-wrapper {
  /* max-width: 1200px; */
  margin: 0 auto;
  padding: 0 20px;
  background: var(--dark-color1);
  height: 100vh;
  display: flex;
}
/* width */
::-webkit-scrollbar {
  width: 10px;
}

/* Track */
::-webkit-scrollbar-track {
  background: #f1f1f1;
}

/* Handle */
::-webkit-scrollbar-thumb {
  background: #888;
}

/* Handle on hover */
::-webkit-scrollbar-thumb:hover {
  background: #555;
}
</style>
