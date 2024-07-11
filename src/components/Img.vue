<script>
export default {
  props: ['class', 'src', 'alt'],
  computed: {
    format() {
        return this.src.substring(this.src.lastIndexOf('.') + 1);
    },
  }
}
</script>
<template>
  <picture v-if="format !== 'svg'">
    <img :class="class" :src="`/img/${src}`" :alt="alt" :title="alt"/>
  </picture>
  <img v-else :class="class" :src="`/img/${src}`" :alt="alt" :title="alt"/>
</template>
<style lang="sass">
.main-img
  position: relative
  left: 5.8rem

.tariff-img
  position: absolute
  top: -10%
  right: -10%
  width: 9rem
  height: 9rem

.advantages .item-img
  width: 4.8rem
  height: 4.8rem

.presentation-main-img
  position: relative
  top: 3.3rem
  left: -0.6rem

</style>
