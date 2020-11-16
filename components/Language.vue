<template>
  <v-card
    class="mx-auto"
    max-width="344"
  >
    <v-img
      :src="language.img"
      height="200px"
    />

    <v-card-title>
      {{ language.name }}
    </v-card-title>

    <v-card-subtitle>
      Je code en  {{ language.name }} depuis {{ language.years }} ans.
      <JudgeStar :nb-star="language.star" />
    </v-card-subtitle>

    <v-card-actions>
      <v-btn
        color="orange lighten-2"
        text
        @click="show = !show"
      >
        Explication
      </v-btn>

      <v-spacer />

      <v-btn
        icon
        @click="show = !show"
      >
        <v-icon>{{ show ? 'mdi-chevron-up' : 'mdi-chevron-down' }}</v-icon>
      </v-btn>
    </v-card-actions>

    <v-expand-transition>
      <div v-show="show">
        <v-divider />

        <v-card-text>
          {{ language.description || "lol" }}
        </v-card-text>
      </div>
    </v-expand-transition>
  </v-card>
</template>

<script>
import JudgeStar from '~/components/JudgeStar'
export default {
  components: {
    JudgeStar
  },
  props: {
    language: {
      type: Object,
      required: true
    },
    nb: {
      type: Number,
      required: true
    }
  },

  data: () => ({
    show: false
  })

}
</script>

<style>
    /* data-aos="flip-left"
    :data-aos-delay="(nb * 100) + 100" */
</style>
