<template>
  <div class="home">
    <story-sticky-note
      v-for="story in stories"
      :key="story.id"
     />
  </div>
</template>

<script>
import StoryStickyNote from '@/components/story-sticky-note.vue'

export default {
  name: 'Home',
  components: {
    StoryStickyNote
  },
  data() {
    return {
      stories: [{id: 1, title: "hoge", point: 3}]
    }
  }
}
</script>
