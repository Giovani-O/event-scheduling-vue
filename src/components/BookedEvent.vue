<template>
  <RoundedCard>
    <div class="w-full flex justify-between items-center p-4">
      <div v-if="$slots.description" name="description-slot">
        <slot name="description"></slot>
      </div>

      <div v-if="$slots.button" name="button-slot">
        <slot name="button"></slot>
      </div>
    </div>
  </RoundedCard>
</template>

<script setup>
import RoundedCard from './RoundedCard.vue'
</script>
