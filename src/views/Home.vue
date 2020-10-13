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
      <v-btn
       @click="addTaskStickyNote(story.id)"
     >
     追加
     </v-btn>
      <v-col>
        todo
        <v-col>
          <v-row
            v-for="task in story.tasks"
            :key="task.id">
            <task-sticky-note
              :task="task"
            />
          </v-row>
        </v-col>
      </v-col>
      <v-col>
        doing
        <v-col>
          <v-row
            v-for="task in story.tasks"
            :key="task.id">
            <task-sticky-note
              :task="task"
            />
          </v-row>
        </v-col>
      </v-col>
      <v-col>
        done
        <v-col>
          <v-row
            v-for="task in story.tasks"
            :key="task.id">
            <task-sticky-note
              :task="task"
            />
          </v-row>
        </v-col>
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
      stories: [{id: 1, title: "hoge", point: 3, feel: '🐷', tasks: []},{id: 2, title: "hoge", point: 3, feel: '🐸', tasks: []}]
    }
  },
  methods: {
    addStoryStickyNote() {
      this.stories.push({id: null, title: null, point: null, feel: null, tasks: []})
    },
    addTaskStickyNote(target) {
      let task_list = this.stories.find((list) => {
        return (list.id == target)
      })
      task_list.tasks.push({content: null, time: null})
    }
  }
}
</script>
