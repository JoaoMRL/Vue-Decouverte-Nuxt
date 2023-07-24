<script lang="ts" setup>
import { Dog } from '../entities';
import {Ref} from 'vue';

const wof:Ref<Dog> =ref<Dog>({name:'',breed:'',birthdate:''});
  // const emit = defineEmits=(['submitted']);
const emit = defineEmits<{
  (e:'submitted',wof:Dog):void
}>();


function handleSubmit() {
  emit('submitted',wof.value);
}
</script>

<template>
  <div>
    <form action="" method="post" @submit.prevent="handleSubmit()">
      <label for="name">name</label>
      <input type="text" id="name" placeholder="name" v-model="wof.name">
      <label for="breed">breed</label>
      <input type="text" id="breed" placeholder="breed"  v-model="wof.breed">
      <label for="birthdate">birthdate</label>
      <input type="date" id="birthdate" placeholder="birthdate"  v-model="wof.birthdate">
      <button >Submit</button>
    </form>
  </div>
</template>

<style scoped></style>
