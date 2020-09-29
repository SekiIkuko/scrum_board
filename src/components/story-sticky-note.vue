<template>
  <v-card
    class="mx-auto"
    max-width="344"
    outlined
  >
    <v-list-item three-line>
      <v-list-item-content>
        <v-text-field
          label="id"
          placeholder="Placeholder"
          v-model="tubu.id"
        ></v-text-field>

        <v-text-field
          label="title"
          placeholder="Placeholder"
          v-model="tubu.title"
        ></v-text-field>
        <v-text-field
          label="point"
          placeholder="Placeholder"
          v-model="tubu.point"
        ></v-text-field>
        <v-select
          :items="items"
          label="お気持ち"
          v-model="tubu.feel"
        ></v-select>
      </v-list-item-content>
    </v-list-item>
  </v-card>

</template>
<script>
export default {
  data () {
    return {
      items: ['🐸', '🐯', '🐼', '🐷']
    }
  },
  props: {
    tubu: {
      type: Object,
      required: true
    }
  }
}
</script>