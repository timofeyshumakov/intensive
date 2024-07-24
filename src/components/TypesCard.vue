<script>
import Img from './Img.vue';
  export default {
    components: { Img },
    props: {
        card: Object
    }
  }
</script>
<template>
    <div class="card">
        <Img class="card-img" :src="`${card.img.src}`" alt=" " />
        <div class="card-txt">{{ card.txt }}</div>
    </div>
</template>
<style scoped lang="sass">
@import "../vars.sass"

.card
  display: flex
  align-items: center
  border: 1px red solid
  position: relative
  border: 3px solid #4c3d74
  border-radius: 30px
  background: #f2eef7
  min-height: 10rem


.card-img
  transform: translate(-50%, -1rem)
  position: absolute

.card-txt
  padding: 1rem 4rem 1rem 3.5rem
  font-size: 1.15rem
  line-height: 1.5
  color: #4c3d74

@media screen and (max-width: 768px)

  .card
    min-height: 6rem

  .card-img
    width: 58px

  .card:not(:nth-child(2)) .card-img
    transform: translate(-15%, -87%)

  .card:nth-child(2) .card-img
    transform: translate(-15%, -80%)
    right: 0

@media screen and (max-width: 360px)

  .card:nth-child(1) .card-txt, .card:nth-child(3) .card-txt
    padding-right: 1rem

  .card:nth-child(2) .card-txt
    padding-left: 1rem

</style>