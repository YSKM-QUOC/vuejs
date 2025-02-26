<script setup>
import { ref, reactive } from "vue";
const color = ref("blue");
const background = ref("yellow");
const fontSize = ref(30);

const styleObject = reactive({
  border: "none",
  borderRadius: "6px",
});
</script>

<template>
  <div>
    <button
      :style="[
        {
          color,
          background,
          fontSize: fontSize + 'px',
        },
        styleObject,
      ]"
    >
      Button
    </button>
  </div>
</template>