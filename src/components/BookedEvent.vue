<template>
  <article class="bg-zinc-900 border border-zinc-800 rounded-md p-4">
    <div class="w-full flex justify-between">
      <div name="description-slot">
        <slot name="description"></slot>
      </div>

      <div name="button-slot">
        <slot name="button"></slot>
      </div>
    </div>
  </article>
</template>

<script setup></script>
