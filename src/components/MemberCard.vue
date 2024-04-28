<template>
  <div
    class="w-48 aspect-[3/4] bg-white rounded-md m-3 flex justify-start items-center flex-col"
  >
    <img
      class="bg-cover w-full rounded-md"
      :src="props.memberImage"
    />
    <p class="text-2xl font-bold p-4">{{ props.memberName }}</p>
    <p class="text-sm font-medium p-4">{{ props.description }}</p>
  </div>
</template>
<script setup>
import { defineProps } from 'vue'
const props = defineProps(['memberImage', 'description', 'memberName'])
</script>
<style scoped lang="css"></style>
