<template>
  <div class="flex w-full flex-col">
    <NavBar />
    <imageBanner
      title="ELECTROS"
      text="We aim for the best."
    />
    <div
      class="home-page-wrapper w-full bg-gray-800 flex flex-row items-center justify-center"
    >
      <MemberCard
        v-for="member in members"
        :key="member.name"
        :memberImage="member.image"
        :memberName="member.name"
        :description="member.description"
      />
    </div>
  </div>
</template>

<script setup lang="ts">
import ref from 'vue'
import NavBar from '../components/NavBar.vue'
import imageBanner from '../components/ImageBanner'
import MemberCard from '../components/MemberCard'
import first_mem from '../assets/first_mem.jpg'
import second_mem from '../assets/second_mem.jpg'
import third_mem from '../assets/third_mem.jpg'
const members = [
  {
    image: first_mem,
    name: 'Mohamed Khedr',
    description: 'A personal trainer.'
  },
  { image: second_mem, name: 'Ali Badr', description: 'A football player.' },
  {
    image: third_mem,
    name: 'Ahmed Monir',
    description: 'A new football member.'
  }
]
</script>

