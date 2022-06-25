<template>
  <div class="modal" :class="showModal ? 'show' : 'hide'">
    <div class="create-modal" v-if="createModal">
      <div class="header">
        <div class="close-btn" @click="$emit('closeCreateModal')">x</div>
        <div class="title"><p>New Order</p></div>
      </div>
      <p>Create New Order easily and delightfully</p>
    </div>
    <div class="edit-modal" v-if="editModal">
      <div class="header">
        <div class="close-btn" @click="$emit('closeEditModal')">x</div>
        <div class="title"><p>Edit Order</p></div>
      </div>
      <p>Edit Order {{editOrderId}}</p>
    </div>
  </div>
</template>

<script setup>
/*
  imports
  */
import { ref, reactive } from "vue";

const props = defineProps(["showModal","createModal", "editModal", "editOrderId"]);
const emit = defineEmits(["closeCreateModal", "closeEditModal"]);
</script>

<style scoped>
.modal {
  position: fixed;
  top: 0;
  right: 0;
  z-index: 40;
  height: 100vh;
  width: 700px;
  background: var(--dark-color1);
  transition: all 0.32s ease-in-out;
}
.create-modal {
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
