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
        <li v-if="sectionName !== 'faq' && sectionName !== 'programm'" :class = "`${sectionName}__item item`" v-for="(item, index) in litem">
          <Img v-if="item.src !==undefined" class="item-img" :src="item.src" alt="Image of a cat" />
          <a v-if="item.link !== '' && item.link !== undefined"  :href="`${item.link}`" class = "link">{{ item.txt }}</a>
          <span :class="`${sectionName}__item-title`" v-if="item.title !==undefined">{{ item.title }}</span>
          <span :class="`${sectionName}__txt txt`" v-else-if="sectionName === 'programm'">УРОК {{ index + 1}}. {{ item.txt }}</span>
          <span :class="`${sectionName}__mark mark`" v-else-if="sectionName === 'tariffs'">{{ index < litem.length - (2 - tariffsIndex) ? '+' : '-' }}</span>
          <span :class="`${sectionName}__txt txt`" v-if="sectionName !== 'programm' && item.link === undefined">{{ item.txt }}</span>
          <span :class="`${sectionName}__mark mark`" v-if="sectionName === 'programm'">+</span>
        </li>
        <li v-if="sectionName === 'faq' || sectionName === 'programm'" :class = "`${sectionName}__item item`" v-for="(item, index) in litem"><details>{{ item.details }}<summary>{{ item.txt }}</summary></details></li>
    </ul>
</template>

<style lang="sass">
.header__item:nth-child(2)
  margin-right: 2rem

details 
  display: block
  width: 100%

details summary::-webkit-details-marker
  display: none

details summary
  list-style-position: inside
  list-style-type: none


details summary::before
  content: "+"
  font-size: 1.2em
  position: absolute
  right: 0

.txt
  padding: 1rem
  padding-left: 0
  
.item
  display: flex
  align-items: center
  position: relative

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

  &item:nth-child(1)
    border-top: 3px solid

.programm__
  &list
    width: 100%
    flex-direction: column

  &item
    border-bottom: 3px solid
    justify-content: space-between

  &item:nth-child(1)
    border-top: 3px solid

.mark
  transform: translate(0px, -0.3rem)
  font-size: 1.6rem
  height: 1rem

.advantages__
  &item
    gap: 1.5rem

  &item-title
    font-size: 3.6rem

.presentation .advantages__list
  margin-top: -2rem
  row-gap: 0.6rem

.presentation .advantages__item
  gap: 0
  align-items: flex-start
  flex-direction: column

.footer__list:not(:first-child) .link
  text-decoration: underline

.footer__list:nth-child(3) .item
  justify-content: flex-end

.footer__list:nth-child(2) .item
  justify-content: center
</style>