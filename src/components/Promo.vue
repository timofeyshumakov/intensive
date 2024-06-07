<script>
import Img from './Img.vue';
import Button from './Button.vue';
export default {
  components: { Img, Button},
  data() {
    return {
      sectionName: 'promo'
    };
  },
}
</script>
<template>
    <section :class="sectionName">
      <div :class="sectionName + '__container container'">
      <div class="block">
        <div class="top-title">ПЕРВЫЙ В МИРЕ ИНТЕНСИВ</div>
        <div class="title">ПО СКОРОСТНОМУ НАРАЩИВАНИЮ РЕСНИЦ</div>
        <div class="txt">ХОЧЕШЬ НАРАЩИВАТЬ 4D ЗА 1 ЧАС? НАУЧУ ТЕБЯ НА ИНТЕНСИВЕ 29 МАРТА</div>
        <div class="buttons">
          <Button class="button primary-button" link="#1" txt="ЗАПИСАТЬСЯ"/>
          <Button class="button secondary-button" link="#1" txt="ПРОГРАММА"/>
        </div>
      </div>
      <Img class="main-img" src="promo/main-img.png" alt="Image of a cat" />
      </div>
    </section>
</template>
<style scoped lang="sass">
@import "../vars.sass"

.promo
  padding-bottom: 13rem

.block
  display: flex
  flex-direction: column
  gap: 3.1rem
  margin-top: 6rem

.buttons
  display: flex
  flex-direction: row
  gap: 2rem

.top-title
  font-size: 1.43rem
  line-height: 1.15
  margin: 1.5rem 0 1rem

.title
  font-size: 3.58rem
  line-height: 1.18
  max-width: 39rem
  margin-top: -2.5rem

.txt
  font-size: 1.43rem
  line-height: 1.5
  max-width: 24rem

</style>