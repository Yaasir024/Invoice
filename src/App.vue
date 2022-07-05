<script setup>
/*
  imports
  */
import { RouterLink, RouterView } from "vue-router";
import { ref, reactive, computed, onMounted } from "vue";
import Nav from "@/components/Nav.vue";
import Header from "@/components/Header.vue";
/*
Check Screen Size
*/
const mobile = ref(false);
const checkScreen = () => {
  if (window.innerWidth <= 750) {
    mobile.value = true;
    console.log("check screen");
  } else {
    mobile.value = false;
  }
};
onMounted(() => {
  console.log("created");
  window.addEventListener("resize", checkScreen);
});
</script>

<template>
  <div v-if="!mobile" class="app-wrapper">
    <Nav />
    <main>
      <Header />
      <RouterView />
    </main>
  </div>
  <div v-else class="mobile-message">
    <h2>Sorry, This App is not supported on mobile devices</h2>
    <p>Kindly use on a computer or Tablet</p>
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
.mobile-message {
  display: flex;
  flex-direction: column;
  text-align: center;
  justify-content: center;
  align-items: center;
  height: 100vh;
}
.mobile-message p {
  margin-top: 16px;
}

/* Scrollbar Styles */
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
