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
import { generateTimelineItems } from '../functions'
import ThelineItem from '../components/TimelineItem.vue'

const timelineItems = generateTimelineItems()
</script>
