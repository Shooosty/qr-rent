<template>
  <b-navbar type="dark" variant="dark" class="d-flex footer justify-content-center">
    <div class="d-inline-flex info">
      <a class="tel" href="tel: +995 598 669 999">+ 995 598 669 999</a>
      <span class="ml-1">EN RU ქართ</span>
    </div>
  </b-navbar>
</template>

<script>
export default {
  name: 'FooterLayout'
}
</script>

<style scoped>
.footer {
  -webkit-box-shadow: 0 -7px 8px 0 rgba(34, 60, 80, 0.2);
  -moz-box-shadow: 0 -7px 8px 0 rgba(34, 60, 80, 0.2);
  box-shadow: 0 -7px 8px 0 rgba(34, 60, 80, 0.2);
  height: 4rem;
  margin-top: auto;
}

.info, .tel {
  color: rgba(246, 246, 246, 0.93);
}
</style>
