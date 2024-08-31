<template>
  <div class="border border-zinc-800 bg-zinc-900 rounded-md">
    <h3 class="p-4 font-medium text-xl border-b border-zinc-800">{{ title }}</h3>
    <p class="p-4 border-b border-zinc-800">{{ when }}</p>
    <p class="p-4">{{ description }}</p>

    <section class="flex justify-end p-4">
      <button
        class="text-sm font-medium border border-zinc-800 rounded-full px-3 py-1 bg-zinc-950 hover:bg-zinc-900"
        @click="$emit('register')"
      >
        Register
      </button>
    </section>
  </div>
</template>

<script setup>
defineProps({
  title: String,
  when: String,
  description: String
})

defineEmits(['register'])
</script>
