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
      >
        <v-expand-transition>
          <div v-if="hover" class="d-flex transition-fast-in-fast-out orange darken-2 v-card--reveal display-3 white--text" style="height: 100%;"> $14.99 </div>
        </v-expand-transition>
      </v-img>
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

    <!-- <v-card-subtitle
      :href="project.link"
      target="_blank"
    >
      {{ project.shortDes }}
      <JudgeStar :nb-star="project.star" />
    </v-card-subtitle> -->
    <v-card-subtitle>
      <v-chip v-for="t in project.technos" :key="t.name" :color="t.color" :text-color="t.textColor" class="project-chip">
        {{ t.name }}
      </v-chip>
    </v-card-subtitle>

    <v-card-actions>
      <v-btn
        color="orange lighten-2"
        text
        @click="show = !show"
      >
        Détails
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
// import JudgeStar from '~/components/JudgeStar'
export default {
  components: {
    // JudgeStar
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

.project-chip {
  margin-bottom: 10px;
}

.v-card--reveal {
    align-items: center;
    bottom: 0;
    justify-content: center;
    opacity: .5;
    position: absolute;
    width: 100%;
}

.v-application--wrap {
    min-height: 100vh;
    justify-content: center;
}
</style>
