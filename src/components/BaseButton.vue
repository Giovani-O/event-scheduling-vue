<template>
  <button
    class="text-sm font-medium border rounded-full px-3 py-1 opacity-60"
    :class="[variants[variant] ?? variants.default]"
    @click="$emit('click')"
  >
    <slot> </slot>
  </button>
</template>

<script setup>
const variants = {
  default: 'border-zinc-800 bg-zinc-950 hover:bg-zinc-900',
  danger: 'border-rose-800 bg-rose-950 hover:bg-rose-900',
  success: 'border-green-800 bg-green-950 hover:bg-green-900'
}

defineEmits(['click'])
defineProps({
  variant: {
    type: String,
    default: 'default'
  }
})
</script>
