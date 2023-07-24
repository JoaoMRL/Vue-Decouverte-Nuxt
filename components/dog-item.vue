<script lang="ts" setup>
import{Dog}from '../entities';
const props = defineProps<{doggy:Dog}>()

</script>

<template>
  <div>
    {{ props.doggy.name }} est un(e) {{ props.doggy.breed }}
  </div>
</template>

<style scoped></style>
