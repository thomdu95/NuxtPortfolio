<template>
  <div class="super-box">
    <div class="passionContainer">
      <div :id="passion.title" class="mybox">
        <div class="icon_bg" />
      </div>
      <div class="passionIcon">
        <v-icon v-text="passion.icon" />
      </div>
    </div>
    <div class="text">
      <p class="title">
        {{ passion.title }}
      </p>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    passion: {
      type: Object,
      required: true
    }
  },
  mounted () {
    this.applyCSS()
  },
  beforeUpdate () {
    this.applyCSS()
  },
  methods: {
    applyCSS () {
      const cssRule = `#${this.passion.title}::after {content: "${this.passion.description}"}`
      const style = document.createElement('style')
      style.type = 'text/css'
      // append the style node as child of current component
      this.$el.appendChild(style)
      style.innerHTML = cssRule
    }
  }

}
</script>

<style scoped>
</style>
