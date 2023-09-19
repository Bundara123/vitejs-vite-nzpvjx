<script setup lang="ts">
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://v3.vuejs.org/api/sfc-script-setup.html#sfc-script-setup
import Tags from './components/Tags.vue';
const tags = [];
for (let i = 0; i < 200; i++) {
  tags.push({
    id: i,
    title: `popular ${i}`,
  });
}
</script>

<template>
  <div class="overflow-x-scroll w-full">
    <div class="h-[35px] flex flex-row gap-1.5 px-2.5">
      <Tags
        v-for="(tag, index) in tags"
        :key="index"
        :title="tag.title"
        :id="tag.id"
        :isPopular="1"
      />
    </div>
  </div>
  <div
    class="
      flex flex-row
      overflow-x-scroll
      space-x-24
      bg-purple-700
      p-4
      mx-14
      mt-5
      h-36
    "
  >
    <div class="bg-yellow-400 p-2 m-2">1</div>
    <div class="bg-yellow-400 p-2 m-2">2</div>
    <div class="bg-yellow-400 p-2 m-2">3</div>
    <div class="bg-yellow-400 p-2 m-2">4</div>
    <div class="bg-yellow-400 p-2 m-2">5</div>
    <div class="bg-yellow-400 p-2 m-2">6</div>
  </div>
  <HelloWorld color="#245682" />
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
