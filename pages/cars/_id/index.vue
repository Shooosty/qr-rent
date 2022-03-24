<template>
  <div class="main">
    <CarSlider :photos="photos" />
    <CarInfo :info="info" />
    <div class="d-flex justify-content-center">
      <b-button
        class="mt-3 mb-3"
        variant="dark"
        @click="onClickBack"
      >
        Back to list
      </b-button>
    </div>
    <FooterLayout />
  </div>
</template>

<script>
import CarSlider from '~/components/Elements/CarSlider'
import CarInfo from '~/components/Elements/CarInfo'
import CarModel from '~/models/car-model'
import FooterLayout from '~/components/Layout/FooterLayout'

export default {
  components: { FooterLayout, CarSlider, CarInfo },

  data() {
    return {
      CarModel
    }
  },

  computed: {
    photos() {
      return this.CarModel.cars.find(item => item.id === parseInt(this.$route.params.id)).photos
    },

    info() {
      return this.CarModel.cars.find(item => item.id === parseInt(this.$route.params.id)).info
    }
  },

  methods: {
    onClickBack() {
      this.$router.back()
    }
  }
}
</script>
