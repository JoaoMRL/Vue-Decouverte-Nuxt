<script lang="ts" setup>
import { Dog } from 'entities';
const { data: count } = await useFetch<Dog>('http://localhost:8000/api/dog')


</script>

<template>
  <div>
    <p v-for="item of count">
      <DogItem :doggy="item" />
    </p>
  </div>
</template>

<style scoped></style>
