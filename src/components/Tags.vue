<template>
  <div
    class="
      bg-yellow
      pt-[9px]
      pb-[10px]
      px-[10px]
      rounded-md
      text-xs
      font-semibold
      capitalize
      whitespace-nowrap
      cursor-pointer
    "
  >
    {{ props.title }}
  </div>
</template>
<script lang="ts" setup>
interface Tag {
  title?: string;
}

const props = defineProps<Tag>();
</script>
