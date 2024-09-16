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
import { HOURS_IN_DAY } from '../constants'
import ThelineItem from '../components/TimelineItem.vue'

defineProps({
  timelineItems: {
    required: true,
    type: Array,
    validator(timelineItems) {
      return timelineItems.every(
        ({ hour }) => typeof hour === 'number' && hour >= 0 && hour < HOURS_IN_DAY
      )
    }
  }
})
</script>
