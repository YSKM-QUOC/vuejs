<script setup>
import { ref } from "vue";

const submit = (event) => {
  if (event.type === "keyup" && event.altKey && event.key === "Enter") {
    alert("Xin chào");
  } else if (event.type === "click" && event.shiftKey) {
    alert("Xin chào");
  }
};
</script>

<template>
  <div>
    <h1>Event handling</h1>
    <!-- Bắt sự kiện Alt + Enter -->
    <input @keyup="submit" placeholder="Nhập tên của bạn" />

    <!-- Bắt sự kiện Shift + Click -->
    <button @click="submit">Submit</button>
  </div>
</template>
