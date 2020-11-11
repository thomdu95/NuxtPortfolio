// :data-aos="index % 2 == 0 ? 'flip-right' : 'flip-left'"
<template>
  <div class="timeline">
    <div class="icon" />
    <div class="date-content">
      <div class="date-outer">
        <span class="date">
          <span class="month">{{ elem.month || "2 Years" }}</span>
          <span class="year">{{ elem.year || 2013 }}</span>
        </span>
      </div>
    </div>
    <div class="timeline-content">
      <h5 class="title">
        {{ elem.title || "Visual Art &amp; Design" }}
      </h5>
      <p class="subtitle">
        {{ elem.company }}
      </p>
      <p class="description">
        {{ elem.description || "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed efficitur\
        ex sit amet massa scelerisque scelerisque. Aliquam erat volutpat. Aenean\
        interdum finibus efficitur. Praesent dapibus dolor felis, eu ultrices\
        elit molestie." }}
      </p>
      <v-chip v-for="t in elem.technos" :key="t.name" :color="t.color" :text-color="t.textColor">
        {{ t.name }}
      </v-chip>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    elem: {
      type: Object,
      required: true
    },
    index: {
      type: Number,
      required: true
    }
  }
}
</script>

<style>
.subtitle {
    font-size: 1.3rem;
}

.v-chip {
    margin-right: 10px;
}

</style>
