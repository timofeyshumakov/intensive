<script setup>
import TheHeader from './components/TheHeader.vue';
import Promo from './components/Promo.vue';
import Types from './components/Types.vue';
import Advantages from './components/Advantages.vue';
import Programm from './components/Programm.vue';
import Tariffs from './components/Tariffs.vue';
import Faq from './components/Faq.vue';
import TheFooter from './components/TheFooter.vue';
import './reset.css';

</script>
<template>
  <div class="wrapper">
    <TheHeader/>
    <Promo/>
    <Types/>
    <Advantages/>
    <Programm/>
    <Tariffs/>
    <Faq/>
    <TheFooter/>
  </div>
</template>

<style lang="sass">
@import "vars.sass"

@font-face
  font-style: regular
  font-weight: 400
  font-display: swap
  font-family: "RobotoCondensed"
  src: local("RobotoCondensed-Regular")
  src: url("../fonts/RobotoCondensed-Regular.woff2") format("woff2")
  src: url("../fonts/RobotoCondensed-Regular.woff") format("woff")
  src: url("../fonts/RobotoCondensed-Regular.ttf") format("ttf")

/*#scrollbar*/
::-webkit-scrollbar-track
  background-color: yellow

::-webkit-scrollbar-thumb
  border-radius: 0.5rem

::-webkit-scrollbar-thumb:active
  background-color: yellow
  border: 0.1rem solid yellow

::-webkit-scrollbar
  width: 0.6rem

/*#common*/
html
  font: 400 14px /1.2 'RobotoCondensed', sans-serif
  text-transform: uppercase

h2
  font-size: 3.57rem
  line-height: 1.18

.container
  display: flex
  padding: 0 2rem
  margin: 0 auto
  box-sizing: content-box
  max-width: 82rem
  justify-content: space-between
  align-items: center

footer
  background: rgba(37, 25, 51, 1)

section:nth-child(odd)
  background: $white
  color: $violet

section:nth-child(even)
  background: $violet
  color: $white

.logo
  height: 6em
  padding: 1.5em
  will-change: filter
  transition: filter 300ms

a
  color: white

footer a
  line-height: 1.5

</style>