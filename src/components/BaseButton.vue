<template>
  <button
    class="text-sm font-medium border rounded-full px-3 py-1 opacity-60"
    :class="{
      'border-zinc-800 bg-zinc-950 hover:bg-zinc-900': variant === 'default',
      'border-rose-800 bg-rose-950 hover:bg-rose-900': variant === 'danger',
      'border-green-800 bg-green-950 hover:bg-green-900': variant === 'success'
    }"
    @click="$emit('click')"
  >
    <slot> </slot>
  </button>
</template>

<script setup>
defineEmits(['click'])
defineProps({
  variant: {
    type: String,
    default: 'default',
    validator(value) {
      return ['default', 'danger', 'success'].includes(value)
    }
  }
})
</script>
