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
      <div v-if="sectionName === 'faq' || sectionName === 'tariffs'" :class="`${sectionName}__block block`">
        <a v-if="sectionName === 'faq'" class="social-link" href="#"><Img class="social" src="common/telegram.svg" alt="telegram"/></a>
        <Img v-if="sectionName === 'tariffs'" class="gift-img" src="common/gift.svg" alt=" " />
        <div v-html="txt" :class="`${sectionName}__txt txt`"></div>
      </div>
      <div v-else v-html="txt" :class="`${sectionName}__txt txt`"></div>
        <Button v-if="sectionName !== 'faq' && sectionName !== 'tariffs'"  :formClassName="`${sectionName}__form`" buttonClassName="button primary-button" link="#tariffs" txt="ЗАПИСАТЬСЯ"/>
        <Button v-else-if="sectionName === 'programm'" formClassName="button primary-button" link="#tariffs" txt="ЗАПИСАТЬСЯ"/>
        <Button v-else-if="sectionName === 'faq'" buttonClassName="button primary-button" link="https://t.me/yuliaVormanIntensive_bot" txt="НАПИСАТЬ"/>
        <Button v-else-if="sectionName === 'tariffs'" buttonClassName="button secondary-button" link="https://t.me/yuliaVormanIntensive_bot" txt="СТОРИС-ШАБЛОН"/>
        <Img v-if="sectionName !== 'tariffs'" class="img" src="common/woman-supervillain.svg" alt=" " />
        <span v-else>@ULIAVORMAN</span>
    </div>
</template>
<style scoped lang="sass">
    
.section-footer
  display: flex
  width: 100%
  gap: 5rem

.block
  display: flex
  align-items: center
  gap: 2rem

.txt
  font-size: 1.43rem
  line-height: 1.5

.programm__form
  order: -1

.programm__txt
  justify-self: self-start
  margin-left: -3rem


  &section-footer
    margin-top: 4rem

.faq__

  &section-footer
    justify-content: start

  &block
    align-items: flex-start
    
.section-footer
  display: flex
  width: 100%
  gap: 5rem

.section-footer:not(.programm__section-footer)
  justify-content: start

.social
  width: 3.3rem
  height: 3.3rem

.txt
  color: #4c3d74
  max-width: 300px

.tariffs__
  &txt
    color: white
    max-width: 612px
    font-size: 1.15rem

.types__form
  position: relative
  left: -2.7rem

.types__txt
  max-width: 500px
  position: relative

.img:not(.types img)
  width: 17.4rem
  height: 17.4rem
  margin-right: 2rem

.gift-img
  width: 4.5rem
  height: 4.5rem

.tariffs__section-footer
  gap: 2.3rem
  align-items: center
  margin-top: 3.5rem

.programm__section-footer
  margin-top: 0.85rem
  justify-content: space-between
  display: grid
  grid-template-columns: 0.6fr 1fr 0.8fr

@media screen and (max-width: 1023px)

  .section-footer
    flex-direction: column
    align-items: center

  .section-footer:not( .faq__section-footer)
    text-align: center

@media screen and (max-width: 912px)
  .faq__

    &block
      align-items: center

  .img:not(.types img)
    width: 15.4rem
    height: 15.4rem
    margin-right: 0

  .types__

    &txt
      text-align: center
      font-size: 1rem
      padding: 0 2rem

    &form
      left: 0

  .section-footer
    gap: 4rem

  .tariffs__block
    flex-direction: column
    align-items: center
  
  .programm__section-footer
    justify-content: center
    align-items: center
    display: flex

  .programm__txt
    margin: 0
  
  .programm__form
    order: 0
  
  .faq__block
    margin-left: 5%

@media screen and (max-width: 479px)

  .block
    gap: 1rem

  .img
    width: 15.5rem
    height: 15.5rem
 
@media screen and (max-width: 360px)

  .section-footer
    gap: 3rem

  .faq__

    &block
      margin-left: 0

    &txt 
      font-size: 1.15rem

  .types__

    &txt
      text-align: center
      font-size: 1rem
      padding: 0 1rem

</style>