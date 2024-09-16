<template>
  <div class="mt-7">
    <ul>
      <ThelineItem
        v-for="timelineItem in timelineItems"
        :key="timelineItem.hour"
        :timeline-item="timelineItem"
      />
    </ul>
  </div>
</template>

<script setup>
import ThelineItem from '../components/TimelineItem.vue'

defineProps(['timelineItems'])
</script>
