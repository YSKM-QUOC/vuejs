<script setup>
import { useCounter } from "./composable/useCounter";
import { useMouse } from "./composable/useMouse";
const { count, increment, decrement } = useCounter();
const { x, y } = useMouse();
</script>

<template>
  <div>
    <h1>Composable</h1>
    <p>Count: {{ count }}</p>
    <button @click="increment">Increment</button>
    <button @click="decrement">Decrement</button>

    <p>X: {{ x }}, Y: {{ y }}</p>
  </div>
</template>