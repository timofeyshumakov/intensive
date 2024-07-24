<script>
export default {
  props: ['class', 'src', 'alt'],
}
</script>

<template>
  <img :class="class" :src="`assets/img/${src}`" :alt="alt" :title="alt"/>
</template>

<style lang="sass">

.tariff-img
  position: absolute
  top: -10%
  right: -10%
  width: 9rem
  height: 9rem



</style>
