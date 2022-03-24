<template>
  <b-card
    :title="title"
    class="card"
    :img-src="require(`~/assets/photos/${img}`)"
  >
    <b-card-text>
      <div class="d-flex justify-content-between align-items-center">
        <span class="description" v-text="description" />
        <span class="price" v-text="price" />
      </div>
    </b-card-text>
  </b-card>
</template>

<script>
export default {
  name: 'CarCard',

  props: {
    title: {
      type: String,
      required: true
    },
    img: {
      type: String,
      required: true
    },
    description: {
      type: String,
      required: true
    },
    price: {
      type: String,
      required: true
    }
  },
}
</script>

<style scoped lang="scss">
.card {
  margin: 1rem;
  min-height: 10rem;
  min-width: 12rem;
  cursor: pointer;

  &:hover {
    opacity: .5;
    transform: scale(1.1);
   }
}

.description {
  font-size: 1rem;
  color: #333131;
}

.price {
  font-size: 0.8rem;
  color: #939393;
}
</style>
