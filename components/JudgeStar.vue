<template>
  <p class="mt-2">
    <v-icon
      v-for="i in 5"
      :key="i"
      color="orange lighten-2"
    >
      {{ i > nbStar ? 'mdi-star-outline' : 'mdi-star' }}
    </v-icon>
  </p>
</template>

<script>
export default {
  props: {
    nbStar: {
      type: Number,
      required: true
    }
  }
}
</script>

<style>
</style>
