<script setup>
import { computed, ref } from 'vue'

const firstName = ref('Nguyên Thế')
const lastName = ref('Quốc')

const fullName = computed({
  get() {
    return firstName.value + ' ' + lastName.value
  },
  set(newValue) {
    [firstName.value, lastName.value] = newValue.split(',')
  }
})

const changeFullname = () => {
  fullName.value = "Nguyễn Thế,Quốc"
}
</script>

<template>
  <div>
    <p id="count">Fullname: {{ fullName }}</p>
    <p id="count">First name: {{ firstName }}</p>
    <p id="count">Last name: {{ lastName }}</p>
    <button @click="changeFullname">Change fullname</button>
  </div>
</template>