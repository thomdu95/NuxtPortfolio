<template>
  <v-footer
    padless
  >
    <v-card
      class="flex"
      flat
      tile
      dark
    >
      <v-card-title class="hFooter">
        <strong class="subheading">Si vous voulez me suivre !</strong>

        <v-spacer />
        <v-tooltip
          v-for="icon in icons"
          :key="icon.tool"
          top
        >
          <template v-slot:activator="{ on, attrs }">
            <v-btn
              class="mx-4"
              icon
              :href="icon.link"
              v-bind="attrs"
              v-on="on"
            >
              <v-icon size="24px">
                {{ icon.icon }}
              </v-icon>
            </v-btn>
          </template>
          <span>{{ icon.tool }}</span>
        </v-tooltip>
      </v-card-title>

      <v-card-text class="py-2 text-center fFooter">
        {{ new Date().getFullYear() }} — <strong>Thomas Jamais, fait avec <v-icon size="20px" style="color: #273133">
          mdi-heart
        </v-icon> !</strong>
      </v-card-text>
    </v-card>
  </v-footer>
</template>
<script>
export default {
  data: () => ({
    icons: [
      {
        icon: 'mdi-github',
        link: 'https://github.com/thomdu95',
        tool: 'Git Hub'
      },
      {
        icon: 'mdi-gitlab',
        link: 'https://gitlab.com/thomas.jamais95',
        tool: 'GitLab'
      },
      {
        icon: 'mdi-linkedin',
        link: 'www.linkedin.com/in/thomas-jamais-0968369a',
        tool: 'Linkedin'
      },
      {
        icon: 'mdi-grass',
        link: 'https://www.hamacattitude.fr',
        tool: 'HamacAttitude'
      }
    ]
  })
}
</script>

<style>
.hFooter {
    background-color: #273133 !important;
}

.fFooter {
    color: #273133 !important;
    background-color: white !important;
}
</style>
