<template>
  <div class="border border-zinc-800 bg-zinc-900 rounded-md">
    <h3 class="p-4 font-medium text-xl border-b border-zinc-800">{{ title }}</h3>
    <p class="p-4 border-b border-zinc-800">{{ when }}</p>
    <p class="p-4">{{ description }}</p>

    <section class="flex justify-end p-4">
      <BaseButton @click="$emit('register')"><pre>Register</pre></BaseButton>
    </section>
  </div>
</template>

<script setup>
import BaseButton from './BaseButton.vue'

defineProps({
  title: String,
  when: String,
  description: String
})

defineEmits(['register'])
</script>
