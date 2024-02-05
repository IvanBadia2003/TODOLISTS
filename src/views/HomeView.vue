<script setup lang="ts">
import Name from '@/components/Name.vue';
import { ref } from 'vue';

const userName = ref('Pedro')
const counter1 = ref(0)
const counter2 = ref(0)
</script>

<template>
  <main>
    <Name :name="userName" :counter="counter1" @increment="counter1++" />
    <Name :name="userName" :counter="counter2" @increment="counter2++"/>
  </main>
</template>
