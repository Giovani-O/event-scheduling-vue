<template>
  <main class="container mx-auto my-8 space-y-8">
    <h1 class="text-4xl font-medium">Event Booking App</h1>
    <h2 class="text-2xl font-medium">All Events</h2>
    <section class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
      <EventCard v-for="(i, index) in 9" :key="index">
        <template #title> {{ 'Lorem Ipsum 2024' }} </template>
        <template #when> {{ '2024-10-01' }} </template>
        <template #description> {{ 'Lorem Ipsum Dolor Sit Amet' }} </template>
        <template #button>
          <BaseButton @click="console.log('Tenoí')">Register</BaseButton>
        </template>
      </EventCard>
    </section>
    <h2 class="text-2xl font-medium">Your Events</h2>
    <section class="grid grid-cols-1 gap-8">
      <BookedEvent v-for="(i, index) in 3" :key="index">
        <template #description> {{ 'Lorem Ipsum 2024' }} </template>

        <template #button>
          <BaseButton variant="danger">Cancel</BaseButton>
        </template>
      </BookedEvent>
    </section>
  </main>
</template>

<script setup>
import EventCard from '@/components/EventCard.vue'
import BookedEvent from './components/BookedEvent.vue'
import BaseButton from './components/BaseButton.vue'
</script>
