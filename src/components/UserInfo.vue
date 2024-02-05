<script setup lang="ts">

const props = defineProps<{
    id: number
    name: string,
    surname: string
}>();

const emit = defineEmits(['delete'])
</script>


<template>
    <div class="user-info">
        <div>ID {{ id }}</div>
        <div>Name: {{ name }}</div>
        <div>Surname: {{ surname }}</div>
        <button @click="emit('delete', id)">Eliminar</button>
    </div>
</template>