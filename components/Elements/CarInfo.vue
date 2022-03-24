<template>
  <div>
    <b-list-group>
      <b-list-group-item v-for="(item, index) in info" :key="index">
        <span class="title" v-text="item.title" />
        <span class="value" v-text="item.value" />
      </b-list-group-item>
    </b-list-group>
  </div>
</template>

<script>
export default {
  name: 'CarInfo',

  props: {
    info: {
      type: Array,
      required: true
    }
  }
}
</script>

<style scoped>
.title {
  color: #333131;
}

.value {
  color: #939393;
}
</style>
