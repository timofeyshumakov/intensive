<script>
import Img from './Img.vue';
import Button from './Button.vue';
export default {
  components: { Img, Button },
  props: ['sectionName', 'img', 'button', 'txt', 'social', 'prize', 'hashtag']
}
</script>
<template>
    <div v-if="sectionName === 'programm'">

    </div>
    <div :class="`${sectionName}__section-footer section-footer`">
      <div v-if="sectionName === 'faq' || sectionName === 'tariffs'" class="block">
        <Img v-if="sectionName === 'faq'" class="social" src="common/telegram.svg" alt="Image of a cat" />
        <Img v-if="sectionName === 'tariffs'" class="gift-img" src="common/gift.svg" alt="Image of a cat" />
        <div v-html="txt" :class="`${sectionName}__txt txt`"></div>
      </div>
      <div v-else v-html="txt" :class="`${sectionName}__txt txt`"></div>
        <Button v-if="sectionName !== 'faq' && sectionName !== 'tariffs'" class="button primary-button" link="#1" txt="ЗАПИСАТЬСЯ"/>
        <Button v-else-if="sectionName === 'faq'" class="button primary-button" link="#1" txt="НАПИСАТЬ"/>
        <Button v-else-if="sectionName === 'tariffs'" class="button secondary-button" link="#1" txt="СТОРИС-ШАБЛОН"/>
        <Img v-if="sectionName !== 'tariffs'" class="img" src="common/woman-supervillain.svg" alt="Image of a cat" />
        <span v-else>@ULIAVORMAN</span>
    </div>
</template>
<style scoped lang="sass">

.tariffs__
  &txt
    color: white
    max-width: 612px

  &section-footer
    margin-top: 4rem

.faq__
  &section-footer
    justify-content: start
    
.section-footer
  display: flex
  width: 100%
  gap: 5rem

.section-footer:not( .faq__section-footer)
  justify-content: center

.social
  width: 3.3rem
  height: 3.3rem

.txt:not(.tariffs__txt)
  color: #4c3d74
  max-width: 300px
  
.txt
  font-size: 1.43rem
  line-height: 1.5

.types form
  position: relative
  left: -2.7rem

.types .types__txt
  max-width: 500px
  top: -1.4rem
  left: -0.9rem
  position: relative

.img:not(.types img)
  width: 17.4rem
  height: 17.4rem
  margin-right: 2rem
  
.block
  display: flex
  gap: 1.5rem

.gift-img
  width: 4.5rem
  height: 4.5rem

.programm__section-footer
  margin-top: 0.85rem

@media screen and (max-width: 1023px)

  .section-footer
    flex-direction: column
    align-items: center

  .section-footer:not( .faq__section-footer)
    text-align: center

@media screen and (max-width: 767px)

  .types__
    &txt
      text-align: center
      font-size: 1rem

@media screen and (max-width: 479px)
  .img
    width: 15.5rem
    height: 15.5rem
</style>