<template>
  <div>
    <b-carousel
      id="carousel"
      :interval="5000"
      fade
      class="carousel d-flex"
      controls
      indicators
    >
      <b-carousel-slide v-for="(photo, index) in photos" :key="index" class="image">
        <template #img>
          <img
            class="d-flex image"
            :src="require(`~/assets/photos/${photo}`)"
            alt="image"
          >
        </template>
      </b-carousel-slide>
    </b-carousel>
  </div>
</template>

<script>
export default {
  props: {
    photos: {
      type: Array,
      required: true
    }
  }
}
</script>

<style scoped>
.image {
  width: 100%;
  height: auto;
}
</style>
