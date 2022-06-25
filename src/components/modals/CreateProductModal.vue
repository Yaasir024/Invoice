<template>
  <div class="create-modal" :class="openAddModal ? 'show' : 'hide'">
    <div class="invoice-content">
    <div class="header">
        <div class="close-btn" @click="$emit('closeAddModal')">
            x
        </div>
        <div class="title"><p>Add Product</p></div>
    </div>
        <p>Add New product easily and delightfully</p>
    </div>
  </div>
</template>

<script setup>
/*
  imports
  */
import { ref, reactive } from "vue";

const props = defineProps(["openAddModal",]);
const emit = defineEmits(['closeAddModal'])
</script>

<style scoped>
.create-modal {
    position: fixed;
    top: 0;
    right: 0;
    z-index: 40;
    height: 100vh;
    width: 700px;
    background: var(--dark-color1);
    transition: all 0.32s ease-in-out;
}
.invoice-content {
    
    padding: 20px 25px;
}
.show {
    opacity: 1;
    right: 0;
}
.hide {
    opacity: 0;
    right: -100%;
}
.close-btn {
  color: #fff;
  cursor: pointer;
  background-color: #212752;
  padding: 0;
  border: 0;
  border-radius: 50%;
  width: 32px;
  height: 32px;
  display: flex;
  align-items: center;
  justify-content: center;
}
.title {
    text-align: center;
    margin-top: 10px;
}
.title p {
    font-size: 26px;
    font-weight: 700;
    
}
</style>