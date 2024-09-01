<template>
  <RoundedCard>
    <header
      v-if="$slots.title"
      name="title-slot"
      class="p-4 font-medium text-xl border-b border-zinc-800"
    >
      <slot name="title"></slot>
    </header>

    <aside v-if="$slots.when" name="when-slot" class="p-4 border-b border-zinc-800">
      <slot name="when"></slot>
    </aside>

    <aside v-if="$slots.description" name="description-slot" class="p-4">
      <slot name="description"></slot>
    </aside>

    <footer v-if="$slots.button" name="button-slot" class="flex justify-end p-4">
      <slot name="button"></slot>
    </footer>
  </RoundedCard>
</template>

<script setup>
import RoundedCard from './RoundedCard.vue'
</script>
