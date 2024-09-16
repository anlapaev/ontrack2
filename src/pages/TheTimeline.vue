<template>
  <div class="mt-7">
    <ul>
      <ThelineItem
        v-for="timelineItem in timelineItems"
        :key="timelineItem.hour"
        :timeline-item="timelineItem"
        :activity-select-options="activitySelectOptions"
      />
    </ul>
  </div>
</template>

<script setup>
import { validateTimelineItems, validateSelectOptions } from '../validators'
import ThelineItem from '../components/TimelineItem.vue'

defineProps({
  timelineItems: {
    required: true,
    type: Array,
    validator: validateTimelineItems
  },
  activitySelectOptions: {
    required: true,
    type: Array,
    validator: validateSelectOptions
  }
})
</script>
