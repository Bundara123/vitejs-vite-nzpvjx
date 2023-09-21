<template>
  <div><SwiperSlider /></div>
  <!-- <div class="overflow-x-scroll w-full">
    <div class="h-[35px] flex flex-row gap-1.5 px-2.5">
      <Tags
        v-for="(tag, index) in tags"
        v-model="tagAtive"
        :key="index"
        :title="tag.title"
        :id="tag.id"
        :isPopular="1"
      />
    </div>
  </div> -->
</template>
<script setup lang="ts">
import Tags from './components/Tags.vue';
import SwiperSlider from './components/SwiperSlider.vue';
const tagAtive = 1;
const tags = [];
for (let i = 0; i < 200; i++) {
  tags.push({
    id: i,
    title: `popular ${i}`,
  });
}
</script>
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
