<template>
  <v-card
    class="mx-auto"
    max-width="344"
    outlined
  >
    <v-list-item three-line>
      <v-list-item-content>
        <v-text-field
          label="content"
          placeholder="Placeholder"
          v-model="task.content"
        ></v-text-field>

        <v-text-field
          label="time"
          placeholder="Placeholder"
          v-model="task.time"
        ></v-text-field>
      </v-list-item-content>
    </v-list-item>
  </v-card>
</template>
<script>
export default {
  props: {
    task: {
      type: Object,
      required: true
    }
  }
}
</script>