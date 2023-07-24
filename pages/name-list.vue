<script lang="ts" setup>
const list:Ref<string[]> = ref(['Billy','Bill','Bob','DIO']);
const newName:Ref<string>=ref('');


function addName() {
  list.value.push(newName.value);
}
</script>

<template>
  <div>
    <input type="text" v-model="newName">
    <button @click="addName()">Ajouter au tableau</button>
  </div>
  <div>
    <ul>
      <li v-for="item of list">{{ item }}</li>
    </ul>
  </div>
</template>

<style scoped></style>
