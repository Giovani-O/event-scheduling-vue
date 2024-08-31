<template>
  <main class="container mx-auto my-8 space-y-8">
    <h1 class="text-4xl font-medium">Event Booking App</h1>
    <h2 class="text-2xl font-medium">All Events</h2>
    <section class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
      <EventCard
        v-for="(i, index) in 9"
        :key="index"
        title="Lorem Ipsum 2024"
        when="2024-10-01"
        description="Lorem Ipsum Dolor Sit Amet"
        @register="console.log('Tenoí')"
      />
    </section>
    <h2 class="text-2xl font-medium">Your Events</h2>
  </main>
</template>

<script setup>
import EventCard from '@/components/EventCard.vue'
</script>
