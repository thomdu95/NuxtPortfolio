<template>
  <v-card
    class="mx-auto"
    max-width="344"
  >
    <a
      :href="project.link"
      target="_blank"
      class="myLink"
    >
      <v-img
        :src="project.img"
        height="200px"
        :href="project.link"
        target="_blank"
      />
    </a>

    <v-card-title>
      <a
        :href="project.link"
        target="_blank"
        class="myLink"
      >
        {{ project.name }}
      </a>
    </v-card-title>

    <v-card-subtitle
      :href="project.link"
      target="_blank"
    >
      {{ project.shortDes }}
      <JudgeStar :nb-star="project.star" />
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
          {{ project.description || "lol" }}
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
    project: {
      type: Object,
      required: true
    }
  },

  data: () => ({
    show: false
  })

}
</script>

<style>
.myLink {
    color: #11270B;
    text-decoration: none;
}
</style>
