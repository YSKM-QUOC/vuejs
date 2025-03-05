<script setup>
import { reactive, ref, watch, watchEffect } from "vue";

const x = ref(0);
const y = ref(0);

const user = reactive({
  age: 18,
  class: {
    students: 0,
    name: "A",
  },
});

// Theo dõi cụ thể user.class.students
watch(
  () => user.class.students,
  (newVal, oldVal) => {
    console.log(`Students thay đổi từ ${oldVal} thành ${newVal}`);
  }
);

watchEffect(() => {
  console.log(`Giá trị x: ${x.value}, y: ${y.value}`);
});

const increment = () => {
  x.value++;
  y.value++;
};

const changeAge = () => {
  user.class.students++;
};
</script>

<template>
  <div>
    <h1>Watchers</h1>
    <button @click="increment">Increment</button>
    <p>{{ x }}, {{ y }}</p>

    <button @click="changeAge">Change Students</button>
    <p>{{ user.class.students }}</p>
  </div>
</template>
