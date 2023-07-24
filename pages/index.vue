<script lang="ts" setup> 
const first = ref('test');


function changeCa() {
  first.value ='Prout';
}
</script>

<template>
  <div>
    {{ first }}
    
  </div>
  <button @click="changeCa()">Ne cliquez pas !</button>
</template>

<style scoped></style>
