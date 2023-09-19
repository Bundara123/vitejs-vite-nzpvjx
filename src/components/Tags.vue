<template>
  <div
    :class="[
      'pt-[9px] pb-[10px] px-[10px] rounded-md text-xs font-semibold capitalize whitespace-nowrap cursor-pointer text-white',
      {
        'bg-yellow': isNew,
        'bg-green-300': isPremium,
        'bg-sky-500': isPopular,
      },
    ]"
  >
    {{ props.title }}
  </div>
</template>
<script lang="ts" setup>
import { ref, computed } from 'vue';
interface Tag {
  id?: number;
  title?: string;
  isNew?: boolean;
  isPremium: boolean;
  isPopular: boolean;
}

const props = withDefaults(defineProps<Tag>(), { isNew: true });
const isNew = computed(() => props.isNew === 1);
const isPopular = computed(() => props.isPopular === 1);
const isPremium = computed(() => props.isPremium === 1);
const emit = defineEmits<{
  click: [id: number];
}>();

function handleClick(id) {
  console.log('id', id);
  emit('click', id);
}
</script>
