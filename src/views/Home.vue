<template>
  <div class="home">
    <v-row
      class="mb-6"
      no-gutters
      v-for="story in stories"
      :key="story.id"
    >
      <v-col>
        <story-sticky-note
          :tubu="story"
        />
      </v-col>
      <v-col>
        <task-sticky-note
        />
      </v-col>
    </v-row>
     <v-btn
       @click="addStoryStickyNote"
     >
     追加
     </v-btn>
  </div>
</template>

<script>
import StoryStickyNote from '@/components/story-sticky-note.vue'
import TaskStickyNote from '@/components/task-sticky-note.vue'

export default {
  name: 'Home',
  components: {
    StoryStickyNote,
    TaskStickyNote
  },
  data() {
    return {
      stories: [{id: 1, title: "hoge", point: 3, feel: '🐷'},{id: 2, title: "hoge", point: 3, feel: '🐸'}]
    }
  },
  methods: {
    addStoryStickyNote() {
      this.stories.push({id: null, title: null, point: null, feel: null})
    }
  }
}
</script>
