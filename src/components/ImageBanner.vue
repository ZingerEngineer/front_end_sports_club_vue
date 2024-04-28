<template>
  <div class="wrapper w-full flex justify-center items-center relative">
    <div
      class="text-wrapper flex flex-col absolute w-full items-center mt-20 text-white"
    >
      <img
        class="team-logo w-80"
        :src="teamLogo"
      />
      <p
        id="title"
        class="text-4xl font-bold"
      >
        {{ props.title }}
      </p>
      <p
        id="text"
        class="text-xl font-medium"
      >
        {{ props.text }}
      </p>
    </div>
    <div
      id="image-div"
      class="image w-full overflow-hidden"
    ></div>
  </div>
</template>
<script setup>
import { defineProps } from 'vue'
import teamLogo from '../assets/team_logo.png'
const props = defineProps(['title', 'text'])
</script>
<style lang="css">
#image-div {
  background: url('../assets/landing_image.jpg');
  background-size: cover;
  background-color: #101b33;
  background-repeat: no-repeat;
  background-blend-mode: overlay;
  height: 60vh;
  background-position-y: center;
}
</style>
