<script>
import Img from './Img.vue';

  export default {
    components: { Img },
    props: {
      litem: Object,
      markSheme: String,
      tariffsIndex: Number,
      sectionName: String
    },
  }
</script>
<template>
    <ul :class = "`${sectionName}__list list`">
        <li v-if="sectionName !== 'faq'" :class = "`${sectionName}__item item`" v-for="(item, index) in litem">
          <Img v-if="item.src !==undefined" :class="`${sectionName}__item-img`" :src="item.src" alt=" " />
          <a v-if="item.link !== '' && item.link !== undefined"  :href="`${item.link}`" class = "link">{{ item.txt }}</a>
          <span :class="`${sectionName}__item-title title`" v-if="item.title !==undefined">{{ item.title }}</span>
          <span :class="`${sectionName}__txt txt`" v-else-if="sectionName === 'programm'"><details><span :class = "`${sectionName}__details-txt details-txt`">{{ item.details }}</span><summary>УРОК {{ index + 1}}. {{ item.txt }}</summary></details></span>
          <span :class="`${sectionName}__mark mark`" v-else-if="sectionName === 'tariffs'">{{ index < litem.length - (2 - tariffsIndex) ? '+' : '-' }}</span>
          <span :class="`${sectionName}__txt txt`" v-if="sectionName !== 'programm' && item.link === undefined">{{ item.txt }}</span>
        </li>
        <li v-if="sectionName === 'faq'"  :class = "`${sectionName}__item item`" v-for="(item, index) in litem"><details><span :class = "`${sectionName}__details-txt details-txt`">{{ item.details }}</span><summary>{{ item.txt }}</summary></details></li>
    </ul>
</template>

<style lang="sass">

.details-txt
  padding-bottom: 1em
  display: inline-block
  padding-right: 2em
  line-height: 1.5
  
details 
  display: block
  width: 100%

summary::-webkit-details-marker
  display: none

summary
  list-style-position: inside
  list-style-type: none
  cursor: pointer
  min-height: 3.5em
  padding: 1em 2em 1em 0
  line-height: 1.5

summary::before
  content: "+"
  font-size: 2em
  position: absolute
  right: 0.3em
  top: 0
  height: 100%
  display: flex
  align-items: center

summary:hover
  transform: scale(1.01)
  transition: 0.3s

summary:hover::before
  transform: scale(1.15)
  transition: 0.3s

.txt
  padding-left: 0
  width: 100%
  
.item
  display: flex
  align-items: center
  position: relative

.tariff:nth-child(1) .tariffs__item:nth-last-child(-n + 2)
  text-decoration: line-through

.tariff:nth-child(2) .tariffs__item:nth-last-child(-n + 1)
  text-decoration: line-through

.tariffs__item:nth-last-child(-n + 2)
  padding: 1.8rem 0

.tariffs__
  &list
    display: flex
    flex-direction: column

  &item
    display: flex
    align-items: flex-start
    padding: 0.5rem 0
    gap: 1rem

  &txt
    padding: 0
    font-size: 1.15rem

.list
  display: flex

.faq__

  &list
    width: 100%
    flex-direction: column

  &item
    border-bottom: 3px solid
    justify-content: space-between
    font-size: 1.3rem
    
  &item:nth-child(1)
    border-top: 3px solid

.programm__

  &list
    width: 100%
    flex-direction: column

  &item
    border-bottom: 3px solid
    justify-content: space-between
    font-size: 1.3rem

  &item:nth-child(1)
    border-top: 3px solid

.mark
  transform: translate(0px, -0.3rem)
  font-size: 1.6rem
  height: 1rem

.advantages__
  
  &list
    grid-template-columns: repeat(3, 1fr)

  &item
    gap: 1rem
  
  &item-img
    width: 4.8rem
    height: 4.8rem

.presentation__

  &item
    gap: 1.5rem

  &item-title
    font-size: 3.6rem

.presentation__list
  margin-top: -2rem
  row-gap: 0.6rem

.presentation__item
  gap: 1rem
  align-items: flex-start
  flex-direction: column

.footer__list:not(:first-child) .link
  text-decoration: underline

.footer__list:nth-child(3)
  align-items: end

.footer__list:nth-child(2)
  align-items: center

@media screen and (max-width: 912px)

  .advantages__
  
    &list
      grid-template-columns: repeat(2, 1fr)

@media screen and (max-width: 767px)

  .advantages__
  
    &list
      grid-template-columns: 1fr
      margin-left: 3rem

    &item-img
      width: 3.1rem
      height: 3.1rem

  .footer .footer__list
    align-items: flex-start


@media screen and (max-width: 480px)

  .advantages__
  
    &list
      margin-left: 1rem

@media screen and (max-width: 360px)

  .advantages__txt
    font-size: 1rem

</style>