<script setup lang="ts">
interface Props {
  message: string;
  itsMine: boolean;
  image?: string;
}

defineProps<Props>();
</script>
<template>
  <div :class="{ 'flex': true, 'justify-end': itsMine, 'justify-start': !itsMine }">
    <div :class="{ 'bg-blue-200': itsMine, 'bg-gray-300': !itsMine }" class="text-black p-2 rounded-lg max-w-xs">
      <span class="capitalize">{{ message }}</span>
      <img v-if="image" :src="image" alt="YesNoImage" class="w-52 h-52 object-cover rounded-md" />
    </div>
  </div>
</template>
