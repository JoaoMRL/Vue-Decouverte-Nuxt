<script lang="ts" setup>
import { Dog } from 'entities';
const { data: count,refresh } = await useFetch<Dog>('http://localhost:8000/api/dog')

async function addDog(dog:Dog){
  await $fetch('http://localhost:8000/api/dog',{
    method:'POST',
    body:dog
  });
  refresh();
}

</script>

<template>
  <div>
    <FormDog @submitted="addDog($event)" />
  </div>
  <div>
    <p v-for="item of count">
      <DogItem :doggy="item" />
    </p>
  </div>
  
</template>

<style scoped></style>
