<script setup lang="ts">
import { ref } from 'vue';


// let count = ref(0);

const props = defineProps<{
name: string,
counter: number
}>();

const emit = defineEmits(['increment'])

</script>

<template>
    <h1>Hola {{ name }}</h1>
    <button @click="emit('increment')">aumentar</button>
    <h1>{{ counter }}</h1>
</template>