<script>
import Img from './Img.vue';
import Button from './Button.vue';
export default {
  components: { Img, Button}
}
</script>

<template>
    <section class="promo">
      <div class="promo__container container">
      <div class="promo__block">
        <div class="top-title">ПЕРВЫЙ В МИРЕ ИНТЕНСИВ</div>
        <div class="title">ПО СКОРОСТНОМУ НАРАЩИВАНИЮ РЕСНИЦ</div>
        <div class="txt">ХОЧЕШЬ НАРАЩИВАТЬ 4D ЗА 1 ЧАС? НАУЧУ ТЕБЯ НА ИНТЕНСИВЕ 29 МАРТА</div>
        <div class="buttons">
          <Button buttonClassName="button primary-button" link="#tariffs" txt="ЗАПИСАТЬСЯ"/>
          <Button buttonClassName="button secondary-button" link="#programm" txt="ПРОГРАММА"/>
        </div>
      </div>
      <div class="bg-container">
        <Img class="main-img" src="promo/main-img.webp" alt=" "/>
        <div class="bg"></div> 
      </div>
      </div> 
    </section>
</template>

<style scoped lang="sass">
@import "../vars.sass"

.bg
  width: 25rem
  height: 25rem
  background: #A387C4
  filter: blur(16rem)
  position: absolute
  right: 0

.main-img
  position: relative
  max-width: 26rem
  max-height: 29rem
  width: 100%
  height: 100%
  top: 2rem

.promo__

  &container
    overflow: hidden
    flex-wrap: nowrap
    flex-direction: row
    justify-content: space-between
    max-width: 80rem
    position: relative
    padding-bottom: 5rem
    padding-right: 4rem

  &block
    display: flex
    flex-direction: column
    gap: 4.2rem
    margin-top: 5rem

.buttons
  display: flex
  flex-direction: row
  gap: 2rem
  margin-top: -1rem

.top-title
  font-size: 1.43rem
  line-height: 1.15
  margin-top: 2.2rem

.title
  font-size: 3.58rem
  line-height: 1.18
  width: 11em
  margin-top: -2.5rem

.txt
  font-size: 1.43rem
  line-height: 1.5
  max-width: 25rem
  margin-top: -1rem

@media screen and (max-width: 912px)

  .promo
    padding: 0

  .bg
    transform: translate(-70%)
    width: 20rem
    height: 20rem

  .promo__
    
    &container
      flex-wrap: wrap
      justify-content: center
      gap: 4rem
      padding-bottom: 12rem
      padding-right: 2rem

    &block
      align-items: center
      text-align: center

@media screen and (max-width: 767px)

  .promo__

    &container
      gap: 2.5rem

  .title
    font-size: 2.86rem

  .buttons
    flex-wrap: wrap
    justify-content: center

  .main-img
    padding: 0 2rem

  .top-title
    font-size: 1.3rem

  .txt
    font-size: 1.3rem

  h1
    font-size: 0.85rem

@media screen and (max-width: 480px) 

  .promo__
    
    &container
      gap: 1rem

  .title
    text-align: center
    font-size: 2.14rem

@media screen and (max-width: 360px)

  .title
    font-size: 1.8rem

  .promo__
    
    &container
      padding-bottom: 8rem

</style>