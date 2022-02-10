<script setup>
import SideBar from '@/components/SideBar.vue';
import MainContent from '@/components/MainContent.vue';
import RightBar from '@/components/RightBar.vue';
</script>

<template>
  <main class="main">
    <SideBar />
    <MainContent />
    <RightBar />
  </main>
</template>

<style scoped>
.main {
  display: grid;
  grid-template-columns: 0.9fr 2fr 1fr;
  /* padding: 0.4rem; */
}
</style>
