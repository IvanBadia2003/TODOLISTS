<script setup lang="ts">
import UserInfo from '@/components/UserInfo.vue';
import { reactive } from 'vue';


const users  = reactive([
  {id: 0, name: 'Ivan', surname: 'Badia'},
  {id: 1, name: 'Diego', surname: 'Marica'},
  {id: 2, name: 'Diego', surname: 'Marica'}
])

function deleteUser(id: number) {
 const index = users.findIndex(user => user.id === id);
        users.splice(index, 1);
    
}
</script>

<template>
  <main>
    Lista de Users

    <UserInfo v-for="user in users" :id="user.id" :name="user.name" :surname="user.surname" @delete="deleteUser"/>
  </main>
</template>
