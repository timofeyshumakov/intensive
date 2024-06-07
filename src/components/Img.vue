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
  <img v-else :src="`/img/${src}`" :alt="alt" :title="alt"/>
</template>
<style lang="sass">
.main-img
  position: relative
  left: 5.8rem
</style>
