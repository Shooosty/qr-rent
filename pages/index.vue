<template>
  <div class="main">
    <b-container class="mt-2">
      <b-card-group deck>
        <CarCard
          v-for="card in CarModel.cars"
          :key="card.id"
          :price='card.price'
          :title="card.title"
          :img="card.img"
          :description="card.description"
          @click.native="onClickCard(card.id)"
        />
      </b-card-group>
    </b-container>

    <FooterLayout />
  </div>
</template>

<script>
import CarModel from '~/models/car-model'
import CarCard from '~/components/Cards/CarCard'
import FooterLayout from '~/components/Layout/FooterLayout'

export default {
  name: 'Index',

  components: { FooterLayout, CarCard },

  data() {
    return {
      CarModel
    }
  },

  methods: {
    onClickCard(ID) {
      this.$router.push(`cars/${ID}`)
    }
  }
}
</script>
