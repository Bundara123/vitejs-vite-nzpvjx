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
    @click="handleClick(props.id)"
  >
    {{ props.title }}
  </div>
</template>
<script lang="ts" setup>
interface Tag {
  id?: number;
  title?: string;
}

const props = defineProps<Tag>();
const emit = defineEmits<{
  click: [id: number];
}>();

function handleClick(id) {
  console.log('id', id);
  emit('click', id);
}
</script>
